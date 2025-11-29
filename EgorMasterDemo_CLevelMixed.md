# FADDOM C-LEVEL DEMO SCRIPT
## Mixed Audience: CPO, CTO, CRO + Bar
### 90-Minute Window | Outcome-Focused | Technically Credible

---

## PRE-DEMO SETUP (Do This Before They Arrive)

**Technical Prep:**
- Open Faddom in one browser tab
- Have a second tab ready for any backup demos
- Clear browser history/cache for performance
- Test search functionality beforehand
- Verify VLAN 3 example still works
- Have export examples ready to show (don't generate live unless asked)

**Mental Prep:**
- This is a performance, not a lecture
- Outcomes first, technical depth on demand
- Let silence work for you - don't fill gaps
- When they ask technical questions, answer crisply then return to the flow
- Bar needs to see you command the room, not scramble

---

## OPENING (3 minutes)
### Goal: Frame the conversation around their pain, not your product

**Say:**
"Thanks for your time today. Before we jump into the platform, here's the one-minute context on why this matters.

Every organization today has the same challenge: you have legacy systems, virtual infrastructure, cloud workloads, Kubernetes, SaaS, physical hardware, and servers you inherited. Nobody really knows what talks to what.

Documentation is outdated the moment it's written. CMDBs are bloated and inaccurate. Tribal knowledge lives in the heads of two or three people.

And that lack of visibility shows up at the worst possible moment:
- During an outage
- During a migration  
- During a cyber incident
- During maintenance windows
- During staff turnover

What I'm going to show you today is how Faddom eliminates that blind spot permanently - giving you real-time, accurate visibility into how your environment actually works, not how you think it works."

**Pause. Let that land.**

---

## SECTION 1: DASHBOARD - THE COMMAND CENTER (5 minutes)
### Goal: Show unified visibility without overwhelming detail

**Click:** Dashboard

**Say:**
"This is where everything comes together. Every widget can be customized per team - operations, networking, security, migration teams each see what matters to them.

Notice this platform guidance feature. [Toggle it on/off quickly] Short contextual explanations so anyone can pick up the platform in minutes. This removes the tribal knowledge problem on day one."

**Point out (don't deep-dive):**
- Real-time metrics updating
- Multiple dashboard capability
- Role-based customization

**Value statement:**
"One unified view of your entire infrastructure. No tool switching. No blind spots."

**CTO will likely ask:** "What data sources feed this?"
**Answer:** "NetFlow, sFlow, IPFIX from your network infrastructure, plus API integrations with VMware, AWS, Azure, GCP, and Nutanix. Everything stays on-prem - nothing leaves your environment. I'll show you the collection architecture in detail if you want to dive into that."

---

## SECTION 2: SEARCH - GOOGLE FOR YOUR INFRASTRUCTURE (7 minutes)
### Goal: First "drop the mic" moment

**Click:** Search bar

**Say:**
"This is usually my first move. Think of it as Google for your infrastructure."

**Type:** `VLAN 3` (or whatever your best example is)

**As results appear:**
"Type anything - a server name, IP, subnet, VLAN, tag, custom group. Instant results.

But here's what matters..."

**Open the map view**

**Say:**
"Each arrow shows real traffic. The direction shows who initiated the connection. And once we know the direction of a connection, we immediately know the dependency.

Green means active right now.
Red means request sent but no response - usually a firewall block or service down.
Gray means previously active.

This is live. This is what's happening in your environment right now."

**Click on a connection, show details**

**Say:**
"Port, protocol, volume, timestamps. Everything you need to understand the relationship."

**Switch to list view**
"Same data, different view. Export to CSV, Visio, PNG, or pull through REST API."

**Value statement:**
"This replaces tribal knowledge on day one. The engineer who set this up five years ago and just left? You don't need them anymore."

**DROP THE MIC MOMENT #1:** The instant visualization of live dependencies

---

## SECTION 3: APPLICATION MAPPING - THE HEART OF IT (12 minutes)
### Goal: Show how you transform traffic into business understanding

**Click:** Application Maps → Create & Discover Map

**Say:**
"This is the core of what we do. We map applications the same way your users access them."

**Walk through creating a map:**
1. "Enter the entry point - URL, load balancer, hostname"
2. "Select the ports that matter"
3. "Watch Faddom discover the tiers automatically"

**As the map builds:**
"See how it groups left to right - client tier, application tier, backend tier. This is real traffic, real behavior, happening right now.

Purple connections? Those are newly discovered dependencies. Real-time."

**Save the map**

**Click:** Change Summary

**Say:**
"Here's what changed. New servers added, removed, new connections discovered.

Let me tell you why this matters. [Lean in slightly]

When an engineer goes on vacation for a week, they come back and see exactly what changed - fully documented, no log diving, no asking around.

We make the organization the owner of the topology, not any single individual."

**CTO will likely ask:** "How does this handle dynamic environments like Kubernetes?"
**Answer:** "Kubernetes pods are ephemeral - mapping them is useless. We map service-to-service communication, not pod-to-pod. The business cares about stable service dependencies, not which pod is running this second. Want me to show you a K8s example?"

**Value statement:**
"This shifts knowledge from individuals to the organization."

**DROP THE MIC MOMENT #2:** The change tracking that shows what happened while someone was gone

---

## SECTION 4: IMPACT SET - NO MORE SCREAM TESTS (6 minutes)
### Goal: Show predictive impact analysis

**Click:** Pick a server → Add to Impact Set

**Say:**
"Here's a question every IT leader dreads: 'What breaks if we take this server down?'

Traditional answer? The scream test - take it down and see who screams.

Faddom's answer? Two clicks."

**Show the impact visualization**

**Say:**
"These are all the applications that depend on this server. These are the users who will be affected. This is the blast radius.

Before you touch anything, you know:
- Who relies on it
- What systems it supports  
- What unexpected connections exist
- How critical it is to the business

No spreadsheets. No guessing. No surprises."

**CPO will likely ask:** "Can this integrate with our change management process?"
**Answer:** "Yes - REST API, webhooks, and Syslog integration. Many customers auto-generate impact analysis in their ServiceNow or Jira change tickets. Want to see the API documentation?"

**DROP THE MIC MOMENT #3:** Two clicks to know what breaks

---

## SECTION 5: ROOT CAUSE INVESTIGATION (8 minutes)
### Goal: Show how you compress MTTR

**Click:** Pick a server with interesting traffic patterns → Charts

**Say:**
"During an outage, the question is always: What changed, and what's impacted?

Let me show you how Faddom answers that."

**Point to a traffic spike or anomaly**

**Click:** The timestamp

**Say:**
"We're now looking at this exact moment. See these new connections that appeared? See the volume change? See which users were active?

Most incidents are solved the moment you know where the change occurred. This gives you that answer in seconds, not hours."

**Show the investigate panel**

**Say:**
"Historical charts, trends, spikes, timestamps. Everything you need for root cause analysis without log diving."

**Value statement:**
"Mean time to resolution drops dramatically when you can see the dependency chain instantly."

**DROP THE MIC MOMENT #4:** Click a timestamp, see exactly what changed

---

## SECTION 6: SUBNET DEPENDENCIES - THE BIRD'S EYE VIEW (7 minutes)
### Goal: Show network-wide visibility and segmentation

**Click:** Maps → Subnet Dependencies

**Say:**
"This is the bird's eye view of your entire network. Every subnet, every connection, live.

You can group this by:
- Production, test, dev
- Geography  
- Data center
- Business unit

Watch what happens when we apply grouping..."

**Apply a grouping**

**Say:**
"Now you see traffic patterns across your entire organization. East-west internal traffic and north-south external traffic.

Let me tell you a story. Last week during an onboarding, an IT director saw that their test environment was communicating with production. We identified the source in seconds.

This is instant segmentation validation and firewall rule planning."

**CRO will likely ask:** "What's the business impact of finding these issues?"
**Answer:** "One customer prevented a compliance violation worth $2M in fines by catching test-to-production communication before an audit. Another avoided a ransomware spread that would have cost them 72 hours of downtime. We help you find problems before they become expensive."

**DROP THE MIC MOMENT #5:** Finding test-to-production communication that shouldn't exist

---

## SECTION 7: SECURITY - SHADOW IT AND RISK SCORING (8 minutes)
### Goal: Show proactive security posture

**Click:** Security → Shadow IT

**Say:**
"These are servers with no meaningful traffic. Leftover projects, forgotten test systems, orphaned machines.

Every one of these is a door you didn't know was open."

**Click:** Security → Servers at Risk

**Say:**
"This isn't just a CVE list. We combine:
- Vulnerabilities
- OS end-of-life  
- Software state
- External exposure
- Business context
- Traffic behavior

Into a single priority score based on actual business impact."

**Point to a high-risk server**

**Say:**
"This server matters because it's connected to your payment processing. This one doesn't because it's isolated in dev. Same CVE, different priority.

This is your go-to screen every morning - open it and instantly see what needs attention."

**Value statement:**
"Visibility becomes security when you can see the shadows."

---

## SECTION 8: MIGRATION PLANNING (10 minutes)
### Goal: Show how this prevents migration disasters

**Click:** Migration & DR → Create Wave

**Say:**
"This is where Faddom pays for itself.

Cloud migrations break when hidden dependencies show up too late. Same with datacenter exits, VMware to Nutanix shifts, application modernization.

Let me show you how we eliminate that risk."

**Create a wave example**

**Say:**
"We plan migrations by dependencies, not by spreadsheets.

Choose your target - AWS, Azure, GCP, on-prem.
Add applications, servers, or subnets.
See all dependencies automatically.
Identify anything that will break.
Get infrastructure requirements - DNS, NTP, firewall rules, everything."

**Show the cost analysis**

**Say:**
"Estimate costs for compute, storage, egress. Adjustable based on your enterprise pricing.

But here's the critical part..."

**Show the dependency visualization**

**Say:**
"One server left behind is enough to break the business. Faddom ensures nothing is missed.

Every dependency is visible, measurable, traceable."

**CPO will likely ask:** "How does this integrate with our existing migration tooling?"
**Answer:** "API exports for wave planning, dependency lists, cost estimates - all programmatically available. Customers integrate with ServiceNow, Jira, Azure Migrate, AWS Migration Hub. We provide the visibility layer, you use your existing process."

**DROP THE MIC MOMENT #6:** Showing a dependency that would have been missed

---

## SECTION 9: OPTIMIZATION - EVERY MEGABYTE HAS A COST (5 minutes)
### Goal: Show cost reduction opportunities

**Click:** Optimization

**Say:**
"Every megabyte of RAM has a cost - whether on-prem or cloud.

Based on live behavior, we recommend:
- Downsizing idle systems
- Upsizing stressed systems  
- Right-sizing for actual usage

For VMware environments, recommendations are based on allocated memory since ESXi doesn't expose actual consumption."

**Show examples**

**Say:**
"This system can be downsized - saving $X per month.
This one is under-provisioned and should be scaled up - before it becomes an incident.

Continuous optimization without manual analysis."

---

## SECTION 10: THE AI LAYER (8 minutes)
### Goal: Show the intelligence, not just visibility

**Click:** Compass AI (but DON'T run queries unless asked)

**Say:**
"If the search bar is Google for your infrastructure, Compass AI is your ChatGPT.

You can ask questions like:
- When is the best time to take down Tomcat1?
- Which users depend on this server?  
- What changed in the last 48 hours?
- Show all outbound connections from Application Y

All processing happens in Faddom cloud, but all data stays in your environment. Nothing leaves."

**Mention Lighthouse AI:**
"Lighthouse AI is our traffic anomaly detection - currently in alpha. It learns your patterns and alerts you to:
- DoS attacks
- MITM attempts  
- DNS spoofing
- Port scans
- Data exfiltration
- Performance degradation

Requires two weeks of baseline data and an internet connection. All data sent is anonymized and encrypted."

**Value statement:**
"Visibility becomes intelligence."

---

## SECTION 11: TECHNICAL ARCHITECTURE (5 minutes - Only if CTO asks)
### Goal: Establish technical credibility without derailing

**Say:**
"Let me show you how this actually works under the hood.

Faddom is fully on-premises. Virtual appliance running Tomcat and PostgreSQL. Nothing leaves your environment.

Traffic collection:
- VMware: Sensors in promiscuous mode on each ESXi host for east-west visibility
- Hyper-V/KVM: HostSFlow on the hypervisor hosts
- Cloud: Native flow logs from AWS VPC, Azure NSG, GCP VPC
- Network: NetFlow, sFlow, IPFIX from your existing infrastructure

Discovery:
- Agentless - no agents installed on servers
- Credentials optional - they enhance the map but aren't required for core functionality
- API integration with hypervisors and cloud providers

Deployment takes under an hour. Results appear live immediately."

**CTO follow-up:** "What about performance impact?"
**Answer:** "Sensors use high CPU by design due to small vCPU allocation - this is normal and expected. Promiscuous mode traffic forwarding, not active scanning. Zero impact on production workloads. We can discuss sizing for your environment specifically."

---

## CLOSING (5 minutes)
### Goal: Tie it all together with clear next steps

**Return to Dashboard**

**Say:**
"Let me bring this full circle.

In the last hour, you've seen how Faddom:
- Eliminates blind spots across your entire hybrid infrastructure
- Reduces operational risk through dependency awareness  
- Accelerates migrations with complete visibility
- Detects threats early through anomaly detection
- Speeds up incident response with root cause analysis
- Optimizes performance and cost continuously
- Unifies tribal knowledge across teams

All of this from a single platform that deploys in under an hour, runs agentless, and keeps all data in your environment.

The question isn't whether you need visibility. You already know you do.

The question is: how long can you afford to operate blind?"

**Pause.**

**Then:**
"What questions do you have?"

---

## HANDLING THE Q&A SESSION

**General principles:**
1. **Listen completely** - Don't interrupt, don't start formulating your answer while they're talking
2. **Pause before answering** - 2 seconds of silence shows you're thinking, not scrambling
3. **Answer the question asked** - Not the question you wish they asked
4. **Check if you answered** - "Does that address your question?"
5. **Return to outcomes** - Every technical answer should end with "which means [business value]"

**When you don't know:**
"That's a great question. I don't have the exact answer on hand, but I can get that to you by [specific time]. Let me note that down."

**When they push back:**
"I understand your concern. Let me show you how we've addressed that..." [Then demonstrate, don't defend]

**When they go technical and you need to redirect:**
"Absolutely - and I want to make sure I give you the complete technical answer. Can I take that offline with your team after this demo so we don't lose time on the business outcomes? I'll send over detailed documentation today."

---

## POST-DEMO ACTIONS

**Within 2 hours:**
- Email thank you with summary
- Include any promised documentation
- Answer any questions you noted
- Propose specific next steps

**Within 24 hours:**
- Follow up with Bar on how it went
- Document what went well and what didn't
- Note any unexpected questions for future prep

---

## EMERGENCY RECOVERY PHRASES

**If the demo breaks:**
"No problem - let me show you this alternative view while that loads..."

**If you blank on what to say:**
"Let me show you something interesting here..." [Click anything and use it as a bridge]

**If they're losing interest:**
"Let me show you the most important thing..." [Jump to Impact Set or Migration]

**If you're running long:**
"I want to respect your time - what's the one area you'd like me to dive deeper into?"

**If you start overexplaining:**
Stop. Mid-sentence if necessary.
"Actually, here's the key point: [one sentence]"
Then show, don't tell.

---

## THE 7 DROP THE MIC MOMENTS

1. **Search → Instant live topology** - "This replaces tribal knowledge on day one"

2. **Change tracking** - "When an engineer goes on vacation for a week, they come back and see exactly what changed"

3. **Impact Set** - "Two clicks to know what breaks. No more scream tests."

4. **Root cause investigation** - "Click a timestamp, see exactly what changed at that moment"

5. **Subnet dependencies** - "Last week we found test-to-production communication in seconds"

6. **Migration dependencies** - "One server left behind is enough to break the business"

7. **The final value statement** - "The question is: how long can you afford to operate blind?"

---

## REMEMBER

You're not here to show them every feature.
You're here to show them how their world changes with Faddom.

Features are what the product has.
Benefits are what the customer gets.
Outcomes are what the business achieves.

Always land on outcomes.

Good luck tomorrow. You've got this.
