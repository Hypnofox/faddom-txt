---


---

<h1 id="faddom-phsa-demo-flow"><strong>Faddom PHSA Demo Flow</strong></h1>
<hr>
<h3 id="introduction--overview"><strong>1) Introduction &amp; Overview</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Before we dive into the visuals, let’s start with what Faddom actually is. We’re a real-time, agentless application dependency mapping solution. Using network statistic protocols like NetFlow, sFlow, and cloud flow logs, we can map out your entire hybrid IT environment—every server, every interconnection, and every dependency.”</p>
<p><strong>Demonstration:</strong><br>
Explain that Faddom operates as a <strong>virtual appliance</strong>, collecting flow data from your existing infrastructure.<br>
Deployment takes roughly <strong>60 minutes</strong>, after which results appear live.<br>
Emphasize that <strong>no data leaves your environment</strong>—everything remains fully contained within your network or cloud.</p>
<p><strong>Value:</strong><br>
Faddom provides full, agentless visibility across VMware, AWS, Azure, and on-prem systems—without changing how you operate. It’s fast to deploy, secure by design, and significantly more cost-effective than traditional agent-based or SaaS dependency tools.</p>
<hr>
<h3 id="core-use-cases"><strong>2) Core Use Cases</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Let’s set the stage with what Faddom is most commonly used for—because this is exactly where your current initiatives fit.”</p>
<p><strong>Demonstration:</strong><br>
Walk through examples:</p>
<ul>
<li>CMDB population and IT documentation</li>
<li>Network and application dependency mapping</li>
<li>Migration and data center consolidation planning</li>
<li>Rightsizing and optimization projects</li>
<li>Security segmentation and microsegmentation validation</li>
</ul>
<p><strong>Value:</strong><br>
From discovery to modernization, Faddom replaces manual effort and disconnected tools with a single, unified visibility platform.</p>
<hr>
<h3 id="dashboard"><strong>3) Dashboard</strong></h3>
<p><strong>Opening Statement:</strong><br>
“This is the main Faddom dashboard. Everything here is customizable—different teams can have different dashboards based on what matters to them.”</p>
<p><strong>Demonstration:</strong><br>
Show the main dashboard.<br>
Create a new one to demonstrate role-based customization: operations, network, migration, or security.<br>
Highlight how metrics and KPIs update in real time using live NetFlow and API data.</p>
<p><strong>Value:</strong><br>
Instant, unified visibility—no context switching, no juggling tools. Each stakeholder gets their view of the same truth.</p>
<hr>
<h3 id="vlan--network-mapping"><strong>4) VLAN &amp; Network Mapping</strong></h3>
<p><strong>Opening Statement:</strong><br>
“This is what a typical VLAN view looks like in Faddom. It’s the foundational layer—live network visibility.”</p>
<p><strong>Demonstration:</strong><br>
Display a <strong>VLAN map</strong> showing all servers, VMs, and devices.<br>
Explain color coding:</p>
<ul>
<li><strong>Green lines</strong> show live, active connections</li>
<li><strong>Red lines</strong> indicate non-responsive or blocked traffic (firewall or offline system)</li>
<li><strong>Gray lines</strong> mark inactive or scheduled connections</li>
</ul>
<p>Each connection displays <strong>source, port, and destination</strong>.<br>
Mention that the visualization updates in real time using NetFlow data—no active scanning or probes required.</p>
<p><strong>Value:</strong><br>
You see exactly what’s happening now—not last week.<br>
Perfect for microsegmentation projects, firewall validation, and identifying communication paths before any change or migration.</p>
<hr>
<h3 id="application-maps"><strong>5) Application Maps</strong></h3>
<p><strong>Opening Statement:</strong><br>
“This is where Faddom moves from infrastructure visibility to true application dependency mapping.”</p>
<p><strong>Demonstration:</strong><br>
Create an application map using traffic from a single entry point.<br>
Show how Faddom automatically groups systems by <strong>tiers</strong>—web, application, database.<br>
Highlight purple lines showing <strong>new, recently discovered connections</strong>.<br>
Switch between <strong>server-based</strong> and <strong>tier-based</strong> views for clarity.</p>
<p><strong>Change Tracking:</strong><br>
Demonstrate color-coded changes:</p>
<ul>
<li><strong>Purple or gold:</strong> additions or removals<br>
Show the <strong>Change Summary List</strong> to review what changed, when, and by whom.<br>
Use the <strong>Compare</strong> view to track differences between two snapshots—e.g., changes between October 19 and October 23.</li>
</ul>
<p><strong>Value:</strong><br>
Real-time dependency awareness and full change visibility—no more relying on the “scream test” to find out what’s broken.</p>
<hr>
<h3 id="root-cause-analysis-rca"><strong>6) Root Cause Analysis (RCA)</strong></h3>
<p><strong>Opening Statement:</strong><br>
“When something goes wrong, finding the ‘why’ shouldn’t be detective work.”</p>
<p><strong>Demonstration:</strong><br>
Drill into a server or connection.<br>
Open the traffic timeline to show spikes or drops.<br>
Display when new connections appeared or vanished, and correlate with user logins or configuration changes.</p>
<p><strong>Value:</strong><br>
Faddom compresses RCA time from hours to minutes—showing when, where, and who changed what.</p>
<hr>
<h3 id="load-balancers--firewalls"><strong>7) Load Balancers &amp; Firewalls</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Visibility doesn’t stop at the network edge—Faddom maps through your load balancers and firewall layers too.”</p>
<p><strong>Demonstration:</strong><br>
Show failed connections (in red) that point to blocked ports.<br>
Explain that Faddom can trace these connections through IP groups and NetFlow from load balancers.<br>
Highlight how traffic paths through balancing layers remain visible for end-to-end analysis.</p>
<p><strong>Value:</strong><br>
You see not just that traffic failed—but <em>where</em> it failed, and why.</p>
<hr>
<h3 id="migration-planning"><strong>8) Migration Planning</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Now let’s move into what matters most for PHSA—migration and data center consolidation.”</p>
<p><strong>Demonstration:</strong><br>
Open the <strong>Migration Portal</strong>.<br>
Create a new migration wave, e.g., <em>“PHSA Data Center Consolidation.”</em><br>
Select servers, applications, or subnets to move.<br>
Show <strong>Members &amp; Dependencies</strong> lists and visual dependency mapping.<br>
Demonstrate <strong>Infrastructure Dependencies</strong>, displaying required ports like DNS, NTP, or database links.</p>
<p>Highlight <strong>Cost Estimation:</strong><br>
Show how Faddom uses API calls to VMware, AWS, and Azure for accurate compute, memory, and storage cost projections.<br>
Mention that custom enterprise pricing can be uploaded for private rate integration.</p>
<p><strong>Value:</strong><br>
Every dependency is visible before you move.<br>
One missed server no longer breaks the rollout.<br>
Accurate, transparent migration waves replace risky manual planning.</p>
<hr>
<h3 id="cloud-architecture--data-collection"><strong>9) Cloud Architecture &amp; Data Collection</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Coverage is only as good as what you can see—and Faddom is built for complex hybrid networks.”</p>
<p><strong>Demonstration:</strong><br>
Explain <strong>flow collection options:</strong></p>
<ul>
<li>NetFlow, sFlow, or IPFIX</li>
<li>VMware distributed switch NetFlow</li>
<li><strong>Sensors</strong> for east-west traffic capture on ESXi hosts</li>
<li>Proxy collectors for remote sites</li>
</ul>
<p><strong>Value:</strong><br>
Faddom achieves near 100% visibility, even for east-west or multi-cloud traffic. It adapts to your architecture, not the other way around.</p>
<hr>
<h3 id="subnet-dependency-maps"><strong>10) Subnet Dependency Maps</strong></h3>
<p><strong>Opening Statement:</strong><br>
“This is the macro view—the full network, all subnets, every data center, live and connected.”</p>
<p><strong>Demonstration:</strong><br>
Show a <strong>Subnet Map</strong> linking production, DMZ, and test environments.<br>
Explain that each line represents live traffic flow.<br>
Highlight an example of DMZ-to-Production communication that triggers a <strong>policy violation alert</strong>.<br>
Demonstrate resolving it by applying a firewall rule, refreshing, and watching the alert disappear in real time.</p>
<p><strong>Value:</strong><br>
Zero blind spots for segmentation and zero-trust validation.<br>
Instant detection of policy violations before they become incidents.</p>
<hr>
<h3 id="inventory--data-retention"><strong>11) Inventory &amp; Data Retention</strong></h3>
<p><strong>Opening Statement:</strong><br>
“All the data you’ve seen so far lives in your environment—Faddom just organizes it for you.”</p>
<p><strong>Demonstration:</strong><br>
Open the <strong>Inventory view</strong>:</p>
<ul>
<li>Show servers, OS versions, and installed software</li>
<li>Highlight end-of-life systems</li>
<li>Display logged-in users and inactive accounts</li>
</ul>
<p>Discuss retention defaults:</p>
<ul>
<li><strong>Connection history:</strong> 14 days (customizable)</li>
<li><strong>Inventory data:</strong> 30 days (customizable)</li>
</ul>
<p><strong>Value:</strong><br>
Automatic CMDB enrichment without manual updates.<br>
All agentless, secure, and fully under your control.</p>
<hr>
<h3 id="cloud-cost-management"><strong>12) Cloud Cost Management</strong></h3>
<p><strong>Opening Statement:</strong><br>
“When you model migrations, cost matters as much as connectivity.”</p>
<p><strong>Demonstration:</strong><br>
Open the <strong>Cloud Cost Dashboard.</strong><br>
Show how Faddom retrieves live cost data from AWS, Azure, and GCP via APIs.<br>
Explain that custom pricing agreements can be uploaded for private contract rates.</p>
<p><strong>Value:</strong><br>
Accurate, transparent forecasting—Faddom shows what migration actually costs before you spend a dollar.</p>
<hr>
<h3 id="pricing-overview"><strong>13) Pricing Overview</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Let’s talk about commercial structure—simple, transparent, and based only on what you actually use.”</p>
<p><strong>Demonstration:</strong><br>
Explain pricing is based solely on the <strong>number of servers, VMs, or instances</strong> monitored.<br>
Endpoints and users do not affect cost.</p>
<p>For PHSA’s environment of roughly <strong>8,000 servers</strong>, the annual subscription would be approximately <strong>$280,000 to $300,000</strong>.<br>
Multi-year options are available for longer-term projects.</p>
<p><strong>Value:</strong><br>
Predictable cost, scalable coverage, and full flexibility for both on-prem and cloud.</p>
<hr>
<h3 id="next-steps--timeline"><strong>14) Next Steps &amp; Timeline</strong></h3>
<p><strong>Opening Statement:</strong><br>
“Based on your roadmap—data center consolidation, modernization, and hybrid visibility—timing is everything.”</p>
<p><strong>Demonstration (Planning Context):</strong><br>
Recommend internal review and a follow-up call in two weeks.<br>
Mention Faddom’s <strong>two-week trial license</strong>, extendable as needed for evaluation.</p>
<p><strong>Timeline Guidance:</strong><br>
For an April–May 2026 migration window, final tool selection by <strong>January</strong> ensures sufficient testing, configuration, and readiness.</p>
<p><strong>Value:</strong><br>
A clear, low-risk path forward—real testing in your own environment before any commitment.</p>
<hr>
<h3 id="wrap-up"><strong>15) Wrap-Up</strong></h3>
<p><strong>Closing Statement:</strong><br>
“Faddom gives you end-to-end visibility across your entire hybrid infrastructure—agentless, real-time, and entirely under your control. You’ll see every dependency, plan every move, and validate every change before it affects production.”</p>
<p><strong>Add-on Mention:</strong><br>
Captain AI and Compass AI deliver conversational and predictive insights within the platform, ensuring you’re never guessing—only confirming.</p>
<p><strong>Final Line:</strong><br>
“Whether it’s modernization, migration, or consolidation, Faddom ensures you move with clarity, confidence, and zero surprises.”</p>

