---


---

<h1 id="faddom-deep-technical-guide"><strong>Faddom Deep Technical Guide</strong></h1>
<p><em>A unified technical narrative built from three engineering sessions</em></p>
<h2 id="introduction"><strong>Introduction</strong></h2>
<p>This document provides a consolidated and accurate description of how Faddom works, how to deploy it correctly across different hypervisors, how to collect traffic, how discovery operates, and how to validate each module. It merges the lessons, questions, and real technical clarifications that came up in multiple engineering calls and organizes them into a coherent reference.</p>
<p>The goal of the guide is to help an engineer understand the platform at a deeper level so that deployment, troubleshooting, and demonstrations can be done confidently and correctly.</p>
<p>Faddom is an on-premises dependency mapping and analysis platform. It discovers machines, dependencies, user activity, software, CVEs, policies, segmentation gaps, and optimization findings. All data stays inside the customer environment.</p>
<p>The accuracy of the platform depends on two major components:</p>
<ol>
<li>Correct traffic collection</li>
<li>Correct discovery configuration</li>
</ol>
<p>Everything in this document revolves around setting these two up properly.</p>
<hr>
<h2 id="deployment-overview"><strong>1. Deployment Overview</strong></h2>
<p>Faddom can be installed on either:</p>
<ul>
<li>A Linux OVA (main option)</li>
<li>A Windows server (mandatory when integrating with Hyper-V or KVM because of WMI requirements)</li>
</ul>
<p>The platform runs a Tomcat service and a PostgreSQL database. Both are installed automatically. You can separate the database to another server if required.</p>
<p>You control where Faddom runs. It is never hosted by Faddom and does not send data externally.</p>
<h3 id="traffic-collection-methods"><strong>1.1 Traffic Collection Methods</strong></h3>
<p>Faddom has three traffic collection methods, depending on the hypervisor.</p>
<h4 id="vmware-vsphere"><strong>VMware vSphere</strong></h4>
<p>Traffic between VMs on the same vCenter cannot be seen through NetFlow.<br>
To solve this, Faddom uses <strong>sensors</strong>, which are lightweight virtual machines deployed into each ESXi host.</p>
<p>The sensor:</p>
<ul>
<li>Runs in promiscuous mode on the vSwitch</li>
<li>Collects east-west VM-to-VM traffic</li>
<li>Sends traffic to the Faddom server</li>
<li>Uses high CPU by design (default small vCPU count). This is normal.</li>
</ul>
<p>The sensor is not an agent. It does not scan or poll. It simply forwards traffic.</p>
<p>Deployment is fully automated once you provide:</p>
<ul>
<li>An IP for the sensor</li>
<li>The vCenter content library and datastore</li>
<li>A network for management</li>
<li>A port group for promiscuous mode</li>
</ul>
<p>Deployment takes about 5 to 15 minutes.</p>
<h4 id="hyper-v-and-kvm"><strong>Hyper-V and KVM</strong></h4>
<p>Sensors cannot run on Hyper-V or KVM.</p>
<p>Instead, you must install <strong>HostSFlow</strong>, a third-party sFlow implementation, on each hypervisor host.</p>
<p>HostSFlow:</p>
<ul>
<li>Runs on the Hyper-V host OS or the KVM host OS</li>
<li>Sends traffic samples and interface statistics to the Faddom server</li>
<li>Covers east-west visibility in these hypervisors</li>
</ul>
<p>The exact steps vary by distribution or vendor, but the principle is:</p>
<ol>
<li>Install HostSFlow on the hypervisor host</li>
<li>Configure it to export to the Faddom collector</li>
<li>Ensure firewall rules are open</li>
<li>Validate traffic is received</li>
</ol>
<p>Some KVM distributions or vendors have native sFlow or IPFIX. In those cases, use the built-in mechanism instead of HostSFlow.</p>
<p>Customers have successfully run the Linux OVA on Proxmox by converting it, but support is limited to best effort because of the complexity of KVM variations.</p>
<hr>
<h2 id="discovery-scope"><strong>2. Discovery Scope</strong></h2>
<p>Faddom discovers servers based on subnets you define in the discovery scope.</p>
<p>Everything with an IP address in a discovered subnet will be inventoried.</p>
<p>If you want to limit licensing or reduce noise, you have two mechanisms:</p>
<h3 id="limiting-discovery-by-subnet"><strong>2.1 Limiting Discovery by Subnet</strong></h3>
<p>Faddom inventories only the first set of machines it sees in enabled subnets. For example, if 100 are licensed but 150 exist, discovery may rotate which machines appear each day.</p>
<h3 id="filters"><strong>2.2 Filters</strong></h3>
<p>Filters allow you to exclude specific machines from maps or from inventory presentation, even if traffic exists.<br>
This is commonly used for:</p>
<ul>
<li>VDI machines</li>
<li>Backups</li>
<li>Monitoring appliances</li>
<li>Vendor boxes</li>
<li>Firewalls</li>
<li>Load balancers</li>
</ul>
<p>Filters can be applied globally or per map.</p>
<hr>
<h2 id="application-mapping"><strong>3. Application Mapping</strong></h2>
<p>Mapping is done from the perspective of how users access an application.</p>
<ol>
<li>
<p>Specify an entry point</p>
<ul>
<li>URL</li>
<li>Load balancer</li>
<li>VIP</li>
<li>Host and port</li>
</ul>
</li>
<li>
<p>Let the system discover downstream dependencies</p>
</li>
<li>
<p>Review the tiered view</p>
</li>
<li>
<p>Review purple highlights for newly discovered connections</p>
</li>
</ol>
<p>The direction of each connection is essential.<br>
If A connects to B, then B depends on A.</p>
<p>Powerful exports are available:</p>
<ul>
<li>Visio</li>
<li>CSV</li>
<li>Image</li>
</ul>
<hr>
<h2 id="change-tracking"><strong>4. Change Tracking</strong></h2>
<p>Every map has change tracking. It shows:</p>
<ul>
<li>New servers</li>
<li>Removed servers</li>
<li>New connections</li>
<li>Removed connections</li>
</ul>
<p>This helps:</p>
<ul>
<li>Migration projects</li>
<li>DR validation</li>
<li>Year-over-year change audits</li>
<li>Documentation updates</li>
</ul>
<hr>
<h2 id="impact-sets"><strong>5. Impact Sets</strong></h2>
<p>Impact Sets show which applications or servers depend on a given machine.</p>
<p>Two clicks reveal:</p>
<ul>
<li>Which maps a server belongs to</li>
<li>Which downstream services will break if it is taken offline</li>
<li>How many applications will be affected</li>
</ul>
<p>It eliminates manual spreadsheets or “scream tests”.</p>
<hr>
<h2 id="investigate"><strong>6. Investigate</strong></h2>
<p>The investigate tool allows you to choose:</p>
<ul>
<li>A server</li>
<li>A timeslot of unusual activity</li>
<li>A specific timestamp</li>
</ul>
<p>You can see:</p>
<ul>
<li>Connection changes</li>
<li>Volume changes</li>
<li>Which new servers appeared</li>
<li>User activity around the event</li>
</ul>
<p>This is one of the fastest ways to do root cause analysis.</p>
<hr>
<h2 id="security-module"><strong>7. Security Module</strong></h2>
<p>The security area includes several components.</p>
<h3 id="shadow-it"><strong>7.1 Shadow IT</strong></h3>
<p>Shows servers with no meaningful activity.<br>
Usually old projects, vendor machines, or forgotten systems.</p>
<h3 id="servers-at-risk"><strong>7.2 Servers at Risk</strong></h3>
<p>A combined view of CVEs, end-of-life OS versions, software risks, and business impact.</p>
<h3 id="user-discovery"><strong>7.3 User Discovery</strong></h3>
<p>User discovery requires:</p>
<ul>
<li>A Windows proxy (when running Faddom Linux)</li>
<li>WMI permissions</li>
<li>Ports 135, 445, 139, and 49152 to 65535</li>
<li>Correct AD rights to fetch event logs</li>
</ul>
<p>User discovery correlates users with the servers they interact with, based on event logs.</p>
<h3 id="cve-discovery"><strong>7.4 CVE Discovery</strong></h3>
<p>CVE discovery for Linux requires:</p>
<ul>
<li>SSH access from Faddom or the proxy</li>
<li>Sudo rights</li>
<li>Port 22</li>
</ul>
<p>CVE results include:</p>
<ul>
<li>Raw CVSS score</li>
<li>A Faddom business impact score</li>
<li>A list of affected maps</li>
<li>External reference links (NIST, vendor)</li>
</ul>
<h3 id="software-discovery"><strong>7.5 Software Discovery</strong></h3>
<p>Software Discovery supports both Linux and Windows.</p>
<p>Linux requires:</p>
<ul>
<li>SSH</li>
<li>Sudo</li>
<li>Port 22</li>
</ul>
<p>Windows requires:</p>
<ul>
<li>
<p>A Windows proxy</p>
</li>
<li>
<p>WMI permissions</p>
</li>
<li>
<p>The ability to run</p>
<ul>
<li><code>SELECT * FROM MSFT_NetTCPConnection</code></li>
<li><code>SELECT * FROM Win32_Process</code></li>
</ul>
</li>
</ul>
<p>Missing software discovery usually comes from:</p>
<ul>
<li>Missing credentials</li>
<li>Wrong proxy assignment</li>
<li>Missing WMI permissions</li>
<li>Firewall blocks</li>
<li>Domain trust issues</li>
<li>Wrong account type (needs server log reading permission)</li>
</ul>
<hr>
<h2 id="operating-system-end-of-life"><strong>8. Operating System End of Life</strong></h2>
<p>Faddom maintains an OS lifecycle database.<br>
You can:</p>
<ul>
<li>Update it online</li>
<li>Upload an offline file</li>
<li>Refresh the database manually</li>
</ul>
<p>Alerts can be generated for:</p>
<ul>
<li>Servers beyond end-of-life</li>
<li>Servers beyond extended support</li>
<li>Unsupported releases</li>
</ul>
<hr>
<h2 id="notifications-and-reporting"><strong>9. Notifications and Reporting</strong></h2>
<p>Notifications can be sent through:</p>
<ul>
<li>Email</li>
<li>Syslog</li>
<li>Webhooks</li>
</ul>
<p>The Linux OVA includes a local SMTP server for basic functionality.<br>
For production, customers typically use their own SMTP.</p>
<p>Notifications include:</p>
<ul>
<li>OS lifecycle</li>
<li>Software policy violations</li>
<li>CVEs</li>
<li>External traffic alerts</li>
<li>Subnet traffic policy violations</li>
<li>Summary report generation</li>
</ul>
<p>Summary reports can be scheduled and sent regularly.</p>
<hr>
<h2 id="subnet-traffic-policy"><strong>10. Subnet Traffic Policy</strong></h2>
<p>This feature controls and monitors allowed traffic between subnets.</p>
<h3 id="automatic-policy"><strong>10.1 Automatic Policy</strong></h3>
<p>Click Generate Policy to create allowed subnet rules based on observed traffic.</p>
<p>This is useful for:</p>
<ul>
<li>Segmentation projects</li>
<li>Firewall validation</li>
<li>Microsegmentation planning</li>
<li>Detecting unexpected cross-network access</li>
</ul>
<p>You can regenerate policies anytime.</p>
<h3 id="manual-policies"><strong>10.2 Manual Policies</strong></h3>
<p>You can manually add rules defining:</p>
<ul>
<li>Source subnet</li>
<li>Target subnet</li>
<li>Port</li>
</ul>
<p>Rules can be removed individually or in bulk.</p>
<h3 id="alerts-and-violations"><strong>10.3 Alerts and Violations</strong></h3>
<p>When traffic violates the policy, Faddom:</p>
<ul>
<li>Logs an event</li>
<li>Flags the connection in the properties panel</li>
<li>Raises a notification if configured</li>
</ul>
<h3 id="properties-panel"><strong>10.4 Properties Panel</strong></h3>
<p>Selecting a subnet shows:</p>
<p><strong>Inventory</strong><br>
All members of the subnet.</p>
<p><strong>Dependencies</strong><br>
Inbound and outbound connections organized by port, with the ability to allow specific connections.</p>
<p>Columns include:</p>
<ul>
<li>Subnet</li>
<li>Count</li>
<li>Source</li>
<li>Target</li>
<li>Alerts</li>
</ul>
<hr>
<h2 id="external-traffic-policy"><strong>11. External Traffic Policy</strong></h2>
<p>Monitors all communication between internal systems and the outside world.</p>
<p>Supports:</p>
<ul>
<li>Baseline creation through Apply Current as Policy</li>
<li>Manual rule creation</li>
<li>Blacklisted country configuration</li>
<li>Country database updates (online or offline)</li>
<li>External traffic dashboards</li>
<li>Server-level external traffic visibility</li>
</ul>
<p>Blacklisted countries appear in pink in the dashboard.</p>
<hr>
<h2 id="apis-and-automation"><strong>12. APIs and Automation</strong></h2>
<p>Faddom includes a full API for:</p>
<ul>
<li>Exporting maps</li>
<li>Pulling configuration</li>
<li>Pulling CVEs</li>
<li>Pulling software data</li>
<li>Triggering tasks</li>
<li>Exporting Visio or images</li>
</ul>
<p>This is used for:</p>
<ul>
<li>Monthly DR documentation</li>
<li>Application owner reports</li>
<li>CMDB integration</li>
<li>Automated wave planning</li>
<li>ServiceNow or Jira automation</li>
</ul>
<hr>
<h2 id="troubleshooting-and-support-workflow"><strong>13. Troubleshooting and Support Workflow</strong></h2>
<p>When something fails, the correct technical procedure is:</p>
<ol>
<li>Click Server Logs</li>
<li>Download all logs</li>
<li>Open Chrome DevTools</li>
<li>Reproduce the error</li>
<li>Export the HAR file</li>
<li>Email both to support</li>
</ol>
<p>The support email reaches the entire engineering team.</p>
<p>Examples of common issues:</p>
<ul>
<li>Proxy cannot reach a subnet</li>
<li>WMI permission missing</li>
<li>Firewall missing RPC range</li>
<li>Incorrect DNS</li>
<li>Wrong domain credentials</li>
<li>Duplicate proxy names</li>
<li>Discovery tasks pointing to incorrect subnets</li>
</ul>
<hr>
<h2 id="migration-dr-and-licensing-considerations"><strong>14. Migration, DR, and Licensing Considerations</strong></h2>
<h3 id="migration-support"><strong>Migration support</strong></h3>
<p>Faddom ensures no dependent servers are missed.<br>
Wave planning includes:</p>
<ul>
<li>Firewall rules</li>
<li>Dependencies</li>
<li>Cost estimation</li>
<li>Traffic usage</li>
<li>Required ports</li>
</ul>
<h3 id="dr-support"><strong>DR support</strong></h3>
<p>Users often export maps monthly, either:</p>
<ul>
<li>Manually</li>
<li>Via API</li>
<li>Via script</li>
</ul>
<p>This gives a known-good dependency map for disaster scenarios.</p>
<h3 id="licensing-considerations"><strong>Licensing considerations</strong></h3>
<p>You can license only part of the environment.<br>
Discovery must be limited by subnet if you want to control which hosts count toward license usage.</p>
<p>Traffic collection continues regardless of licensing, but inventory may rotate.</p>

