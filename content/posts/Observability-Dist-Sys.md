---
title: "From Observability to Significance in Distributed Systems"
date: 2023-10-22T14:41:47+03:00
draft: false
categories:
- observability
- distributed systems
tags:
- observability
- distributed systems
keywords:
- observability
- distributed systems
autoThumbnailImage: true
thumbnailImagePosition: left
thumbnailImage: //d1u9biwaxjngwg.cloudfront.net/welcome-to-tranquilpeak/city-750.jpg
#coverImage: //d1u9biwaxjngwg.cloudfront.net/welcome-to-tranquilpeak/city.jpg
metaAlignment: center
---
Mark Burgess, a well-known theoretical physist and creator of the configuration management tool CFEngine, formulated the idea of "Promise Theory" as a model to understand and describe the behavior of distributed systems.

 "Promise Theory" offers a way to reason about system configurations and the autonomy of system components. It's a generalization of how individual system components can operate independently and yet still cooperate to achieve a larger system goal. He went ahead and wrote a book about it which is freely available in his website: https://markburgess.org/promises.html along with several other treatises on systems and system administration.
## Observability
In 2019 Burgess published a paper on Observability  https://markburgess.org/cognitive2.pdf to delve deeper into understanding the essence of distributed systems beyond just configuration management.

**Distributed Systems are Complex** and this complexity introduces challenges in understanding, managing, and drawing insights from these systems. How do we move from simply observing these systems (observability) to deeply understanding their behaviors (significance)?

This is a distinction that needs to be made between observability and significance: **Observability** is the ability to monitor and watch system components. Tools like logs, metrics, and traces allow us to see system behavior in real-time or retrospectively. **Significance** goes beyond just observing. It’s about comprehending the "why" behind certain behaviors, their importance, and their implications for system health and performance.

Distributed systems are independent processes and they lack a global state but they don’t function in isolation. To understand significance, one must factor in the broader context in which a system operates.
There is the  **internal context** of a distributed system: configuration, health of individual nodes, communication between nodes, etc.
Then there is the **external context** of a distributed system: User demand, network latency, third-party services, etc.

Promise theory provides a foundational understanding of distributed systems. It introduces the entities of **agents** and **promises** . An agent is each component of the distributed system that makes 'promises' about its behavior. A promise is an assertion made by an agent about its behavior, without any compulsion to act in a particular way.Understanding how agents keep or break promises gives insights into the significance of observed behaviors.

Observability requires tracing causality, not just metrics.
Moving from Observability to Significance is akin to moving from recognizing **signs** (observable behaviors, metrics, or logs) to deciphering their **meaning** (the interpretation of signs, based on system knowledge and context).
Significance is not straightforward. Distributed systems are non-static, adapting and changing based on load, failures, and other factors. One component’s behavior can impact others. A problem in one node can cascade and affect the entire system. At the same time, the amounts of log data and metrics are huge and make it difficult to spot anomalies. Instrumentation should focus on significant events and semantics rather than exhaustive logs.

That's why advanced tools and methodologies that can help derive significance are needed: machine learning algorithms that can detect anomalies, predict failures, and recognize patterns, and holistic monitoring AI Tools that not only show data but also provide contextual insights, correlating different metrics and logs.

Hopefully the latest revolution and prolifaration of generative AI will help in that direction. As previously mentioned, distributed information systems are complex and any insiught provided by an AI assistant (that doesn't hallucinate much) is more than welcome!

P.S.: Still reading the paper...

<!-- derive significance
Here is a concise summary of the key points:

The passage discusses challenges in modeling and observing IT systems for effective monitoring and
debugging. It argues current approaches overly focus on brute force data collection without
considering relevance, accuracy, and semantics. It proposes connecting observability to achieving
consensus in distributed systems. It advocates applying Promise Theory and Semantic Spacetime to
analyze systems across multiple scales. A key challenge is real-time monitoring relies on small,
statistically inadequate samples whose significance is hard to assess. The passage aims to address
the neglect of detailed models for process monitoring in IT systems.




That is why I used LangChain and Anthropic's Claude-2 model from AWS Bedrock to get a few insights from Burgess's paper:
Here is a concise summary of the key points made in the passage:

- Monitoring distributed systems is challenging due to independent processes and lack of global
state.

- Promise theory models systems as agents making promises.

- Observability requires tracing causality, not just metrics.

- Instrumentation should focus on significant events and semantics rather than exhaustive logs.

- Reasoning involves searching relationships and promises, not just logic.

- Decouple systems by separating timescales and namespaces to reveal invariants. -->