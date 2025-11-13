---


---

<h1 id="faddom.-executive-demo-script-final-corrected-2025"><strong>FADDOM. EXECUTIVE DEMO SCRIPT (FINAL, CORRECTED, 2025)</strong></h1>
<hr>
<h1 id="intro---why-faddom-matters-in-2025"><strong>INTRO - Why Faddom Matters in 2025</strong></h1>
<p>“Before we jump into the product, here’s 60 seconds of context.”</p>
<p>Faddom is a hybrid-IT observability and dependency-mapping platform recognized by Gartner in 2025 as a <strong>stand-alone, agentless tool</strong> built for migrations, risk reduction, cloud acceleration, and operational clarity.</p>
<p>The core value is simple:</p>
<p><strong>fast deployment, instant visibility, and always-accurate topology.</strong></p>
<p>Faddom deploys in under an hour, runs <strong>agentless and can operate fully offline</strong>, keeps <strong>all data on-prem</strong>, and integrates with every major platform - <strong>VMware, Hyper-V, AWS, Azure, GCP, and Nutanix</strong>.</p>
<p>And it is aligned with ISO-27001 and approved for sensitive, regulated environments.</p>
<p><strong>“Faddom delivers real-time visibility without agents or instrumentation. Credentials are only required for optional enrichments such as CVEs, user discovery, and hypervisor integration.”</strong></p>
<hr>
<h1 id="section-1.-dashboard-the-single-pane-of-truth"><strong>SECTION 1. DASHBOARD (THE SINGLE PANE OF TRUTH)</strong></h1>
<p>“This is where everything comes together.”</p>
<h3 id="highly-customizable"><strong>Highly Customizable</strong></h3>
<p>Every widget can be added, removed, resized, or rearranged so Operations, Security, Architecture, or Leadership can each see what matters most.</p>
<h3 id="platform-guidance"><strong>Platform Guidance</strong></h3>
<p>Faddom includes built-in guidance with:</p>
<ul>
<li><strong>contextual explanations about each screen</strong></li>
<li><strong>short descriptions of what the user is viewing</strong></li>
</ul>
<p>This makes the product immediately usable for first-time engineers and executives.</p>
<p>“This is real-time, not a manually drawn diagram.”</p>
<hr>
<h1 id="section-2.-change-management-live-topology--rca"><strong>SECTION 2. CHANGE MANAGEMENT (LIVE TOPOLOGY &amp; RCA)</strong></h1>
<p>“This is the heart of the platform - continuous, real-time change detection.”</p>
<h3 id="search-→-instant-map"><strong>Search → Instant Map</strong></h3>
<p>Search for “VLAN 3”:</p>
<ul>
<li>directional connections</li>
<li>color-coded traffic (green, red, gray)</li>
<li>list view and export (CSV, Visio, PNG, REST API)</li>
</ul>
<h3 id="the-value"><strong>The Value</strong></h3>
<p>Once we know <strong>direction</strong>, we know <strong>dependency</strong>, the core of accurate mapping.</p>
<h3 id="baselines--comparisons"><strong>Baselines &amp; Comparisons</strong></h3>
<p>Record a baseline → compare to current:</p>
<ul>
<li>what changed</li>
<li>what was added</li>
<li>what was removed</li>
<li>when it happened</li>
</ul>
<h3 id="impact-set"><strong>Impact Set</strong></h3>
<p>Select a server → “Add to Impact Set”<br>
See exactly which applications would break if it disappeared.</p>
<p>“No more scream test, you know before you act.”</p>
<h3 id="investigate--rca"><strong>Investigate / RCA</strong></h3>
<p>Open any connection → charts, trends, spikes, timestamps.</p>
<p><strong>“Most incidents are solved the moment you know where the change occurred.”</strong></p>
<hr>
<h1 id="section-3.-discovery-automatic-adm--asset-intelligence"><strong>SECTION 3. DISCOVERY (AUTOMATIC ADM + ASSET INTELLIGENCE)</strong></h1>
<h3 id="hybrid-application-mapping"><strong>Hybrid Application Mapping</strong></h3>
<p>Create an app map from real traffic (e.g., 10.16.3.10):</p>
<ul>
<li>auto-tiered layout</li>
<li>purple = new dependencies</li>
<li>filtering (remove noise from monitoring/email agents)</li>
<li>save map in seconds</li>
<li>export to CMDB, REST, Visio, CSV</li>
</ul>
<p>“This makes the organization, not an individual — the owner of the application topology.”</p>
<h3 id="inventory-lightweight-cmdb"><strong>Inventory (Lightweight CMDB)</strong></h3>
<p>Faddom automatically collects:</p>
<ul>
<li>servers</li>
<li>OS versions.</li>
<li>installed software</li>
<li>recent user activity*</li>
<li>SSL certificates</li>
<li>IP groups &amp; custom tags</li>
</ul>
<p>(<em>requires optional credential enrichment</em>)</p>
<p>Use case:<br>
A customer discovered a rogue <strong>Bitcoin miner</strong> installed on an unmonitored system.</p>
<h3 id="user-discovery-optional-credential-integration"><strong>User Discovery (optional credential integration)</strong></h3>
<p>Track who logged into which servers and when.</p>
<p>Use case:<br>
A company discovered a <strong>dormant account</strong> was still active and was later used maliciously.</p>
<hr>
<h1 id="section-4.-cybersecurity-risk-shadow-it-anomalies"><strong>SECTION 4. CYBERSECURITY (RISK, SHADOW IT, ANOMALIES)</strong></h1>
<p>“This is where visibility turns into security.”</p>
<h3 id="shadow-it"><strong>Shadow IT</strong></h3>
<p>Find outdated, unused, unpatched, or orphaned systems.</p>
<p>“It’s like discovering a hidden door in your house, and now you get to lock it.”</p>
<h3 id="risk-scoring"><strong>Risk Scoring</strong></h3>
<p>Faddom prioritizes risks by combining:</p>
<ul>
<li>CVEs*</li>
<li>OS EOL status</li>
<li>business context</li>
<li>external exposure</li>
<li>traffic patterns</li>
</ul>
<p>(<em>requires credentials for CVE enrichment</em>)</p>
<h3 id="ssl-certificates"><strong>SSL Certificates</strong></h3>
<p>See certificate health and expiration across the estate.</p>
<h3 id="segmentation--zero-trust-planning"><strong>Segmentation / Zero Trust Planning</strong></h3>
<p>North–south + east–west traffic mapped automatically.</p>
<p>Use case:<br>
Customer immediately noticed <strong>test</strong> talking to <strong>production</strong> by mistake.</p>
<h3 id="lighthouse-ai.-traffic-anomaly-detection"><strong>Lighthouse AI. Traffic Anomaly Detection</strong></h3>
<p>(Alpha / Early Access)</p>
<p>Detects:</p>
<ul>
<li>DoS</li>
<li>MITM</li>
<li>DNS spoofing</li>
<li>port scans</li>
<li>data exfiltration</li>
<li>outages</li>
<li>packet loss</li>
<li>latency spikes</li>
</ul>
<p>Requires:</p>
<ul>
<li>2 weeks of data</li>
<li>Internet connection</li>
</ul>
<p>All data sent is anonymized and encrypted.</p>
<p>“This is your early-warning radar.”</p>
<hr>
<h1 id="section-5.-migration--dr-planning"><strong>SECTION 5. MIGRATION &amp; DR PLANNING</strong></h1>
<p>“This is where Faddom pays for itself.”</p>
<h3 id="migration-waves"><strong>Migration Waves</strong></h3>
<ul>
<li>Give the wave a name</li>
<li>Choose target cloud (AWS / Azure / GCP)</li>
<li>Add apps, servers, subnets</li>
<li>See all dependencies</li>
<li>Catch anything that would break</li>
<li>Generate required infra (DNS, NTP, ports, LB rules)</li>
</ul>
<h3 id="cost-analysis"><strong>Cost Analysis</strong></h3>
<p>Faddom calculates expected cloud cost:</p>
<ul>
<li>compute</li>
<li>storage</li>
<li>bandwidth/egress</li>
</ul>
<p>All adjustable by the organization.</p>
<p><strong>Value:</strong><br>
“One forgotten server is enough to break an entire migration.”</p>
<h3 id="dr--business-continuity"><strong>DR / Business Continuity</strong></h3>
<p>Same engine, but different question:<br>
What must be restored together?</p>
<hr>
<h1 id="section-6.-optimization-performance--cost"><strong>SECTION 6. OPTIMIZATION (PERFORMANCE &amp; COST)</strong></h1>
<p>“Every megabyte of RAM has a cost.”</p>
<p>Faddom analyzes:</p>
<ul>
<li>CPU</li>
<li>RAM</li>
<li>network behavior</li>
<li>historical peaks</li>
</ul>
<h3 id="rightsizing"><strong>Rightsizing</strong></h3>
<p>Recommend:</p>
<ul>
<li>downsizing idle servers</li>
<li>upsizing stressed servers</li>
<li>optimizing both on-prem and cloud</li>
</ul>
<p>For VMware memory recommendations, Faddom uses allocated memory (since consumed is not exposed).</p>
<hr>
<h1 id="section-7.-the-ai-layer-compass-lighthouse-captain"><strong>SECTION 7. THE AI LAYER (COMPASS, LIGHTHOUSE, CAPTAIN)</strong></h1>
<p>“This is where we go from visibility to intelligence.”</p>
<h3 id="compass-ai---chatgpt-for-your-environment"><strong>Compass AI - ChatGPT for Your Environment</strong></h3>
<p>If the search bar is Google, Compass AI is the ChatGPT interface over your entire topology.</p>
<p>Ask things like:</p>
<ul>
<li>“When is the best time to take down Tomcat1?”</li>
<li>“Which users will be impacted if Server X goes offline?”</li>
<li>“Show all outbound connections from Application Y.”</li>
</ul>
<p>Requires Internet + licensed seat.<br>
Processing happens securely in Faddom’s cloud; results stay local.</p>
<h3 id="lighthouse-ai---anomaly-detection"><strong>Lighthouse AI - Anomaly Detection</strong></h3>
<p>(Already covered above)</p>
<h3 id="captain-ai---support-automation"><strong>Captain AI - Support Automation</strong></h3>
<p>Captain is the AI support assistant inside Faddom.</p>
<p>The value:<br>
<strong>Every conversation automatically opens a support ticket.</strong><br>
The support team is looped in when needed, without the user doing anything.</p>
<hr>
<h1 id="section-8.-offline-mode-agentless-architecture--integrations"><strong>SECTION 8. OFFLINE MODE, AGENTLESS ARCHITECTURE &amp; INTEGRATIONS</strong></h1>
<h3 id="agentless-architecture"><strong>Agentless Architecture</strong></h3>
<ul>
<li>No agents</li>
<li>No instrumentation</li>
<li>No performance overhead</li>
<li>All core mapping is 100% passive</li>
</ul>
<p>(<strong>Credentials only needed for enrichments.</strong>)</p>
<h3 id="offline-mode"><strong>Offline Mode</strong></h3>
<p>Core mapping works with <strong>no Internet at all</strong>, which is perfect for air-gapped networks.</p>
<p>(Compass &amp; Lighthouse require Internet.)</p>
<h3 id="integrations"><strong>Integrations</strong></h3>
<ul>
<li>Syslog</li>
<li>Webhooks</li>
<li>REST APIs</li>
<li>CMDB population</li>
<li>SIEM &amp; SOAR enrichment</li>
<li>External ticketing systems</li>
</ul>
<hr>
<h1 id="conclusion.-why-executives-care"><strong>CONCLUSION. WHY EXECUTIVES CARE</strong></h1>
<p>“In 60 minutes we went from zero visibility to full clarity.”</p>
<p>Faddom helps organizations:</p>
<ul>
<li>eliminate blind spots</li>
<li>reduce operational risk</li>
<li>accelerate migrations</li>
<li>detect threats early</li>
<li>respond to incidents faster</li>
<li>optimize cost and performance</li>
<li>cut through complexity</li>
<li>unify tribal knowledge</li>
</ul>
<p>“This is how you turn a complex, hybrid environment into something predictable and manageable.”</p>

