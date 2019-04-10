# Mountkirk Games Case Study
> https://cloud.google.com/certification/guides/cloud-architect/casestudy-mountkirkgames-rev2
## Company Overview
Mountkirk Games makes online, session-based, multiplayer games for mobile platforms. They build all of their games using some server-side integration. Historically, they have used cloud providers to lease physical servers.

Due to the unexpected popularity of some of their games, they have had problems scaling their global audience, application servers, MySQL databases, and analytics tools.

Their current model is to write game statistics to files and send them through an ETL tool that loads them into a centralized MySQL database for reporting.

## Solution Concept
Mountkirk Games is building a new game, which they expect to be very popular. They plan to deploy the game’s backend on Google Compute Engine so they can capture streaming metrics, run intensive analytics, and take advantage of its autoscaling server environment and integrate with a managed NoSQL database.

## Business Requirements

- Increase to a global footprint
- Improve uptime - downtime is loss of players
- Increase efficiency of the cloud resources we use
- Reduce latency to all customers

## Technical Requirements
### Requirements for Game Backend Platform

- Dynamically scale up or down based on game activity.
- Connect to a transactional database service to manage user profiles and game state.
- Store game activity in a timeseries database service for future analysis.
- As the system scales, ensure that data is not lost due to processing backlogs.
- Run hardened Linux distro.

### Requirements for Game Analytics Platform

- Dynamically scale up or down based on game activity.
- Process incoming data on the fly directly from the game servers.
- Process data that arrives late because of slow mobile networks.
- Allow queries to access at least 10 TB of historical data.
- Process files that are regularly uploaded by users’ mobile devices.

## Executive Statement
Our last successful game did not scale well with our previous cloud provider, resulting in lower user adoption and affecting the game’s reputation. Our investors want more key performance indicators (KPIs) to evaluate the speed and stability of the game, as well as other metrics that provide deeper insight into usage patterns so we can adapt the game to target users. Additionally, our current technology stack cannot provide the scale we need, so we want to replace MySQL and move to an environment that provides autoscaling, low latency load balancing, and frees us up from managing physical servers.

---

# Guides
> https://cloud.google.com/solutions/mobile/mobile-gaming-analysis-telemetry
#### Figure 1: Game telemetry reference architecture
![Figure 1: Game telemetry reference architecture](https://cloud.google.com/solutions/mobile/images/telemetry-01-reference-architecture.png)
#### Figure 2: Real-time processing of events from game clients and game servers
![Figure 2: Real-time processing of events from game clients and game servers](https://cloud.google.com/solutions/mobile/images/telemetry-02-real-time-event-processing.png)

---

# Exams
## Question 1
#### For this question, refer to the Mountkirk Games case study.
Mountkirk Games wants to set up a continuous delivery pipeline. Their architecture includes many small services that they want to be able to update and roll back quickly. Mountkirk Games has the following requirements:
- Services are deployed redundantly across multiple regions in the US and Europe.
- Only frontend services are exposed on the public internet.
- They can provide a single frontend IP for their fleet of services.
- Deployment artifacts are immutable. Which set of products should they use?  
> 
- [ ] A. Google Cloud Storage, Google Cloud Dataflow, Google Compute Engine
- [ ] B. Google Cloud Storage, Google App Engine, Google Network Load Balancer
- [ ] C. Google Container Registry, Google Container Engine, Google HTTP(s) Load Balancer
- [ ] D. Google Cloud Functions, Google Cloud Pub/Sub, Google Cloud Deployment Manager

<details><summary>ANSWER</summary>
- [x] C. Google Container Registry, Google Container Engine, Google HTTP(s) Load Balancer
</details>

---
## Question 2
#### For this question, refer to the Mountkirk Games case study. 
Mountkirk Games wants to set up a real-time analytics platform for their new game. The new platform must meet their technical requirements. Which combination of Google technologies will meet all of their requirements?

- [ ] A. Container Engine, Cloud Pub/Sub, and Cloud SQL
- [ ] B. Cloud Dataflow, Cloud Storage, Cloud Pub/Sub, and BigQuery
- [ ] C. Cloud SQL, Cloud Storage, Cloud Pub/Sub, and Cloud Dataflow
- [ ] D. Cloud Dataproc, Cloud Pub/Sub, Cloud SQL, and Cloud Dataflow
- [ ] E. Cloud Pub/Sub, Compute Engine, Cloud Storage, and Cloud Dataproc

<details><summary>ANSWER</summary>
- [x] B. Cloud Dataflow, Cloud Storage, Cloud Pub/Sub, and BigQuery
</details>

---
![](./gcp-exams-mountkirk.png)