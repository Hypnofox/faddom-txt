# FADDOM TRICKY QUESTIONS PLAYBOOK
## Anticipated C-Level Questions with Crisp Answers

---

## CATEGORY 1: TECHNICAL CREDIBILITY QUESTIONS (Usually from CTO)

### Q: "How does this actually collect the data without agents?"

**Crisp Answer:**
"Three collection methods depending on your infrastructure:

For VMware: Lightweight sensors in promiscuous mode on each ESXi host - they forward traffic, they don't scan or poll.

For Hyper-V and KVM: HostSFlow running on the hypervisor host OS.

For cloud: Native flow logs from AWS VPC Flow Logs, Azure NSG Flow Logs, GCP VPC Flow Logs.

For network: NetFlow, sFlow, or IPFIX from your existing network infrastructure.

All traffic stays in your environment - nothing leaves. Want me to show you the architecture diagram?"

**Why this works:** Specific, technical, but doesn't spiral into implementation details unless asked.

---

### Q: "What's the performance impact on our production environment?"

**Crisp Answer:**
"Zero impact on production workloads. Here's why:

The sensors forward traffic passively - no active scanning, no probes, no polling. They're designed to use high CPU relative to their small vCPU allocation, which is normal and expected behavior.

For credentials-based discovery on Windows or Linux, we use standard protocols - WMI for Windows, SSH for Linux - same as your existing management tools.

The Faddom appliance itself is sized based on your environment - typically 8-16 vCPU and 32-64GB RAM for most deployments. I can provide detailed sizing recommendations for your specific scale."

**Why this works:** Addresses the concern directly, provides specifics, offers to go deeper.

---

### Q: "How do you handle Kubernetes and containerized environments?"

**Crisp Answer:**
"Kubernetes pods are ephemeral - mapping them is useless. What matters to the business is service-to-service communication, not which pod is running at any given second.

Faddom maps stable service dependencies in Kubernetes the same way we map the rest of your environment - through actual traffic patterns. You see how your microservices actually communicate, not just how they're supposed to communicate.

This removes the chaos and exposes the logic. Want me to show you a K8s environment example?"

**Why this works:** Reframes the question from "do you support Kubernetes" to "here's why our approach is better."

---

### Q: "What about security? You're collecting all our traffic."

**Crisp Answer:**
"Everything stays in your environment. Faddom is a virtual appliance that runs on-premises - your data never leaves your network.

We're aligned with ISO 27001 and approved for sensitive environments. Many customers run Faddom in air-gapped networks with zero internet connectivity.

The AI modules - Compass and Lighthouse - require internet, but all processing happens in Faddom cloud and only anonymized, encrypted metadata is sent. You control which AI features are enabled.

For full air-gap deployments, you get complete visibility without any AI features. Want to see the detailed security architecture?"

**Why this works:** Addresses privacy and compliance immediately, shows flexibility.

---

### Q: "How accurate is this? How do we know we can trust it?"

**Crisp Answer:**
"Traffic doesn't lie. We're reading actual network flows - the same data your firewalls and routers are generating right now.

This isn't based on agents that might be out of date or documentation that might be wrong. It's what's actually happening in your environment at this moment.

For dependencies, we show direction - who initiated the connection. That's how we know A depends on B, not the other way around.

Accuracy improves over time as we observe more traffic patterns. Most environments see 95%+ visibility within 48 hours of deployment."

**Why this works:** Appeals to evidence-based thinking, quantifies the claim.

---

## CATEGORY 2: BUSINESS VALUE QUESTIONS (Usually from CPO/CRO)

### Q: "What's the ROI? How do we justify this investment?"

**Crisp Answer:**
"Faddom pays for itself in three ways:

First: **Prevented incidents.** One avoided outage from a bad change typically saves more than the annual subscription. A customer prevented a compliance violation worth $2M by catching test-to-production communication before an audit.

Second: **Faster migrations.** Customers report 30-40% reduction in migration time because they're not discovering dependencies during the move. For a $500K migration project, that's $150-200K in labor savings alone.

Third: **Optimized spending.** The rightsizing recommendations typically identify 15-20% of infrastructure that can be downsized or retired. On a $1M annual cloud spend, that's $150-200K per year.

Most customers see positive ROI within the first migration or major infrastructure project."

**Why this works:** Concrete numbers, real customer examples, multiple value paths.

---

### Q: "Why not just use [competitor tool] we already have?"

**Crisp Answer:**
"Great question. Most tools fall into one of three categories:

APM tools like Dynatrace or AppDynamics require agents and focus on application performance, not infrastructure dependencies.

CMDB tools rely on manual updates or agents and are typically 60-70% accurate at best.

Cloud-native tools like AWS Systems Manager only see one cloud provider - they don't give you the hybrid view.

Faddom is purpose-built for one thing: accurate, real-time dependency mapping across your entire hybrid environment - on-prem, multi-cloud, containers, everything.

Agentless, fast deployment, always current. That's why customers who already have those other tools still need Faddom."

**Why this works:** Respects their existing investments, shows how Faddom complements rather than replaces.

---

### Q: "This seems complicated. How long before we see value?"

**Crisp Answer:**
"Deployment takes under an hour. Results appear immediately.

First day: You can search for any server and see its dependencies.
First week: You have complete application maps and baseline traffic patterns.
First month: You're using it for change planning, migration waves, and security analysis.

The platform is designed to be self-teaching with built-in guidance. Most customers have their teams fully operational within two weeks.

Compare that to agent-based solutions that take 6-12 months to deploy and CMDB projects that never finish."

**Why this works:** Quantifies time-to-value, contrasts with painful alternatives.

---

### Q: "What if we start small and expand later? Can we do that?"

**Crisp Answer:**
"Absolutely. Many customers start with:
- A specific data center they're migrating
- A critical application set
- A single cloud environment
- A compliance zone

Licensing is based on the number of servers monitored. You control the scope through subnet discovery settings.

Start with 500 servers, prove the value, expand to 5,000. The platform scales seamlessly.

Want me to show you how scope control works?"

**Why this works:** Reduces perceived risk, shows flexibility, offers proof-of-concept path.

---

## CATEGORY 3: COMPARISON AND COMPETITIVE QUESTIONS

### Q: "How is this different from ServiceNow's CMDB?"

**Crisp Answer:**
"ServiceNow CMDB is great for tracking IT assets and their relationships - if you keep it updated.

The challenge? Manual updates or agent-based discovery means it's always out of date. Most ServiceNow CMDBs are 60-70% accurate.

Faddom automatically discovers real-time dependencies from actual traffic. No manual updates, always current.

Many customers use both: Faddom feeds accurate dependency data into ServiceNow via REST API, and ServiceNow remains the system of record for IT assets.

Best of both worlds."

**Why this works:** Doesn't bash the competitor, shows integration value.

---

### Q: "We're looking at [Agent-based APM tool]. Why not just use that?"

**Crisp Answer:**
"APM tools are excellent for application performance monitoring - response times, error rates, transaction tracing.

But they have three limitations for dependency mapping:

First: Agents. Every server needs one. Deployment takes months. Legacy systems often can't support them.

Second: Application-focused. They don't see infrastructure dependencies - DNS servers, load balancers, firewalls, network traffic.

Third: Cost. Licensing is typically per-agent per-month. For 5,000 servers, you're looking at significant ongoing costs.

Faddom gives you infrastructure-wide visibility in under an hour with zero agents.

Customers often use both: APM for application performance, Faddom for infrastructure dependencies."

**Why this works:** Respects the APM tool's strengths, shows Faddom's different use case.

---

### Q: "Can't our firewall or network team just export flow logs and analyze them?"

**Crisp Answer:**
"Absolutely - and that's exactly what Faddom does, we just do it continuously and automatically.

The challenge with manual analysis:
- It's a full-time job to keep current
- It requires deep networking expertise
- It doesn't scale across hybrid environments
- It doesn't correlate with business context

Faddom takes those flow logs and transforms them into business understanding - application maps, dependency chains, impact analysis, migration waves, security posture.

We turn raw network data into actionable intelligence."

**Why this works:** Validates their capability, shows the value-add.

---

## CATEGORY 4: RISK AND OBJECTION QUESTIONS

### Q: "What happens if Faddom goes down? Do we lose visibility?"

**Crisp Answer:**
"If the Faddom appliance goes offline, you lose the real-time visualization and analysis capability, but:

First: Your infrastructure keeps running normally - Faddom is observational only, never in the data path.

Second: Most customers export critical maps weekly or monthly for documentation purposes.

Third: We recommend HA deployment for production - two Faddom instances in active-passive configuration.

Fourth: The appliance itself is a VM - standard backup, snapshot, and DR procedures apply.

Deployment time from backup is under an hour. Want me to walk through the HA architecture?"

**Why this works:** Addresses the risk, shows mitigation options, maintains confidence.

---

### Q: "This sounds expensive. What's the pricing model?"

**Crisp Answer:**
"Pricing is based solely on the number of servers, VMs, or instances monitored. Endpoints, users, containers don't count - only the infrastructure systems.

For a typical 2,000-server environment, annual subscription is in the range of $80-100K.

For 8,000 servers, approximately $280-300K annually.

Multi-year agreements are available with discounts.

Compare that to:
- Agent-based APM at $100-200 per server per year = $160-400K for 2,000 servers
- CMDB projects that take 18 months and $500K in consulting
- Migration disasters that cost millions in delays and rework

Most customers see positive ROI within the first major project."

**Why this works:** Transparent on pricing, contextualizes the cost.

---

### Q: "What if our network team doesn't want to enable NetFlow or give you access?"

**Crisp Answer:**
"Two approaches:

First: We only need read access to flow data that's already being generated. Most networks already have NetFlow enabled for security or capacity planning. We're just another consumer of that data.

Second: For networks where flow isn't enabled, we can deploy proxy collectors that sit on network segments and generate flows locally.

The key conversation is usually: 'Do you want visibility into dependencies and changes, or do you want to keep operating blind?'

Once network teams see the value - especially for firewall rule validation and segmentation planning - they typically become our biggest champions.

Happy to join a conversation with your network team to address their specific concerns."

**Why this works:** Acknowledges the political challenge, offers partnership.

---

## CATEGORY 5: IMPLEMENTATION AND CHANGE QUESTIONS

### Q: "Our team is already overwhelmed. Who's going to manage this?"

**Crisp Answer:**
"Faddom is designed to be low-touch after initial deployment:

Day 1: One engineer deploys the appliance - under an hour.
Week 1: Configure discovery scopes and integrations - 2-4 hours.
Ongoing: Platform updates itself, maps update automatically, minimal maintenance.

Most customers assign ownership to either:
- Network operations (for infrastructure visibility)
- Application teams (for dependency mapping)
- Migration teams (for project planning)

The platform becomes a shared resource that reduces workload - fewer incidents, faster troubleshooting, cleaner migrations.

Your team gets time back, not more work."

**Why this works:** Reframes from "one more tool to manage" to "time saver."

---

### Q: "What's the learning curve? How long to train our team?"

**Crisp Answer:**
"The platform is designed to be intuitive with built-in guidance:

Day 1: Basic search and mapping - 30 minutes
Week 1: Application mapping and change tracking - 2 hours  
Week 2: Advanced features like migration planning - 4 hours

We provide:
- Online documentation
- Video tutorials  
- Live training sessions
- In-app Captain AI support

Most teams are fully operational within two weeks. The search functionality is so intuitive that people often skip the training and just start using it."

**Why this works:** Quantifies the learning curve, shows support options.

---

## CATEGORY 6: STRATEGIC AND FUTURE-LOOKING QUESTIONS

### Q: "What's your product roadmap? Where is this going?"

**Crisp Answer:**
"Three major directions:

First: **Deeper AI integration.** Lighthouse AI for anomaly detection is currently in alpha. Compass AI for natural language queries is in production. We're expanding both.

Second: **Broader integrations.** Every quarter we add support for new platforms - recently added enhanced Kubernetes support, expanded cloud provider coverage.

Third: **Automation capabilities.** API-first architecture means customers are building automated workflows - change tickets with auto-generated impact analysis, migration wave automation, security policy enforcement.

The core platform continues to get faster, more accurate, and easier to use. Want to see the public roadmap?"

**Why this works:** Shows investment and direction without overpromising.

---

### Q: "How do you stay current with our changing environment?"

**Crisp Answer:**
"Faddom is always current because it's reading live traffic right now.

When you add a new server, it appears in Faddom the moment it starts communicating.
When you decommission a server, it shows as inactive immediately.
When you change a firewall rule, the traffic change is visible in real-time.

Unlike CMDBs that require manual updates or agents that need deployment, Faddom automatically discovers and maps based on actual behavior.

You never have to 'update' Faddom. It updates itself by observing your environment."

**Why this works:** Contrasts with tools that require active maintenance.

---

## CATEGORY 7: TRUST AND VENDOR QUESTIONS

### Q: "We've never heard of Faddom. Are you going to be around in 5 years?"

**Crisp Answer:**
"Faddom was founded in 2016 and is recognized by Gartner as a leader in agentless dependency mapping as of 2025.

Customer base includes Fortune 500 enterprises, government agencies, healthcare systems, and financial services firms - organizations that do extensive vendor due diligence.

The platform runs on-premises - you own the appliance, you control the data. Even if Faddom disappeared tomorrow, your deployment keeps running.

Support is based in [location], with engineering teams in [location]. We're not going anywhere, but the architecture ensures you're never locked in.

Happy to provide customer references in your industry."

**Why this works:** Provides credibility signals, addresses lock-in concern.

---

### Q: "Can we talk to other customers who are using this?"

**Crisp Answer:**
"Absolutely. We have customer references across multiple industries:

- Healthcare: Large hospital systems using Faddom for HIPAA compliance and migration planning
- Financial services: Banks using it for zero-trust segmentation and DR planning  
- Manufacturing: Using it for OT/IT convergence and modernization
- Government: Air-gapped deployments for sensitive environments

I can connect you with customers in similar situations - what industry or use case is most relevant for you?"

**Why this works:** Shows willingness, offers targeted references.

---

## EMERGENCY PHRASES WHEN YOU DON'T KNOW THE ANSWER

### Option 1: "I don't have the exact details on that"
"That's a great question. I don't have the exact details on that in front of me, but I can get you a detailed answer by [specific time]. Let me note that down so I don't forget."

### Option 2: "Let me connect you with engineering"
"That's getting into deep technical territory that our engineering team would give you a better answer on. Can I set up a follow-up technical deep dive with them?"

### Option 3: "Let me show you something related"
"I want to make sure I give you the complete answer on that. Let me show you how this works in practice, and then I'll follow up with the technical documentation afterward."

### Option 4: "That's a good edge case"
"Interesting question - that's a specific edge case I haven't seen come up before. The standard approach would be [general answer], but let me verify the exact implementation with engineering and get back to you."

---

## HANDLING HOSTILE OR SKEPTICAL QUESTIONS

### Principle: Never get defensive, always get curious

**Hostile:** "This looks like just another monitoring tool we don't need."

**Response:**
"I understand the skepticism - you probably have 5-10 monitoring tools already. Can I ask what specific visibility gaps you're experiencing right now? [Listen] Here's how Faddom addresses that differently..."

---

**Skeptical:** "I don't believe this can be accurate without agents."

**Response:**
"That's a reasonable concern - agents have been the standard for decades. Let me show you how we achieve accuracy through traffic analysis... [Demo] ...and then you can tell me if this looks accurate for your environment."

---

**Dismissive:** "We've tried tools like this before and they didn't work."

**Response:**
"I'd love to learn from that experience - what specifically didn't work about those tools? [Listen] Let me show you how Faddom addresses those exact issues..."

---

## THE MOST IMPORTANT RULE

**When you're not sure how to answer:**

1. **Pause** - 2-3 seconds of silence shows you're thinking
2. **Clarify if needed** - "Just to make sure I understand your question..."
3. **Answer what you know** - Be honest about what you don't know
4. **Commit to follow-up** - Give a specific time
5. **Return to the demo** - "In the meantime, let me show you..."

**Never:**
- Make up an answer
- Overpromise capabilities  
- Bash competitors
- Get defensive
- Spiral into technical details to avoid saying "I don't know"

---

You've got this. These questions are opportunities to build credibility, not threats.
