# IRTF 125 IDRNG sidemeeting minutes

## Introduction

- Title: Next-Generation Inter-Domain Routing Architecture and Protocols (IDRNG)
- Date/Time: Wednesday, March 18, 2026, 10:00-12:00 ( Asia/Shanghai )
- Venue: Jiangsu
- Organizer: idrng · idrng.thu@gmail.com
- Areas: IRTF
- Attendees: It has almost 50 in-person attendees and 40 (peak at 43) remote participants via WebEx.

## Abstract

The IDRNG side meeting provides an open forum for researchers, operators, and protocol designers to discuss the evolution of inter-domain routing architectures and protocols in the AI era. It serves as a platform for exchanging ideas on architectural design, protocol development, security, manageability, and operational considerations for next-generation routing. Key topics include AI-driven routing control and optimization, routing security and assurance mechanisms, and emerging requirements driven by AI workloads, including compute–network co-scheduling, latency-sensitive traffic, and energy-aware constraints. The meeting also explores multi-agent and agentic routing models across administrative domains, supports shared methodologies and experimental evaluation, and fosters collaboration on research outputs and IRTF/IETF documents. The side meeting is open to all participants and follows IETF/IRTF principles of open participation, technical merit, and consensus-based discussion.

## Agenda
- 10:00-10:05 Host (5 mins)
    - History of IDR/BGP
    - Limitations of IDR/BGP
    - Agentic IDR
- Global ROV Audit and Triangulation Tool (Terry Sweetser - APNIC - 20 mins)
    - Canceled for some reason.
- 10:05-10:15 The MANRS Development Process. (Di Ma - MANRS Steering Committee Member - 20 mins)
    - MANRS Development Process
    - MANRS is maturing
- 10:15-10:35 When RPKI Meets Reality: Understanding the causes and risks of RPKI-Invalid (Weitong Li - Virginia Tech - 20 mins)
    - Current RPKI status
    - Q1: Why RPKI-invalid happens
    - Q2: What’s the impact of RPKI-invalid
    - Q3: Can this be explored by an adversary
- 10:35-10:40 Reducing Time to BGP Changes (Susan Hares)
    - Challenges to get new BGP ideas
    - How can we shrink the time to change
    - Work Planned –Experiment with BGP and LMM
- 10:40-11:10 The Routing Deadlock: Challenges We Can No Longer Ignore. (Cuicui Wang - China Unicom - 20 mins)
    - Evolution of BGP for 35+ years
    - Triple challenges: security & management & scalability
    - Root cause: the initial design(1989) vs today’s internet requirements(20xx)
- 11:10-11:35 QA and Discussions (30 mins)
- 11:55-12:00 Next Steps (5 mins)
    
## Discussions

- Zhuotao Liu: Several questions/comments. First, think about how to use the large language model to reduce the time of BGP chains.
- Joseph: LLMs can be quite good at comprehending the logical relations. LLM requires structuring these rules in a certain way so that LLMs don't get confused. The answer is yes, but it requires that intermediate step.
- Dirk: Talk about the kind of known BGP security problems. What are promising topics that are rooted in good research that address really relevant problems and that also have a chance to lead to continuous research?
- Dirk: If this were to become a continuous activity, would this be more like a BGP forum, or would there be more substantial, maybe more future-looking research?
- Tony: For those who think that BGP has security problems, I encourage you to take a look at BGPsec. Cost lots of time on BGPsec. If you want to talk about a routing deadlock, you're going to ask the question why haven't we deployed it?
- Tony: And before you go off thinking about a brand new architecture for doing your domain routing, think about also how you are going to get your brand new architecture deployed? Because that's where we're really stuck.
- Qi Li: to Joseph: SCION team may join next meeting.
- Nicola: SCION has a similar motivation to this. SCION re-designs everything, and then over time, as it got some commercial adoption, it got transferred into more limited domains, so in some kind of federated networks, more for specialized ecosystems.
- Nicola: The question of deployment, especially when you're targeting the global Internet space, is really important. Our interest is more in how we may bring this work in the medium term to do some IETF work, some more standardization, and interoperability. How to bring this forward more on the industrial level, rather than pure research. This is a very complex thing.
- Tony: The routing security parts seem almost isomorphic to the BGP set except for having a distributed trust model. The other part of SCION that seems problematic is the link-layer link-level forwarding verification. That seemed very difficult to make work in practical applications because of traffic engineering.
- Nicola: But if I were to do some standards work on SCION, I would definitely look at the data plate first and see how this can be evolved.
- Sue: Echoes agreements with Tony.
- Zhuotao Liu: One of the major goals of this group is basically discussing how we can embrace AI into this next-generation routing.
- Dirk: Think about a more coherent research agenda. This probably needs more thought and more discussion. I don't think that's already enough to warrant a continuous activity.
- Michael: The problem is not only with the BGP protocol, but also with the hardware that is still used by some old providers.
- Michael: The second is about the RPKI invalid. Many Trust Anchors from several NICs indicate that there may be some data inconsistency. We should share the information, maybe give some alert on it.
- Nicola: More meetings about AI. There might be opportunities when it comes to the needs of performance resilience, and work on this. But wondering if there's any idea what the best value is within IRTF or EITF to the requirements from this industry, because right now this doesn't really seem clear in terms of “do we need to do something that's arousing there, or is it more different things like identities near DNS?”
- Sue: Trying to work on the problem in a different way. It need for really good minds that we've created an immense system. I'd like a flag day, but can't stop the Internet. We have challenge of trying to change the engine while the car that is the Internet is running. Looking at one small problem in one small area.
- Dirk: I think what this group should do is collect these problems and ideas, and reach out to people.
- Joseph: Our purpose is not really to use LLMs for their own sake. We’ve been using them as linguistic tools, not as thinking tools. Structuring the information from RFCs into a particular kind of form. Input conditions, the output assertions as simple declarative statements, and all the logic relations in a separate array. using that structure to both deliver information to developers and to routers.
