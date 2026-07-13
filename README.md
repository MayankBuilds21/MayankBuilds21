ew



# <div align="center">🌌 Mayank Jha</div>
<div align="center">
  <img src="https://readme-typing-svg.demolab.com/?font=Outfit&size=24&duration=3000&pause=1000&color=7aa2f7&center=true&vCenter=true&width=750&lines=Staff+Software+Engineer+%7C+Distributed+Systems;GenAI+Platform+Architect+%7C+eBPF+%26+Cloud+Native;Open+Source+Maintainer+%7C+Building+the+Future+of+Web3;Designing+for+99.999%25+Availability+%26+Sub-millisecond+Latency" alt="Typing SVG" />
  <p align="center">
    <strong>Developing resilient, ultra-scalable distributed infrastructures, cognitive multi-agent platforms, and performance-optimized cloud architectures.</strong>
  </p>
  <p align="center">
    <a href="https://linkedin.com/in/alexchen-dev"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
    <a href="mailto:alex.chen.dev@proton.me"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=protonmail&logoColor=white" alt="Email" /></a>
    <a href="https://alexchen.dev"><img src="https://img.shields.io/badge/Portfolio-7aa2f7?style=for-the-badge&logo=react&logoColor=white" alt="Portfolio" /></a>
    <a href="https://leetcode.com/alexchen_dev"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode" /></a>
  </p>
  <p align="center">
    <img src="https://komarev.com/ghpvc/?username=alexchen-dev&color=7aa2f7&style=flat-square&label=TRANSMISSION+RECEPTIONS" alt="Visitor Counter" />
  </p>
  
  <img src="https://raw.githubusercontent.com/alexchen-dev/alexchen-dev/output/github-contribution-grid-snake.svg" alt="Contribution Snake" width="100%" />
</div>
---
### 🧠 About Me
```yaml
engineer:
  name: "Alex Chen"
  role: "Staff Software Engineer"
  location: "San Francisco, CA"
  education:
    degree: "M.S. in Computer Science"
    institution: "UC Berkeley"
    focus: "Distributed Systems & Machine Learning Systems"
  mindset: "Simplicity is the ultimate sophistication. Optimize only after measuring."
```
* **Engineering Philosophy**: I build systems that degrade gracefully and scale horizontally. I believe in deep-dive observability, data-driven decisions, and writing highly readable, self-documenting code.
* **Areas of Specialization**: High-Throughput Distributed Ledgers, eBPF Service Meshes, Large Language Model (LLM) Orchestration, Raft & Paxos Consensus, Kernel-Space Networking, and Performance Tuning (CPU/Memory profiling).
* **Technical Interests**: Compilers, WebAssembly (Wasm) at the Edge, Zero-Knowledge Proofs, and Event-Sourced Architectures.
---
### 🏆 Competitive Programming & Achievements
<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>💻 Competitive Programming Profiles</h4>
      <ul>
        <li><strong>LeetCode Guardian</strong> (Max Rating: <code>2,480</code>, Top 0.1% Globally)</li>
        <li><strong>Codeforces Master</strong> (Max Rating: <code>2,150</code>)</li>
        <li><strong>CodeChef 6★</strong> (Max Rating: <code>2,210</code>)</li>
        <li><strong>HackerRank Gold</strong> (Problem Solving & Algorithms)</li>
        <li><strong>GeeksforGeeks</strong> (Top 100 Institution Rank)</li>
      </ul>
    </td>
    <td width="50%" valign="top">
      <h4>🥇 Key Achievements & Leadership</h4>
      <ul>
        <li><strong>1st Place</strong> — Global Generative AI Hackathon 2025 (Out of 1,200+ teams)</li>
        <li><strong>Core Maintainer</strong> — Contributed over 10,000+ lines of code to CNCF sandbox projects</li>
        <li><strong>AWS Certified Solutions Architect</strong> — Professional</li>
        <li><strong>Technical Lead</strong> — Spearheaded transition of monolithic core billing platform to Event-Sourced microservices at Stripe</li>
      </ul>
    </td>
  </tr>
</table>
---
### 💼 Featured Projects
#### ☄️ 1. AetherDB: Distributed LSM-Tree Key-Value Store
> A distributed, raft-consensus based, LSM-tree key-value store built in Rust, achieving sub-millisecond tail latencies under heavy write workloads.
```
                  ┌───────────────┐
                  │  gRPC Client  │
                  └───────┬───────┘
                          │ (Protobuf)
                          ▼
            ┌───────────────────────────┐
            │       Aether Node         │
            │  ┌─────────────────────┐  │
            │  │   Raft Consensus    │  │
            │  └──────────┬──────────┘  │
            │             │ (Replicated │
            │             ▼  Log)       │
            │  ┌─────────────────────┐  │
            │  │    LSM-Tree Engine  │  │
            │  │  ┌───────────────┐  │  │
            │  │  │    MemTable   │  │  │
            │  │  └───────┬───────┘  │  │
            │  │          │ (Flush)  │  │
            │  │          ▼          │  │
            │  │  ┌───────────────┐  │  │
            │  │  │   SSTables    │  │  │
            │  │  └───────────────┘  │  │
            │  └─────────────────────┘  │
            └───────────────────────────┘
```
* **Business Problem Solved**: Replaced a costly, high-latency external memory store with a custom in-house distributed cache, reducing API cloud spending by 42% and eliminating random latency spikes.
* **Architecture**: Masterless read-replicas with Raft-driven strongly consistent writes, implementing multi-version concurrency control (MVCC) and active compaction.
* **Tech Stack**: `Rust` | `gRPC` | `Protobuf` | `Raft` | `Tokio` | `RocksDB (underlying concept)`
* **Key Scalability & Security Considerations**:
  * Sharded by key ranges using consistent hashing.
  * Native mTLS encryption for intra-cluster communication with automatic cert rotation.
* **Engineering Challenges**: Overcoming major head-of-line blocking in the compaction threads under write-heavy loads. Solved by implementing a priority-based compaction scheduler with dynamic thread-pool allocation.
* **Production-Readiness**: Chaos tested with ChaosMesh; withstood 35% node failure rates while maintaining zero data loss (RPO = 0, RTO < 3s).
---
#### 🧠 2. CognitiveFlow: Multi-Agent AI Orchestration Platform
> An enterprise-grade, multi-agent AI orchestration platform running on Kubernetes, supporting dynamically routed RAG pipelines and tool use.
* **Business Problem Solved**: Enabled customer support automation to handle complex multi-step inquiries, reducing manual ticket resolution time by 68%.
* **Architecture**: Microservices-based event-driven agent mesh communicating via Apache Kafka. Uses a centralized vector registry with semantic caching.
* **Tech Stack**: `Go` | `Python` | `Kubernetes` | `PyTorch` | `LangChain` | `Pinecone` | `Apache Kafka` | `gRPC`
* **Key Scalability & Security Considerations**:
  * Built-in token-rate-limiting to prevent cascading OpenAI/Anthropic API rate-limit errors.
  * AES-256 encryption at rest for prompt templates and user context histories.
* **Engineering Challenges**: LLM hallucinations and long response times in agent-to-agent loops. Resolved by introducing a deterministic supervisor node that validates intermediate JSON outputs against schema graphs before routing.
* **Production-Readiness**: Built-in OpenTelemetry instrumentation tracing agent reasoning traces (DAGs) in Jaeger. Handles over 15M agent executions daily.
---
### ⚡ Engineering Stack
<table>
  <tr>
    <td valign="top" width="50%">
      <h4>💻 Programming Languages</h4>
      <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
      <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" alt="Rust" />
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
      <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white" alt="C++" />
    </td>
    <td valign="top" width="50%">
      <h4>⚙️ Backend Engineering</h4>
      <img src="https://img.shields.io/badge/gRPC-00ADD8?style=flat-square&logo=grpc&logoColor=white" alt="gRPC" />
      <img src="https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white" alt="GraphQL" />
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
      <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node" />
      <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" alt="Spring" />
    </td>
  </tr>
  <tr>
    <td valign="top" width="50%">
      <h4>🗄️ Databases & Caching</h4>
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" />
      <img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white" alt="Elasticsearch" />
      <img src="https://img.shields.io/badge/Cassandra-1287B1?style=flat-square&logo=apachecassandra&logoColor=white" alt="Cassandra" />
      <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB" />
    </td>
    <td valign="top" width="50%">
      <h4>☁️ Cloud & DevOps</h4>
      <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS" />
      <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
      <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white" alt="Terraform" />
      <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus" />
    </td>
  </tr>
  <tr>
    <td valign="top" width="50%">
      <h4>🤖 Artificial Intelligence</h4>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
      <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=white" alt="HuggingFace" />
      <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=chainlink&logoColor=white" alt="LangChain" />
      <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI" />
    </td>
    <td valign="top" width="50%">
      <h4>⛓️ Blockchain & Web3</h4>
      <img src="https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white" alt="Solidity" />
      <img src="https://img.shields.io/badge/Ethereum-3C3C3D?style=flat-square&logo=ethereum&logoColor=white" alt="Ethereum" />
      <img src="https://img.shields.io/badge/Web3.js-F16822?style=flat-square&logo=web3dotjs&logoColor=white" alt="Web3" />
      <img src="https://img.shields.io/badge/Ethers.js-2535A0?style=flat-square&logo=ethereum&logoColor=white" alt="Ethers" />
    </td>
  </tr>
  <tr>
    <td valign="top" width="50%">
      <h4>📊 Data Engineering</h4>
      <img src="https://img.shields.io/badge/Apache_Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white" alt="Spark" />
      <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" alt="Kafka" />
      <img src="https://img.shields.io/badge/Flink-E6522C?style=flat-square&logo=apacheflink&logoColor=white" alt="Flink" />
      <img src="https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white" alt="dbt" />
    </td>
    <td valign="top" width="50%">
      <h4>🔐 Security & Systems</h4>
      <img src="https://img.shields.io/badge/eBPF-18565F?style=flat-square&logo=linux&logoColor=white" alt="eBPF" />
      <img src="https://img.shields.io/badge/OAuth_2.0-2F2F2F?style=flat-square&logo=jsonwebtokens&logoColor=white" alt="OAuth2" />
      <img src="https://img.shields.io/badge/Vault-000000?style=flat-square&logo=hashicorp&logoColor=white" alt="Vault" />
      <img src="https://img.shields.io/badge/WireGuard-88171A?style=flat-square&logo=wireguard&logoColor=white" alt="WireGuard" />
    </td>
  </tr>
</table>
---
### 🏗️ Engineering Experience
* **Production Backend Systems**: Designed and maintained microservices processing over **50,000 requests per second** with a 99.99% SLA.
* **Event-Driven Architecture & CQRS**: Implemented event sourcing using **Apache Kafka** and **Apache Flink** to handle real-time inventory adjustments and transaction accounting, decoupling downstream reporting databases.
* **Distributed Consensus**: Deployed **Raft-consensus** based key-value stores to coordinate state machine replication across multi-region configurations, mitigating split-brain scenarios.
* **AI & LLM Platform Engineering**: Built auto-scaling inference proxies utilizing semantic caching to reduce model token consumption by **35%** and optimize GPU utilization.
* **Performance Tuning & Kernel Hacking**: Utilized **eBPF** for network packet interception, dropping unauthorized traffic directly at the XDP layer and lowering API gateway memory overhead by **18%**.
* **Zero-Trust & Security Compliance**: Standardized role-based access control (RBAC) via **Open Policy Agent (OPA)** and automated secret management with **HashiCorp Vault**.
---
### 🏆 Professional Highlights
* 📈 **12+ Production Services** architected and launched.
* ⚡ **Sub-10ms P99 Latency** maintained across core API gateways.
* 📦 **50+ Open-Source PRs** merged into mainstream packages (Kubernetes, Rust Tokio, Prometheus).
* 👥 **15+ Engineers** mentored, facilitating promotions to Senior & Staff roles.
* 💰 **$2.4M Annual Cloud Savings** achieved through resource rightsizing, auto-scaling, and code optimizations.
---
### 📈 GitHub Metrics
<div align="center">
  <table width="100%">
    <tr>
      <td width="50%"><img src="https://github-readme-stats.vercel.app/api?username=alexchen-dev&show_icons=true&theme=tokyonight&count_private=true" alt="GitHub Stats" width="100%" /></td>
      <td width="50%"><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=alexchen-dev&layout=compact&theme=tokyonight" alt="Top Languages" width="100%" /></td>
    </tr>
    <tr>
      <td width="50%"><img src="https://github-readme-streak-stats.herokuapp.com/?user=alexchen-dev&theme=tokyonight" alt="GitHub Streak" width="100%" /></td>
      <td width="50%"><img src="https://github-profile-trophy.vercel.app/?username=alexchen-dev&theme=tokyonight&margin-w=15" alt="GitHub Trophies" width="100%" /></td>
    </tr>
  </table>
  <br />
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=alexchen-dev&bg_color=1a1b26&color=7aa2f7&line=7aa2f7&point=9ece6a&area=true&hide_border=true" alt="Activity Graph" width="100%" />
</div>
---
### 🌱 Currently Exploring
```markdown
- 🤖 Agentic AI Frameworks (LangGraph, CrewAI, AutoGen)
- 🎛️ WASM-based Cloud-Native Micro-Runtimes
- 🕸️ Decentralized Consensus Systems (BFT, HotStuff)
- 🚀 Linux Kernel Networking (eBPF, XDP, io_uring)
- 🧬 Vector Search Scaling in Multi-Billion Document Databases
```
---
### 🤝 Let's Connect
<p align="left">
  <a href="mailto:alex.chen.dev@proton.me"><img src="https://img.shields.io/badge/Email-alex.chen.dev@proton.me-7aa2f7?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://linkedin.com/in/alexchen-dev"><img src="https://img.shields.io/badge/LinkedIn-Alex_Chen-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://github.com/alexchen-dev"><img src="https://img.shields.io/badge/GitHub-alexchen--dev-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" /></a>
  <a href="https://alexchen.dev"><img src="https://img.shields.io/badge/Portfolio-alexchen.dev-9ece6a?style=flat-square&logo=react&logoColor=white" alt="Portfolio" /></a>
  <a href="https://leetcode.com/alexchen_dev"><img src="https://img.shields.io/badge/LeetCode-alexchen__dev-FFA116?style=flat-square&logo=leetcode&logoColor=white" alt="LeetCode" /></a>
  <a href="https://x.com/alexchen_dev"><img src="https://img.shields.io/badge/Twitter-@alexchen__dev-1DA1F2?style=flat-square&logo=twitter&logoColor=white" alt="Twitter" /></a>
</p>
---
<div align="center">
  <i>"Make it work, make it right, make it fast. In that order. The fastest code is the code that never runs."</i> — <strong>Alex Chen</strong>
</div>
