# L2. Current state

---

## Components
* Blockchain contracts for channels;
* Backend for route and matching users requests;
* Signer for sign users requests(auth, open/close orders);
* Frontend for human UI


---?color=linear-gradient(180deg, white 75%, black 25%)
@title[Customize Slide Layout]

@snap[west span-50]
## Version
@snapend

@snap[south span-100 text-white]
 Alpha > Beta > Charlie > Delta
@snapend

---

@size[1.5em](Alpha) 
#### Task: concept verification. 
#### July 2018.
- Channels: EOS and ETH.
- Backend - simple monolite arch. 
- Frontend - very simple, just for presentation.
- Signer - integrated in frontend.
--- 

@size[1.5em](Beta)
#### Task: identify bottlenecks. 
#### November 2018
- Channels: EOS, ETH, NEO, QTUM.
- Backend - micro-service arch, node.js implementation.
- Frontend - usual trading interface, but single user mode only.
- Signer - chrome extension based.
--- 
@size[1.5em](Charlie)
#### Task: production ready architecture. 
ETA: August 2019
- Channels: BTC(LN), LTC, OMNI, EOS, ETH, NEO, QTUM. 
- Backend - latency reduce and throughput maximize architecture.
- Frontend - clients oriented solution, paswordless auth.
- Signer - security and UX focused solution. 
- Orchestrator - manage and update production implementation; 
--- 
@size[1.5em](Charlie)
#### Channels
- All chain possible to support(1st and 2nd gen).
- Lightning network, seamless integration.
---
@size[1.5em](Charlie. Details)
#### Backend
- 3 types of API's
Rust for security and latency focused API layer. 
- Golang for order engine and latency agnostic api components.


---

@size[1.5em](Charlie. Details)
#### Frontend
- PWA based trading interface, multi-user mode, keyless.id auth.

---

@size[1.5em](Charlie. Details)
#### Signer
- Security and UX focused pwa solution. webpayments api for simple UI, MPC for security. 
- Separation of the solution into an independent project.

---

@size[1.5em](Delta)
#### Task: Increasing productivity, improving security, reducing the cost of ownership.
#### ETA: Q4 2019 - Q1 2020
* Channels - replication for forks.
* Backend - All api must Rust implementation, on state-less function with zero-copy serialisation/deserialisation.
* Sequencer as separate component. 
* Matching engine move to OS kernel ring, for maximize throughput with software implementation.


@ulend
@snapend

@snap[east span-45]
@snapend

---



## Current status

--- 
@size[1.5em](Channels) 
* Done: we implement BTC(LN) contracts, tested they works with ETH contracts from v2.
* In work: OMNI and LTC versions, integrate and test all contracts as union solution.

---
@size[1.5em](Backend)

* Done: Nasdaq itch 5.0 protocol modification and implement for latency sensitive trade api. 
* Latency agnostic api components re-implement in golang. 
* Matching engine implement and tested: 1.5 mps. MQ1: IPC and UDP based special designed MQ for API↔Matching engine.
* In work: Implement new, MPC based sign algo, for enhance security TX Auth service. Check HSM possibilities use.

---

@size[1.5em](Frontend)

* Done: Auth and trade integration with new signer. 
* In work: Client design implementing. 
* Transition to multithreaded architecture(via service workers also can know as “progressive web app’s design concept”).

---

@size[1.5em](Signer)

* Done: First “durty”  webpayments API version with eth and btc(ln) tx signer. 
* Web auth mode implement and test. 
* Device agnostic face auth.
* In work: MPC implement, History TX storage, Nice look design and enhance UX. 

 ---
 
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)

---
## @size[1.0em](Future vector of development) 

---

@size[1.5em](Tech key-points:)  

* Maximize bandwidth and minimize latency all backend components; formal verification for all components.
* Move for serverless functions architecture for non-FPGA components.
* Move to FPGA implementation for matching orders; serilize/deserilize; sign/prove tx.

---

@size[1.5em](Non tech key-points:)

* Derivative version of L2, Identify the optimal licensing policy. 
* Going beyond crypto-markets: EDS, user authorization market, managing secrets and configurations of world-services in the cloud infrastructure. 
* Development of patent policy of the company.

@snapend
