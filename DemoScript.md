---


---

<h1 id="faddom-customer-success-demo-script-slide-aligned-version">Faddom Customer Success Demo Script (Slide-Aligned Version)</h1>
<hr>
<h2 id="slide-1-–-agentless-start">Slide 1 – Agentless Start</h2>
<h3 id="presenter-notes">Presenter Notes</h3>
<p><strong>Opening Statement:</strong><br>
Let’s start with how Faddom connects to your environment. Everything you’re about to see begins here.<br>
Faddom collects data <em>agentlessly</em> from multiple sources — VMware, Hyper-V, AWS, Azure, Google Cloud, Nutanix, OpenStack, Kubernetes, Oracle — all without credentials or agents. Nothing needs to be installed on your servers, and no firewalls need to be opened.</p>
<p><strong>Action:</strong><br>
Point to the icons on the left side of the slide. Emphasize breadth of integrations.</p>
<p><strong>Transition:</strong><br>
Now look to the right side of the slide. This is what Faddom automatically builds — a unified, real-time view of your infrastructure, including application dependency maps, network relationships, and inventory.<br>
Everything we’ll see today comes from this live topology.</p>
<p><strong>Mention the three key values at the bottom:</strong></p>
<ul>
<li><strong>Fast:</strong> Deployment in under 60 minutes.</li>
<li><strong>Secure:</strong> No agents, no credentials, no open ports.</li>
<li><strong>Cost-effective:</strong> Scales fairly for any size environment.</li>
</ul>
<p>Then switch to the live interface or screenshot of the <strong>Dashboard</strong>.</p>
<hr>
<h2 id="dashboard">Dashboard</h2>
<p><strong>Opening Statement:</strong><br>
There’s a lot here—it’ll all make sense as we move through the demo. Everything on this screen is fully customizable. You can create multiple dashboards tailored to different teams or roles.</p>
<p><strong>Demonstration:</strong><br>
Show existing dashboards and create a new one quickly. Point out widgets that summarize system health, alerts, and usage.</p>
<p><strong>Value:</strong><br>
All your critical information at a glance. No switching between consoles or reports.</p>
<hr>
<h2 id="search-vlan-3-example">Search (VLAN 3 Example)</h2>
<p><strong>Opening Statement:</strong><br>
This is one of our most powerful features. Think of it as a Google search for your environment. It’s the fastest and easiest way to find and map any IT asset in real time.</p>
<p><strong>Demonstration:</strong><br>
Search for “VLAN 3”. Show the resulting map layout:</p>
<ul>
<li>Nodes represent servers or devices.</li>
<li>Lines represent active connections.</li>
<li>Arrows show direction of communication.</li>
</ul>
<p><strong>Explain Colors:</strong><br>
Green = active connections.<br>
Red = failed or blocked connections.<br>
Gray = inactive or historical links.</p>
<p><strong>List View and Export:</strong><br>
Switch to list view, filter or sort, and export as CSV, image, or Visio.</p>
<p><strong>Value:</strong><br>
Once we know the direction of the connection, we know the dependency. That’s what makes Faddom unique.</p>
<p><strong>Slide 2 Connection:</strong><br>
This part aligns with <strong>Discovery</strong> on the second slide — hybrid ADM, asset discovery, and CMDB population.</p>
<hr>
<h2 id="application-maps">Application Maps</h2>
<p><strong>Opening Statement:</strong><br>
This is the core of Faddom — mapping your applications and understanding exactly how they interact.</p>
<p><strong>Demonstration:</strong><br>
Create a new map using traffic flow from IP <code>10.16.3.10</code>.<br>
Explain that Faddom reads real network traffic and automatically organizes servers left-to-right — client, application, and backend tiers.<br>
New connections appear in purple, showing live discovery.</p>
<p><strong>Save and Filter:</strong><br>
Save the map to demonstrate how quick it is.<br>
Use filters to remove irrelevant systems (for example, email or monitoring servers).<br>
Mention that AI suggestions help automatically filter noise.</p>
<p><strong>Notifications and Integrations:</strong><br>
Show notification settings. Explain they’re modular and integrate with Syslog, Webhooks, or REST APIs.<br>
“This is what makes Faddom proactive for you.”</p>
<p><strong>Impact Set:</strong><br>
Demonstrate adding a server to the Impact Set to see which applications depend on it.<br>
“This is the easiest way to prevent the scream test.”</p>
<p><strong>Investigate and RCA:</strong><br>
Drill into a server, open traffic charts, and show timestamp analysis.<br>
“This is where 90% of the solution is knowing the problem.”</p>
<p><strong>Baselines and Comparison:</strong><br>
Show Baseline, Current, and Compare.<br>
“If an engineer goes on vacation for a week, they can come back and immediately see what changed.”<br>
“We make the organization the owner of the topology, not any single individual.”</p>
<p><strong>Value:</strong><br>
Everything needed for root cause analysis in one place. Dramatically reduces incident response time.</p>
<p><strong>Slide 2 Connection:</strong><br>
This aligns with <strong>Change Management</strong> — application change detection, impact analysis, and root cause analysis.</p>
<hr>
<h2 id="compass-ai">Compass AI</h2>
<p><strong>Opening Statement:</strong><br>
Now that we’ve seen the main use cases, let’s meet Compass AI — your chat interface for the infrastructure.</p>
<p>“This is like ChatGPT for your environment. You can ask it anything.”</p>
<p><strong>Demonstration:</strong><br>
Type: <em>When is the best time to take down Tomcat1 for maintenance?</em></p>
<p><strong>While it loads:</strong><br>
“It takes around half a minute to process. All the analysis happens within your environment — nothing leaves your network.”</p>
<p><strong>Explain Output:</strong><br>
Compass AI analyzes historical traffic and utilization, then returns the optimal downtime window and which users would be affected.</p>
<p><strong>Value:</strong><br>
The fastest way to get accurate answers. Ideal for teams unfamiliar with every screen.<br>
All responses can be exported to CSV for documentation.</p>
<p><strong>Slide 2 Connection:</strong><br>
This corresponds to the bottom bar on slide 2 — <em>Compass AI: Chat with Your Infrastructure.</em></p>
<hr>
<h2 id="subnet-dependencies-mapping">Subnet Dependencies Mapping</h2>
<p><strong>Opening Statement:</strong><br>
This is the most powerful bird’s-eye view of your network.</p>
<p><strong>Demonstration:</strong><br>
Show the subnet view with live traffic.<br>
“This is full visibility — zero blind spots.”</p>
<p><strong>Validation:</strong><br>
Explain that you can export this data and validate it against firewall rules.<br>
If new traffic appears, Faddom alerts you automatically.</p>
<p><strong>Story:</strong><br>
During an onboarding, an IT director noticed that test and production environments were communicating. We identified the cause in seconds.</p>
<p><strong>Value:</strong><br>
The easiest way to plan and validate segmentation. Group networks by business unit, geography, or environment.</p>
<p><strong>Slide 2 Connection:</strong><br>
This supports <strong>Cybersecurity</strong> — micro-segmentation planning and north-south / east-west visibility.</p>
<hr>
<h2 id="shadow-it">Shadow IT</h2>
<p><strong>Opening Statement:</strong><br>
Shadow IT is often overlooked. Servers come online for short projects and stay forgotten — like leaving a door open you didn’t know existed.</p>
<p><strong>Demonstration:</strong><br>
Show the inactive server view where no traffic is detected.</p>
<p><strong>Value:</strong><br>
Faddom exposes hidden systems, closing every door in your environment and eliminating blind spots.</p>
<p><strong>Slide 2 Connection:</strong><br>
This also belongs under <strong>Cybersecurity</strong> — shadow IT discovery.</p>
<hr>
<h2 id="servers-at-risk-faddom-score">Servers at Risk (Faddom Score)</h2>
<p><strong>Explanation:</strong><br>
Faddom consolidates all the information — vulnerabilities, outdated OS versions, external connections, and application criticality — into a single risk score.<br>
This view prioritizes issues by business impact, not just technical severity.</p>
<p><strong>Value:</strong><br>
Your daily control panel for risk management. Open it in the morning and see immediately what matters most.</p>
<p><strong>Slide 2 Connection:</strong><br>
Still within <strong>Cybersecurity</strong> — vulnerability and access detection.</p>
<hr>
<h2 id="lighthouse-ai-traffic-anomaly-detection">Lighthouse AI (Traffic Anomaly Detection)</h2>
<p><strong>Opening Statement:</strong><br>
Lighthouse AI is our upcoming anomaly-detection engine. It learns your traffic patterns and alerts you to abnormal behavior automatically.</p>
<p><strong>Explanation:</strong><br>
This removes the need for manual thresholds or static rules — it continuously adapts as your environment evolves.</p>
<p><strong>Slide 2 Connection:</strong><br>
Appears on slide 2 under <strong>Cybersecurity – AI Traffic Anomaly Detection.</strong></p>
<hr>
<h2 id="migration-and-disaster-recovery-planning">Migration and Disaster Recovery Planning</h2>
<p><strong>Opening Statement:</strong><br>
This is where you can plan all migrations and disaster recovery.<br>
The screen starts by showing a full lift-and-shift cost estimate, including right-sizing and optimization, but most migrations happen by application or service — what we call <em>migration waves.</em></p>
<p><strong>Demonstration:</strong><br>
Create a wave, select destination (for example, AWS or Azure), choose applications, servers, and subnets.<br>
Show findings:</p>
<ul>
<li><strong>Cost Analysis:</strong> Instance type, network pricing, right-sizing.</li>
<li><strong>Dependencies:</strong> Which systems rely on each other.</li>
<li><strong>Infrastructure Ports:</strong> DNS, NTP, and other critical services.</li>
</ul>
<p><strong>Value:</strong><br>
One server left behind can break the business. Faddom ensures nothing is missed during migration or DR.</p>
<p><strong>Slide 2 Connection:</strong><br>
This maps to <strong>Migration</strong> — cloud migration assessment, data center transformation, and DR/BC planning.</p>
<hr>
<h2 id="optimization">Optimization</h2>
<p><strong>Opening Statement:</strong><br>
Every megabyte of RAM has a cost, whether on-prem or in the cloud.</p>
<p><strong>Demonstration:</strong><br>
Show optimization recommendations:</p>
<ul>
<li>Some servers can be downsized to save cost.</li>
<li>Others need scaling to maintain performance.<br>
Explain that VMware shows allocated memory, not consumed, but Faddom still provides guidance based on real utilization metrics.</li>
</ul>
<p><strong>Value:</strong><br>
Continuous optimization of resources — lower cost, higher performance.</p>
<p><strong>Slide 2 Connection:</strong><br>
This matches <strong>Optimization</strong> — inactive server discovery and rightsizing.</p>
<hr>
<h2 id="inventory-and-asset-management">Inventory and Asset Management</h2>
<p><strong>Opening Statement:</strong><br>
This acts as a lightweight CMDB. All assets are discovered automatically, kept current, and can be exported for audits.</p>
<p><strong>Demonstration:</strong></p>
<ul>
<li><strong>Data Sources:</strong> Show connected systems.</li>
<li><strong>Software:</strong> List installed packages on Windows and Linux.<br>
<em>Example:</em> An IT manager once found a Bitcoin miner running on a forgotten VM through this view.</li>
<li><strong>Operating Systems:</strong> Identify end-of-life versions.<br>
<em>Example:</em> A customer discovered two outdated Linux distributions they didn’t know existed.*</li>
<li><strong>Users:</strong> Show recent logins, user-to-server maps, and inactive accounts.<br>
<em>Example:</em> A company was breached through an inactive account — Faddom would have flagged it.*</li>
</ul>
<p><strong>Value:</strong><br>
You can instantly see who will be affected when a server is taken offline. Be proactive, not reactive.</p>
<p><strong>Slide 2 Connection:</strong><br>
This supports <strong>Discovery</strong> — software inventory, IT audit, and documentation.</p>
<hr>
<h2 id="wrap-up-and-dashboard-return">Wrap-Up and Dashboard Return</h2>
<p>Return to the Dashboard to close the loop.<br>
Now everything on the dashboard makes sense — all the data points, alerts, and widgets stem from what we just explored.</p>
<p>Mention <strong>Captain AI Support</strong> — built-in guidance and direct access to Faddom support.</p>
<p><strong>Closing Statement:</strong><br>
Faddom unifies change management, discovery, cybersecurity, migration, and optimization — all agentlessly, in real time, from a single platform.</p>

