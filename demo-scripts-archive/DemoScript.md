---


---

<h1 id="faddom-customer-success-demo-flow-enriched-edition"><strong>Faddom Customer Success Demo Flow (Enriched Edition)</strong></h1>
<hr>
<h2 id="dashboard"><strong>1) Dashboard</strong></h2>
<p><strong>Opening Statement:</strong><br>
“There’s a lot here—it’ll all make sense as we go through the demo. What’s important right now is that everything you see is fully customizable. You can have multiple dashboards and create new ones easily, tailored to different roles or teams.”</p>
<p><strong>Demonstration:</strong><br>
Show that multiple dashboards exist and demonstrate creating a new one. Highlight how KPIs, alerts, and widgets can be customized for operations, networking, or security teams.</p>
<p><strong>Value:</strong><br>
At a glance, you get full visibility into your critical IT metrics, without needing to switch tools. Everything that matters is on one screen—clear, centralized, and actionable.</p>
<hr>
<h2 id="search-–-example-vlan-3"><strong>2) Search – Example: VLAN 3</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This is one of our most powerful features—it’s like a Google search for your environment. It’s the fastest and easiest way to find and map any IT asset or connection in real time.”</p>
<p><strong>Demonstration:</strong><br>
Search for <code>VLAN 3</code>.<br>
Show the resulting map: each node represents a server or device, and each line represents a live network connection.</p>
<p><strong>Explain Layout:</strong><br>
Green lines indicate active connections, red show failed connections (usually a blocked port or down service), and gray represents inactive or historical links.<br>
Clarify direction arrows to show who’s initiating versus responding—this directional visibility is what makes Faddom unique.</p>
<p>Switch to list view, demonstrate filtering or sorting, and then show how to export the data as CSV, image, or Visio.</p>
<p><strong>Value:</strong><br>
“Once we know the direction of a connection, we immediately know the dependency.”<br>
This is what transforms Faddom from just a visual map into a dynamic dependency engine—automating what used to take hours of manual tracing.</p>
<hr>
<h2 id="application-maps"><strong>3) Application Maps</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This is the core of Faddom—mapping your applications and understanding exactly how they interact.”</p>
<p><strong>Demonstration:</strong><br>
Create an application map using traffic flow from <code>10.16.3.10</code>.<br>
Explain that Faddom reads real network traffic and automatically groups servers left to right—client, application, and backend tiers.<br>
When new connections appear, they’re highlighted in <strong>purple</strong>, showing live discovery.</p>
<p><strong>Save and Filter:</strong><br>
“It’s that quick and easy to create a map.”<br>
Show how filters can remove unnecessary noise—like email servers or monitoring agents—and mention AI-driven suggestions that help identify irrelevant systems automatically.</p>
<p><strong>Integrations &amp; Alerts:</strong><br>
Faddom’s notifications are granular and modular. They can be integrated with Syslog, Webhooks, or REST APIs, ensuring proactive alerts instead of post-incident analysis.<br>
“This is what makes Faddom proactive for you.”</p>
<p><strong>Impact Set:</strong><br>
Highlight the <em>Impact Set</em> feature. When a server is taken offline, you can instantly see which applications would be affected—avoiding what we call <em>the scream test</em>.</p>
<p><strong>Investigate &amp; RCA:</strong><br>
Drill into a server, open traffic charts, and show timestamp analysis.<br>
“This is where 90% of the solution is knowing the problem.”<br>
If traffic spikes or anomalies appear, Faddom helps pinpoint when and why, often before users even notice.</p>
<p><strong>Baselines &amp; Comparison:</strong><br>
Show the <strong>Current</strong>, <strong>Baseline</strong>, and <strong>Compare</strong> views.<br>
Tell the story:</p>
<blockquote>
<p>“If an engineer goes on vacation for a week, they can come back and immediately see all the changes that occurred—what was added, removed, or modified—without having to dig through logs.”<br>
Finish with:<br>
“We make the organization the owner of the topology, not any single individual.”</p>
</blockquote>
<p><strong>Value:</strong><br>
Every detail for root cause analysis (RCA) lives here—dramatically cutting response time for incidents and making post-incident forensics simple and transparent.</p>
<hr>
<h2 id="compass-ai"><strong>4) Compass AI</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This is like ChatGPT for your environment. You can ask it anything.”</p>
<p>Example: <em>‘When is the best time to take down Tomcat1 for maintenance?’</em><br>
Run the query.</p>
<p>While it processes (~30–40 seconds), mention:<br>
“All the data stays inside your environment. Nothing is sent to the cloud. It’s fully secure.”</p>
<p><strong>Explain Output:</strong><br>
Compass AI analyzes historical traffic and utilization, then returns the optimal downtime window and affected users.</p>
<p><strong>Value:</strong><br>
It’s the easiest way to get the right information—especially for new teams who don’t yet know where to find everything. Results can be exported to CSV for documentation and reporting.</p>
<hr>
<h2 id="subnet-dependencies-mapping"><strong>5) Subnet Dependencies Mapping</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This is the most powerful bird’s-eye view of your network.”</p>
<p><strong>Demonstration:</strong><br>
Show all subnets and the live traffic between them.<br>
“This view provides zero blind spots—you see everything, including east-west traffic between internal networks.”</p>
<p>Explain validation:<br>
These insights can be exported and cross-checked against your firewall rules. If something new appears, Faddom automatically alerts you.</p>
<p><strong>Story:</strong></p>
<blockquote>
<p>“Just last week, during an onboarding, the IT director saw that their test environment was communicating with production. We identified the source in seconds.”</p>
</blockquote>
<p><strong>Value:</strong><br>
It’s the easiest way to plan and validate segmentation. You can group networks by business unit, geography, or environment—production, test, DMZ—and immediately see unwanted communication.</p>
<hr>
<h2 id="shadow-it-detection"><strong>6) Shadow IT Detection</strong></h2>
<p><strong>Opening Statement:</strong><br>
“Shadow IT is often overlooked. Servers go online for temporary projects and never get taken down—it’s like leaving a door open that you didn’t even know existed.”</p>
<p><strong>Demonstration:</strong><br>
Show how inactive servers (no incoming or outgoing traffic) are identified automatically.</p>
<p><strong>Value:</strong><br>
Faddom closes those invisible doors—eliminating blind spots and improving security posture across your entire infrastructure.</p>
<hr>
<h2 id="servers-at-risk-–-faddom-score"><strong>7) Servers at Risk – Faddom Score</strong></h2>
<p><strong>Explanation:</strong><br>
Using all collected insights—traffic, dependencies, CVEs, OS versioning, and business context—Faddom assigns each server a <strong>risk score</strong>.</p>
<p>This isn’t just a vulnerability report; it prioritizes based on <strong>business impact</strong>, showing which servers matter most.</p>
<p><strong>Value:</strong><br>
“This is your go-to screen for daily risk management—open it in the morning, and you’ll instantly see what needs attention.”</p>
<hr>
<h2 id="lighthouse-ai-anomaly-detection"><strong>8) Lighthouse AI (Anomaly Detection)</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This is an upcoming feature—Lighthouse AI. It learns your traffic patterns and alerts you to anomalies automatically.”</p>
<p>This will eliminate manual threshold tuning, providing intelligent, context-aware alerts about unusual activity.</p>
<hr>
<h2 id="migration-and-dr-planning"><strong>9) Migration and DR Planning</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This is where you can plan all your migrations and disaster recovery strategies.”</p>
<p>The main screen shows all data sources and provides an initial lift-and-shift cost estimate, including right-sizing and optimization. But most organizations migrate by <strong>application</strong>, not the whole environment at once—these are called <em>migration waves</em>.</p>
<p><strong>Demonstration:</strong><br>
Create a new wave (for example, “AWS Migration – Europe”).<br>
Select applications, servers, or subnets.<br>
Show findings:</p>
<ul>
<li><strong>Cost analysis:</strong> based on instance type, network pricing, and right-sizing.</li>
<li><strong>Members &amp; Dependencies:</strong> automatically lists what will be affected.</li>
<li><strong>Dependency Mapping:</strong> visually displays upstream and downstream systems.</li>
<li><strong>Infrastructure Dependencies:</strong> identifies ports like DNS or NTP that must remain open.</li>
</ul>
<p><strong>Value:</strong><br>
“One server left behind is enough to break the business.”<br>
Faddom ensures nothing is missed—every dependency is visible, measurable, and traceable.</p>
<hr>
<h2 id="optimization"><strong>10) Optimization</strong></h2>
<p><strong>Opening Statement:</strong><br>
“Every megabyte of RAM has a cost—whether you’re on-prem or in the cloud.”</p>
<p><strong>Demonstration:</strong><br>
Show optimization recommendations:</p>
<ul>
<li>Some systems can be downsized to save costs.</li>
<li>Others are under-provisioned and should be scaled up.</li>
</ul>
<p>Explain that on VMware, RAM optimization shows allocation vs. usage, not actual consumption (since ESXi doesn’t expose that metric).</p>
<p><strong>Value:</strong><br>
Faddom continuously identifies the most efficient configuration for every resource—lowering costs without sacrificing performance.</p>
<hr>
<h2 id="inventory-and-asset-management"><strong>11) Inventory and Asset Management</strong></h2>
<p><strong>Opening Statement:</strong><br>
“This acts like a lightweight CMDB—automatically updated, agentless, and exportable.”</p>
<p><strong>Demonstration:</strong></p>
<ul>
<li>
<p><strong>Data Sources:</strong> List all connected environments.</p>
</li>
<li>
<p><strong>Software:</strong> Show installed applications across Windows and Linux servers.</p>
<blockquote>
<p>Story: An IT manager found a policy violation—a Bitcoin miner running on a forgotten VM. Faddom detected it immediately.</p>
</blockquote>
</li>
<li>
<p><strong>Operating Systems:</strong> Display end-of-life OS versions.</p>
<blockquote>
<p>Story: A customer was shocked to find two old Linux distributions they didn’t even know existed.</p>
</blockquote>
</li>
<li>
<p><strong>Users:</strong><br>
Show recently logged-in users, their activity maps, and inactive accounts.</p>
<blockquote>
<p>Story: One company discovered a breach through an inactive user who had left the company—Faddom caught the trace.</p>
</blockquote>
</li>
</ul>
<p><strong>Value:</strong><br>
You can see exactly who will be affected when a server goes offline—bringing it full circle to the “scream test.”<br>
“Be proactive, not reactive.”</p>
<hr>
<h2 id="wrap-up"><strong>12) Wrap-Up</strong></h2>
<p>Return to the <strong>Dashboard</strong> and tie it all together.<br>
Now, every widget, number, and alert makes sense in context—it’s the central hub that reflects everything you’ve just demonstrated.</p>
<p>Mention <strong>Captain AI Support</strong> for real-time in-app assistance and the ability to reach Faddom’s support team directly.</p>

