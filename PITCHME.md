# Keyless.ID Current state

---

## components
1. Blockchain contracts for channels;
2. Backend orchestrator for route and matching users requests;
3. Signer for sign users requests(auth, open/close orders);
4. Frontend for human UI

![](assets/img/presentation.png)

---?color=linear-gradient(180deg, white 75%, black 25%)
@title[Customize Slide Layout]

@snap[west span-50]
## history
@snapend

@snap[east span-50]
![](assets/img/presentation.png)
@snapend

@snap[south span-100 text-white]

@snapend

---?color=linear-gradient(90deg, #E27924 65%, white 35%)
@title[Add A Little Imagination]

@snap[north-west h4-white]

@snapend

@snap[west span-55]
@ul[spaced text-white]
- 1st version. Task: concept verification. July 2018.

Channels - EOS and ETH.
Backend - simple monolite node.js 
Frontend - very simple, just for presentation.
Signer - integrated in frontend.
- 2nd version. Task: identify bottlenecks. November 2018
Channels - EOS, ETH, NEO, QTUM.
Backend - micro-service arch, still node.js implementation
Frontend - usual trading interface, but single user mode only.
Signer - chrome extension based.
- 3rd version. Task: building production architecture. August 2019
Channels - BTC(LN), LTC, OMNI, EOS, ETH, NEO, QTUM 
Backend - advanced latency reduce and throughput maximize architecture, rust and golang implementation. Rust for security and latency focused API layer. Golang for order engine and latency agnostic api components.
Frontend - PWA based trading interface, multi-user mode, keyless.id auth.
Signer - security and UX focused pwa solution. webpayments api for simple UI, MPC for security; separation of the solution into an independent project.
Orchestrator - manage and update production implementation; 

- 4th version. Task: Increasing productivity, improving security, reducing the cost of ownership. Q4 2019 - Q1 2020
Channels - replication for forks.
Backend - All api must Rust implementation, on state-less function with zero-copy serialisation/deserialisation; Sequencer as separate component; Matching engine move to OS kernel ring, for maximize throughput with software implementation

@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---?image=assets/img/presenter.jpg

@snap[north span-100 h2-white]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend
