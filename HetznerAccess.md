---


---

<h1 id="opening"><strong>0. OPENING</strong></h1>
<p><strong>Say:</strong><br>
“Thanks for the time today. Before we start, here is the one line that frames everything you’re about to see.<br>
Faddom is a <strong>Business Application Dependency Mapping solution</strong>.<br>
It discovers how your applications actually behave in real time and gives you fast and accurate visibility across your entire environment using real traffic. Everything here is live, agentless, and easy to understand. We’ll go screen by screen, and feel free to stop me anytime.”</p>
<p><strong>Click:</strong><br>
<code>Dashboard</code></p>
<p><strong>Say:</strong><br>
“You will see the entire environment from here. This is where everything begins.”</p>
<hr>
<h1 id="dashboard"><strong>1. DASHBOARD</strong></h1>
<h3 id="high-level"><strong>High Level</strong></h3>
<p>“Faddom has three built-in dashboards: IT, Security, and Migration. You can create your own dashboards for networking, operations, asset teams, or executives. Dashboards can be public or private.”</p>
<p><strong>Click:</strong><br>
<code>Dashboard → Toggle Platform Guidance</code></p>
<p><strong>Say:</strong><br>
“This panel explains every screen. The platform teaches itself. Anyone can pick it up in minutes.”</p>
<h3 id="deep-dive"><strong>Deep Dive</strong></h3>
<p>Show a widget. Move it. Add one. Duplicate the dashboard.</p>
<h3 id="value--wow"><strong>Value / Wow</strong></h3>
<p>“This is your single pane of truth. No switching tools or hunting for context.”</p>
<hr>
<h1 id="search"><strong>2. SEARCH</strong></h1>
<h3 id="high-level-1"><strong>High Level</strong></h3>
<p>“This is your entry point into anything in the environment.”</p>
<h3 id="deep-dive-1"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Search → type VLAN 3</code><br>
(or IP, hostname, URL, port, subnet, tag, or user)</p>
<p><strong>Say:</strong><br>
“You can search for practically anything. VLANs, servers, URLs, ports, subnets.<br>
If Active Directory is integrated, you can even search for a user and see their login activity and every server they accessed.”</p>
<h3 id="value--wow-1"><strong>Value / Wow</strong></h3>
<p>“One search replaces tribal knowledge and takes you straight into topology.”</p>
<hr>
<h1 id="basic-map"><strong>3. BASIC MAP</strong></h1>
<h3 id="high-level-2"><strong>High Level</strong></h3>
<p>“This is your real traffic. Every arrow is a real connection.”</p>
<h3 id="deep-dive-2"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
Open the map.</p>
<p>Explain color codes:</p>
<ul>
<li><strong>Green</strong> – active right now</li>
<li><strong>Red</strong> – request sent with no response (firewall block, VM down, service not listening)</li>
<li><strong>Gray</strong> – historical traffic (example: last night’s backup run)</li>
</ul>
<p><strong>Click:</strong><br>
<code>Export → CSV, Visio, PNG</code></p>
<p><strong>Say:</strong><br>
“You can export documentation instantly or pull it through the API.”</p>
<p>Then:<br>
<code>Save this search as a map</code></p>
<h3 id="value--wow-2"><strong>Value / Wow</strong></h3>
<p>“You just created a live, dynamic map in one click. From now on Faddom tracks all changes for you.”</p>
<hr>
<h1 id="application-map-creation"><strong>4. APPLICATION MAP CREATION</strong></h1>
<h3 id="high-level-3"><strong>High Level</strong></h3>
<p>“We can create maps in three ways: saving a search, using Traffic Flow, or using tags.”</p>
<p><strong>Say:</strong><br>
“Faddom pulls tags automatically from VMware, Nutanix, Azure, and AWS. Hyper-V tags can be imported. You can map by ownership, environment, region, or anything else you tag.”</p>
<hr>
<h2 id="traffic-flow"><strong>Traffic Flow</strong></h2>
<h3 id="high-level-4"><strong>High Level</strong></h3>
<p>“This is how you map an application based on real user traffic.”</p>
<h3 id="deep-dive-3"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Application Maps → Create and Discover Map → Traffic Flow</code></p>
<p><strong>Say:</strong><br>
“The hint here shows exactly what you can enter.<br>
<strong>URL / Server:port / Partial hostname.</strong><br>
Even partial information is enough. Faddom does the rest.”</p>
<p>Steps:</p>
<ol>
<li>Enter <code>10.16.3.10</code></li>
<li>Select ports</li>
<li>Generate the map</li>
</ol>
<p>Explain layers:<br>
“Each layer is a hop in the network. You control depth so dependencies are mapped with absolute clarity.”</p>
<p>Explain tiers:<br>
“Tiers are grouped by behavior and ports. You can lock tiers, hover to see outbound dependencies, and pin important connections so they are always shown.”</p>
<p>Explain purple:<br>
“Purple means newly discovered live traffic.”</p>
<p>Explain slider:<br>
“Toggles help reduce noise and adjust visibility.”</p>
<hr>
<h2 id="list-view"><strong>List View</strong></h2>
<h3 id="high-level-5"><strong>High Level</strong></h3>
<p>“This is your microsegmentation table.”</p>
<h3 id="deep-dive-4"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>List View</code></p>
<p>“Excel style. Source → Port → Destination.<br>
Filter by servers or connections. Add OS name, CPU peaks, RAM peaks, and more.”</p>
<h3 id="value--wow-3"><strong>Value / Wow</strong></h3>
<p>“You can build segmentation policy or firewall rules directly from this table.”</p>
<hr>
<h1 id="baselines-and-change-tracking"><strong>5. BASELINES AND CHANGE TRACKING</strong></h1>
<h3 id="high-level-6"><strong>High Level</strong></h3>
<p>“Faddom tracks drift automatically.”</p>
<h3 id="deep-dive-5"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Baseline → Compare</code><br>
Show ports, servers, and tiers that changed.</p>
<h3 id="value--wow-4"><strong>Value / Wow</strong></h3>
<p>“Someone leaves for a week and returns to a complete change log. Zero detective work.”</p>
<hr>
<h1 id="root-cause-analysis"><strong>6. ROOT CAUSE ANALYSIS</strong></h1>
<h3 id="high-level-7"><strong>High Level</strong></h3>
<p>“This is troubleshooting made simple.”</p>
<h3 id="deep-dive-6"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
Server → <code>Charts</code></p>
<p>Choose a low point. Choose a spike.</p>
<p><strong>Say:</strong><br>
“Faddom shows who connected, what changed, and what started or stopped communicating. Everything is clickable and exportable.”</p>
<p>Add user insight:<br>
“Zero user activity can be just as important.”</p>
<h3 id="value--wow-5"><strong>Value / Wow</strong></h3>
<p>“Ninety percent of the fix is understanding the problem. Here it takes seconds.”</p>
<hr>
<h1 id="impact-set"><strong>7. IMPACT SET</strong></h1>
<h3 id="high-level-8"><strong>High Level</strong></h3>
<p>“This shows what breaks if a server goes offline.”</p>
<h3 id="deep-dive-7"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Add to Impact Set</code><br>
Show the application impact.</p>
<h3 id="value--wow-6"><strong>Value / Wow</strong></h3>
<p>“This kills the scream test. You know the blast radius before touching anything.”</p>
<hr>
<h1 id="segmentation-and-subnet-dependencies"><strong>8. SEGMENTATION AND SUBNET DEPENDENCIES</strong></h1>
<h3 id="high-level-9"><strong>High Level</strong></h3>
<p>“This is the bird’s eye view of your network.”</p>
<h3 id="deep-dive-8"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Maps → Subnet Dependencies</code></p>
<p>Group subnets by:</p>
<ul>
<li>prod, dev, test</li>
<li>data center</li>
<li>business unit</li>
<li>region</li>
</ul>
<h3 id="value--wow-7"><strong>Value / Wow</strong></h3>
<p>“Accidental communication jumps out instantly. Test talking to production is always a moment.”</p>
<hr>
<h1 id="security-module"><strong>9. SECURITY MODULE</strong></h1>
<h3 id="high-level-10"><strong>High Level</strong></h3>
<p>“This is where visibility becomes security.”</p>
<h3 id="deep-dive-9"><strong>Deep Dive</strong></h3>
<p><strong>Shadow IT:</strong><br>
Systems with little or no traffic.</p>
<p><strong>Servers at Risk:</strong><br>
Risk score combining CVEs, OS lifecycle, software, exposure, and application impact.</p>
<p><strong>Certificates:</strong><br>
Expiration for all certificates in the environment.</p>
<h3 id="value--wow-8"><strong>Value / Wow</strong></h3>
<p>“You see risks no CMDB or monitoring tool can detect. And you see them in minutes.”</p>
<hr>
<h1 id="optimization"><strong>10. OPTIMIZATION</strong></h1>
<h3 id="high-level-11"><strong>High Level</strong></h3>
<p>“Every resource has a cost.”</p>
<h3 id="deep-dive-10"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Optimization</code></p>
<p>Show downsize and upsize opportunities.</p>
<p>VMware note: memory is based on allocation.</p>
<h3 id="value--wow-9"><strong>Value / Wow</strong></h3>
<p>“Right sizing becomes obvious. Instant savings.”</p>
<hr>
<h1 id="migration-and-dr-planning"><strong>11. MIGRATION AND DR PLANNING</strong></h1>
<h3 id="high-level-12"><strong>High Level</strong></h3>
<p>“This is one of the biggest value drivers.”</p>
<h3 id="deep-dive-11"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Migration and DR → Create Wave</code></p>
<p>Steps:</p>
<ol>
<li>Name wave</li>
<li>Add servers, apps, or subnets</li>
<li>Members and Dependencies</li>
<li>Cost Analysis</li>
<li>Infrastructure Dependencies</li>
</ol>
<h3 id="value--wow-10"><strong>Value / Wow</strong></h3>
<p>“One missing server breaks a migration. With Faddom it is impossible to miss anything.”</p>
<hr>
<h1 id="inventory"><strong>12. INVENTORY</strong></h1>
<h3 id="high-level-13"><strong>High Level</strong></h3>
<p>“Your lightweight CMDB, always accurate.”</p>
<h3 id="deep-dive-12"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Inventory</code></p>
<p>Show:</p>
<ul>
<li>Servers</li>
<li>OS versions</li>
<li>Installed software</li>
<li>Logged-in users</li>
<li>Inactive accounts</li>
<li>End of life systems</li>
</ul>
<h3 id="value--wow-11"><strong>Value / Wow</strong></h3>
<p>“This is not documentation. This is reality.”</p>
<hr>
<h1 id="compass-ai"><strong>13. COMPASS AI</strong></h1>
<h3 id="high-level-14"><strong>High Level</strong></h3>
<p>“This is natural language for your infrastructure.”</p>
<h3 id="deep-dive-13"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Compass AI</code></p>
<p>Ask example:<br>
“When is the best time to take Tomcat1 down”<br>
“Which users depend on Server X”<br>
“What changed in the last 48 hours”</p>
<p>Clarify data handling:<br>
Data stays inside. Only analysis is external.</p>
<h3 id="value--wow-12"><strong>Value / Wow</strong></h3>
<p>“It gives new teams instant understanding.”</p>
<hr>
<h1 id="offline-mode-agentless-design-integrations"><strong>14. OFFLINE MODE, AGENTLESS DESIGN, INTEGRATIONS</strong></h1>
<h3 id="high-level-15"><strong>High Level</strong></h3>
<p>“Faddom runs without agents and can operate fully offline.”</p>
<h3 id="deep-dive-14"><strong>Deep Dive</strong></h3>
<p><strong>Click:</strong><br>
<code>Settings → Notifications</code></p>
<p>Show integration options:</p>
<ul>
<li>Syslog</li>
<li>Webhooks</li>
<li>REST API</li>
<li>ServiceNow</li>
<li>CMDBs</li>
<li>SIEM</li>
<li>SOAR</li>
<li>Ticketing systems</li>
</ul>
<p>Explain offline mode:<br>
“All core functionality runs without internet. Ideal for air-gapped environments.”</p>
<h3 id="value--wow-13"><strong>Value / Wow</strong></h3>
<p>“The entire environment gets mapped without placing a single agent anywhere. Zero footprint. Zero performance cost.”</p>
<hr>
<h1 id="closing"><strong>15. CLOSING</strong></h1>
<p><strong>Say:</strong><br>
“In this session we went from zero visibility to full clarity. You saw applications, segmentation, dependencies, risks, optimization, migration waves, and user activity, all from one platform.<br>
This is the only fully agentless real time topology solution. It removes guesswork and replaces tribal knowledge.”</p>
<p><strong>Say:</strong><br>
“Now let me know what you want to dive into.”</p>

