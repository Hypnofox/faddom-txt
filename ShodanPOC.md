---


---

<h1 id="shodan-integration-poc-–-one-pager">Shodan Integration POC – One Pager</h1>
<h3 id="objective">Objective</h3>
<p>Today Faddom maps what happens inside the network. With a small step, we can add an <strong>outside-in view</strong> by enriching those maps with data from Shodan. The goal of this proof of concept is to show that we can provide external exposure intelligence without compromising our passive, agentless posture. If we get this right, we prove three things at once: there is real customer value in having outside-in context, the engineering risk is minimal, and the user experience stays clean and intuitive.</p>
<hr>
<h3 id="why-it-matters">Why It Matters</h3>
<p>Every customer wants to know not just <em>what talks to what</em> internally, but also <em>what the world can see</em>. Shodan already indexes that information. If we can bring it into Faddom’s node panels with a click or two, we deliver instant clarity: open ports, exposed services, even known CVEs. Instead of juggling tools, IT and security teams would see internal flows and external exposure in the same map.</p>
<hr>
<h3 id="approach">Approach</h3>
<p>We add a lightweight <strong>enrichment service</strong> that handles all outbound calls. The service is stateless, cache-first, and always falls back to Shodan’s free InternetDB for baseline results. When a customer provides their own Shodan API key, or when we enable a demo key, the system can fetch deeper enrichment from the Shodan Host API. Results are cached with a sensible TTL, stored per tenant, and returned as a unified JSON payload.</p>
<p>From the user’s perspective it looks simple. They click a node in the map, open the side panel, and see an “Exposure Summary.” Open ports appear as chips, top CVEs are flagged with severity badges, and details can be expanded. They can refresh, run a deep lookup, or export a CSV or PDF report — all without leaving the map.</p>
<hr>
<h3 id="success-criteria">Success Criteria</h3>
<p>For the POC we scope it narrowly:</p>
<ul>
<li>Support a small subset of public IPs (10–50) and enrich them with Shodan data within two or three clicks.</li>
<li>Keep lookup latency under 500 ms on cached results, and acceptable even on cold lookups.</li>
<li>Keep the flow collection and processing path untouched; enrichment must remain out-of-band.</li>
<li>Provide a clear exportable report showing open ports and notable CVEs.</li>
</ul>
<hr>
<h3 id="implementation-plan">Implementation Plan</h3>
<p>This can be done in less than a week.</p>
<ul>
<li>Day 0–1: Spin up the enrichment service, connect Redis for caching, wire tenant auth, and implement the InternetDB client.</li>
<li>Day 2–3: Add the Shodan Host client behind a feature flag, merge models, and support tenant-supplied keys.</li>
<li>Day 4–5: Build the UI side panel with badges and export options, and add observability with latency metrics and cache hit rates.</li>
</ul>
<hr>
<h3 id="risks--mitigation">Risks &amp; Mitigation</h3>
<p>The main risks are rate limits and cost, which we mitigate with caching, on-demand deep lookups, and bring-your-own API keys. Data variance is solved by showing source badges, timestamps, and manual refresh. UX overload is addressed by collapsing details and only highlighting the top risks by default.</p>
<hr>
<h3 id="value">Value</h3>
<p>This POC doesn’t change who we are — a passive, agentless mapping platform. It extends our visibility to include the external footprint that every IT and security leader worries about. The combination of inside-out and outside-in views is powerful, and delivering it with minimal engineering effort makes it an easy win.</p>

