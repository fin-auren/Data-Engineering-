# Data Engineering for Finance

A practical learning repository documenting my journey through Data Engineering, with a focus on applying data engineering principles to financial use cases.

# Introduction

Over the last decade, almost every industry has undergone a fundamental shift toward digital systems. In finance especially, data has become one of the most important assets of an organization. Transactions, market data, customer interactions, risk metrics, regulatory information, financial statements, and operational events are increasingly generated, stored, and processed digitally.

However, having large amounts of data is not enough.

The real challenge is building the infrastructure, pipelines, processes, and data systems required to turn raw data into reliable and usable information.

This repository is my practical learning journey through Data Engineering, based on the concepts, case studies, and hands-on exercises covered throughout the course. While the course provides the foundational principles, I will use this repository to explore how those principles can be applied to financial data and finance-related use cases.

# Why Data Engineering?

One of the key ideas introduced in this course is that data engineering provides the foundation upon which analytics, machine learning, and AI systems are built.

A data scientist may have a sophisticated model or an interesting business question, but without reliable and accessible data, the model cannot deliver meaningful results.

This creates an important relationship:

Data Sources
     ↓
Data Engineering
     ↓
Reliable & Usable Data
     ↓
Analytics / Data Science / ML / AI
     ↓
Business Decisions


For me, this is particularly relevant in finance, where data can be:

High-volume

High-frequency

Time-sensitive

Heterogeneous

Subject to quality and consistency issues

Governed by regulatory and security requirements

A financial analytics or machine-learning system is therefore only as useful as the data infrastructure supporting it.

Data Engineering and Finance

Throughout this course, I will try to look beyond the generic examples and ask:

How would this concept apply if the data were coming from a financial system?

For example, a concept such as a data pipeline could represent a system that moves:

Market Data / Transactions / Financial APIs
                    ↓
              Data Ingestion
                    ↓
             Data Validation
                    ↓
              Transformation
                    ↓
             Data Storage
                    ↓
          Analytics / Reporting
                    ↓
        Risk / Investment / Business Use


The objective is not to force every concept into a financial application, but to use finance as a practical perspective for understanding why the engineering decisions matter.

# Data-Centric Thinking

Another important theme introduced at the beginning of the course is the idea of taking a data-centric approach to AI and machine learning.

The quality of a machine-learning system is not determined only by the algorithm. The data used to train and operate that system is equally important.

For financial applications, this becomes particularly interesting.

A model for predicting market behaviour, assessing credit risk, detecting fraud, forecasting cash flows, or analysing customer behaviour depends on having data that is:

Correct

Consistent

Timely

Well-structured

Traceable

Appropriately transformed

Available at the required scale

This makes data engineering an important part of the broader AI and analytics ecosystem.

What This Repository Will Contain

This repository will evolve alongside the course.

Rather than treating the course as a collection of isolated lectures, I will use the repository to document the progression from concept → implementation → financial application → reflection.

# 1. Course Concepts

Notes and summaries covering the fundamental ideas introduced throughout the course, including:

Data engineering principles

Data engineering lifecycle

Data architecture

Data pipelines

Data ingestion

Data storage

Data transformation

Data modeling

Data quality

Data operations

Pipeline orchestration

Cloud data systems

Data serving

# 2. Practical Sessions

Hands-on implementations from the course will be documented here, including the tools, technologies, architectures, and workflows used during practical exercises.

Where appropriate, I will reproduce or extend the exercises so that I understand why a particular engineering approach is being used rather than simply following the implementation.

# 3. Financial Use Cases

I will progressively adapt selected concepts and practical exercises to financial scenarios.

Potential areas include:

Market data pipelines

Transaction data

Financial APIs

Portfolio data

Risk analytics

Fraud detection

Financial reporting

Time-series data

Customer financial data

Regulatory and compliance data

Financial forecasting

Data platforms for investment analytics

These applications will be exploratory and are intended primarily as engineering learning exercises.

# 4. My Perspective

An important part of this repository will be my own observations and interpretations.

For selected projects, I will document questions such as:

Why is this architecture appropriate?

What would change in a financial environment?

What happens when the data volume increases?

Where could data quality problems occur?

What would need to be monitored?

What are the trade-offs between different approaches?

How could this pipeline be made more reliable?

How would the system behave in a real production environment?

This section will evolve as my understanding of data engineering improves.

# Course Structure

The course series introduces Data Engineering through four broad areas:

Course	Focus
Course 1	Data engineering foundations, mental models, and cloud data pipelines
Course 2	Data ingestion, DataOps, and pipeline orchestration
Course 3	Cloud data storage and its role across the data engineering lifecycle
Course 4	Data modeling, transformation, and serving data for end use cases

The intention of this repository is to follow that progression while gradually building a more complete picture of how a modern data platform works.

# Technology & Tools

As the course progresses, this section will be updated with the technologies and tools used in the lectures and practical sessions.

# The initial learning environment includes concepts and technologies around:

Python

SQL

Cloud platforms

AWS

Data storage

Data processing

Data pipelines

Data orchestration

Data modeling

APIs

Git & GitHub

The specific tools will be added here as they are introduced and used.

# Repository Philosophy

This is not intended to be a collection of copied course notes.

Instead, I want this repository to answer three questions:

What did I learn?

How did I implement it?

How could I apply it to a financial data problem?

The repository will therefore combine:

Course Material
      +
Practical Implementation
      +
Financial Perspective
      +
Personal Reflection
      =
Data Engineering Learning Portfolio


 ## From Business Needs to Data Systems

 The second lecture introduces a scenario that is common across many organizations: a company hires a data scientist to generate insights and build machine-learning systems, only to discover that the data infrastructure required to support those goals does not exist.

 This highlights an important distinction:

 > **Data science and machine learning can create value from data, but data engineering provides much of the infrastructure that makes that work possible.**

 A data engineer's responsibility therefore goes beyond writing pipelines or working with cloud technologies. The role starts with understanding **what the organization is trying to achieve** and translating those needs into reliable data systems.

---

 ## The Data Engineer's Role

 A data engineer sits at an important intersection between business requirements, data, software systems, analytics, and technology.

 A simplified view is:

```
Business / Stakeholders
          ↓
     Business Needs
          ↓
    System Requirements
          ↓
    Data Architecture
          ↓
 Data Engineering Systems
          ↓
 Reliable & Accessible Data
          ↓
 Analytics / ML / AI / Applications
```

 One of the central lessons from this lecture is that the technology should come **after** understanding the problem.

 It can be tempting to immediately think about:

 - Which database should I use?
- Should I use AWS?
- Which orchestration tool should I choose?
- Should I build a batch or streaming pipeline?
- Which programming language or framework should I use?

 But these are implementation questions.

 The more fundamental question is:

 > **What problem are we actually trying to solve, and what does the organization need from the data system?**

---

 ## My Perspective: Applying This to Finance

 This principle becomes particularly important when thinking about financial systems.

 For example, imagine a company wants to improve its portfolio analytics.

 A technology-first approach might immediately lead to questions about databases, APIs, cloud services, or streaming frameworks.

 A data-engineering-first approach would begin differently.

 ### Step 1 — Understand the stakeholder

 Who needs the system?

 Possible stakeholders could include:

 - Portfolio managers
- Risk analysts
- Financial analysts
- Compliance teams
- Executives
- Data scientists
- Software/application teams

 ### Step 2 — Understand the business requirement

 For example:

 > "Portfolio managers need updated portfolio and market information to analyse portfolio performance during the trading day."

 This requirement contains much more information than simply saying:

 > "We need a market-data pipeline."

 ### Step 3 — Translate the requirement into data requirements

 We may need to determine:

 - Which market data is required?
- How frequently should it be updated?
- What historical data is required?
- How much latency is acceptable?
- How accurate does the data need to be?
- How should missing data be handled?
- Who should have access?
- How long should the data be retained?

 ### Step 4 — Design the system

 Only after understanding those requirements should we start considering the architecture and technology.

```
Stakeholder Need
       ↓
Business Requirement
       ↓
Data Requirements
       ↓
System Requirements
       ↓
Architecture
       ↓
Technology Selection
       ↓
Implementation
```

 This sequence is one of the ideas I want to carry throughout the course.

---

 ## Avoiding the "Tool-First" Approach

 One of the strongest points from this lecture is the warning against choosing technologies before understanding the problem.

 Technology changes quickly.

 Cloud platforms, databases, orchestration frameworks, processing engines, and AI tools continue to evolve. However, the underlying process of understanding requirements and designing systems around those requirements is much more durable.

 For this reason, I want to approach the practical projects in this repository with the following mindset:

```
❌ Tool → Problem

Instead:

✅ Problem → Requirements → Architecture → Tool → Implementation
```

 This distinction will become increasingly important as the course introduces more technologies.

---

 ## Data Engineering as a Translation Layer

 Another way I understand the role of a data engineer is as a **translation layer** between different parts of an organization.

```
                    Business
                       │
                       ▼
                 Business Goals
                       │
                       ▼
              ┌─────────────────┐
              │ Data Engineer   │
              └─────────────────┘
                 │           │
                 ▼           ▼
          Data Systems    Data Users
                 │           │
                 ▼           ▼
             Data      Analytics / ML
```

 The data engineer needs to understand enough about the business problem to design an appropriate system, while also understanding enough about the technical environment to implement that system.

 This makes data engineering both a **technical discipline and a problem-solving discipline**.

---

 ## Thinking Before Coding

 An interesting part of this lecture is that the first week does not focus on writing code.

 There are no immediate Python implementations or cloud deployments.

 Instead, the focus is on developing the ability to:

 - Understand the data engineering lifecycle
- Understand stakeholders
- Identify business value
- Gather requirements
- Translate requirements into system requirements
- Think about architecture
- Understand trade-offs
- Select technologies based on requirements

 This is useful for my learning approach because it creates a distinction between **knowing how to use a tool** and **knowing why a tool should be used**.

 I want to maintain this distinction throughout the repository.

---

 ## Course Roadmap Introduced in This Lecture

 The course is structured progressively.

 ### Week 1 — The Data Engineering Mindset

 The focus is on understanding the field at a high level:

 - Data engineering lifecycle
- History of data engineering
- Roles and stakeholders
- Business value
- Stakeholder needs
- System requirements
- Developing a data-engineering mindset

 ### Week 2 — Data Engineering Lifecycle

 The second week goes deeper into the different stages of the data engineering lifecycle.

 It combines conceptual material with a practical AWS lab involving cloud data pipelines.

 ### Week 3 — Data Architecture

 The focus shifts toward principles of good data architecture.

 The objective is to understand how different components come together to create effective data systems.

 ### Week 4 — Designing for Stakeholder Needs

 The final week brings the concepts together by designing and building a data architecture based on stakeholder requirements.

 This creates a progression:

```
Think
  ↓
Understand the Lifecycle
  ↓
Understand Architecture
  ↓
Design a System
  ↓
Build the System
```

---

 ## Financial Case Study Framework

 Going forward, I will use a similar framework when adapting course concepts to financial use cases.

 For each relevant project, I will try to document:

 ### 1\. Business Problem

 What financial or business problem are we trying to solve?

 ### 2\. Stakeholders

 Who will use the data or benefit from the system?

 ### 3\. Requirements

 What does the system need to provide?

 ### 4\. Data

 What data sources are required?

 ### 5\. Architecture

 How should the data move through the system?

 ### 6\. Technology

 Which tools or platforms are appropriate, and why?

 ### 7\. Implementation

 How can the system actually be built?

 ### 8\. Data Quality

 How do we know that the data is reliable?

 ### 9\. Monitoring

 How would we know if something goes wrong?

 ### 10\. Reflection

 What did I learn, and what would I change in a real-world implementation?


 ## From Digital Data to Modern Data Engineering

 The previous lecture focused on **how to think like a data engineer**. This lecture provides the historical context for understanding why modern data engineering looks the way it does today.

 The central idea is simple:

 > **Data engineering has evolved alongside the scale, speed, variety, and business importance of digital data.**

 Data itself is not new. Humans have recorded information for thousands of years through writing, physical records, observations, and other forms of documentation.

 However, in the context of this course, the focus is specifically on **digitally recorded data** — data that can be stored, processed, transmitted, and analyzed by computers.

 Understanding how the technology evolved helps explain why modern data engineers work with such a diverse collection of databases, warehouses, cloud services, processing systems, APIs, and streaming technologies.

---

 ## A Brief History of Data Engineering

 The development of data engineering can be viewed as a progression driven largely by increasing amounts of data and increasingly complex use cases.

```
Computers
   ↓
Databases
   ↓
Relational Databases + SQL
   ↓
Data Warehouses
   ↓
Business Intelligence
   ↓
Web Applications
   ↓
Big Data
   ↓
Distributed Processing
   ↓
Cloud Computing
   ↓
Event Streaming
   ↓
Modern Data Engineering
```

 Each stage solved problems created by the previous stage.

---

 ## 1960s — The Beginning of Computerized Data

 The story of modern digital data begins with the emergence of computers and computerized databases.

 Organizations began moving information that was previously maintained through physical records into computer systems.

 This created new possibilities for:

 - Storing information
- Retrieving information
- Processing information
- Automating business operations

 At this stage, the primary challenge was essentially:

 > **How do we store and retrieve data using computers?**

---

 ## 1970s — Relational Databases and SQL

 Relational databases changed the way structured data could be stored and queried.

 The development of **SQL (Structured Query Language)** provided a standardized way to interact with relational data.

 The relational model became foundational for many business applications and remains highly relevant today.

 A simplified relational system might look like:

```
Customers
   │
   ├── Customer ID
   ├── Name
   └── Account

Transactions
   │
   ├── Transaction ID
   ├── Customer ID
   ├── Date
   └── Amount
```

 The ability to connect related entities through structured data became extremely important for business systems.

 ### Finance Perspective

 Financial institutions have historically relied heavily on structured relational data.

 Examples include:

 - Customer accounts
- Transactions
- Payments
- Loans
- Securities
- Orders
- Positions
- Reference data

 Even with the emergence of newer technologies, relational databases and SQL remain important parts of financial data ecosystems.

---

 ## 1980s — The Data Warehouse

 As organizations accumulated more operational data, they needed ways to transform that data into information that could support **analytical decision-making**.

 This led to the development of the data warehouse.

 The distinction between operational and analytical systems became increasingly important.

```
Operational Systems
       ↓
   Data Collection
       ↓
   Data Warehouse
       ↓
 Analytics / Reporting
       ↓
 Business Decisions
```

 Instead of simply storing data for operational transactions, organizations could create environments specifically designed for analysis.

 ### Finance Perspective

 A financial organization might have operational systems recording individual transactions while an analytical environment could be used to answer questions such as:

 - How has revenue changed over time?
- What is the performance of a portfolio?
- What are the transaction trends?
- Which customer segments generate the most activity?
- How has credit exposure changed?

 This distinction between **systems that run the business** and **systems that analyze the business** remains an important architectural concept.

---

 ## 1990s — Business Intelligence and Data Modeling

 As data systems became more sophisticated, organizations required dedicated pipelines and tools for reporting and business intelligence.

 Data modeling became an important part of analytical system design.

 Two influential approaches associated with this period are the approaches developed by **Ralph Kimball and Bill Inmon**.

 The broader lesson for me is that storing data is only one part of the problem.

 The data also needs to be structured in a way that makes it useful for its intended consumers.

```
Raw / Operational Data
        ↓
Transformation
        ↓
Data Model
        ↓
Business Intelligence
        ↓
Decision Making
```

 This idea will become increasingly important later in the course when we study **data modeling, transformation, and serving**.

---

 ## Mid-1990s — The Internet Changes Everything

 The mainstream adoption of the Internet created a new generation of web-first companies.

 Companies such as Amazon demonstrated the potential of large-scale web applications.

 Web applications generated new forms of data:

 - User activity
- Clicks
- Searches
- Purchases
- Sessions
- Application events
- Logs

 The growth of these applications meant that organizations needed increasingly capable:

 - Servers
- Databases
- Storage systems
- Data pipelines

 The amount of data being generated began growing much faster than traditional systems were designed to handle.

---

 ## The Big Data Era

 By the early 2000s, companies such as Google, Yahoo, and Amazon were dealing with data volumes that challenged traditional database and warehouse architectures.

 This led to the era commonly referred to as **Big Data**.

 A common way of describing Big Data is through the **three Vs**:

```
          BIG DATA

     Volume
        +
     Velocity
        +
      Variety
```

 ### Volume

 The amount of data being generated and stored.

 ### Velocity

 The speed at which data is generated and needs to be processed.

 ### Variety

 The increasing number of different data formats and sources.

 These dimensions are particularly relevant to financial systems.

 For example:

```
Financial Data
     │
     ├── Market Prices
     ├── Transactions
     ├── News
     ├── Customer Data
     ├── Regulatory Data
     ├── Financial Statements
     └── Alternative Data
```

 Not all of these sources have the same structure, frequency, or processing requirements.

---

 ## MapReduce and Distributed Processing

 A major milestone in this period was Google's work on **MapReduce**, which introduced a scalable approach to processing very large datasets.

 The broader significance was the emergence of **distributed data processing**.

 Instead of relying on a single machine:

```
Traditional Processing

        Data
         ↓
    ┌─────────┐
    │ Machine │
    └─────────┘
```

 large datasets could be processed across many machines:

```
Distributed Processing

             Data
              ↓
       ┌──────┼──────┐
       ↓      ↓      ↓
    Machine Machine Machine
       ↓      ↓      ↓
       └──────┼──────┘
              ↓
           Result
```

 This idea became fundamental to modern large-scale data processing.

---

 ## Hadoop and the Rise of the Big Data Engineer

 The ideas behind distributed processing inspired the development and adoption of technologies such as **Apache Hadoop**.

 This created an ecosystem around processing and storing very large datasets.

 Organizations increasingly needed engineers who could build and maintain these systems.

 The role of the **big data engineer** emerged.

 However, these systems could also be complex and expensive to operate.

 A significant amount of engineering effort could go into maintaining the infrastructure itself.

 This created another important shift in the evolution of data engineering.

---

 ## The Cloud Revolution

 At roughly the same time, companies were developing new approaches to scalable computing and storage.

 Amazon developed technologies such as:

 - Amazon EC2 for scalable compute
- Amazon S3 for scalable storage
- DynamoDB for scalable NoSQL workloads

 These technologies eventually became part of **Amazon Web Services (AWS)**.

 The cloud introduced a major change in how organizations could build data systems.

 Instead of purchasing and maintaining all physical infrastructure themselves, organizations could increasingly consume computing and storage as services.

```
Traditional Data Center

Company
   ↓
Buy Hardware
   ↓
Install Infrastructure
   ↓
Maintain Infrastructure
   ↓
Run Data Systems
```

 versus:

```
Cloud

Company
   ↓
Define Requirements
   ↓
Select Cloud Services
   ↓
Build Data Systems
   ↓
Scale Resources as Required
```

 The cloud therefore changed not only the technology but also the economics and accessibility of data infrastructure.

---

 ## Democratization of Data Technology

 One of the most significant consequences of cloud computing was that smaller organizations could gain access to technologies that previously required enormous infrastructure investments.

 This reduced the barrier to building sophisticated data systems.

 A startup no longer necessarily needed to own an enormous data center to experiment with large-scale computing and storage.

 This is particularly important for my learning because many of the technologies introduced in this course are now accessible through cloud platforms.

---

 ## From Batch Processing to Streaming

 Another major transition was the move from exclusively processing data in batches toward processing **continuous streams of events**.

 ### Batch Processing

 Data is collected and processed periodically.

```
Data → Data → Data → Data
              ↓
         Batch Process
              ↓
           Result
```

 For example:

 > Process all yesterday's transactions every morning.

 ### Event Streaming

 Data is processed continuously as events occur.

```
Event → Event → Event → Event → Event
   ↓       ↓       ↓       ↓       ↓
       Continuous Processing
```

 For example:

 > Process transactions as they occur.

 This distinction becomes particularly interesting in finance.

 A daily batch process might be sufficient for some reporting workloads, while other applications may require much lower latency.

 Examples could include:

 - Transaction monitoring
- Market-data processing
- Fraud detection
- Real-time risk monitoring
- Trading-system analytics

 The appropriate architecture therefore depends on the requirements established earlier in the course.

---

 ## From "Big Data" to Data Engineering

 An interesting observation from the lecture is that the term **Big Data** has become less central to how we describe data systems.

 Data continues to grow rapidly, but large-scale data processing has become increasingly accessible.

 As a result, the specialized role of the "big data engineer" has largely become part of the broader discipline of **data engineering**.

 The focus has shifted from simply handling enormous datasets toward solving broader organizational problems with data.

 This includes:

 - Data ingestion
- Data storage
- Data transformation
- Data quality
- Data architecture
- Data orchestration
- Data governance
- Data serving
- Analytics
- Machine learning
- AI

---

 ## Modern Data Engineering as Integration

 One of my main takeaways from this lecture is that modern data engineering is increasingly about **interoperability**.

 There is rarely one technology responsible for the entire data platform.

 Instead, modern data systems often combine many components:

```
Sources
  ↓
Ingestion
  ↓
Storage
  ↓
Processing
  ↓
Transformation
  ↓
Data Warehouse / Lake / Lakehouse
  ↓
Analytics / ML / AI / Applications
```

 The data engineer's role is often to connect these components effectively.

 This is similar to assembling building blocks:

 > **The challenge is not simply knowing each individual component. It is understanding how the components work together to deliver a useful system.**

---

 # Finance Perspective

 The historical evolution of data engineering can also be viewed through the evolution of financial data.

```
Financial Data Evolution

Paper Records
      ↓
Digital Records
      ↓
Relational Databases
      ↓
Data Warehouses
      ↓
Enterprise Data Platforms
      ↓
Big Data
      ↓
Cloud Data Platforms
      ↓
Streaming Financial Data
      ↓
Real-Time Analytics / AI
```

 The underlying financial questions have existed for a long time.

 What has changed is the **scale, speed, and diversity of the data available to answer them**.

 For example, consider portfolio analytics.

 An older system might have relied on periodic files containing end-of-day prices.

 A modern system might combine:

```
Market Data
     +
Transactions
     +
Portfolio Positions
     +
Reference Data
     +
News / Alternative Data
     +
Customer Data
     ↓
Financial Data Platform
     ↓
Analytics / Risk / Reporting / ML
```

 The engineering challenge is therefore no longer simply:

 > "How do I store financial data?"

 It becomes:

 > **"How do I reliably connect, process, store, transform, and serve many different forms of financial data so that downstream users can derive value from it?"**

---

 # Key Takeaways

 My main takeaways from this lecture are:

 1. **Modern data engineering is the result of decades of evolution in data technology.**
2. **Relational databases and SQL established a major foundation for structured data management.**
3. **Data warehouses introduced a dedicated environment for analytical decision-making.**
4. **The Internet dramatically increased the amount and variety of data being generated.**
5. **Big Data introduced new challenges around volume, velocity, and variety.**
6. **Distributed processing enabled organizations to work with datasets beyond the limits of individual machines.**
7. **Cloud computing made scalable infrastructure more accessible and flexible.**
8. **Streaming introduced the ability to process continuously generated events.**
9. **Modern data engineering is increasingly about integrating many technologies rather than relying on a single platform.**
10. **The ultimate purpose remains the same: building systems that enable organizations to derive value from data.**

---

 # Reflection

 This lecture helped me understand that today's data-engineering ecosystem did not appear suddenly.

 Many of the technologies and architectural patterns we use today are responses to specific historical problems:

```
More Data
   ↓
Better Storage
   ↓
Better Databases
   ↓
Better Analytical Systems
   ↓
Distributed Processing
   ↓
Cloud Infrastructure
   ↓
Streaming
   ↓
Modern Data Platforms
```

 For my finance-focused perspective, this history is especially useful because financial institutions have experienced many of these transitions themselves.

 A financial data platform today may need to combine traditional relational systems with cloud storage, analytical warehouses, APIs, distributed processing, and real-time streaming.

 Therefore, learning data engineering is not simply about learning a list of modern tools.

 It is about understanding **why these technologies exist, what problems they solve, and how they can be combined to build systems that deliver value**.

 That historical context will be important as the course moves from concepts into the data engineering lifecycle, architecture, and practical implementation.


 ## Data Engineering Does Not Happen in a Vacuum

 A data engineer's job can be summarized simply:

 > **Take raw data, transform it into something useful, and make it available for downstream use cases.**

 But the word **useful** is important.

 Data is not useful simply because it has been cleaned, stored, or transformed. It is useful when it satisfies the needs of the people and systems that consume it.

 This means that data engineering is fundamentally connected to **stakeholders**.

 A successful data engineer needs to understand both sides of the data pipeline:

```
        UPSTREAM
           │
           ▼
    Source Systems
           │
           ▼
     Data Engineer
           │
           ▼
   Data Systems / Pipelines
           │
           ▼
       DOWNSTREAM
           │
           ▼
 Analysts / ML / Business
```

 The data engineer is therefore both a **consumer of upstream data** and a **provider of downstream data**.

---

 # Downstream Stakeholders

 Downstream stakeholders are the people, teams, or systems that consume the data produced by the data engineering systems.

 Depending on the organization, these might include:

 - Data analysts
- Data scientists
- Machine-learning engineers
- Software engineers
- Product teams
- Marketing teams
- Sales teams
- Risk teams
- Executives
- Other business users

 Their requirements can be very different.

 For example, a data scientist might need a large historical dataset for model development, while an executive might need a small number of highly reliable metrics on a dashboard.

 The data engineer therefore needs to understand the **actual use case**, rather than simply delivering data.

---

 # Example: Serving a Business Analyst

 Consider a business analyst who needs to query a database to build dashboards and analyze trends.

 At first glance, the requirement might appear simple:

 > "Give the analyst access to the sales data."

 But a data engineer needs to ask deeper questions.

 ### Frequency

 How often does the analyst need the data?

```
Daily?
Hourly?
Every 15 minutes?
Near real-time?
```

 ### Data Requirements

 What information does the analyst actually need?

 Which:

 - Tables?
- Columns?
- Metrics?
- Dimensions?
- Filters?

 ### Query Performance

 Will the analyst repeatedly perform expensive joins or aggregations?

 If so, could some of this work be performed upstream so that the analyst receives data in a more useful form?

 ### Latency

 How old can the data be?

 For example:

```
Real-time
    ↓
5 minutes
    ↓
1 hour
    ↓
1 day
    ↓
1 week
```

 The answer depends entirely on the business use case.

---

 # A Simple Example: What Is a "Day"?

 One of the most useful examples from this lecture is surprisingly simple.

 Suppose an analyst asks:

 > "Give me the total sales for each day."

 This sounds unambiguous.

 But imagine the company operates globally.

 What exactly defines a day?

```
00:00 ─────────────────────── 23:59
          Which Time Zone?
```

 Is the business day based on:

 - UTC?
- Local customer time?
- Headquarters time?
- Regional time?
- Exchange time?

 The calculation itself may be trivial.

 The **definition of the metric** is not.

 This illustrates an important data-engineering principle:

 > **Data engineering problems are often definition problems before they are technical problems.**

---

 # Finance Perspective: The Definition of a Metric

 This becomes especially important in finance.

 Imagine a stakeholder asks:

 > "What was the daily trading volume?"

 Before building a pipeline, several questions need to be clarified.

 What counts as:

 - A trade?
- A transaction?
- Trading volume?
- A trading day?
- A cancelled trade?
- A corrected trade?
- A partial execution?

 And which time zone defines the trading day?

 For financial markets, the relevant time boundary may depend on the specific market or instrument.

 Therefore:

```
Business Question
       ↓
Metric Definition
       ↓
Data Definition
       ↓
Transformation Logic
       ↓
Final Dataset
```

 A technically perfect pipeline can still produce a misleading result if the underlying business definition is wrong.

---

 # Upstream Stakeholders

 The other side of the relationship is the **upstream stakeholder**.

 These are the people or teams responsible for the systems from which the data engineer obtains raw data.

 They may include:

 - Software engineers
- Application teams
- Database administrators
- Internal platform teams
- External API providers
- Third-party system owners

 In this relationship, the roles are reversed.

 The data engineer becomes the **data consumer**.

```
Source System
     │
     │ Raw Data
     ▼
Data Engineer
     │
     │ Processed Data
     ▼
Downstream Consumer
```

 The data engineer therefore needs to understand the source system just as downstream users need to understand the data they consume.

---

 # Understanding the Source

 When working with an upstream system, important questions include:

 ### Volume

 How much data will be generated?

```
MB?
GB?
TB?
PB?
```

 ### Frequency

 How frequently is data generated?

```
Once per day?
Every hour?
Every minute?
Continuously?
```

 ### Format

 What format does the source provide?

 For example:

 - CSV
- JSON
- XML
- Parquet
- Database tables
- API responses
- Event streams

 ### Schema

 What fields exist?

 What are their data types?

 What relationships exist between entities?

 ### Reliability

 What happens when the source system becomes unavailable?

 ### Security

 Does the data contain sensitive information?

 ### Compliance

 Are there regulatory or organizational requirements governing the data?

 ### Schema Changes

 What happens when the source system changes?

 For example:

```
Before:
customer_id
name
amount

After:
customer_id
name
currency
amount
```

 A seemingly small schema change can potentially break downstream pipelines.

---

 # Communication Is Part of Data Engineering

 One of the most important lessons from this lecture is that communication is not separate from engineering.

 Good communication with upstream teams can provide early warnings about:

 - System outages
- Planned maintenance
- Schema changes
- New fields
- Removed fields
- Changes in data volume
- Changes in data frequency
- Changes in business logic

 This allows the data engineering team to prepare rather than react.

 A healthy relationship might look like:

```
Source Team
    │
    │  Changes / Expectations
    ▼
Data Engineering
    │
    │  Requirements / Feedback
    ▼
Source Team
```

 This feedback loop can improve the reliability of the overall data system.

---

 # Finance Perspective: Upstream Systems

 In a financial environment, upstream sources could include:

```
                Financial Data Sources
                        │
       ┌────────────────┼────────────────┐
       ↓                ↓                ↓
 Transaction        Market Data       Customer
 Systems            Providers         Systems
       │                │                │
       └────────────────┼────────────────┘
                        ↓
                 Data Engineering
                        ↓
              Financial Data Platform
                        ↓
       ┌────────────────┼────────────────┐
       ↓                ↓                ↓
     Risk           Analytics          ML/AI
```

 Each source can have completely different characteristics.

 For example, transaction systems may produce structured records, while market-data providers may deliver continuous event streams.

 This means the data engineer must understand not only the destination but also the **characteristics of every important source**.

---

 # The Data Engineer as a Bridge

 A useful mental model from this lecture is to think of the data engineer as a bridge between two worlds.

```
             UPSTREAM
          Source Systems
               │
               │
               ▼
       ┌───────────────┐
       │               │
       │ DATA ENGINEER │
       │               │
       └───────────────┘
               │
               │
               ▼
            DOWNSTREAM
      Business / Analytics
          / ML / AI
```

 The data engineer needs to understand both directions.

 ### Looking upstream

 Ask:

 > **What data am I receiving, where does it come from, and what can affect its reliability?**

 ### Looking downstream

 Ask:

 > **Who is consuming this data, what are they trying to achieve, and what does "useful" mean to them?**

---

 # Stakeholder Requirements Framework

 This lecture provides a useful framework that I can apply to future projects in this repository.

 ## Upstream Requirements

 When dealing with source systems:

 - What is the source?
- Who owns it?
- What data does it produce?
- How frequently is it generated?
- What is the expected volume?
- What format does it use?
- What is the schema?
- How reliable is the source?
- How are changes communicated?
- Are there security or regulatory constraints?

 ## Downstream Requirements

 When dealing with data consumers:

 - Who consumes the data?
- What problem are they solving?
- What data do they need?
- How frequently do they need it?
- How fresh does it need to be?
- What level of accuracy is required?
- What metrics need to be defined?
- What query patterns are expected?
- What performance is required?
- What decisions will the data support?

---

 # Applying the Framework to a Financial Project

 For future financial projects in this repository, I want to explicitly document both sides.

 For example:

 ### Project: Financial Transaction Analytics Pipeline

```
UPSTREAM
───────────────
Transaction System
      │
      │
      ▼
Raw Transactions
      │
      ▼
DATA ENGINEERING
───────────────
Ingestion
Validation
Transformation
Storage
Quality Checks
      │
      ▼
DOWNSTREAM
───────────────
Risk Analysts
Financial Analysts
Data Scientists
Dashboards
ML Models
```

 Before implementing the pipeline, I would want to understand:

 **Upstream**

 - How are transactions generated?
- How frequently are they available?
- What fields are provided?
- Can transactions be corrected?
- Can records arrive late?
- Can the schema change?

 **Downstream**

 - Who needs the transaction data?
- What metrics are required?
- How fresh must the data be?
- What historical period is needed?
- What aggregations are commonly performed?
- What decisions will the resulting data support?

 Only after answering these questions should implementation decisions begin.

---

 # Key Takeaways

 My main takeaways from this lecture are:

 1. **Data engineering is fundamentally stakeholder-driven.**
2. **The data engineer serves downstream consumers while depending on upstream systems.**
3. **Understanding the source data is as important as understanding the destination.**
4. **Data requirements include more than columns and data types; they also include volume, frequency, latency, reliability, security, and compliance.**
5. **Metrics need precise definitions before they can be implemented correctly.**
6. **Time zones and business definitions can materially affect analytical results.**
7. **Communication with upstream system owners can improve pipeline reliability.**
8. **Downstream requirements should influence how data is transformed and served.**
9. **A data pipeline should be designed around the needs of its users rather than around a technology alone.**
10. **In financial data engineering, precise definitions and stakeholder alignment are particularly important because small differences in interpretation can change analytical results.**

---

 # Reflection

 This lecture expands on the idea from the previous lecture that **technology should follow requirements**.

 I now see the data engineer as someone operating between two boundaries:

```
What the organization produces
             ↓
          UPSTREAM
             ↓
      DATA ENGINEERING
             ↓
        DOWNSTREAM
             ↓
What the organization needs
```

 The interesting part is that the data engineer has to understand both.

 If I only understand the source, I may build a technically reliable pipeline that nobody finds useful.

 If I only understand the consumer, I may design an excellent analytical dataset without understanding the limitations or reliability of the underlying source.

 The real objective is to connect the two.

 For the financial projects in this repository, I therefore want to make **stakeholder analysis and requirements gathering part of the project itself**, rather than treating them as documentation added after the implementation.


 ## Why Requirements Come Before Technology

 The previous lecture established that a data engineer needs to understand both upstream and downstream stakeholders.

 This lecture takes the next step:

 > **How do we translate what stakeholders need into something we can actually build?**

 Before writing code, selecting a database, or deploying cloud infrastructure, a data engineer needs to understand the requirements of the system.

 The overall process can be viewed as:

```
Business Goals
      ↓
Stakeholder Needs
      ↓
System Requirements
      ↓
Architecture
      ↓
Technology
      ↓
Implementation
```

 This reinforces one of the principles from the earlier lectures:

 > **Don't start with the technology. Start with the problem and the requirements.**

---

 # Three Levels of Requirements

 A useful distinction introduced in this lecture is that requirements exist at different levels.

```
Business Requirements
        ↓
Stakeholder Requirements
        ↓
System Requirements
```

 Each level answers a different question.

---

 ## 1\. Business Requirements

 Business requirements describe the **high-level goals of the organization**.

 Examples might include:

 - Increase revenue
- Reduce operating costs
- Increase customer retention
- Improve decision-making
- Reduce operational risk
- Expand into a new market

 These requirements are generally expressed in business language rather than technical language.

 For example:

 > "Improve the accuracy and speed of financial reporting."

 This is a business objective.

 It does not yet tell the data engineer what system to build.

---

 ## 2\. Stakeholder Requirements

 Stakeholder requirements describe what a particular person or team needs to accomplish their work.

 For example, a financial analyst might need:

 > "Access reliable daily portfolio performance data so that I can generate performance reports."

 A risk analyst might need:

 > "Receive updated exposure data frequently enough to monitor changes in portfolio risk."

 A data scientist might need:

 > "Access historical transaction data in a format suitable for developing fraud-detection models."

 These are more specific than business requirements, but they still do not fully define the technical system.

---

 ## 3\. System Requirements

 System requirements translate stakeholder needs into things the actual system must be capable of doing.

 For example:

```
Stakeholder Need
       ↓
"Analyst needs updated portfolio data"
       ↓
System Requirement
       ↓
"System must update portfolio data
 every hour"
```

 System requirements therefore form the bridge between **business needs and engineering implementation**.

---

 # Functional vs Non-Functional Requirements

 System requirements can be divided into two broad categories:

```
             SYSTEM REQUIREMENTS
                     │
            ┌────────┴────────┐
            ↓                 ↓
       Functional       Non-Functional
            │                 │
           WHAT              HOW / QUALITY
```

---

 ## Functional Requirements

 Functional requirements describe **what the system needs to do**.

 They represent the capabilities or behaviours of the system.

 Examples include:

 - Ingest financial transaction data
- Update a database every hour
- Calculate daily portfolio metrics
- Detect anomalies in incoming data
- Send an alert when a data-quality check fails
- Provide historical data for analysis
- Make transformed data available to downstream users

 A functional requirement might look like:

 > **The system must ingest new transaction records every 15 minutes.**

 This describes what the system must accomplish.

---

 # Non-Functional Requirements

 Non-functional requirements describe **how the system should perform or what constraints it must satisfy**.

 These can include:

 - Performance
- Reliability
- Scalability
- Security
- Availability
- Cost
- Latency
- Maintainability
- Compliance
- Data retention

 For example:

 > **The transaction pipeline should make newly received data available to downstream users within five minutes.**

 Or:

 > **The system must restrict access to sensitive financial data to authorized users.**

 The distinction can be summarized as:

```
Functional
"What must the system do?"

          vs.

Non-Functional
"How well must it do it,
and under what constraints?"
```

---

 # Finance Example — Portfolio Analytics Platform

 Consider a hypothetical financial organization that wants to improve portfolio analytics.

 The initial business request might be:

 > "We need better portfolio reporting."

 That is not enough information to start building a pipeline.

 We need to progressively translate it.

 ### Business Requirement

 > Improve the timeliness and reliability of portfolio reporting.

 ### Stakeholder Requirement

 A portfolio analyst needs:

 > Reliable portfolio positions and market data to calculate performance metrics.

 ### Functional Requirements

 The system must:

 - Ingest portfolio positions
- Ingest relevant market prices
- Associate securities with portfolios
- Calculate required metrics
- Store historical results
- Make the resulting data available for analytics

 ### Non-Functional Requirements

 The system must consider:

 - Data freshness
- Query performance
- Reliability
- Security
- Scalability
- Data retention
- Operational cost
- Regulatory requirements

 The result is a much more concrete system definition.

---

 # Requirements Are More Than Features

 One important lesson from this lecture is that requirements can exist at many levels of detail.

 They can describe:

```
Business Goals
      ↓
User Needs
      ↓
Data Products
      ↓
System Features
      ↓
Pipeline Behaviour
      ↓
Infrastructure
      ↓
Compute / Memory / Storage
```

 For example, a requirement could eventually influence something as technical as:

 - Memory capacity
- Storage capacity
- Compute resources
- Processing frequency
- Database configuration
- Pipeline orchestration
- Network requirements

 This is why good requirements gathering is foundational to architecture and implementation.

---

 # Requirements Gathering Is a Conversation

 Stakeholders usually do not approach a data engineer with a perfectly written technical specification.

 Instead, they may say things like:

 > "I need a dashboard that is always up to date."

 or:

 > "We need better risk data."

 or:

 > "Can you give me all the historical transactions?"

 The data engineer's responsibility is to investigate what these statements actually mean.

 This requires asking questions.

 For example:

 ### "Always up to date"

 Could mean:

 - Every few seconds
- Every minute
- Every hour
- Once per day

 ### "Historical transactions"

 Could mean:

 - Last month
- Last year
- Five years
- All available history

 ### "Better risk data"

 Could mean:

 - More frequent updates
- More accurate calculations
- Additional fields
- Better data quality
- Better historical coverage
- Faster queries

 The initial stakeholder statement is therefore only the **starting point**.

---

 # Requirements Gathering Questions

 For future projects, I want to use a structured set of questions.

 ## Business

 - What business problem are we solving?
- Why is this problem important?
- What business outcome are we trying to improve?
- How will success be measured?

 ## Stakeholder

 - Who will use the data?
- What are they trying to accomplish?
- What decisions depend on the data?
- What does "useful" mean to them?

 ## Data

 - What data is required?
- Where does it come from?
- How frequently is it generated?
- How much historical data is needed?
- What quality is expected?

 ## Freshness

 - How quickly must new data become available?
- Is batch processing sufficient?
- Is streaming required?
- What latency is acceptable?

 ## Performance

 - How many users will consume the data?
- What queries will they run?
- How quickly should those queries respond?
- Are precomputed aggregations useful?

 ## Reliability

 - What happens when a source fails?
- What happens when data is missing?
- How should duplicate records be handled?
- How should late-arriving data be handled?

 ## Security

 - Who should have access?
- Does the data contain sensitive information?
- What access controls are required?

 ## Compliance

 - Are there regulatory requirements?
- How long should data be retained?
- Does the data need to be auditable?
- Are there restrictions on where the data can be stored?

 ## Cost

 - What infrastructure budget is available?
- What level of performance justifies the cost?
- What resources are likely to scale with data volume?

---

 # Finance Perspective: Requirements Can Change the Architecture

 Financial use cases make the connection between requirements and architecture particularly visible.

 Consider two hypothetical requirements.

 ### Requirement A

 > "Generate an end-of-day portfolio report every morning."

 This might be well suited to a batch-oriented architecture.

```
Daily Data
    ↓
Batch Processing
    ↓
Portfolio Calculations
    ↓
Report
```

 ### Requirement B

 > "Provide continuously updated portfolio exposure for monitoring."

 This may require a very different architecture.

```
Continuous Events
       ↓
Streaming / Event Processing
       ↓
Real-Time Data Store
       ↓
Risk Monitoring
```

 The key point is not that one architecture is universally better.

 The architecture should be driven by the **requirements**.

---

 # Requirement Trade-Offs

 Requirements can also conflict with each other.

 For example:

```
Lower Latency
      ↕
Higher Cost

Higher Reliability
      ↕
Greater Complexity

More Historical Data
      ↕
Higher Storage Cost

Higher Query Performance
      ↕
Potentially More Compute
```

 This means that data engineering is also a discipline of making **engineering trade-offs**.

 A stakeholder may want:

 - Real-time data
- Perfect reliability
- Unlimited historical storage
- Extremely fast queries
- Maximum security
- Minimum cost

 In practice, the engineer needs to understand which requirements are essential and which can be relaxed.

---

 # Requirements Traceability

 For larger projects, I want to maintain a clear connection between the original business goal and the implementation.

 For example:

```
Business Goal
"Improve portfolio reporting"
        ↓
Stakeholder Need
"Analysts need reliable daily positions"
        ↓
Functional Requirement
"Ingest and validate daily positions"
        ↓
Non-Functional Requirement
"Data available by 07:00 UTC"
        ↓
Architecture
"Scheduled batch pipeline"
        ↓
Implementation
"Ingestion → Validation → Transformation → Storage"
```

 This provides a useful form of **requirements traceability**.

 If a technical decision cannot be connected to a requirement, it is worth asking why that decision exists.

---

 # Requirements Template for Future Projects

 For the finance projects in this repository, I plan to use a template similar to this:

 | Category | Question |
| --- | --- |
| Business Goal | What problem are we solving? |
| Stakeholders | Who needs the data? |
| Use Case | What will they do with it? |
| Data Sources | Where does the data come from? |
| Functional Requirements | What must the system do? |
| Freshness | How current must the data be? |
| Performance | How quickly must it respond? |
| Reliability | What level of availability is required? |
| Security | Who can access the data? |
| Compliance | What rules apply? |
| Scalability | How might volume grow? |
| Cost | What constraints exist? |
| Data Quality | What makes the data trustworthy? |
| Output | What data product will be delivered? |

This template will evolve as I learn more throughout the course.

---

 # Key Takeaways

 My main takeaways from this lecture are:

 1. **Requirements should be gathered before implementation begins.**
2. **Business requirements describe organizational goals.**
3. **Stakeholder requirements describe what people need to accomplish their work.**
4. **System requirements translate those needs into something engineers can design and implement.**
5. **Functional requirements describe what the system must do.**
6. **Non-functional requirements describe how well the system must operate and the constraints it must satisfy.**
7. **Requirements can extend from high-level business goals all the way down to infrastructure resources.**
8. **Stakeholders usually communicate in terms of goals and needs rather than technical specifications.**
9. **Requirements gathering therefore requires active communication and questioning.**
10. **Architecture and technology choices should be consequences of requirements rather than assumptions made at the beginning.**

---

 # Reflection

 This lecture connects several of the ideas introduced so far.

 The progression now looks like:

```
Understand the Business
        ↓
Understand the Stakeholders
        ↓
Understand Their Needs
        ↓
Translate Needs into Requirements
        ↓
Design the Architecture
        ↓
Select Technologies
        ↓
Build the System
```

 This gives me a much stronger framework for approaching the practical projects later in the course.

 In particular, I want to avoid the common pattern of starting a project with:

 > "Which technology should I use?"

 Instead, I want to start with:

 > **"What problem am I solving, who needs the solution, and what does the system need to accomplish?"**

 Only after answering those questions should I decide how to implement the system.

 For the financial projects in this repository, this means that the **requirements section should come before the architecture diagram and before the code**.

 That gives each project a clear chain of reasoning:

```
Financial Problem
      ↓
Stakeholder Need
      ↓
Requirements
      ↓
Architecture
      ↓
Technology
      ↓
Implementation
      ↓
Data Product
      ↓
Business Value
```

## Data Engineering Is Also a Communication Discipline

 The previous lecture established that requirements gathering begins with understanding stakeholder needs and translating them into system requirements.

 This lecture adds another important dimension:

 > **Understanding the business is not optional if a data engineer wants to create meaningful value.**

 A data engineer may understand:

 - Data pipelines
- Databases
- APIs
- Cloud infrastructure
- Data models
- Distributed systems
- Orchestration
- Data quality

 But technical knowledge alone does not guarantee that the system will solve the right business problem.

 The data engineer needs to understand **why the data matters**.

---

 # The Data Engineer as a Translator

 One of the strongest ideas from this lecture is the role of the data engineer as a translator between technical and business worlds.

```
                    BUSINESS
                       │
                       │ Business Goals
                       ▼
              ┌─────────────────┐
              │  DATA ENGINEER  │
              │                 │
              │   Translation   │
              └─────────────────┘
                       │
                       │ Technical Requirements
                       ▼
                   DATA SYSTEM
```

 The translation works in both directions.

 ### Business → Technical

 A business leader might say:

 > "We need better visibility into customer behaviour."

 The data engineer needs to determine:

 - What does "better visibility" mean?
- Which customers?
- Which behaviours?
- What data is required?
- How frequently should it be updated?
- Who will use it?
- What decisions will it support?

 ### Technical → Business

 The data engineer may then need to explain:

 > "We are building an incremental ingestion pipeline that updates the analytical dataset every hour."

 But a business stakeholder may care more about:

 > "Your dashboard will now reflect customer activity within approximately one hour instead of waiting until the next day."

 The underlying technical work is the same.

 The **communication is different**.

---

 # Data Engineers Hold Important Context

 A particularly useful perspective from the lecture is that data engineers often have visibility into how information flows through an organization.

 They may understand:

```
Source Systems
      ↓
Ingestion
      ↓
Transformation
      ↓
Storage
      ↓
Data Products
      ↓
Analytics / ML / Applications
```

 This gives them an important perspective across the organization.

 The data engineer may know:

 - Where data originates
- How it is transformed
- Which systems depend on it
- Where quality problems occur
- How frequently it changes
- Which downstream teams consume it
- What limitations exist in the current architecture

 That context can make the data engineer an important participant in business discussions.

---

 # From Back Office to Business Context

 The lecture challenges the idea that data engineering should be treated purely as a back-office technical function.

 The technical work is important, but its value ultimately comes from enabling something else.

 For example:

```
Data Pipeline
     ↓
Reliable Data
     ↓
Better Analysis
     ↓
Better Information
     ↓
Better Business Decisions
```

 The pipeline itself is rarely the final objective.

 The objective is usually the **value enabled by the pipeline**.

 This changes the way I want to approach projects in this repository.

 Instead of documenting only:

 > "I built an AWS data pipeline."

 I want to document:

 > "I built an AWS data pipeline to provide \[stakeholder\] with \[data product\] so they can \[business/use-case objective\]."

---

 # Knowing Your Audience

 A central lesson from the discussion is:

 > **Know your audience.**

 Not every stakeholder has the same technical background.

 A useful mental model is:

```
Functional Stakeholder
        │
        │ Less technical
        ▼
   Business Language

Techno-Functional
        │
        │ Mixed
        ▼
Business + Selected Technical Concepts

Technical Stakeholder
        │
        │ Highly technical
        ▼
Technical Language
```

 The same project may therefore need to be explained differently to different people.

---

 # Functional Stakeholders

 A functional stakeholder may primarily care about:

 - Revenue
- Customers
- Costs
- Risk
- Operations
- Marketing
- Product performance
- Business KPIs

 They may not need to know the details of:

 - Data pipelines
- Semantic layers
- Source-to-target mappings
- Orchestration
- Distributed processing

 For this audience, the conversation should begin with the business problem.

 For example, rather than:

 > "We're implementing an incremental ELT architecture."

 A more useful explanation might be:

 > "The data will be refreshed throughout the day, so the operations team can monitor transaction activity without waiting for the next daily batch."

 The second statement communicates the same underlying goal in business terms.

---

 # Technical Stakeholders

 Technical stakeholders may want much more detail.

 Depending on their role, it may be appropriate to discuss:

 - Architecture
- APIs
- Data contracts
- Schemas
- Data models
- Processing patterns
- Infrastructure
- Performance
- Failure modes
- Observability
- Security

 In this situation, technical detail is useful because it helps communicate the actual engineering decisions.

 The important principle is not to avoid technical language.

 It is to **use the appropriate level of technical language for the audience**.

---

 # How to Determine the Right Level

 The lecture suggests several signals that can help determine how technical a stakeholder may be.

 ### 1\. Their role

 Look at their job title and responsibilities.

 ### 2\. Where they report

 Their organizational position can provide clues about whether their role is primarily technical, functional, or strategic.

 ### 3\. Their questions

 The easiest way to determine technical depth may simply be to listen.

 If they ask:

 > "How are you handling schema evolution?"

 That may indicate comfort with technical detail.

 If they ask:

 > "When will the dashboard reflect the new data?"

 They may primarily care about the business outcome.

 ### 4\. Let the conversation guide you

 A useful principle is:

 > **Start with the business context and increase technical depth when the stakeholder demonstrates that it is useful.**

---

 # Finance Perspective — Communicating the Same Pipeline

 Consider a financial transaction monitoring pipeline.

 The underlying architecture might look like:

```
Transaction API
      ↓
Ingestion
      ↓
Validation
      ↓
Transformation
      ↓
Cloud Storage
      ↓
Analytics Layer
      ↓
Monitoring Dashboard
```

 Different stakeholders may describe the value differently.

 ### Executive

 > "We can see transaction activity throughout the day instead of waiting for the daily report."

 ### Operations Manager

 > "The dashboard provides updated transaction activity so the team can identify unusual changes earlier."

 ### Risk Analyst

 > "The pipeline provides refreshed transaction-level data that can be used for exposure and anomaly analysis."

 ### Data Engineer

 > "The pipeline ingests transaction events, validates the schema, applies transformations, and publishes curated datasets to the analytical layer."

 ### Data Scientist

 > "The curated transaction dataset provides consistent historical features for model development."

 Same system.

 Different language.

---

 # Business Context Is Critical in Finance

 This principle is especially relevant to financial data engineering.

 Financial datasets can contain technically simple fields whose meaning depends heavily on context.

 For example:

```
amount
price
volume
balance
return
exposure
risk
transaction_date
settlement_date
```

 Knowing the field name is not enough.

 A data engineer needs to understand what the field represents within the business process.

 For example:

```
Transaction Date
       ≠
Settlement Date
```

 Both may be valid dates, but they represent different events.

 Similarly:

```
Price
   ≠
Market Value
   ≠
Notional Value
```

 Without business context, it is possible to build a technically functioning pipeline that produces the wrong analytical interpretation.

---

 # Communication and Data Quality

 This connects directly to data quality.

 Suppose a stakeholder says:

 > "The numbers don't look right."

 A purely technical response might be:

 > "The pipeline completed successfully."

 But successful execution does not necessarily mean correct business results.

 A better investigation is:

```
Did the pipeline run?
       ↓
Was the data complete?
       ↓
Was the transformation correct?
       ↓
Were the business definitions correct?
       ↓
Does the result match stakeholder expectations?
```

 This demonstrates another important distinction:

 > **Pipeline correctness and business correctness are not necessarily the same thing.**

---

 # Communication as an Engineering Skill

 This lecture changes the way I think about the skill set of a data engineer.

 A simplified view might be:

```
Technical Skills
      +
Data Skills
      +
Business Understanding
      +
Communication
      ↓
Effective Data Engineering
```

 Technical skills allow us to build systems.

 Data skills allow us to work with information.

 Business understanding allows us to understand **why the system matters**.

 Communication allows us to make sure that different stakeholders understand and can use what we build.

---

 # A Stakeholder Communication Framework

 For future projects, I want to separate communication into four layers.

 ## 1\. Context

 What is the business problem?

 > Why are we doing this?

 ## 2\. Outcome

 What will change if the project succeeds?

 > What value will the stakeholder receive?

 ## 3\. Data

 What information is required?

 > What data enables the outcome?

 ## 4\. Technology

 How will we build it?

 > What architecture and tools will satisfy the requirements?

 This gives us:

```
WHY
 ↓
WHAT OUTCOME
 ↓
WHAT DATA
 ↓
HOW
```

 Rather than beginning with the final question.

---

 # Finance Project Documentation Pattern

 For the projects I build throughout this course, I want to capture this reasoning explicitly.

 For example:

 ### Business Problem

 Financial analysts need more timely visibility into transaction activity.

 ### Stakeholder

 Financial analytics team.

 ### Desired Outcome

 Enable analysts to monitor transaction activity throughout the business day.

 ### Data Required

 - Transaction records
- Transaction timestamps
- Account/customer identifiers
- Transaction amounts
- Transaction categories

 ### Functional Requirement

 The system must ingest and make new transaction records available to analysts periodically throughout the day.

 ### Non-Functional Requirements

 The system should consider:

 - Freshness
- Reliability
- Security
- Scalability
- Cost
- Data quality

 ### Technical Solution

 Only now do we decide:

 - Batch vs streaming
- Storage technology
- Processing technology
- Orchestration
- Cloud services
- Data model

 This preserves the connection between the business problem and the technical implementation.

---

 # Key Takeaways

 My main takeaways from this lecture are:

 1. **Data engineers need business context, not just technical skills.**
2. **Data engineering can act as a bridge between business and technology.**
3. **Understanding how information flows through an organization is valuable.**
4. **Communication should be adapted to the stakeholder's technical background.**
5. **Functional stakeholders generally need business outcomes rather than technical implementation details.**
6. **Technical stakeholders may benefit from deeper architectural and engineering discussions.**
7. **The same data system may need to be explained differently to different audiences.**
8. **Business correctness is not necessarily the same as technical pipeline correctness.**
9. **Understanding the meaning of financial data is just as important as moving it through a pipeline.**
10. **A data engineer should be able to explain not only what was built, but why it matters.**

---

 # Reflection

 The previous lectures taught me to start with stakeholders and requirements.

 This lecture adds another layer:

 > **I need to understand the stakeholder well enough to communicate the requirements and proposed solution in a way that makes sense to them.**

 The progression now looks like:

```
Business Context
      ↓
Stakeholders
      ↓
Their Needs
      ↓
Requirements
      ↓
Business + Technical Communication
      ↓
Architecture
      ↓
Implementation
      ↓
Business Value
```

 For my finance-focused projects, I want to make this particularly explicit.

 I don't want the repository to become a collection of:

 > "Here is a Python script that processes financial data."

 Instead, I want each project to answer:

 > **Who needs this data?**

 > **What are they trying to accomplish?**

 > **What does the data mean in its business context?**

 > **What requirements follow from those needs?**

 > **How does the architecture satisfy those requirements?**

 > **What value does the resulting data product provide?**

 ## Data Products Only Create Value When People Can Use Them

 The previous lecture focused on communicating with stakeholders and adapting technical communication to the audience.

 This lecture takes the idea one step further.

 A data product can be technically excellent and still fail to create value if the people who are supposed to use it:

 - Do not understand it
- Do not trust it
- Do not know how to use it
- Do not see how it relates to their work
- Do not feel comfortable working with data

 This is where **data literacy** becomes important.

---

 # What Is Data Literacy?

 In the lecture, data literacy is described as the ability to:

 - Read data
- Work with data
- Analyze data
- Communicate with data

 But an important aspect is **comfort and confidence**.

 The goal is not to turn every employee into a data professional.

 Instead:

 > **People should be sufficiently comfortable with data to use the data products available to them effectively.**

 This creates an important relationship:

```
Good Data Product
       +
Data Literacy
       ↓
Effective Adoption
       ↓
Business Value
```

 Simply producing a dashboard or dataset does not guarantee that people will use it correctly.

---

 # The Adoption Problem

 Imagine that a company spends significant resources building a sophisticated financial analytics dashboard.

 The dashboard provides:

 - Real-time metrics
- Historical trends
- Risk indicators
- Portfolio analytics
- Automated alerts

 Technically, the system works.

 But users don't understand:

 - What the metrics mean
- Where the numbers come from
- How frequently they update
- What assumptions are behind them
- When they should use one metric instead of another

 The result could be poor adoption.

```
Technology
    ↓
Data Product
    ↓
        ┌──────────────────┐
        │ User understands?│
        └────────┬─────────┘
                 │
          ┌──────┴──────┐
          ↓             ↓
         Yes             No
          ↓               ↓
       Adoption        Friction
          ↓               ↓
     Business Value    Low Usage
```

 Therefore, the success of a data product depends on more than its technical implementation.

---

 # Requirements Gathering Is Also Audience Understanding

 One of the strongest points from this lecture is:

 > **Requirements gathering should include understanding the audience for whom the product is being built.**

 This means asking two different questions.

 ### Business-level question

 > What is the organization trying to accomplish?

 ### Audience-level question

 > What is this particular stakeholder trying to accomplish?

 These are related, but they are not necessarily identical.

```
                BUSINESS
                   │
            Overall Objectives
                   │
          ┌────────┼────────┐
          ↓        ↓        ↓
       Finance   Sales   Marketing
          │        │        │
          ↓        ↓        ↓
       Different Stakeholder Needs
```

 A successful data product needs to account for both.

---

 # Stakeholder Personas

 Different stakeholders can have different goals even when they consume the same underlying data.

 For example, consider a financial data platform.

 ### Chief Financial Officer

 May care about:

 - Cash flow
- Revenue
- Costs
- Financial performance
- Forecasting

 ### Chief Risk Officer

 May care about:

 - Exposure
- Risk measures
- Exceptions
- Concentration
- Risk trends

 ### Sales Team

 May care about:

 - Customer activity
- Sales targets
- Customer segmentation
- Pipeline performance

 ### Marketing Team

 May care about:

 - Customer behaviour
- Campaign performance
- Segmentation
- Conversion

 ### Data Scientist

 May care about:

 - Historical data
- Feature availability
- Data quality
- Consistent definitions
- Reproducibility

 The same underlying data infrastructure may support all of them.

 But the **data product and communication layer may need to be different**.

---

 # Finance Example — One Dataset, Multiple Audiences

 Suppose we build a transaction data platform.

 At the core:

```
Transaction Sources
       ↓
Data Pipeline
       ↓
Curated Transaction Dataset
```

 This dataset can then support multiple consumers.

```
                    Curated
                 Transaction Data
                        │
          ┌─────────────┼─────────────┐
          ↓             ↓             ↓
        Risk         Finance        Data Science
      Analytics      Reporting       / ML
          │             │             │
          ↓             ↓             ↓
      Exposure       Revenue       Fraud Model
      Analysis       Analysis      Development
```

 The underlying data may be shared.

 But the **requirements are different**.

---

 # Data Literacy and Financial Data

 Data literacy becomes particularly important in finance because financial metrics often have specific definitions.

 For example:

 - Revenue
- Profit
- Cash flow
- Exposure
- Return
- Volatility
- Volume
- Balance
- Risk

 A user may see a number on a dashboard and assume they understand it.

 But the data engineer should ask:

 > **What exactly does this number represent?**

 For example:

```
Return
  ├── Simple Return?
  ├── Log Return?
  ├── Daily Return?
  ├── Cumulative Return?
  └── Risk-adjusted Return?
```

 The technical pipeline can calculate a number perfectly.

 But if the user interprets the metric differently from its intended definition, the data product can still be misused.

---

 # The Importance of Context

 This reinforces a concept from the previous lecture:

 > **Context is critical.**

 Data without context can be misleading.

 Consider:

```
Metric: 5.2%
```

 By itself, this tells us very little.

 5.2% of what?

 - Return?
- Growth?
- Default rate?
- Error rate?
- Volatility?
- Conversion rate?

 A good data product should therefore provide enough context for the user to interpret the information correctly.

 This may include:

 - Metric definitions
- Time period
- Units
- Source
- Update frequency
- Calculation methodology
- Relevant filters
- Business context

---

 # Adoption Should Be Considered During Design

 A useful lesson from this lecture is that adoption should not be treated as something that happens after the technical implementation.

 Instead:

```
Requirements
     ↓
Audience Understanding
     ↓
Data Product Design
     ↓
Implementation
     ↓
User Adoption
```

 The intended users should influence the design from the beginning.

 For example, if a financial analyst needs to perform ad-hoc analysis, simply providing a static PDF report may not satisfy the real requirement.

 If an executive needs a high-level KPI view, providing raw transaction tables may technically contain all the required information but may not be an effective interface.

---

 # Business Literacy for Data Engineers

 Another major lesson is the importance of **business literacy**.

 The goal is not to become a business executive or salesperson.

 The goal is to understand how the organization operates.

 For a data engineer, this means developing familiarity with concepts such as:

 - Revenue
- Costs
- Profit
- Cash flow
- Customers
- Products
- Operations
- Risk
- KPIs
- Business processes
- Organizational objectives

 In finance, this becomes even more important.

 A finance-focused data engineer should gradually become comfortable with concepts such as:

 - Financial statements
- Transactions
- Assets and liabilities
- Portfolio concepts
- Market data
- Risk
- Returns
- Trading
- Settlement
- Liquidity
- Regulatory considerations

 The objective is not to become a financial analyst.

 It is to understand enough of the domain to build better data systems.

---

 # Data Engineering + Business Literacy

 The relationship can be represented as:

```
              DATA ENGINEERING
                     +
              BUSINESS CONTEXT
                     +
              DATA LITERACY
                     ↓
           Better Data Products
                     ↓
              Better Adoption
                     ↓
              Business Value
```

 This is an important evolution in how I am thinking about the role.

 The data engineer is not simply responsible for the technical movement of information.

 The engineer also needs to understand the environment in which that information will be used.

---

 # Audience Mapping for Future Finance Projects

 For the projects in this repository, I want to explicitly identify the audience.

 A useful template is:

 | Stakeholder | What they care about | Data needed | Expected output |
| --- | --- | --- | --- |
| Finance | Financial performance | Financial transactions | Reports / KPIs |
| Risk | Exposure and risk | Positions / market data | Risk metrics |
| Sales | Customer and sales performance | Customer / transaction data | Sales analytics |
| Marketing | Customer behaviour | Customer activity | Segmentation / campaign analytics |
| Data Science | Historical patterns | Curated historical data | ML datasets |
| Executive | Business KPIs | Aggregated metrics | Executive dashboard |

This is not a fixed list.

 Each project should identify its own actual stakeholders and requirements.

---

 # A Practical Audience Checklist

 Before building a data product, I want to ask:

 ### Who?

 Who will use this?

 ### Why?

 What are they trying to accomplish?

 ### What?

 What information do they need?

 ### How?

 How will they use it?

 ### When?

 How frequently do they need it?

 ### What does success mean?

 What decision or action should the data enable?

 ### What could go wrong?

 How could misunderstanding or misuse of the data lead to a poor decision?

 This final question is especially important for financial applications.

---

 # Finance Example — Risk Dashboard

 Suppose the project is to build a risk dashboard.

 A simplistic requirement might be:

 > "Build a risk dashboard."

 A better requirements conversation would identify:

 ### Audience

 Risk analysts and risk management.

 ### Business Objective

 Monitor portfolio risk and identify significant changes.

 ### Data

 Potentially:

 - Positions
- Market prices
- Security identifiers
- Exposure
- Historical values
- Risk metrics

 ### Functional Requirements

 The system should:

 - Ingest required data
- Calculate required metrics
- Refresh the dashboard
- Provide historical comparisons
- Flag defined anomalies

 ### Non-Functional Requirements

 Consider:

 - Data freshness
- Reliability
- Security
- Auditability
- Performance
- Scalability

 ### Data Literacy Considerations

 Users should understand:

 - What each risk metric means
- How it is calculated
- What period it represents
- When it was last updated
- What thresholds mean
- What assumptions apply

 Now the project is no longer simply:

 > "Build a dashboard."

 It becomes:

 > **Build a data product that allows a defined audience to perform a defined business task using well-understood financial information.**

---

 # Key Takeaways

 My main takeaways from this lecture are:

 1. **Data literacy means being comfortable and confident working with data.**
2. **Data products need adoption to create practical value.**
3. **Requirements gathering should include understanding the audience.**
4. **Different stakeholders can have different objectives even when consuming related data.**
5. **A single data platform may need to serve multiple stakeholder personas.**
6. **Business objectives and individual stakeholder needs should both be considered.**
7. **Financial data requires context because the meaning of a metric is often dependent on its definition and business use.**
8. **Data engineers benefit from developing business literacy without needing to become business specialists.**
9. **User adoption should influence data-product design from the beginning.**
10. **A successful data engineer understands not only how to move data, but how people will use the resulting information.**

---

 # Reflection

 The previous lectures established:

```
Business Goals
      ↓
Stakeholders
      ↓
Requirements
      ↓
Architecture
```

 This lecture adds another dimension:

```
Business Goals
      ↓
Stakeholders
      ↓
Audience Understanding
      ↓
Requirements
      ↓
Data Product
      ↓
Adoption
      ↓
Business Value
```

 This changes how I want to approach the finance projects in this repository.

 I don't want to assume that providing technically correct data automatically means I have created a useful product.

 For every significant project, I want to ask:

 > **Who is the audience?**

 > **What are they trying to accomplish?**

 > **What does the data mean to them?**

 > **What level of data literacy can I assume?**

 > **How should the data product communicate its meaning?**

 > **How will I know whether the product is actually useful?**

Absolutely. I’ll keep the **same README style, structure, depth, and first-person “My Perspective: Applying This to Finance” angle** from your previous lecture, while adapting the AWS concepts into a financial-data-engineering context.

 ## AWS Cloud Infrastructure for Data Engineering

 This lecture introduces the foundational concepts of cloud computing and how AWS provides the infrastructure needed to build modern data systems.

 The central idea is that cloud platforms allow organizations to consume computing resources **on demand**, rather than purchasing and maintaining all of the required infrastructure themselves.

 AWS describes cloud computing as the **on-demand delivery of IT resources over the Internet with pay-as-you-go pricing**.

 This creates a fundamentally different approach to building data systems compared with traditional on-premises infrastructure.

 Instead of purchasing servers, storage systems, and networking equipment in advance, an organization can provision the resources it needs when required and scale them as demand changes.

---

 ## From On-Premises Infrastructure to the Cloud

 Traditionally, organizations would build their own data centers and purchase infrastructure upfront.

 For example, a company might need to purchase:

 - Servers for computation
- Storage systems for data
- Networking equipment
- Database infrastructure
- Backup systems
- Physical facilities
- Hardware maintenance

 This creates a significant challenge because the organization needs to estimate its future capacity requirements.

 If the company purchases too much infrastructure, resources may remain unused.

 If it purchases too little, the infrastructure may become a bottleneck when demand increases.

 Cloud computing changes this model.

```
Traditional Infrastructure

Estimate Future Demand
        ↓
Purchase Hardware
        ↓
Build Data Center
        ↓
Install & Configure
        ↓
Maintain Infrastructure
        ↓
Scale Manually
```

 Compared with:

```
Cloud Infrastructure

Business Requirement
        ↓
Provision Resources
        ↓
Use Resources
        ↓
Scale When Needed
        ↓
Pay for Usage
        ↓
Remove Resources When No Longer Needed
```

 The cloud therefore changes infrastructure from something that organizations primarily **own** into something they can **consume as a service**.

---

 ## The Three Fundamental Infrastructure Resources

 One of the important concepts introduced in this lecture is that many cloud services can be understood through three fundamental infrastructure categories:

 - **Compute**
- **Storage**
- **Networking**

 These three building blocks form the foundation for many data engineering systems.

---

 ## Compute

 Compute resources provide places where code can execute.

 In simple terms:

 > **Compute is where processing happens.**

 AWS provides several different ways to obtain compute resources.

 These include:

 - Virtual machines
- Container hosting
- Serverless functions
- Other managed compute services

 The appropriate choice depends on the requirements of the system.

 For example, a data engineering pipeline might require compute resources to:

 - Process incoming financial data
- Transform raw market data
- Calculate financial metrics
- Run ETL/ELT workloads
- Execute machine-learning workloads
- Validate incoming datasets

 The important point is that compute is not simply about "having a server."

 It is about providing the appropriate processing capacity for the workload.

---

 ## Storage

 Storage is where data is persisted.

 AWS provides multiple storage options, including services such as **Amazon S3** and **Amazon Elastic Block Store (EBS)**, as well as various database services.

 Different storage systems are designed for different requirements.

 For example:

```
Raw Data
   ↓
Object Storage
   ↓
Processed Data
   ↓
Database / Data Warehouse
   ↓
Analytics / ML
```

 In a financial data system, storage could contain:

 - Historical market prices
- Trade records
- Portfolio positions
- Financial statements
- Reference data
- Transaction data
- Risk calculations
- Model outputs
- Alternative data

 This makes storage a particularly important part of financial data engineering because financial systems often need to retain large amounts of historical information.

---

 ## Networking

 Networking provides the connectivity between different resources and external systems.

 In AWS, an important networking concept is the **Amazon Virtual Private Cloud (VPC)**.

 A VPC allows organizations to create a private network within AWS.

 This becomes important when building systems that contain sensitive financial information.

 For example:

```
External Data Source
        ↓
     Internet
        ↓
     AWS Network
        ↓
       VPC
   ┌────┴────┐
   ↓         ↓
Compute    Storage
   ↓         ↓
Database   Data Lake
```

 Networking therefore provides the connectivity required for different components of a data architecture to communicate with each other while also supporting security and isolation.

---

 ## Beyond Compute, Storage, and Networking

 AWS provides many more categories of services beyond these fundamental infrastructure components.

 These include services related to:

 - Security
- Data ingestion
- Data streaming
- Data transformation
- Databases
- Monitoring
- Analytics
- Machine learning
- Application development

 This is important from a data engineering perspective because modern data systems are rarely built using a single technology.

 Instead, engineers combine multiple services together.

```
Data Source
     ↓
Ingestion
     ↓
Storage
     ↓
Transformation
     ↓
Data Warehouse / Lake
     ↓
Analytics / ML
     ↓
Business Users
```

 Each component may be implemented using a different managed cloud service.

---

 ## Scalability and Elasticity

 One of the major advantages of cloud infrastructure is **scalability and elasticity**.

 These concepts are related but slightly different.

 **Scalability** refers to the ability of a system to handle increasing or decreasing workloads.

 **Elasticity** refers to the ability to dynamically adjust resources according to demand.

 For example, imagine a financial data pipeline that normally processes a moderate amount of data during the day but experiences a large increase in activity during market volatility.

 A traditional infrastructure approach might require the company to purchase enough hardware in advance to handle the maximum expected workload.

 With cloud infrastructure, resources can be adjusted according to demand.

```
Normal Demand
     ↓
Smaller Resources
     ↓
Demand Increases
     ↓
More Resources
     ↓
Demand Decreases
     ↓
Reduce Resources
```

 This is particularly useful for financial systems because workloads are not always constant.

 Market activity can change significantly depending on:

 - Trading hours
- Market events
- Economic announcements
- Earnings releases
- Major geopolitical events
- Market volatility
- End-of-day processing

 Cloud elasticity allows infrastructure to respond to these changes more efficiently.

---

 ## The Electricity Analogy

 The lecture compares cloud computing with electricity.

 When using electricity, we generally do not need to know:

 - Where the power was generated
- Which physical equipment generated it
- How the electricity was transported
- How the infrastructure is maintained

 We simply consume the electricity and pay for what we use.

 Cloud computing provides a similar abstraction.

```
Physical Infrastructure
        ↓
      AWS
        ↓
Cloud Services
        ↓
   Our Application
```

 As a data engineer, I can focus more on designing the data system rather than physically managing the underlying data-center infrastructure.

 This is one of the major abstractions provided by cloud computing.

---

 ## AWS Global Infrastructure

 AWS services are hosted in physical data centers distributed around the world.

 However, as users of AWS, we generally interact with this infrastructure through higher-level concepts such as:

 - Regions
- Availability Zones

 This allows engineers to design systems without directly managing individual physical data centers.

---

 ## AWS Regions

 An AWS **Region** represents a geographical area containing multiple Availability Zones.

 Examples include regions associated with locations such as:

 - US East (Northern Virginia)
- Asia Pacific (Mumbai)
- Europe (Frankfurt)

 When deploying AWS resources, the region becomes an important architectural decision.

 The choice of region can affect:

 - Latency
- Data residency
- Availability
- Compliance
- Cost
- Disaster recovery
- Proximity to users and data sources

 This becomes especially important in financial systems because financial data can be subject to regulatory and geographical requirements.

---

 ## Availability Zones

 Each AWS Region contains multiple **Availability Zones (AZs)**.

 An Availability Zone represents a grouping of data centers within a region.

 The architecture can therefore be understood as:

```
AWS Region
│
├── Availability Zone 1
│      ├── Data Center
│      └── Data Center
│
├── Availability Zone 2
│      ├── Data Center
│      └── Data Center
│
└── Availability Zone 3
       ├── Data Center
       └── Data Center
```

 The separation between Availability Zones is designed to reduce the impact of failures.

 For example, if an issue affects one Availability Zone, workloads can potentially fail over to another Availability Zone.

 This provides an important foundation for building **highly available and resilient systems**.

---

 ## Reliability and Fault Tolerance

 This concept is particularly relevant to financial systems.

 Imagine a system responsible for processing:

 - Trading data
- Portfolio positions
- Risk calculations
- Transaction records

 If the infrastructure supporting the system fails, the consequences could be significant.

 Therefore, data engineers need to think about:

 - Availability
- Redundancy
- Fault tolerance
- Disaster recovery
- Backup
- Recovery time
- Recovery point

 AWS regions and Availability Zones provide infrastructure that can be used to design systems with greater resilience.

 The important architectural principle is:

 > **Do not assume that individual infrastructure components will never fail. Design the system so that failures can be handled.**

---

 ## AWS Global Network

 AWS connects its infrastructure through a global network of high-speed links.

 This allows different facilities and Availability Zones to communicate with each other with low latency.

 From a data engineering perspective, this network becomes part of the underlying infrastructure that allows different components of a data platform to work together.

 For example:

```
Data Ingestion
      ↓
Processing
      ↓
Storage
      ↓
Database
      ↓
Analytics
```

 Each component may be deployed in different infrastructure locations while still communicating through the cloud network.

---

 ## AWS as Building Blocks

 One of the ideas I find particularly useful from this lecture is to think of AWS services as **building blocks**.

 A data engineer rarely uses one AWS service in isolation.

 Instead, multiple services can be combined to create a complete data system.

 For example:

```
External Financial Data
        ↓
   Data Ingestion
        ↓
     Amazon S3
        ↓
   Transformation
        ↓
 Data Warehouse / Lake
        ↓
 Analytics / ML
        ↓
 Financial Insights
```

 The specific AWS services can change depending on the requirements.

 The architecture should therefore come first, while the individual services are selected based on what the system needs.

 This connects directly to the previous lecture's principle:

```
Problem
   ↓
Requirements
   ↓
Architecture
   ↓
Technology Selection
   ↓
Implementation
```

---

 ## My Perspective: Applying This to Financial Modelling

 This is where I see a strong connection between data engineering and financial modelling.

 A financial model is often treated primarily as a mathematical or analytical problem.

 However, the quality of a financial model depends heavily on the quality of the data feeding it.

 For example, suppose I want to build a portfolio-risk model.

 The model might require:

 - Historical prices
- Corporate actions
- Trading volumes
- Portfolio positions
- Security identifiers
- Interest rates
- FX rates
- Economic indicators
- Company fundamentals

 The modelling layer is only one part of the overall system.

 A more complete architecture could look like:

```
Financial Data Sources
        ↓
Data Ingestion
        ↓
Raw Data Storage
        ↓
Data Validation
        ↓
Data Transformation
        ↓
Curated Financial Dataset
        ↓
Feature Engineering
        ↓
Financial Model
        ↓
Risk / Return Analytics
        ↓
Decision Making
```

 This makes it clear that **financial modelling and data engineering are closely connected**.

 A sophisticated model cannot compensate for unreliable or poorly managed input data.

---

 ## Example: Building a Market Data System

 Imagine I want to build a system that collects daily stock-market data.

 The system might receive:

```
Ticker
Date
Open
High
Low
Close
Volume
Adjusted Close
```

 Instead of putting everything directly into a database, I could design a layered architecture.

 ### Raw Layer

 Store the original data exactly as received.

```
Raw Market Data
      ↓
Amazon S3
```

 ### Processing Layer

 Validate and transform the data.

 Examples:

 - Check missing prices
- Validate ticker symbols
- Standardize dates
- Handle duplicates
- Adjust data types
- Apply corporate-action adjustments

```
Raw Data
   ↓
Validation
   ↓
Transformation
```

 ### Curated Layer

 Produce a clean dataset suitable for analytics and modelling.

```
Clean Market Data
       ↓
Financial Features
       ↓
Models
```

 This separation is useful because it preserves the original data while allowing the processed datasets to evolve.

---

 ## Why Cloud Infrastructure Matters for Financial Modelling

 Financial datasets can grow significantly over time.

 For example, a research platform may eventually contain:

 - Decades of historical prices
- Thousands of securities
- Intraday market data
- Fundamental datasets
- Economic data
- Alternative datasets
- Millions or billions of records

 The infrastructure needs to support this growth.

 Cloud systems provide several useful properties:

 - Elastic storage
- Scalable computation
- Managed networking
- High availability
- Geographic distribution
- Integration between services
- Pay-as-you-go infrastructure

 This means I can start with a relatively small financial-data project and potentially scale the architecture as the dataset and workload grow.

---

 ## Infrastructure Decisions Become Financial Decisions

 Another important connection I see is that infrastructure decisions can directly affect the economics of a financial modelling system.

 For example:

 > How much data should be stored?

 > How frequently should data be processed?

 > Should computation happen in real time or in batches?

 > How long should historical data be retained?

 > Where should the data be stored?

 > How much redundancy is required?

 These are not purely technical questions.

 They involve trade-offs between:

 - Cost
- Performance
- Reliability
- Accuracy
- Latency
- Complexity
- Regulatory requirements

 This reinforces the idea from the previous lecture that data engineering is fundamentally about **requirements and trade-offs**, not simply choosing technologies.

---

 ## A Financial Data Engineering Architecture

 Combining the concepts from this lecture with my financial-modelling objective, I can think about a simplified cloud architecture like this:

```
                 Financial Data Sources
                          │
                          ▼
                   Data Ingestion
                          │
                          ▼
                  ┌───────────────┐
                  │   Raw Layer   │
                  │   Amazon S3   │
                  └───────┬───────┘
                          │
                          ▼
                    Data Processing
                          │
                          ▼
                  ┌───────────────┐
                  │ Curated Data  │
                  └───────┬───────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
        Analytics     Financial ML   Reporting
             │            │            │
             └────────────┼────────────┘
                          ▼
                    Business Decisions
```

 This architecture is still intentionally high level.

 The goal at this stage is not to memorize every AWS service.

 Instead, I want to understand **how infrastructure components fit together to support a data system**.

---

 ## From Physical Infrastructure to Financial Insights

 One of the biggest takeaways from this lecture is the number of abstraction layers involved in a modern data platform.

```
Physical Data Centers
        ↓
AWS Regions
        ↓
Availability Zones
        ↓
Cloud Infrastructure
        ↓
AWS Services
        ↓
Data Pipelines
        ↓
Data Products
        ↓
Financial Models
        ↓
Business Decisions
```

 As a data engineer, I may not directly interact with the physical data centers.

 Instead, I work with the abstractions provided by the cloud platform.

 This allows me to focus on designing systems that reliably transform raw data into useful information.

---

 ## Key Takeaways

 The main concepts I want to retain from this lecture are:

 - Cloud computing provides IT resources on demand.
- AWS follows a pay-as-you-go model.
- Compute provides processing capacity.
- Storage provides persistent data storage.
- Networking connects systems and resources.
- Cloud infrastructure provides scalability and elasticity.
- AWS organizes infrastructure into Regions and Availability Zones.
- Multiple Availability Zones can improve system resilience.
- AWS services can be combined as building blocks to create data systems.
- Infrastructure decisions should be driven by system requirements.
- Cloud architecture is particularly useful for growing financial datasets and workloads.
- Financial modelling depends not only on models but also on reliable data infrastructure.

---

 ## Connecting This Lecture to the Previous One

 The previous lecture introduced the principle:

 > **Problem → Requirements → Architecture → Tool → Implementation**

 This lecture adds another layer to that thinking.

 Once the architecture has been defined, cloud platforms such as AWS provide the infrastructure building blocks required to implement it.

 Therefore, I see the progression as:

```
Business Problem
      ↓
Stakeholder Requirements
      ↓
Data Requirements
      ↓
System Requirements
      ↓
Architecture
      ↓
Cloud Infrastructure
      ↓
AWS Services
      ↓
Data Pipelines
      ↓
Reliable Data
      ↓
Financial Models
      ↓
Business Decisions
```

 This is the connection I want to maintain throughout the rest of the course.

 I am not learning AWS simply to learn AWS services.

 I am learning cloud infrastructure as a way to **design, build, and operate reliable data systems**, and eventually apply those systems to financial modelling and analytics.

---

 ## What I Want to Carry Forward

 The most important mindset shift from this lecture is:

 > **Cloud infrastructure is not the end goal. It is an abstraction that allows us to build scalable and reliable data systems.**

 For my financial-data projects, I therefore want to avoid approaching AWS as a collection of services that I simply need to memorize.

 Instead, I want to understand:

```
What does the financial problem require?
              ↓
What data does the system need?
              ↓
How should that data flow?
              ↓
What architecture supports that flow?
              ↓
Which cloud services provide the required capabilities?
              ↓
How can the system scale reliably?
```

 This brings the technical infrastructure back to the original purpose:

 > **Turning data into reliable information that can support financial analysis, modelling, and decision-making.**

 ## Core AWS Services for Data Engineering

 The services are organized into five broad categories:

 - Compute
- Networking
- Storage
- Databases
- Security

 The important thing for me is not to memorize these services individually.

 Instead, I want to understand **what capability each service provides and where it fits into a larger data architecture**.

---

 ## The Five Core AWS Categories

 A simplified view of the AWS services introduced in this lecture is:

```
                    AWS Cloud
                        │
        ┌───────────────┼───────────────┐
        ↓               ↓               ↓
     Compute         Network         Storage
        │               │               │
       EC2             VPC              S3
     Lambda                            EBS
     ECS/EKS                            EFS
        │
        └───────────────┬───────────────┘
                        ↓
                    Databases
                        │
                       RDS
                    Redshift
                        │
                        ↓
                    Security
                        │
              Shared Responsibility
```

 These categories provide a useful mental model for understanding how different AWS services contribute to a complete system.

---

 ## Compute — Where Processing Happens

 The first category is **compute**.

 Compute resources provide the environment where code executes.

 The main service introduced in this lecture is **Amazon Elastic Compute Cloud (EC2)**.

 EC2 provides virtual machines, or VMs, in the AWS Cloud.

 A virtual machine can be thought of as a virtual computer or server.

```
EC2 Instance
     │
     ├── Operating System
     │
     ├── Applications
     │
     ├── Libraries
     │
     └── Data Processing
```

 When I create an EC2 instance, I have significant control over the environment.

 I can control:

 - The operating system
- Installed applications
- Software dependencies
- Networking configuration
- Processing workloads
- Other aspects of the virtual machine

 This makes EC2 a very flexible compute option.

---

 ## EC2 in Data Engineering

 An EC2 instance can be used for many different workloads.

 For example:

 - Development environments
- Web servers
- Data-processing applications
- Container workloads
- Machine-learning workloads
- Custom data pipelines

 A data engineer could potentially use EC2 to run a Python-based financial-data processing application.

```
Financial Data
      ↓
EC2 Instance
      ↓
Python Processing
      ↓
Validation / Transformation
      ↓
Processed Data
```

 EC2 can also be deployed as a fleet of machines.

 Instead of using one large machine, multiple instances can be used to distribute workloads.

 This is known as **horizontal scaling**.

```
             Incoming Workload
                    ↓
          ┌─────────┼─────────┐
          ↓         ↓         ↓
        EC2-1     EC2-2     EC2-3
          │         │         │
          └─────────┼─────────┘
                    ↓
             Processed Data
```

 This becomes useful when data-processing workloads increase.

---

 ## Other Compute Options

 EC2 is not the only way to perform computation on AWS.

 The lecture also introduces:

 - **AWS Lambda**
- **Amazon Elastic Container Service (ECS)**
- **Amazon Elastic Kubernetes Service (EKS)**

 These services represent different approaches to running applications.

 ### AWS Lambda

 Lambda provides a serverless execution model.

 Instead of managing a virtual machine directly, I can deploy code that executes in response to an event or trigger.

```
Event
  ↓
Lambda Function
  ↓
Processing
  ↓
Output
```

 This can be useful for event-driven data processing.

 For example:

```
New Financial File
        ↓
S3 Event
        ↓
Lambda
        ↓
Validate File
        ↓
Trigger Pipeline
```

 This architecture can be useful when processing tasks need to happen automatically when new data arrives.

---

 ## Containers: ECS and EKS

 The lecture also introduces container-based compute.

 Containers provide a way to package an application together with its dependencies so that it can run consistently across environments.

 AWS provides services such as:

 - Amazon ECS
- Amazon EKS

 These can be useful when data-processing applications become more complex and need containerized deployment.

 For example, a financial modelling application could be packaged into a container:

```
Financial Model
      +
Python
      +
Libraries
      +
Dependencies
      ↓
   Container
      ↓
 AWS Compute
```

 This provides another level of abstraction between the application and the underlying infrastructure.

---

 ## Networking — Amazon VPC

 Whenever I create an EC2 instance or many other AWS resources, those resources need to exist within a network.

 AWS provides **Amazon Virtual Private Cloud (VPC)** for this purpose.

 A VPC is essentially a private network within AWS that I can configure and control.

```
AWS Region
│
└── VPC
     │
     ├── Subnet
     │    ├── EC2
     │    └── Database
     │
     └── Subnet
          ├── Application
          └── Processing
```

 A VPC allows me to control how resources communicate with each other and with external systems.

---

 ## Subnets

 A VPC can be divided into smaller networks called **subnets**.

 This allows different resources to be organized into different parts of the network.

 For example:

```
VPC
│
├── Public Subnet
│      └── Application
│
└── Private Subnet
       ├── Database
       └── Processing
```

 This type of network segmentation becomes particularly important for systems handling sensitive financial information.

 I would not necessarily want every component of a financial data platform to be directly accessible from the public internet.

---

 ## Regions and Data Residency

 One important concept from this lecture is that many AWS resources are **region-bound**.

 A VPC exists within a particular AWS Region.

 Therefore:

```
Region: Mumbai
       │
       └── VPC
            ├── Subnet
            ├── EC2
            └── Database
```

 If I want to operate in another region, I generally need to create the required infrastructure there as well.

 Data and resources do not automatically move between regions.

 This has an important implication for financial systems.

 Data location can matter because organizations may have requirements related to:

 - Data residency
- Compliance
- Privacy
- Regulatory requirements
- Security
- Latency

 Therefore, choosing an AWS Region is not simply a technical decision.

 It can become a **business and regulatory decision**.

---

 # Storage

 The next major category is **storage**.

 AWS provides different storage models for different requirements.

 The lecture introduces three important types:

 - Object storage
- Block storage
- File storage

 These are different abstractions for storing data.

---

 ## Object Storage

 Object storage is designed for storing objects such as:

 - Documents
- Logs
- Images
- Videos
- Data files
- Raw datasets

 AWS's primary object-storage service is **Amazon S3**.

 S3 is particularly important for data engineering because it can serve as the foundation of a data lake.

```
                 Amazon S3
                     │
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
    Raw Data     Processed Data   Logs
       │             │
       ↓             ↓
   Historical     Analytics
     Data            Data
```

 For my financial-data projects, S3 could potentially store:

 - Historical stock prices
- Intraday market data
- Financial statements
- Economic datasets
- Transaction files
- Model outputs
- Raw API responses

 This makes object storage particularly useful for maintaining a centralized historical data layer.

---

 ## Block Storage

 Block storage works differently from object storage.

 It is commonly used where low latency and high performance are important.

 AWS provides **Amazon Elastic Block Store (EBS)** volumes that can be attached to EC2 instances.

```
EC2 Instance
     │
     ↓
EBS Volume
     │
     ↓
Operating System / Applications
```

 From a financial-modelling perspective, block storage could be useful when a processing application running on EC2 needs high-performance storage.

 For example:

```
EC2
 │
 ├── Python Application
 │
 ├── Financial Model
 │
 └── EBS
       ↓
  Local Processing Data
```

---

 ## File Storage

 The third storage model is **file storage**.

 File storage organizes information into files and directories, similar to the filesystem on a personal computer.

 AWS provides **Amazon Elastic File System (EFS)** as a managed file-storage service.

 The important distinction is:

```
Object Storage
       ↓
Objects / Files

Block Storage
       ↓
Disk-like storage

File Storage
       ↓
Files + Directories
```

 Different storage models therefore solve different problems.

---

 # Databases

 The next category is **databases**.

 At first glance, databases might appear to be another form of storage.

 However, databases provide additional functionality for working with structured data.

 They provide capabilities such as:

 - Querying
- Indexing
- Data organization
- Transactions
- Structured data management

 This makes databases different from simply storing files.

---

 ## Relational Databases

 A relational database stores structured data using tables.

 For example, a financial dataset could look like:

```
Trades
--------------------------------
trade_id
security_id
trade_date
quantity
price
portfolio_id
```

 Another table might contain security information:

```
Securities
--------------------------------
security_id
ticker
company_name
sector
currency
```

 These tables can be related to each other using keys.

 This relational model is extremely important in financial systems because financial data is often highly structured.

---

 ## Amazon RDS

 The lecture introduces **Amazon Relational Database Service (RDS)**.

 RDS is a managed relational database service.

 Instead of manually managing all of the underlying database infrastructure, AWS manages many of the operational components.

 A simplified architecture is:

```
Application
     ↓
Amazon RDS
     ↓
Relational Database
     ↓
Structured Financial Data
```

 RDS could potentially be used for:

 - Transactional financial applications
- Reference data
- User information
- Portfolio metadata
- Security master data
- Application databases

---

 # Amazon Redshift

 Another important service introduced is **Amazon Redshift**.

 Redshift is a cloud data warehouse designed for analytical workloads.

 This distinction is important.

 A relational database might support operational applications, while a data warehouse is typically designed for analytics across large datasets.

```
Operational Systems
        ↓
      RDS
        ↓
   Data Pipeline
        ↓
    Redshift
        ↓
 Analytics / BI / Models
```

 In a financial environment, Redshift could potentially be used to analyze large amounts of:

 - Historical market data
- Trading activity
- Portfolio performance
- Risk data
- Customer activity
- Financial metrics

 This gives me an important conceptual distinction:

```
RDS
↓
Operational / Structured Application Data

Redshift
↓
Analytical / Data Warehouse Workloads
```

---

 # Storage vs Database vs Data Warehouse

 One of the useful lessons from this lecture is that not every piece of data should automatically go into a database.

 Different layers serve different purposes.

 A simplified architecture could be:

```
Raw Financial Data
       ↓
      S3
       ↓
Data Transformation
       ↓
   Redshift
       ↓
 Analytics
       ↓
Financial Models
```

 Meanwhile, operational information might be stored separately:

```
Financial Application
       ↓
      RDS
       ↓
Operational Data
```

 This distinction will become increasingly important as the course moves toward more complex architectures.

---

 # Security — The Shared Responsibility Model

 The final category introduced in this lecture is **security**.

 AWS follows what is called the **Shared Responsibility Model**.

 The core idea is:

 > **AWS is responsible for security of the cloud, while the customer is responsible for security in the cloud.**

 This distinction is extremely important.

 AWS is responsible for securing the underlying infrastructure.

 The customer is responsible for securely configuring and using the services.

---

 ## The Apartment Building Analogy

 The lecture uses an apartment building as an analogy.

 Imagine that AWS operates a large apartment building.

 The building owner is responsible for:

 - The physical structure
- Building infrastructure
- Physical security
- Core facilities

 The tenant is responsible for:

 - Locking their apartment
- Controlling access
- Protecting their belongings
- Using the security features correctly

 The same idea applies to AWS.

```
AWS Responsibility
        ↓
Physical Infrastructure
        ↓
Data Centers
        ↓
Networking Infrastructure
        ↓
Hypervisor
        ↓
Customer Responsibility
        ↓
Operating System
        ↓
Applications
        ↓
Network Configuration
        ↓
Data Access
        ↓
Encryption
```

 The exact boundary changes depending on the AWS service being used.

---

 # Shared Responsibility in EC2

 EC2 provides a useful example.

 AWS manages the underlying infrastructure, including:

 - Physical hardware
- Data centers
- Facilities
- Underlying infrastructure
- Hypervisor layer

 But once I create an EC2 instance, I become responsible for many aspects of the environment.

 For example:

 - Operating-system management
- Software updates
- Security patches
- Network configuration
- Firewall rules
- Access control
- Data protection
- Encryption where required

 Therefore:

```
AWS
 ↓
Secures the Cloud

Customer
 ↓
Secures Resources Within the Cloud
```

 Security is therefore not something I can simply delegate to AWS.

---

 # My Perspective: Applying This to Financial Modelling

 This lecture makes the connection between **financial modelling and cloud infrastructure** even clearer.

 Suppose I want to build a financial modelling platform.

 The system could contain:

```
Market Data APIs
       ↓
     Amazon S3
       ↓
Data Processing
       ↓
   Redshift
       ↓
Feature Engineering
       ↓
Financial Model
       ↓
Risk / Return Analysis
```

 But now security has to exist across the entire architecture.

 For example:

 - Who can access the raw market data?
- Who can modify processed datasets?
- Who can access portfolio information?
- Which applications can access the database?
- Which resources should be publicly accessible?
- Which resources should remain inside private subnets?
- How should sensitive data be encrypted?
- How should credentials and permissions be managed?

 These questions show that **data engineering is inseparable from security**.

---

 # Example: Financial Data Platform on AWS

 I can now combine the services introduced in this lecture into a more concrete architecture.

```
                  Financial Data Sources
                           │
                           ▼
                    Data Ingestion
                           │
                           ▼
                    ┌────────────┐
                    │    S3      │
                    │ Raw Data   │
                    └─────┬──────┘
                          │
                          ▼
                    Data Processing
                     EC2 / Lambda
                          │
                          ▼
                    Curated Data
                          │
                          ▼
                    ┌────────────┐
                    │ Redshift   │
                    │ Warehouse  │
                    └─────┬──────┘
                          │
              ┌───────────┼───────────┐
              ↓           ↓           ↓
          Analytics    Modelling    Reporting
              │           │           │
              └───────────┼───────────┘
                          ↓
                  Financial Decisions
```

 Alongside this architecture:

```
VPC
│
├── Network Isolation
├── Subnets
├── Security Controls
└── Resource Connectivity
```

 And across the entire system:

```
Security
    ↓
Identity
    ↓
Access Control
    ↓
Encryption
    ↓
Network Security
    ↓
Data Protection
```

 This is beginning to look much more like a real financial data platform than simply a collection of AWS services.

---

 # Choosing the Right AWS Service

 Another important lesson from this lecture is that there is no single AWS service that solves every problem.

 The appropriate service depends on the requirement.

 For example:

 | Requirement | Possible AWS Service |
| --- | --- |
| Virtual machine | EC2 |
| Event-driven code | Lambda |
| Container workloads | ECS / EKS |
| Object storage | S3 |
| VM-attached storage | EBS |
| Shared file storage | EFS |
| Relational database | RDS |
| Analytical warehouse | Redshift |
| Private cloud network | VPC |

This is why I should avoid thinking:

 > "I need to learn AWS."

 Instead, I should think:

 > **"I need to understand which AWS capability solves which system requirement."**

---

 # Connecting This Lecture to the Data Engineering Lifecycle

 The previous lectures introduced the importance of starting with business and stakeholder requirements.

 This lecture shows how those requirements eventually translate into concrete cloud services.

```
Business Requirement
        ↓
Data Requirement
        ↓
System Requirement
        ↓
Architecture
        ↓
AWS Service Selection
        ↓
Implementation
```

 For example:

 > "We need to store years of historical financial data and run analytical queries on it."

 This might lead to:

```
Requirement
    ↓
Large-scale historical storage
    ↓
S3

Requirement
    ↓
Analytical querying
    ↓
Redshift
```

 Another requirement:

 > "We need an application database for structured portfolio information."

 Could lead to:

```
Requirement
    ↓
Relational operational database
    ↓
RDS
```

 Another:

 > "We need a private environment for processing sensitive data."

 Could lead to:

```
Requirement
    ↓
Network isolation
    ↓
VPC + Subnets + Security Controls
```

 This demonstrates the importance of requirements-driven architecture.

---

 # The Bigger Picture

 I am beginning to see AWS not as a collection of unrelated products, but as a set of infrastructure building blocks.

```
                    AWS
                     │
      ┌──────────────┼──────────────┐
      ↓              ↓              ↓
   Compute         Storage        Network
      │              │              │
   EC2/Lambda       S3/EBS/EFS      VPC
      │              │              │
      └──────────────┼──────────────┘
                     ↓
                  Databases
                     │
                  RDS/Redshift
                     ↓
                  Data Platform
                     ↓
             Financial Analytics
                     ↓
              Financial Models
                     ↓
              Business Decisions
```

 The services themselves are not the final objective.

 They provide the infrastructure required to build reliable systems.

---

 # What I Want to Remember

 The most important concepts I want to retain from this lecture are:

 - EC2 provides virtual machines for flexible compute workloads.
- Lambda provides serverless, event-driven computation.
- ECS and EKS provide container-based compute options.
- VPC provides private networking within AWS.
- Subnets allow networks to be segmented.
- AWS resources are often region-bound.
- Region selection can matter for compliance, security, latency, and data residency.
- S3 provides object storage and is particularly important for data engineering.
- EBS provides block storage that can be attached to EC2.
- EFS provides managed file storage.
- RDS provides managed relational databases.
- Redshift provides a cloud data warehouse for analytical workloads.
- AWS follows the Shared Responsibility Model for security.
- AWS secures the underlying cloud infrastructure.
- Customers are responsible for securely configuring and using their AWS resources.
- AWS services should be selected based on requirements rather than familiarity or popularity.

---

 # My Financial Engineering Mental Model

 After these AWS lectures, I want to maintain the following mental model for my financial-data projects:

```
                 BUSINESS PROBLEM
                        ↓
              Stakeholder Requirements
                        ↓
                 Data Requirements
                        ↓
                System Requirements
                        ↓
                    ARCHITECTURE
                        ↓
          ┌─────────────┼─────────────┐
          ↓             ↓             ↓
       Compute       Storage       Networking
          ↓             ↓             ↓
     EC2/Lambda        S3            VPC
          │             │             │
          └─────────────┼─────────────┘
                        ↓
                    Databases
                        ↓
                   RDS / Redshift
                        ↓
                 Data Processing
                        ↓
                Financial Features
                        ↓
                Financial Models
                        ↓
              Risk / Return Analysis
                        ↓
                 Business Decisions
```

 And across every layer:

```
                SECURITY
                   │
        ┌──────────┼──────────┐
        ↓          ↓          ↓
     Access     Network    Encryption
     Control    Security    & Data
                           Protection
```

 This gives me a more complete understanding of what it means to build a financial data system.

 I am not simply learning **AWS services**.

 I am learning how to use cloud infrastructure to turn raw financial data into **reliable, secure, scalable, and usable data products** that can eventually support financial modelling and decision-making.

---

 ## From Learning Services to Designing Systems

 The progression across these lectures is becoming clearer.

 The first lectures focused on understanding the **problem and requirements**.

 The previous AWS lecture introduced the **cloud infrastructure model**.

 This lecture introduces the **specific building blocks** available within that infrastructure.

 So the progression is:

```
Understand the Problem
        ↓
Understand Requirements
        ↓
Understand Cloud Infrastructure
        ↓
Understand AWS Services
        ↓
Combine Services into Architecture
        ↓
Build Data Pipelines
        ↓
Create Reliable Data
        ↓
Apply Financial Models
```

 The next step in my learning should therefore not be simply memorizing more AWS services.

 It should be learning how these services are **combined into real data-engineering architectures and pipelines**.

 ## Networking — VPC, IP Addresses & Subnets

 Networking is another fundamental building block of cloud infrastructure.

 In the previous lectures, I learned that a data system is usually composed of multiple resources:

 - Compute
- Storage
- Databases
- Processing systems
- Applications
- External data sources

 These resources need to communicate with each other.

 For example:

```
Data Source
    ↓
Ingestion
    ↓
Processing
    ↓
Storage
    ↓
Database
    ↓
Financial Model
```

 All of these components require some form of network communication.

 This lecture therefore introduces some of the fundamental concepts behind cloud networking:

 - Networks
- IP addresses
- IPv4
- CIDR notation
- Virtual Private Cloud (VPC)
- Subnets
- Public and private resources

---

 ## What Is a Network?

 At the simplest level, a network is a collection of devices that can communicate with each other.

 Communication generally happens through requests and responses.

```
Device A
   │
   │ Request
   ↓
Device B
   │
   │ Response
   ↓
Device A
```

 In a cloud environment, the devices are not necessarily physical computers sitting next to each other.

 They can be:

 - Virtual machines
- Databases
- Applications
- Storage systems
- Containers
- Cloud services

 The network provides the communication layer connecting these components.

---

 ## Why Networking Matters in Data Engineering

 A data pipeline rarely consists of a single component.

 Consider a financial data pipeline:

```
Market Data API
      ↓
Ingestion Service
      ↓
Processing
      ↓
Storage
      ↓
Database
      ↓
Financial Model
```

 Each component may need to communicate with another component.

 For example:

```
EC2
 ↓
Database

Application
 ↓
API

Processing
 ↓
S3

Analytics
 ↓
Data Warehouse
```

 Therefore, networking determines **who can communicate with whom and how that communication happens**.

 This makes networking both a technical and security concern.

---

 # IP Addresses

 To communicate across a network, devices need an address.

 This is where an **IP address** comes in.

 An IP address is used to identify a device within a network.

 A simplified example is:

```
192.101.0.2
```

 The purpose is similar to an address in the physical world.

 If I want to send something to a particular house, I need an address.

 Similarly, if one device wants to communicate with another device, it needs to know where that device is located on the network.

```
Device A
192.101.0.1
      │
      │ Request
      ↓
Device B
192.101.0.2
```

 The network uses these addresses to route communication to the appropriate destination.

---

 ## IPv4 Addresses

 One of the most common versions of the Internet Protocol is **IPv4**.

 IPv4 addresses are represented using four numbers separated by dots:

```
x.x.x.x
```

 Each section can contain a value between:

```
0 → 255
```

 For example:

```
192.101.0.2
```

 is a valid IPv4 address.

 Technically, an IPv4 address is a **32-bit number**.

```
32 bits
   ↓
8 bits . 8 bits . 8 bits . 8 bits
   ↓
192 . 101 . 0 . 2
```

 Understanding IPv4 is useful because cloud networking requires us to define ranges of IP addresses for our networks.

---

 # CIDR Notation

 One of the concepts introduced in this lecture that initially looks confusing is **CIDR — Classless Inter-Domain Routing**.

 CIDR notation provides a way to describe a **range of IP addresses**.

 For example:

```
192.101.0.0/24
```

 The `/24` indicates that the first 24 bits are fixed.

 Since IPv4 contains 32 bits:

```
32 - 24 = 8
```

 This leaves 8 bits available for addresses within the range.

 Therefore:

```
192.101.0.0/24
```

 represents the range:

```
192.101.0.0
       ↓
192.101.0.255
```

 This gives us 256 possible addresses in the theoretical address range.

---

 ## Why CIDR Matters

 CIDR becomes important when designing a cloud network because I need to decide:

 > **How many IP addresses should my network be able to contain?**

 For example, I might create a VPC using:

```
10.0.0.0/16
```

 and then divide that larger network into smaller networks.

```
10.0.0.0/16
      │
      ├── 10.0.1.0/24
      ├── 10.0.2.0/24
      ├── 10.0.3.0/24
      └── ...
```

 This gives me a way to organize and allocate IP addresses efficiently.

---

 # What Is a VPC?

 A **Virtual Private Cloud (VPC)** is an isolated private network within AWS.

 It provides the network environment in which I can launch and organize AWS resources.

 A useful mental model is to think of a VPC as a **protected network boundary** around my cloud resources.

```
                 AWS Region
                     │
              ┌──────────────┐
              │     VPC      │
              │              │
              │   EC2        │
              │   Database   │
              │   Processing │
              │   Storage    │
              │              │
              └──────────────┘
```

 The VPC allows me to define how resources communicate with each other and how they interact with external networks.

---

 ## VPC and AWS Regions

 A VPC exists within a particular AWS Region.

 For example:

```
AWS Region
│
└── VPC
    │
    ├── Availability Zone A
    ├── Availability Zone B
    └── Availability Zone C
```

 A VPC can span multiple Availability Zones within the same Region.

 However, it does not span multiple AWS Regions.

 If I want a network in another Region, I would create a separate VPC there.

 This connects directly to the previous lecture's discussion of AWS Regions and data residency.

---

 # VPC as a Network Boundary

 One of the most useful ways I understand a VPC is as a **network boundary**.

 Imagine a financial-data platform containing:

```
Financial Data Platform
│
├── Data Processing
├── Database
├── Data Warehouse
├── Applications
└── Financial Models
```

 I don't necessarily want all of these resources to be directly exposed to the public internet.

 Instead, I can place them inside a VPC and control how traffic flows.

```
                    Internet
                       │
                       X
                       │
                ┌──────────────┐
                │     VPC      │
                │              │
                │  Resources   │
                │              │
                └──────────────┘
```

 The VPC therefore provides an important layer of isolation.

---

 # VPC CIDR Block

 When creating a VPC, I need to define its IP address range.

 This is done using a **CIDR block**.

 For example:

```
VPC CIDR
10.0.0.0/16
```

 This defines the overall IP address space available inside the VPC.

 Resources created within the VPC can then receive IP addresses from this range.

```
VPC
10.0.0.0/16
      │
      ├── Resource → 10.0.x.x
      ├── Resource → 10.0.x.x
      └── Resource → 10.0.x.x
```

 The VPC CIDR therefore defines the size of the network.

---

 # What Is a Subnet?

 A VPC can be divided into smaller networks called **subnets**.

 I can think of a subnet as a smaller network inside the larger VPC.

```
VPC
│
├── Subnet A
│
├── Subnet B
│
└── Subnet C
```

 Each subnet receives its own CIDR block.

 The subnet CIDR must be a subset of the VPC's CIDR range.

 For example:

```
VPC
10.0.0.0/16
│
├── Subnet A
│   10.0.1.0/24
│
├── Subnet B
│   10.0.2.0/24
│
└── Subnet C
    10.0.3.0/24
```

 This allows me to divide the larger network into logical sections.

---

 # Why Use Subnets?

 The main reason to use subnets is to provide **more granular control over resources and network access**.

 Not every resource in a system needs the same level of exposure.

 For example:

```
                    VPC
                     │
           ┌─────────┴─────────┐
           ↓                   ↓
     Public Subnet        Private Subnet
           │                   │
           ↓                   ↓
      Application          Database
                              │
                              ↓
                         Financial Data
```

 The application might need to communicate with the outside world.

 The database might not need direct public access.

 This separation improves the architecture and provides an additional layer of security.

---

 # Public vs Private Subnets

 A simplified way to think about the two types is:

 ### Public Subnet

 A public subnet can contain resources that need connectivity to the outside world.

 For example:

```
Internet
   ↓
Public Subnet
   ↓
Application
```

 ### Private Subnet

 A private subnet is used for resources that should not be directly accessible from the public internet.

 For example:

```
Public Application
       ↓
Private Subnet
       ↓
Database
```

 This creates a useful separation between externally accessible components and internal components.

---

 # Financial Data Example

 This distinction becomes particularly important when thinking about financial systems.

 Imagine a portfolio-management application.

 I might have:

```
                Internet
                   │
                   ↓
             Public Subnet
                   │
              Application
                   │
                   ↓
            Private Subnet
                   │
                Database
                   │
                   ↓
             Financial Data
```

 The application needs to receive requests from users.

 However, the underlying portfolio database does not necessarily need to be exposed directly to the internet.

 Therefore, separating these components into different network areas reduces unnecessary exposure.

---

 # Subnets and Availability Zones

 Subnets are associated with Availability Zones.

 A simplified architecture could look like:

```
AWS Region
│
└── VPC
     │
     ├── Availability Zone A
     │      └── Subnet A
     │
     └── Availability Zone B
            └── Subnet B
```

 This allows resources to be distributed across Availability Zones.

 For example:

```
                 VPC
                  │
        ┌─────────┴─────────┐
        ↓                   ↓
       AZ-A                AZ-B
        │                   │
   Private Subnet       Private Subnet
        │                   │
    Database A          Database B
```

 This type of architecture can help support availability and resilience.

---

 # Resources Within the Same VPC

 Resources placed within the same VPC can communicate with each other when the appropriate network configuration allows it.

 For example:

```
VPC
│
├── EC2
│
├── Database
│
└── Processing
```

 These components can form a private internal network for the application.

 However, resources in different VPCs do not automatically communicate with each other.

 Similarly, resources do not automatically become publicly accessible simply because they exist in AWS.

 Network connectivity needs to be intentionally configured.

---

 # My Perspective: Applying VPCs to Financial Modelling

 This is where I see networking becoming particularly relevant to my financial-modelling projects.

 Suppose I eventually build a financial modelling platform with several components:

```
Market Data
     ↓
Data Ingestion
     ↓
Processing
     ↓
Data Warehouse
     ↓
Feature Engineering
     ↓
Financial Model
     ↓
Results
```

 These components should not necessarily all have the same network access.

 A possible architecture could be:

```
                         Internet
                            │
                            ↓
                    ┌───────────────┐
                    │ Public Subnet │
                    │               │
                    │ Data/API App  │
                    └───────┬───────┘
                            │
                            ↓
                    ┌───────────────┐
                    │ Private       │
                    │ Subnet        │
                    │               │
                    │ Processing    │
                    │ Database      │
                    │ Models        │
                    └───────────────┘
```

 The principle is:

 > **Expose only what needs to be exposed. Keep internal systems private whenever possible.**

 This is especially important when working with financial information.

---

 # Example: Portfolio Analytics Platform

 Imagine that I build a portfolio analytics system.

 It contains:

 - Market-data ingestion
- Portfolio database
- Historical data
- Risk calculations
- Financial models
- User-facing application

 I could conceptually organize these components as:

```
                         Users
                           │
                           ↓
                    Public Interface
                           │
                           ↓
                    Application Layer
                           │
                           ↓
                    Private Network
                           │
              ┌────────────┼────────────┐
              ↓            ↓            ↓
          Database     Processing     Models
              │            │            │
              └────────────┼────────────┘
                           ↓
                      Financial Data
```

 The VPC provides the overall network boundary.

 Subnets provide additional segmentation within that boundary.

---

 # Networking as a Security Layer

 Before this lecture, I mostly thought about security in terms of:

 - Authentication
- Authorization
- Encryption
- Access permissions

 This lecture adds another important dimension:

 > **Network architecture itself can be part of security.**

 For example, I can reduce exposure by keeping a database inside a private subnet rather than placing it directly on the public internet.

```
Less controlled:

Internet
   ↓
Database

More controlled:

Internet
   ↓
Application
   ↓
Private Network
   ↓
Database
```

 This does not replace authentication or encryption.

 Instead, it adds another layer of defense.

---

 # Thinking in Layers

 I find it useful to think about a cloud network as a hierarchy.

```
AWS Region
     ↓
VPC
     ↓
Subnets
     ↓
Resources
     ↓
Applications
```

 Each layer provides a different level of organization.

 For example:

 ### Region

 Determines the geographical location of the infrastructure.

 ### VPC

 Defines the overall private network.

 ### Subnet

 Divides the VPC into smaller network segments.

 ### Resource

 Represents things such as EC2 instances or databases.

 ### Application

 Uses those resources to perform business functions.

---

 # CIDR as an Architecture Decision

 CIDR notation may initially look like a technical detail, but it actually becomes an architectural decision.

 When designing a VPC, I need to think about:

 - How many resources will exist?
- How many subnets will I need?
- How much might the system grow?
- Will different environments need separate networks?
- Will I need multiple Availability Zones?
- Will networks need to communicate with each other?

 For example:

```
VPC
10.0.0.0/16
       │
       ├── Production
       │     ├── 10.0.1.0/24
       │     └── 10.0.2.0/24
       │
       ├── Development
       │     ├── 10.0.3.0/24
       │     └── 10.0.4.0/24
       │
       └── Analytics
             ├── 10.0.5.0/24
             └── 10.0.6.0/24
```

 The exact design would depend on the requirements.

 Again, this connects back to the core principle from the earlier lectures:

```
Requirements
     ↓
Architecture
     ↓
Network Design
     ↓
Implementation
```

---

 # Connecting Networking to the Data Engineering Lifecycle

 Networking may initially seem separate from data engineering.

 But when I look at an actual data pipeline, the connection becomes clear.

```
Data Source
    ↓
Ingestion
    ↓
Processing
    ↓
Storage
    ↓
Warehouse
    ↓
Analytics
    ↓
Financial Model
```

 Every arrow represents some form of communication.

 Therefore, I need to think about:

```
Who communicates with whom?
          ↓
Where are they located?
          ↓
Which network are they in?
          ↓
Should the communication be public or private?
          ↓
What access should be allowed?
```

 This makes networking an important part of data architecture.

---

 # A Simplified Financial Cloud Architecture

 Bringing together the concepts from the previous AWS lectures, I can now imagine a financial-data platform like this:

```
                         Financial Data Sources
                                  │
                                  ↓
                              Internet
                                  │
                                  ↓
                         ┌────────────────┐
                         │      VPC       │
                         │                │
                         │ Public Subnet  │
                         │                │
                         │ Data Ingestion │
                         └───────┬────────┘
                                 │
                                 ↓
                         Private Subnet
                                 │
                    ┌────────────┼────────────┐
                    ↓            ↓            ↓
                Processing     Database    Data Warehouse
                    │            │            │
                    └────────────┼────────────┘
                                 ↓
                         Financial Models
                                 │
                                 ↓
                          Risk / Analytics
```

 This is still a conceptual architecture rather than a production design.

 The important part is understanding **why the components are separated**.

---

 # What I Want to Remember

 The key concepts from this reading are:

 - A network allows devices and resources to communicate.
- IP addresses identify devices within a network.
- IPv4 addresses use 32 bits and are commonly represented as `x.x.x.x`.
- CIDR notation represents a range of IP addresses.
- A VPC is an isolated private network within an AWS Region.
- A VPC can span multiple Availability Zones within the Region.
- A VPC has a CIDR block defining its IP address space.
- Subnets divide a VPC into smaller networks.
- Each subnet has its own CIDR block.
- Subnet CIDR ranges must fit within the VPC's CIDR range.
- Public and private subnets can be used to separate resources based on their network-access requirements.
- Resources within a VPC can communicate according to the configured networking rules.
- Network architecture can be an important part of security.
- Financial systems can benefit from keeping sensitive databases and processing resources in private network segments.

---

 # My Financial Engineering Mental Model

 I want to connect networking to the larger financial-data architecture I am building in my head.

```
                    BUSINESS PROBLEM
                           ↓
                  Financial Requirements
                           ↓
                    Data Architecture
                           ↓
                  Cloud Infrastructure
                           ↓
                         VPC
                           ↓
                    ┌──────┴──────┐
                    ↓             ↓
              Public Subnet   Private Subnet
                    ↓             ↓
               Applications   Data / Processing
                                  │
                    ┌─────────────┼─────────────┐
                    ↓             ↓             ↓
                Database      Data Warehouse   Models
                    │             │             │
                    └─────────────┼─────────────┘
                                  ↓
                         Financial Analytics
                                  ↓
                         Business Decisions
```

 The key idea for me is:

 > **A data architecture is not only about where data is stored and how it is processed. It is also about how the components communicate and which components are allowed to communicate with each other.**

 This makes networking an important part of designing secure and reliable financial data systems.

---

 ## From Data Pipelines to Network Architecture

 The previous lectures taught me to think about:

```
Problem
   ↓
Requirements
   ↓
Architecture
   ↓
AWS Services
```

 This lecture adds another layer:

```
Problem
   ↓
Requirements
   ↓
Architecture
   ↓
AWS Services
   ↓
Network Architecture
   ↓
VPC
   ↓
Subnets
   ↓
Resource Connectivity
   ↓
Secure Data Pipeline
```

 For my financial-modelling projects, I therefore want to think about networking as part of the architecture from the beginning, rather than something added after the data pipeline has already been built.


 ## Security — AWS Shared Responsibility Model


 These concepts help answer questions such as:

 - Where does my system run?
- Where is my data stored?
- How do different resources communicate?
- Which resources should be public or private?

 This lecture introduces another critical question:

 > **Who is responsible for securing the system and the data?**

 When applications and data are hosted in the cloud, the physical infrastructure is managed by the cloud provider.

 However, moving to the cloud does **not** mean that security becomes entirely the cloud provider's responsibility.

 AWS provides the infrastructure, but the customer still owns and controls the data and is responsible for securing how that data is used.

 This is known as the **AWS Shared Responsibility Model**.

---

 ## The Core Idea

 The model can be summarized very simply:

```
AWS
 ↓
Security OF the Cloud

Customer
 ↓
Security IN the Cloud
```

 Or:

 > **AWS secures the infrastructure. The customer secures what they put and configure within that infrastructure.**

 This distinction is extremely important for data engineering.

---

 # Security of the Cloud

 AWS is responsible for the security of the underlying cloud infrastructure.

 This includes the physical and foundational components required to operate AWS services.

 For example:

 - Physical data centers
- Physical servers
- Storage hardware
- Networking equipment
- Physical facilities
- Global infrastructure
- Cables connecting regions
- Hardware and software supporting AWS services

 A simplified view is:

```
AWS Responsibility
        │
        ├── Physical Facilities
        ├── Hardware
        ├── Networking Infrastructure
        ├── Global Infrastructure
        └── AWS Service Infrastructure
```

 As a customer, I do not need to physically secure the AWS data center.

 AWS takes responsibility for that layer.

 This is one of the major benefits of cloud computing.

---

 # Security in the Cloud

 The responsibility changes once I start using AWS resources.

 I still own my data.

 I am responsible for determining:

 - Who can access the data
- What they can do with the data
- How long they can access it
- How the data is protected
- How the data moves between systems
- How resources are configured
- Which applications can access which datasets

```
Customer Responsibility
        │
        ├── Data
        ├── Access
        ├── Permissions
        ├── Network Configuration
        ├── Encryption
        └── Application Security
```

 This means that simply putting data into AWS does not automatically make the data secure.

 The customer still needs to configure the environment correctly.

---

 # The Apartment Building Analogy

 A useful way to understand the Shared Responsibility Model is to think about an apartment building.

 Imagine that AWS owns and operates a large apartment building.

 The building owner is responsible for:

 - The physical structure
- Building security
- Electricity
- Physical access to the building
- Maintaining the building itself

 But the tenant is responsible for securing their own apartment.

 For example:

```
Building Owner
      ↓
Secure Building
      ↓
Tenant
      ↓
Lock Apartment
      ↓
Protect Personal Belongings
```

 AWS works in a similar way.

```
AWS
 ↓
Secure Cloud Infrastructure
 ↓
Customer
 ↓
Secure Data & Resources
```

 Both sides have responsibilities.

---

 # Why This Matters for Data Engineering

 This model is particularly important for data engineers because data pipelines often connect multiple systems.

 Consider a simple pipeline:

```
Data Source
     ↓
Ingestion
     ↓
Storage
     ↓
Transformation
     ↓
Database
     ↓
Analytics
```

 Every stage potentially contains sensitive data.

 Therefore, I need to think about security across the entire pipeline.

 For example:

 - Who can upload data?
- Who can read raw data?
- Who can modify processed data?
- Which applications can access the database?
- Which users can run the pipeline?
- Can data be accessed from outside the network?
- Is data encrypted?
- How long should access remain available?

 Security therefore becomes part of the **data architecture**, not just an operational afterthought.

---

 # Data Ownership and Control

 One of the most important ideas from this reading is:

 > **The cloud provider hosts the infrastructure, but the customer still owns and controls their data.**

 This means I cannot assume:

 > "My data is on AWS, therefore AWS is responsible for everything."

 Instead, I need to understand exactly what AWS is responsible for and what I am responsible for.

```
AWS
 ↓
Provides Infrastructure
 ↓
I Configure the Infrastructure
 ↓
I Store My Data
 ↓
I Control Access
 ↓
I Protect the Data
```

 This distinction becomes especially important when the data has financial, personal, or regulatory significance.

---

 # Security of Data at Rest

 Data can exist in different states.

 One important state is **data at rest**.

 Data at rest means data that is currently stored somewhere.

 For example:

```
Financial Data
     ↓
S3
```

 or:

```
Financial Data
     ↓
Database
```

 The customer is responsible for ensuring that stored data is appropriately protected.

 Encryption can be an important part of this protection.

```
Plain Data
    ↓
Encryption
    ↓
Encrypted Storage
```

 The exact security implementation depends on the system requirements and AWS service being used.

---

 # Security of Data in Transit

 Data also moves between systems.

 For example:

```
Market Data API
       ↓
Data Pipeline
       ↓
S3
       ↓
Processing
       ↓
Database
```

 Data moving between these components is considered **data in transit**.

 Protecting data while it moves is therefore another important responsibility.

 A simplified model is:

```
Data Source
    │
    │ Secure Communication
    ↓
Data Pipeline
    │
    │ Secure Communication
    ↓
Storage / Database
```

 This distinction gives me two important security questions:

```
Is my data secure while stored?
        ↓
Data at Rest

Is my data secure while moving?
        ↓
Data in Transit
```

---

 # Access Control

 Another major responsibility is managing **who can access data and resources**.

 Suppose I have a financial database containing portfolio information.

 I may have several different users:

```
Portfolio Manager
Data Analyst
Data Engineer
Data Scientist
Application
Administrator
```

 They should not necessarily have identical permissions.

 For example:

```
Portfolio Manager
       ↓
Read Portfolio Data

Data Engineer
       ↓
Build / Maintain Pipeline

Data Scientist
       ↓
Read Curated Data

Application
       ↓
Access Required Database Tables
```

 This leads to an important security principle:

 > **Give users and applications only the access they actually need.**

 This is commonly associated with the principle of **least privilege**.

---

 # Security and Data Pipelines

 The Shared Responsibility Model becomes especially important when building cloud-based pipelines.

 Consider:

```
External Data
      ↓
Ingestion
      ↓
S3
      ↓
Processing
      ↓
Data Warehouse
      ↓
Financial Model
```

 At each stage, I need to consider access.

```
Who can write?
Who can read?
Who can modify?
Who can delete?
Who can execute?
```

 For example:

```
Raw Data
   │
   ├── Ingestion → WRITE
   │
   ├── Processing → READ
   │
   └── Analyst → LIMITED READ
```

 Not every component should automatically receive full access to every dataset.

---

 # My Perspective: Applying This to Financial Modelling

 This is where the Shared Responsibility Model becomes particularly important for my financial-data projects.

 Imagine that I build a portfolio-risk modelling platform.

 The platform might contain:

```
Market Data
     ↓
Raw Data
     ↓
Processing
     ↓
Curated Data
     ↓
Financial Model
     ↓
Risk Results
```

 Some of this information could be highly sensitive.

 For example:

 - Portfolio positions
- Trading activity
- Client information
- Investment strategies
- Risk calculations
- Model outputs
- Proprietary research

 Therefore, I cannot treat security as something that comes after the data pipeline has been built.

 Security needs to be considered from the beginning.

```
Financial Requirement
        ↓
Data Architecture
        ↓
Network Architecture
        ↓
Security Architecture
        ↓
Data Pipeline
        ↓
Financial Model
```

---

 # Example: Portfolio Data Platform

 Suppose I have a portfolio database.

 A simplified architecture could be:

```
                       Users
                         │
                         ↓
                  Application Layer
                         │
                         ↓
                   Private Network
                         │
                         ↓
                    Database
                         │
                         ↓
                  Portfolio Data
```

 The security responsibilities might include:

 - Controlling which users can access the application
- Controlling which applications can access the database
- Restricting network access
- Protecting stored data
- Protecting data during transmission
- Managing permissions
- Removing access when it is no longer required

 The cloud provider secures the underlying infrastructure, but I still need to configure and operate my part of the system securely.

---

 # VPC + Security + Data

 This also connects directly to the previous lecture about VPCs and subnets.

 Previously, I learned that I can create:

```
VPC
│
├── Public Subnet
│
└── Private Subnet
```

 Now I can add security considerations:

```
                         Internet
                            │
                            ↓
                     Public Subnet
                            │
                       Application
                            │
                            ↓
                     Private Subnet
                            │
                     ┌──────┴──────┐
                     ↓             ↓
                  Database     Processing
                     │             │
                     └──────┬──────┘
                            ↓
                       Financial Data
```

 The network architecture helps reduce unnecessary exposure.

 But networking alone is not enough.

 I still need to control:

 - Identity
- Permissions
- Data access
- Encryption
- Application access
- Credentials
- Configuration

 This is why security should be viewed as a **layered approach**.

---

 # Security as Multiple Layers

 I find it useful to think about financial-data security as several layers.

```
                 Security
                     │
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
    Identity       Network        Data
       │             │             │
   Permissions     VPC/Subnets   Encryption
       │             │             │
       └─────────────┼─────────────┘
                     ↓
                Applications
                     ↓
                  Pipelines
                     ↓
                    Data
```

 No single security mechanism is sufficient by itself.

 A secure system combines multiple controls.

---

 # Security Is Part of the Architecture

 One of the biggest lessons I take from this reading is that security should not be treated as something added at the end.

 A common approach might be:

```
Build System
     ↓
Deploy System
     ↓
Think About Security
```

 A better approach is:

```
Understand Requirements
        ↓
Design Architecture
        ↓
Design Security
        ↓
Build System
        ↓
Continuously Monitor & Maintain
```

 This is especially important in financial systems.

 Security requirements should influence architectural decisions from the beginning.

---

 # Financial Data Security Example

 Consider a simplified financial-data platform:

```
             External Market Data
                      │
                      ↓
                 Ingestion
                      │
                      ↓
                     S3
                      │
                      ↓
                Data Processing
                      │
                      ↓
                  Data Warehouse
                      │
              ┌───────┴────────┐
              ↓                ↓
        Financial Model     Analytics
              │                │
              └───────┬────────┘
                      ↓
               Business Users
```

 Now add security responsibilities:

```
Data Source
     │
     ├── Secure Transmission
     ↓
S3
     │
     ├── Access Control
     ├── Encryption
     └── Data Protection
     ↓
Processing
     │
     ├── Restricted Access
     └── Secure Network
     ↓
Warehouse
     │
     ├── Permissions
     └── Controlled Queries
     ↓
Financial Model
     │
     └── Authorized Users
```

 This demonstrates that security follows the data throughout its lifecycle.

---

 # Security and the Data Lifecycle

 I can now think about security in terms of the complete data lifecycle:

```
Collect
  ↓
Transfer
  ↓
Store
  ↓
Process
  ↓
Analyze
  ↓
Share
  ↓
Archive / Delete
```

 At every stage, I should ask:

```
Who can access the data?
What can they do?
Where is the data?
How is it protected?
How long should access exist?
```

 This way of thinking will be particularly useful when working with financial datasets.

---

 # Shared Responsibility Does Not Mean Equal Responsibility

 One subtle but important point is that "shared responsibility" does not mean AWS and the customer perform exactly the same security tasks.

 The responsibility is divided according to the service and infrastructure layer.

```
Physical Infrastructure
        ↓
        AWS
        ↓
Cloud Infrastructure
        ↓
        AWS
        ↓
Resource Configuration
        ↓
      Customer
        ↓
Operating System / Application
        ↓
      Customer
        ↓
Data & Access
        ↓
      Customer
```

 The exact boundary varies depending on which AWS service is being used.

 Therefore, whenever I introduce a new AWS service into a data architecture, I should understand:

 > **What does AWS manage, and what do I need to configure and secure?**

---

 # Connecting This to the Previous Lectures

 The progression across the AWS lectures is becoming clearer.

 First:

```
Cloud Infrastructure
```

 Then:

```
Compute
Storage
Databases
Networking
```

 Then:

```
VPC
Subnets
IP Addresses
CIDR
```

 And now:

```
Security
     ↓
Shared Responsibility
     ↓
Data Protection
     ↓
Access Control
```

 These are not independent concepts.

 They work together to form a complete cloud architecture.

```
                    AWS Cloud
                        │
        ┌───────────────┼───────────────┐
        ↓               ↓               ↓
     Compute         Storage         Network
        │               │               │
        └───────────────┼───────────────┘
                        ↓
                    Databases
                        ↓
                   Data Systems
                        ↓
                    Security
                        │
        ┌───────────────┼───────────────┐
        ↓               ↓               ↓
     Identity        Network          Data
     & Access        Security        Protection
```

---

 # What I Want to Remember

 The key concepts from this reading are:

 - Cloud computing removes the need to manage physical infrastructure directly.
- AWS is responsible for the **security of the cloud**.
- Customers are responsible for **security in the cloud**.
- AWS secures the physical facilities and underlying infrastructure.
- Customers are responsible for securing their data and configurations.
- Customers control who can access their data and resources.
- Data needs protection both **at rest** and **in transit**.
- Access should be carefully controlled.
- Network architecture such as VPCs and subnets contributes to security.
- Different AWS services have different responsibility boundaries.
- Security should be considered during architecture design, not after implementation.
- Data-engineering pipelines need security controls across their entire lifecycle.

---

 # My Financial Engineering Mental Model

 For my financial-data projects, I want to think about security using the following model:

```
                    Financial Data
                          │
                          ↓
                    Data Lifecycle
                          │
          ┌───────────────┼───────────────┐
          ↓               ↓               ↓
       Storage         Processing       Access
          │               │               │
          ↓               ↓               ↓
      Encryption       Network        Permissions
                          │
                          ↓
                       VPC
                          │
                    ┌─────┴─────┐
                    ↓           ↓
                 Public       Private
                 Layer         Layer
                    │           │
                    └─────┬─────┘
                          ↓
                  Financial Models
                          ↓
                  Business Decisions
```

 The important principle for me is:

 > **Financial data should be treated as an asset that needs to be protected throughout its entire lifecycle.**

---

 # From Cloud Infrastructure to Secure Financial Systems

 The overall learning progression now looks like:

```
Business Problem
       ↓
Stakeholder Requirements
       ↓
Data Requirements
       ↓
System Architecture
       ↓
Cloud Infrastructure
       ↓
AWS Services
       ↓
Network Architecture
       ↓
Security Architecture
       ↓
Data Pipeline
       ↓
Reliable & Secure Data
       ↓
Financial Models
       ↓
Business Decisions
```

 This gives me a much broader understanding of data engineering.

 I am not simply learning how to move data from one system to another.

 I am learning how to build systems where data can be:

 - **Collected reliably**
- **Stored appropriately**
- **Processed efficiently**
- **Accessed securely**
- **Protected throughout its lifecycle**
- **Used for analytics and financial modelling**

  ## Data Generation & Source Systems

 The first stage of the data engineering lifecycle is **data generation and source systems**.

 Before building a data pipeline, I need to understand where the data actually comes from.

 This is an important shift in perspective.

 A data engineer does not usually create the original business data. Instead, the data engineer consumes data generated by systems owned and maintained by other teams, organizations, vendors, or platforms.

 A simplified view is:

```
Source Systems
      ↓
Data Generation
      ↓
Data Ingestion
      ↓
Data Processing
      ↓
Data Storage
      ↓
Analytics / ML / Financial Models
```

 This means that the quality and reliability of downstream systems are heavily influenced by the source systems that generate the data.

---

 # What Are Source Systems?

 A **source system** is a system that generates or stores data that another system needs to consume.

 Examples include:

 - Relational databases
- NoSQL databases
- Files
- APIs
- Data-sharing platforms
- IoT devices
- Application systems
- External vendor systems

 For example, an e-commerce company might have:

```
Sales Database
      ↓
Product Files
      ↓
Marketing API
      ↓
Customer Data
      ↓
IoT / Delivery Data
```

 A data engineer might need to combine data from all of these sources into a downstream data platform.

---

 # My Financial Engineering Perspective

 This concept becomes even more interesting when I think about financial modelling.

 A financial model may depend on data from many different sources:

```
                    Financial Model
                          ↑
             ┌────────────┼────────────┐
             │            │            │
             ↓            ↓            ↓
         Market Data   Fundamentals   Portfolio Data
             │            │            │
             ↓            ↓            ↓
          Exchange      Company       Internal
          / Vendor      Filings      Systems
```

 I might need:

 - Stock prices
- OHLCV data
- Corporate actions
- Company financial statements
- Earnings data
- Economic indicators
- Interest rates
- FX rates
- Commodity prices
- Portfolio positions
- Transactions
- Risk data
- Alternative datasets

 Each of these may originate from a completely different source system.

 Therefore, before designing the pipeline, I need to understand the sources.

---

 # Common Types of Source Systems

 The lecture introduces several common categories of source systems.

```
Source Systems
│
├── Databases
├── Files
├── APIs
├── Data Sharing Platforms
└── IoT Devices
```

 Each source has different characteristics and therefore creates different engineering challenges.

---

 # 1\. Databases

 Databases are among the most common source systems.

 A database may contain structured information organized into tables.

 For example:

```
Customers
+---------+----------+----------+
| ID      | Name     | Country  |
+---------+----------+----------+

Transactions
+---------+----------+----------+
| ID      | Customer | Amount   |
+---------+----------+----------+
```

 Relational databases organize data into related tables.

 There are also NoSQL databases, including:

 - Key-value databases
- Document databases
- Other non-relational systems

 These databases may support applications or internal business systems.

---

 # Financial Example — Portfolio Database

 Imagine an investment company has an internal portfolio system.

```
Portfolio Database
│
├── Accounts
├── Positions
├── Transactions
├── Securities
└── Orders
```

 A financial data engineer might need to extract this data and make it available for:

```
Portfolio Database
        ↓
Data Pipeline
        ↓
Data Warehouse
        ↓
Risk Analytics
        ↓
Financial Models
```

 The important point is that the portfolio database may not belong to the data engineering team.

 Another team may own it.

 Therefore, I need to understand how that system works before depending on it.

---

 # 2\. Files

 Another common source system is simply a collection of files.

 Files can include:

 - CSV
- JSON
- XML
- Text files
- Excel files
- Audio
- Video
- Other formats

 For data engineering, files are particularly common because organizations frequently exchange data through file-based systems.

 For example:

```
Vendor
   ↓
CSV Files
   ↓
Data Engineer
   ↓
Data Pipeline
```

---

 # Financial Example — Market Data Files

 Imagine a market-data vendor provides daily files:

```
market_data/
│
├── 2026-01-01.csv
├── 2026-01-02.csv
├── 2026-01-03.csv
└── ...
```

 Each file might contain:

```
Date
Ticker
Open
High
Low
Close
Volume
```

 My financial model may depend on these files.

 But now several engineering questions appear:

 - What happens if a file is missing?
- What happens if the vendor changes the column names?
- What happens if a new column is introduced?
- What happens if a file arrives late?
- What happens if the same file is delivered twice?
- What happens if historical data is corrected?

 These are data-engineering problems rather than purely financial-modelling problems.

---

 # 3\. APIs

 Another common source system is an **API — Application Programming Interface**.

 An API allows one system to request data from another system.

 A simplified flow is:

```
Data Engineer
      │
      │ HTTP Request
      ↓
     API
      │
      │ Response
      ↓
   JSON / XML
```

 For example:

```
GET /market-data/AAPL
```

 might return structured data such as:

```
{
    "ticker": "AAPL",
    "price": 245.32,
    "volume": 1234567
}
```

 The exact API structure depends on the provider.

---

 # APIs in Financial Data Engineering

 APIs are extremely relevant to financial modelling.

 A financial data pipeline might consume:

```
Market Data API
       ↓
Price Data

Economic Data API
       ↓
Macro Data

Company Data API
       ↓
Fundamental Data

FX API
       ↓
Currency Data
```

 These datasets can then be combined:

```
Market Data
     +
Fundamental Data
     +
Macro Data
     +
FX Data
     ↓
Financial Dataset
     ↓
Financial Model
```

 This is one reason API-based ingestion is such an important data-engineering skill for financial applications.

---

 # 4\. Data Sharing Platforms

 Organizations may also provide data through dedicated data-sharing platforms.

 These platforms allow data to be shared:

 - Internally
- Between departments
- With partners
- With vendors
- With external organizations

 A simplified example is:

```
Data Provider
     ↓
Data Sharing Platform
     ↓
Data Engineer
     ↓
Data Pipeline
```

 This can be particularly useful when an organization wants to share large datasets without exposing the underlying operational systems directly.

---

 # 5\. IoT and Streaming Sources

 Another source system mentioned in the lecture is **IoT — Internet of Things**.

 IoT devices can continuously generate data.

 For example:

```
Device 1 ─┐
Device 2 ─┤
Device 3 ─┤
Device 4 ─┤
Device 5 ─┤
          ↓
      Data Stream
          ↓
       Database
```

 This can create a large volume of continuously generated data.

 While IoT may not be the first thing that comes to mind when thinking about finance, the same concept applies to other real-time financial data sources.

 For example:

```
Market Events
     ↓
Continuous Stream
     ↓
Ingestion System
     ↓
Real-Time Processing
     ↓
Trading / Risk / Analytics
```

 This introduces another important dimension:

 > **Data can be generated continuously rather than delivered as periodic batches.**

---

 # Batch vs Real-Time Sources

 Source systems can therefore produce data in different ways.

 ### Batch

 Data arrives periodically.

```
Vendor
  ↓
Daily File
  ↓
Pipeline
```

 For example:

```
End of Day
     ↓
Daily Market Data
     ↓
Data Pipeline
```

 ### Streaming

 Data arrives continuously.

```
Market Events
      ↓
Continuous Stream
      ↓
Pipeline
```

 For example:

```
Trade 1
Trade 2
Trade 3
Trade 4
   ↓
Real-Time Stream
```

 The choice between batch and streaming depends on the business requirements.

---

 # Source Systems Are Usually Outside My Control

 One of the most important lessons from this lecture is that the source system is often **not owned by the data engineer**.

 The system might be maintained by:

 - Software engineers
- Another internal department
- External vendors
- Third-party platforms
- Data providers

 This means:

 > **My data pipeline depends on systems that I may not control.**

 This is a fundamental reality of data engineering.

---

 # The Dependency Problem

 Consider:

```
Source System
      ↓
Data Pipeline
      ↓
Data Warehouse
      ↓
Financial Model
```

 If the source system changes unexpectedly:

```
Source System
      ↓
❌ Changed Schema
      ↓
Data Pipeline
      ↓
❌ Pipeline Failure
      ↓
Financial Model
      ↓
❌ Incorrect / Missing Data
```

 This means that source-system reliability directly affects downstream systems.

---

 # Source Systems Are Not Always Predictable

 In a perfect world, a source system would always provide:

```
Correct Data
+
Correct Schema
+
Expected Format
+
Expected Timing
+
Expected Availability
```

 Unfortunately, real-world systems do not always behave this way.

 Source systems can:

 - Go offline
- Change schemas
- Rename columns
- Delete fields
- Add new fields
- Change data types
- Change business logic
- Deliver data late
- Produce incorrect data
- Change the meaning of existing fields

 This is one of the realities that makes data engineering more challenging than simply writing a pipeline.

---

 # Schema Changes

 One particularly important problem is **schema evolution**.

 Suppose my pipeline expects:

```
Date
Ticker
Price
Volume
```

 Then the source system changes to:

```
Date
Symbol
ClosePrice
Volume
```

 From a human perspective, these fields might appear similar.

 But from the pipeline's perspective:

```
Ticker
   ↓
Missing

Price
   ↓
Missing
```

 The pipeline may fail.

---

 # A Financial Example of Schema Evolution

 Imagine my model expects:

```
ticker
close_price
trade_volume
```

 A vendor changes the dataset to:

```
symbol
closing_price
volume
```

 The financial meaning may not have changed significantly.

 But the data pipeline may still break:

```
Vendor
  ↓
Changed Schema
  ↓
Ingestion
  ↓
Transformation
  ↓
❌ Failure
  ↓
Financial Model
```

 This demonstrates an important lesson:

 > **Data engineering depends not only on data values, but also on the structure and contract of the data.**

---

 # Schema Contracts

 This leads to the idea of treating the expected source structure as a kind of **data contract**.

 For example:

```
Expected Source Contract

ticker       → string
price        → numeric
volume       → integer
timestamp    → datetime
```

 If the source system suddenly changes:

```
ticker
price
volume
timestamp
currency
```

 I need to determine whether the change is:

```
Compatible
     or
Breaking
```

 This is why communication with source-system owners matters.

---

 # Data Can Change Without the Schema Changing

 An even more subtle problem is that the schema may remain exactly the same while the **meaning or quality of the data changes**.

 Suppose I receive:

```
ticker
price
volume
```

 every day.

 The schema hasn't changed.

 But the source system changes the way `price` is calculated.

 The pipeline might continue running successfully.

 Yet the downstream financial model could now be using different data.

```
Schema
  ↓
Same

Pipeline
  ↓
Runs Successfully

Data Meaning
  ↓
Changed

Financial Model
  ↓
Potentially Wrong
```

 This is potentially more dangerous than an obvious pipeline failure because the system may appear healthy.

---

 # Data Engineering Is About Data Reliability

 This gives me an important distinction:

```
Pipeline Reliability
        ≠
Data Reliability
```

 A pipeline can run successfully while producing incorrect results.

 For financial modelling, this distinction is extremely important.

 I therefore need to think about:

 - Data freshness
- Data completeness
- Data accuracy
- Data consistency
- Data validity
- Data lineage
- Schema stability

---

 # Working With Source-System Owners

 The lecture makes an important point about relationships with source-system owners.

 As a data engineer, I should not simply treat the source as:

```
Black Box
    ↓
Data
```

 Instead, I should understand:

```
Who owns the system?
        ↓
How is data generated?
        ↓
When is data generated?
        ↓
What transformations occur?
        ↓
What can change?
        ↓
How are changes communicated?
```

 This requires communication with the teams responsible for the source systems.

---

 # My Financial Data Example

 Suppose I use a market-data provider.

 Instead of simply asking:

 > "How do I download the prices?"

 I should also understand:

 - What is the source of the prices?
- What does the timestamp represent?
- Which timezone is used?
- Are prices adjusted?
- How are corporate actions handled?
- How are missing values represented?
- How frequently is the data updated?
- Can historical values be revised?
- How are corrections communicated?
- What happens during outages?
- What is the expected delivery time?

 These questions become critical when the data feeds a financial model.

---

 # Source-System Documentation

 I want to develop the habit of documenting source systems before building pipelines.

 A simple source-system inventory could look like:

```
Source: Market Data API

Owner:
External Vendor

Format:
JSON

Frequency:
Real-time / periodic

Key Data:
Price, Volume, Timestamp

Access:
API Authentication

Expected Schema:
...

Potential Changes:
Schema / Availability / Data Corrections

Downstream Users:
Analytics / Financial Models
```

 This creates visibility into the dependency.

---

 # Source Systems and Data Lineage

 Understanding source systems also helps with **data lineage**.

 Data lineage answers:

 > **Where did this data come from?**

 For example:

```
Market Data Provider
        ↓
API
        ↓
Raw Data
        ↓
Transformation
        ↓
Curated Market Data
        ↓
Financial Model
        ↓
Risk Metric
```

 If a risk metric looks suspicious, I should be able to trace the data backwards.

```
Risk Metric
    ↑
Financial Model
    ↑
Curated Dataset
    ↑
Transformation
    ↑
Raw Data
    ↑
Market Data API
```

 This is particularly valuable in financial systems where the ability to explain the origin of a result can be important.

---

 # Source Systems and Financial Model Risk

 This also introduces an interesting connection between **data engineering risk** and **model risk**.

 Suppose a financial model produces:

```
Expected Return = 12.4%
```

 I shouldn't only ask:

 > "Is the model mathematically correct?"

 I should also ask:

 > "Where did the model's input data come from?"

```
Financial Model
      ↓
Model Inputs
      ↓
Curated Data
      ↓
Raw Data
      ↓
Source System
```

 If the source data is wrong, the model can be wrong even when the mathematics are perfect.

 Therefore:

 > **Good financial modelling depends on good data engineering.**

---

 # Designing Around Unreliable Sources

 Since source systems can fail or change, downstream systems should be designed with these possibilities in mind.

 Instead of:

```
Source
  ↓
Pipeline
  ↓
Model
```

 I want to think more like:

```
Source
  ↓
Ingestion
  ↓
Raw / Immutable Data
  ↓
Validation
  ↓
Transformation
  ↓
Curated Data
  ↓
Financial Model
```

 This provides more opportunities to detect and isolate problems.

---

 # Source Data as an External Dependency

 A useful mental model is:

```
                 My Data Platform
                       │
                       │ depends on
                       ↓
                Source System
                       │
              ┌────────┴────────┐
              ↓                 ↓
           Schema            Availability
           Changes             Issues
              │                 │
              └────────┬────────┘
                       ↓
                Pipeline Risk
```

 This means source systems should be treated as **dependencies** that need to be monitored and understood.

---

 # The Importance of Communication

 One of the strongest lessons I take from this lecture is that data engineering is not purely a technical activity.

 A successful data engineer needs to communicate with:

 - Software engineers
- Product teams
- Data providers
- Business stakeholders
- Analysts
- Data scientists
- Operations teams

 In the context of financial modelling, this might mean communicating with:

```
Market Data Team
        ↓
Data Engineering
        ↓
Quant / Financial Modelling
        ↓
Risk / Portfolio Teams
```

 Each group sees the data from a different perspective.

 The data engineer needs to connect those perspectives.

---

 # Source System Questions I Want to Ask

 Whenever I work with a new source, I want to develop a standard checklist.

 ### Ownership

 - Who owns the source system?
- Who should I contact if something breaks?

 ### Structure

 - What is the schema?
- What are the data types?
- What are the primary identifiers?

 ### Frequency

 - How often is data generated?
- Is it batch or streaming?
- When should the data arrive?

 ### Quality

 - What does missing data mean?
- Are duplicates possible?
- Can historical data change?
- How are corrections handled?

 ### Reliability

 - What happens when the source is unavailable?
- Is there a backup?
- How long can an outage last?

 ### Changes

 - Can the schema change?
- How are changes communicated?
- Are breaking changes announced in advance?

 ### Business Meaning

 - What does each field actually represent?
- Are there business rules behind the data?

 These questions can prevent many downstream problems.

---

 # Applying This to a Financial Data Platform

 I can now extend my financial architecture:

```
                External Financial Sources
                          │
        ┌─────────────────┼─────────────────┐
        ↓                 ↓                 ↓
    Market API       Fundamentals      Economic Data
        │                 │                 │
        └─────────────────┼─────────────────┘
                          ↓
                     Ingestion
                          ↓
                    Raw Data Layer
                          ↓
                    Data Validation
                          ↓
                  Transformation
                          ↓
                  Curated Data
                          ↓
                  Financial Models
                          ↓
                Risk / Analytics
                          ↓
                 Business Decisions
```

 The first thing I need to understand is not the model.

 It is the **source data feeding the model**.

---

 # Connecting This to the Data Engineering Lifecycle

 This lecture introduces the first stage of the lifecycle:

```
Data Generation & Source Systems
                ↓
            Ingestion
                ↓
          Transformation
                ↓
             Storage
                ↓
        Data Orchestration
                ↓
        Serving / Analytics
```

 The first stage is therefore foundational.

 If I don't understand the source system, every downstream stage becomes more difficult.

```
Poor Source Understanding
          ↓
Poor Ingestion
          ↓
Poor Data Quality
          ↓
Poor Analytics
          ↓
Poor Financial Model
```

 Conversely:

```
Good Source Understanding
          ↓
Reliable Ingestion
          ↓
Good Data Quality
          ↓
Reliable Analytics
          ↓
Better Financial Models
```

---

 # What I Want to Remember

 The key concepts from this lecture are:

 - The first stage of the data engineering lifecycle is **data generation and source systems**.
- Data engineers consume data generated by many different systems.
- Source systems may include databases, files, APIs, data-sharing platforms, and IoT devices.
- Source systems are often owned by other teams or external organizations.
- Therefore, source systems are frequently outside the data engineer's direct control.
- Data pipelines depend heavily on the reliability and structure of their source systems.
- Source systems can change unexpectedly.
- Schema changes can break downstream pipelines.
- Data can change even when the schema remains unchanged.
- Understanding the business meaning of data is as important as understanding its technical structure.
- Data engineers should develop strong relationships with source-system owners.
- Source-system documentation and communication are important parts of reliable data engineering.
- Data lineage helps trace downstream results back to their original sources.
- Financial models are only as reliable as the data feeding them.

---

 # My Financial Engineering Mental Model

 The biggest idea I take from this lecture is:

 > **A financial model does not begin with the modelling algorithm. It begins with understanding the data-generating systems behind the model's inputs.**

 My mental model is therefore:

```
                    Source Systems
                          ↓
                Understand the Source
                          ↓
                     Ingestion
                          ↓
                 Validate the Data
                          ↓
                  Store Raw Data
                          ↓
                   Transform Data
                          ↓
                 Curated Dataset
                          ↓
                 Financial Model
                          ↓
                Risk / Analytics
                          ↓
                Business Decision
```

 This changes how I think about financial modelling.

 Instead of starting with:

 > "Which model should I build?"

 I should first ask:

 > **"What data does the model need, where does that data come from, and how reliable is the system generating it?"**

 That question connects **data engineering directly to financial modelling**.

---

 # From Source Systems to Data Ingestion

 The next stage of the lifecycle is **ingestion**.

 Once I understand:

```
Where the data comes from
        ↓
What the data looks like
        ↓
Who owns the source
        ↓
How frequently it changes
        ↓
What can go wrong
```

 I can then design the next step:

```
Source System
      ↓
    Ingestion
      ↓
Data Platform
```

 ## Data Ingestion — Batch vs Streaming

 After understanding **data generation and source systems**, the next stage of the data engineering lifecycle is **data ingestion**.

 Data ingestion is the process of moving data from source systems into a data pipeline or data platform so that it can be processed, stored, and eventually used by downstream systems.

 A simplified view is:

```
Source Systems
      ↓
   Ingestion
      ↓
Data Platform
      ↓
Processing
      ↓
Analytics / ML / Financial Models
```

 This lecture introduces one of the most important decisions in data ingestion:

 > **How frequently should data be ingested?**

 There are two major patterns:

```
Batch Ingestion
      vs
Streaming Ingestion
```

 The right choice depends on the business requirement rather than simply choosing the most technologically advanced option.

---

 # What Is Data Ingestion?

 Data ingestion means taking data generated by a source system and bringing it into the environment where the data engineering pipeline can process it.

 For example:

```
Market Data API
      ↓
    Ingestion
      ↓
   Raw Data
      ↓
Transformation
      ↓
Financial Dataset
```

 Or:

```
Portfolio Database
      ↓
    Ingestion
      ↓
Data Warehouse
      ↓
Risk Analytics
```

 The ingestion layer therefore acts as a bridge between the **source system** and the **data platform**.

---

 # Why Ingestion Is Important

 The lecture makes an important observation:

 > **Source systems and data ingestion are often major bottlenecks in the data engineering lifecycle.**

 This makes sense because everything downstream depends on the data successfully entering the platform.

```
Source System
      ↓
      ❌
  Ingestion Failure
      ↓
No Data
      ↓
No Processing
      ↓
No Analytics
      ↓
No Financial Model
```

 Even if I have an excellent database, data warehouse, machine-learning model, or financial model, none of them can work correctly if the required data never arrives.

---

 # Connecting Ingestion to the Previous Lecture

 The previous lecture focused on understanding source systems.

 I learned to ask:

```
Where does the data come from?
Who owns the system?
How is the data generated?
What does the schema look like?
How can the source change?
How reliable is the source?
```

 Now the next question is:

 > **How should I move this data into my data platform?**

 This gives us:

```
Source Understanding
        ↓
Ingestion Design
        ↓
Data Platform
```

 The quality of the ingestion design depends heavily on how well I understand the source system.

---

 # Data Is a Continuous Stream of Events

 One interesting concept from this lecture is that data can be thought of as a continuous sequence of events.

 For example, on a website:

```
User Click
    ↓
Page View
    ↓
Purchase
    ↓
Login
    ↓
Logout
```

 These events happen continuously.

 Similarly, in financial markets:

```
Trade
Quote Update
Trade
Order Event
Quote Update
Trade
    ↓
Continuous Event Stream
```

 Data is therefore being generated continuously at the source.

 The difference between batch and streaming is largely about **how we choose to consume and process those events**.

---

 # Batch Ingestion

 **Batch ingestion** means collecting data and processing it in groups at predetermined intervals or after a certain amount of data has accumulated.

 For example:

```
Events
 ↓
 ↓
 ↓
 ↓
 ↓
 ↓
 ↓
 ↓
 ↓
Batch
 ↓
Pipeline
```

 Instead of processing every event individually, I can process a group of events together.

---

 # Example: Daily Batch

 Suppose a market-data provider gives me one file per trading day.

```
Monday
   ↓
Daily Data

Tuesday
   ↓
Daily Data

Wednesday
   ↓
Daily Data
```

 My pipeline might run once per day:

```
Market Data
     ↓
Daily File
     ↓
Batch Ingestion
     ↓
Processing
     ↓
Data Warehouse
```

 This is a simple and practical architecture.

---

 # Batch Based on Time

 Batch ingestion can happen according to a schedule.

 For example:

```
Every hour
     ↓
Ingest Data
```

 Or:

```
Every day at 2 AM
     ↓
Ingest Data
```

 Or:

```
Every week
     ↓
Ingest Data
```

 The appropriate frequency depends on how frequently the business needs updated data.

---

 # Batch Based on Data Size

 Batch processing does not necessarily need to happen at a fixed time.

 It can also happen when enough data has accumulated.

 For example:

```
Events
  ↓
10 MB
  ↓
Batch Trigger
  ↓
Processing
```

 The basic idea is:

 > **Collect data until a predefined condition is met, then process it as a batch.**

---

 # Why Batch Processing Is Still Important

 With the increasing popularity of real-time systems, it can be tempting to assume that streaming is always better.

 That is not the case.

 Batch processing remains extremely useful for:

 - Analytics
- Reporting
- Machine-learning training
- Historical processing
- Data warehousing
- Periodic financial calculations

 For example:

```
End-of-Day Data
       ↓
Batch Processing
       ↓
Daily Portfolio Analytics
       ↓
Risk Report
```

 There may be no business reason to process every individual event in real time.

---

 # Financial Example — End-of-Day Modelling

 Suppose I am building an end-of-day portfolio analytics system.

 The business requirement is:

 > "Calculate portfolio performance and risk every evening after the market closes."

 There is no need to process every market event in real time.

 A batch architecture may be sufficient:

```
Market Data
     ↓
End-of-Day Dataset
     ↓
Batch Ingestion
     ↓
Transformation
     ↓
Portfolio Calculation
     ↓
Risk Metrics
     ↓
Daily Report
```

 A streaming architecture would potentially introduce additional complexity without providing meaningful business value.

---

 # Streaming Ingestion

 **Streaming ingestion** means continuously ingesting events as they are generated.

 Instead of waiting for a batch:

```
Events
 ↓
 ↓
 ↓
 ↓
 ↓
```

 the system processes them continuously:

```
Event 1 → Pipeline
Event 2 → Pipeline
Event 3 → Pipeline
Event 4 → Pipeline
```

 This can make data available to downstream systems very shortly after it is generated.

---

 # Near Real-Time Data

 In the lecture, near real-time means that data becomes available to downstream systems shortly after it is produced.

 In some systems, this could mean:

```
Event Generated
      ↓
< 1 second
      ↓
Data Available
```

 The exact latency requirement depends on the application.

 The important concept is:

 > **Streaming minimizes the delay between data generation and data availability.**

---

 # Financial Example — Real-Time Market Events

 Financial markets are a good example where streaming can potentially be valuable.

 Imagine a stream of market events:

```
09:30:01  AAPL Trade
09:30:01  MSFT Quote
09:30:02  AAPL Quote
09:30:02  TSLA Trade
09:30:03  AAPL Trade
```

 A streaming pipeline could process these events continuously:

```
Market Events
      ↓
Streaming Ingestion
      ↓
Real-Time Processing
      ↓
Risk / Monitoring / Alerts
```

 This could enable use cases such as:

 - Real-time anomaly detection
- Intraday risk monitoring
- Market monitoring
- Real-time alerts
- Event-driven applications

---

 # Batch vs Streaming

 The distinction can be summarized as:

```
BATCH

Events
  ↓
Collect
  ↓
Wait
  ↓
Process Together
  ↓
Output
```

 Versus:

```
STREAMING

Event
  ↓
Process
  ↓
Output

Event
  ↓
Process
  ↓
Output
```

 Or more simply:

```
Batch:
Many events → Process together

Streaming:
Events → Process continuously
```

---

 # Latency Is a Business Requirement

 One of the most important lessons from this lecture is that the choice between batch and streaming should begin with the **business requirement**.

 I should not start with:

 > "Streaming is more modern, so I should use streaming."

 Instead, I should ask:

 > **How quickly does the business actually need the data?**

 For example:

```
Business Requirement
        ↓
Data Freshness Requirement
        ↓
Latency Requirement
        ↓
Ingestion Architecture
```

---

 # Financial Modelling Example

 Consider two different financial use cases.

 ### Use Case 1 — Monthly Valuation Report

 Requirement:

 > "Generate a monthly portfolio valuation report."

 A batch pipeline is probably appropriate:

```
Monthly Data
     ↓
Batch Ingestion
     ↓
Processing
     ↓
Valuation
```

 There is little benefit in building a complex streaming architecture.

 ### Use Case 2 — Real-Time Risk Monitoring

 Requirement:

 > "Detect unusual portfolio exposure during market hours."

 Here, low-latency data may provide significant value:

```
Market Events
      ↓
Streaming
      ↓
Risk Calculation
      ↓
Alert
```

 The business requirement justifies the additional complexity.

---

 # The Cost of Streaming

 Streaming can provide lower latency, but it introduces additional trade-offs.

 I need to consider:

 - Infrastructure complexity
- Operational complexity
- Monitoring
- Maintenance
- Cost
- Failure handling
- Data ordering
- Duplicate events
- Recovery
- Scaling

 Therefore:

```
Lower Latency
     ↓
More Complexity
```

 This is not always a bad trade-off.

 But the business value should justify it.

---

 # The Streaming Question I Want to Ask

 The lecture gives a useful question:

 > **What can I actually do with real-time data that I couldn't do with batch data?**

 I think this is an excellent architecture question.

 Before choosing streaming, I should be able to identify a real benefit.

```
Real-Time Data
      ↓
What decision improves?
      ↓
What action becomes possible?
      ↓
What business value is created?
```

 If I cannot answer these questions, streaming may simply be unnecessary complexity.

---

 # Financial Example — Streaming Justification

 Suppose I am building a portfolio monitoring system.

 Without streaming:

```
Market Data
   ↓
Every 15 minutes
   ↓
Risk Calculation
   ↓
Alert
```

 With streaming:

```
Market Event
   ↓
Risk Calculation
   ↓
Alert
```

 If the business needs immediate alerts when portfolio exposure changes, streaming may be justified.

 But if the business only reviews risk every hour, then:

```
Hourly Batch
```

 might be completely sufficient.

---

 # Batch and Streaming Can Coexist

 Another important lesson is that I do not have to choose one architecture for the entire data platform.

 Real-world systems often combine both.

 For example:

```
             Market Events
                   │
                   ↓
              Streaming
                   │
          ┌────────┴────────┐
          ↓                 ↓
   Real-Time Alerts    Raw Data Store
                            │
                            ↓
                         Batch
                            │
                            ↓
                    Model Training
```

 This is a very important concept.

 A system can use streaming for one requirement and batch processing for another.

---

 # Financial Example — Hybrid Architecture

 Imagine a financial platform that has two requirements:

 ### Requirement 1

 Detect unusual market behaviour immediately.

 ### Requirement 2

 Train a machine-learning model every night.

 The architecture could be:

```
                       Market Data
                           │
                           ↓
                     Event Stream
                           │
             ┌─────────────┴─────────────┐
             ↓                           ↓
       Streaming Path                Raw Storage
             ↓                           ↓
      Real-Time Alerts                  Batch
                                         ↓
                                   Feature Engineering
                                         ↓
                                   Model Training
```

 Here:

```
Streaming → Real-Time Decisions

Batch → Historical / ML Processing
```

 This is often more realistic than trying to make the entire platform purely streaming.

---

 # Pure Streaming Is Rare

 Another lesson from the lecture is that real-world systems often contain both streaming and batch components.

 For example, machine-learning training is commonly performed in batches.

```
Historical Data
      ↓
Batch Processing
      ↓
Training Dataset
      ↓
ML Model
```

 Even if the original data arrived through a streaming system:

```
Events
  ↓
Streaming Ingestion
  ↓
Storage
  ↓
Batch Processing
  ↓
ML Training
```

 Therefore:

 > **Streaming ingestion does not mean the entire data lifecycle must be streaming.**

---

 # Batch and Streaming Boundaries

 A useful way to think about architecture is to decide where streaming is actually necessary.

```
Source
  ↓
Streaming
  ↓
Real-Time Processing
  ↓
Storage
  ↓
Batch Processing
  ↓
Analytics / ML
```

 Or:

```
Source
  ↓
Batch
  ↓
Storage
  ↓
Batch Processing
  ↓
Analytics
```

 The important architectural decision is:

 > **Where does low latency actually create value?**

---

 # Change Data Capture (CDC)

 The lecture also introduces another important ingestion concept: **Change Data Capture (CDC)**.

 CDC means detecting changes that occur in a source system and using those changes to trigger downstream processing.

 Imagine a database containing:

```
Portfolio Positions
```

 A position changes:

```
AAPL
100 shares
     ↓
150 shares
```

 Instead of repeatedly copying the entire database, a CDC system can capture the change:

```
AAPL
100 → 150
```

 and send that change downstream.

---

 # Why CDC Can Be Useful

 Without CDC:

```
Entire Database
       ↓
Copy Everything
       ↓
Pipeline
```

 With CDC:

```
Database
   ↓
Detect Changes
   ↓
Changed Records
   ↓
Pipeline
```

 This can reduce unnecessary data movement.

 It can also enable more timely downstream updates.

---

 # Financial Example — Portfolio Positions

 Imagine a portfolio database:

```
Account | Ticker | Quantity
--------|--------|---------
A001    | AAPL   | 100
A001    | MSFT   | 200
```

 A new transaction changes:

```
AAPL
100 → 150
```

 CDC can capture:

```
Account: A001
Ticker: AAPL
Old Quantity: 100
New Quantity: 150
```

 That event can then trigger downstream processing.

```
Portfolio DB
      ↓
     CDC
      ↓
Position Change
      ↓
Risk Calculation
```

 This can be useful when the business requires timely updates.

---

 # Push vs Pull Ingestion

 Another decision introduced in this lecture is whether data is **pushed** to the data platform or **pulled** from the source.

 ### Pull

 The data engineer actively requests data.

```
Data Pipeline
      │
      │ Request
      ↓
Source System
      │
      │ Response
      ↓
Data Pipeline
```

 APIs are a common example.

```
Pipeline
   ↓
GET /market-data
   ↓
API
   ↓
JSON Response
```

 ### Push

 The source system sends data to the data platform.

```
Source System
      │
      │ Data
      ↓
Data Pipeline
```

 This can be useful for event-driven and streaming architectures.

---

 # Pull Example in Finance

 Suppose I use an API to retrieve daily economic data.

 My pipeline might run:

```
Every Day
    ↓
Call API
    ↓
Download Data
    ↓
Store Data
```

 This is a pull model.

 The pipeline controls when the data is retrieved.

---

 # Push Example in Finance

 Suppose a market-data provider sends events continuously.

```
Market Event
      ↓
Provider
      ↓
My Streaming System
```

 The source pushes events as they occur.

 This is more suitable for real-time architectures.

---

 # Pull vs Push

 The distinction can be summarized as:

```
PULL

Consumer asks:
"Give me the data."

Source
  ↑
  │ Request
  │
Pipeline
```

```
PUSH

Source says:
"Here is new data."

Source
  │
  │ Data
  ↓
Pipeline
```

 The appropriate approach depends on the source system and the business requirements.

---

 # Data Ingestion as a Design Decision

 I now see ingestion as more than simply "moving data."

 It involves several architectural decisions:

```
Source
  ↓
How often?
  ↓
Batch or Streaming?
  ↓
Push or Pull?
  ↓
Full Load or CDC?
  ↓
How much latency?
  ↓
What happens when the source fails?
  ↓
How is the data validated?
```

 These decisions determine the design of the downstream pipeline.

---

 # Financial Data Ingestion Decision Framework

 For my financial-modelling projects, I can use a simple decision framework.

 ### Step 1 — Understand the business requirement

```
What decision is being made?
```

 ### Step 2 — Determine the required freshness

```
Real-time?
Seconds?
Minutes?
Hourly?
Daily?
Weekly?
```

 ### Step 3 — Determine whether batch is sufficient

```
Can the business operate successfully with delayed data?
```

 If yes, batch may be preferable.

 ### Step 4 — Determine whether streaming creates additional value

```
Does lower latency enable a better decision?
```

 If yes, streaming may be justified.

 ### Step 5 — Consider the trade-offs

```
Cost
Complexity
Maintenance
Reliability
Scalability
Operational Risk
```

---

 # Examples From Financial Engineering

 | Use Case | Likely Ingestion Pattern | Reason |
| --- | --- | --- |
| Monthly financial report | Batch | Low freshness requirement |
| Daily portfolio valuation | Batch | End-of-day requirement |
| Historical backtesting | Batch | Large historical datasets |
| Model training | Batch | Training uses historical data |
| Intraday risk monitoring | Streaming / Hybrid | Lower latency can matter |
| Real-time anomaly detection | Streaming | Immediate detection |
| Trade-event processing | Streaming | Events occur continuously |
| Daily fundamentals update | Batch | Data changes periodically |

The important point is that these are **architecture decisions based on requirements**, not universal rules.

---

 # The Financial Modelling Connection

 This lecture changes how I think about the relationship between data engineering and financial modelling.

 I might initially think:

```
Financial Model
      ↓
Need Data
      ↓
Download Data
```

 But a production financial system is more like:

```
Business Requirement
        ↓
Source System
        ↓
Ingestion Architecture
        ↓
Raw Data
        ↓
Validation
        ↓
Transformation
        ↓
Curated Dataset
        ↓
Financial Model
```

 The ingestion architecture determines how fresh, reliable, and available the model's inputs are.

---

 # Data Freshness vs Model Complexity

 One important insight for me is that the complexity of a financial model does not necessarily determine the complexity of the ingestion system.

 For example:

```
Very Complex Model
        ↓
Daily Data
        ↓
Batch Ingestion
```

 can be completely reasonable.

 Conversely:

```
Simple Model
        ↓
Real-Time Decision
        ↓
Streaming Ingestion
```

 may require a much more sophisticated architecture.

 The key factor is the **business requirement and latency requirement**, not simply the sophistication of the model.

---

 # A Financial Data Platform With Both Patterns

 I can now imagine a more complete architecture:

```
                         Financial Sources
                                │
                ┌───────────────┼───────────────┐
                ↓               ↓               ↓
             APIs          Databases          Files
                │               │               │
                └───────────────┼───────────────┘
                                ↓
                          Ingestion Layer
                                │
                  ┌─────────────┴─────────────┐
                  ↓                           ↓
              Streaming                    Batch
                  ↓                           ↓
          Real-Time Data              Historical Data
                  │                           │
                  └─────────────┬─────────────┘
                                ↓
                           Data Storage
                                ↓
                         Transformation
                                ↓
                        Curated Dataset
                                ↓
                ┌───────────────┴───────────────┐
                ↓                               ↓
          Real-Time Risk                 Financial Models
          / Monitoring                   / Analytics
```

 This hybrid approach is much closer to how I should think about real-world financial data systems.

---

 # What I Want to Remember

 The key concepts from this lecture are:

 - **Data ingestion** moves data from source systems into a data pipeline or data platform.
- Source systems and ingestion are often major bottlenecks in the data engineering lifecycle.
- Data is naturally generated as a continuous sequence of events.
- **Batch ingestion** processes data in groups.
- **Streaming ingestion** processes data continuously and with low latency.
- Batch is often appropriate for analytics, reporting, historical processing, and ML training.
- Streaming is useful when low-latency data creates meaningful business value.
- Streaming introduces additional cost, complexity, maintenance, and operational considerations.
- Batch and streaming often coexist within the same architecture.
- **Change Data Capture (CDC)** can capture changes from source systems rather than repeatedly ingesting entire datasets.
- Data can be ingested using a **pull** model, where the pipeline requests data.
- Data can also use a **push** model, where the source sends data to the pipeline.
- The ingestion strategy should be driven by business requirements rather than technology preferences.

---

 # My Financial Engineering Mental Model

 The biggest lesson I take from this lecture is:

 > **Don't choose streaming because it sounds more advanced. Choose it when real-time data creates enough business value to justify the additional complexity.**

 My decision process is:

```
Business Requirement
        ↓
How fresh must the data be?
        ↓
What decisions depend on the data?
        ↓
Can batch satisfy the requirement?
        ↓
        ├── YES → Batch
        │
        └── NO
             ↓
       Streaming / Hybrid
             ↓
     Evaluate Trade-offs
             ↓
       Design Ingestion
```

 This reinforces one of the main principles from the earlier lectures:

```
❌ Technology → Problem

Instead:

✅ Business Problem
        ↓
   Requirements
        ↓
   Data Requirements
        ↓
   Architecture
        ↓
 Ingestion Strategy
        ↓
Technology Selection
```

---

 # From Ingestion to Data Storage

 The lifecycle is now becoming clearer:

```
Data Generation
       ↓
Source Systems
       ↓
Data Ingestion
       ↓
Data Storage
       ↓
Transformation
       ↓
Serving / Analytics
       ↓
Financial Models
```

 The next question is therefore:

 > **Once data has been ingested, where should it be stored?**

 This leads into the next stage of the data engineering lifecycle: **data storage**.

 Storage is not simply a place to put data.

 The type of storage I choose will affect:

 - Performance
- Scalability
- Cost
- Data accessibility
- Processing patterns
- Reliability
- Governance
- Financial modelling workflows

  ## Data Storage — From Physical Storage to Data Lakes and Warehouses

 After understanding **data generation, source systems, and data ingestion**, the next stage of the data engineering lifecycle is **data storage**.

 Data storage is easy to take for granted because almost every digital interaction involves storage in some form.

 When I:

 - Create or delete a file
- Open an application
- Download data
- Save a document
- Send a message
- Store a photograph
- Query a database

 I am interacting with some form of data storage system.

 The same principle applies to data engineering.

 > **The storage architecture I choose has a direct impact on the performance, scalability, reliability, and cost of the entire data system.**

---

 ## Why Storage Matters in Data Engineering

 A simplified view of the lifecycle so far is:

```
Data Generation
       ↓
Source Systems
       ↓
Data Ingestion
       ↓
Data Storage
       ↓
Transformation
       ↓
Analytics / ML / Financial Models
```

 Storage sits between ingestion and transformation, but it is not simply a passive place where data is kept.

 The storage layer influences:

 - How quickly data can be written
- How quickly data can be retrieved
- How much data can be stored
- How much storage costs
- How data can be processed
- How scalable the system is
- How reliable the system is
- How easily downstream users can access the data

 This means that storage is an **architectural decision**, not simply an implementation detail.

---

 # My Financial Modelling Perspective

 This becomes particularly important when thinking about financial modelling.

 A financial model might depend on:

```
Market Data
Economic Data
Company Fundamentals
Portfolio Positions
Transactions
Reference Data
Alternative Data
```

 These datasets have very different characteristics.

 For example:

```
Market Events
      ↓
High Frequency
High Volume
Low Latency
```

 while:

```
Company Fundamentals
      ↓
Lower Frequency
Historical
Structured
```

 Therefore, storing both datasets in exactly the same way may not always be appropriate.

 The storage architecture should reflect the requirements of the data and its downstream use.

---

 # The Physical Ingredients of Storage

 Before thinking about cloud services such as Amazon S3 or databases, it is useful to understand the physical components underneath them.

 Some of the fundamental storage technologies include:

 - Magnetic disks
- Solid-state drives
- RAM

 These components have different characteristics in terms of:

 - Cost
- Speed
- Capacity
- Durability
- Volatility

 A simplified hierarchy is:

```
Faster
  ↑
  │
 RAM
  │
 SSD
  │
 Magnetic Disk
  │
  ↓
Cheaper / Higher Capacity
```

 The exact characteristics depend on the technology and workload, but the general trade-off is important.

---

 # Magnetic Disk Storage

 Magnetic disks have been around for a long time, but they remain extremely important in modern data systems.

 The main reason is cost.

 Magnetic storage can provide large amounts of storage relatively cheaply.

 This makes it useful when:

```
Large Amounts of Data
        +
Lower Cost Priority
        ↓
Disk Storage
```

 For data engineering, this matters because modern systems can contain enormous historical datasets.

 For example, a financial institution might accumulate:

```
Years of
Market Data
     +
Transactions
     +
Portfolio Data
     +
Economic Data
```

 Storing all of this data in the fastest possible storage would often be unnecessarily expensive.

---

 # Solid-State Storage

 Solid-state storage, such as SSDs, provides significantly faster access than traditional magnetic disks.

 SSDs are commonly used when performance matters more.

 For example:

```
Database
   ↓
Fast Reads / Writes
   ↓
SSD Storage
```

 This can be particularly important for workloads involving:

 - Databases
- High-performance applications
- Frequently accessed datasets
- Low-latency systems

 In financial systems, fast storage can become important for applications where data needs to be retrieved quickly.

---

 # RAM — Memory

 RAM is another important form of storage.

 Unlike disk and SSD storage, RAM provides extremely fast access.

 It is commonly used when applications need very fast access to data during computation.

 A simplified model is:

```
Persistent Storage
       ↓
      SSD
       ↓
      RAM
       ↓
     CPU
```

 Data may move closer to the CPU as it is actively being processed.

 However, RAM is much more expensive than persistent storage and is generally volatile.

---

 # Volatile vs Persistent Storage

 One important distinction is whether data survives when the system loses power.

 ### Persistent Storage

 Examples include:

 - Magnetic disks
- SSDs
- Object storage

 Data remains available after the system is restarted.

 ### Volatile Storage

 RAM is typically volatile.

```
Power On
   ↓
Data in RAM
   ↓
Power Loss
   ↓
Data Lost
```

 This is why RAM is primarily used as a fast working area rather than the primary long-term storage layer.

---

 # Storage Is More Than Hardware

 One of the important lessons from this lecture is that modern data storage is not simply about physical disks.

 Modern cloud storage systems are distributed across:

```
Servers
   ↓
Clusters
   ↓
Data Centers
   ↓
Regions
```

 This introduces additional components such as:

 - Networking
- CPU
- Serialization
- Compression
- Caching
- Distributed systems

 Therefore:

 > **Modern data storage is a combination of physical resources, software systems, and distributed architecture.**

---

 # Storage Hierarchy

 I found the hierarchy presented in this lecture particularly useful.

 It can be represented as:

```
                 High-Level Storage Abstractions
              ┌──────────────────────────────────┐
              │ Data Warehouse / Data Lake /     │
              │ Data Lakehouse                   │
              └──────────────────────────────────┘
                              ↓
                    Storage Systems
              ┌──────────────────────────────────┐
              │ Databases / Object Storage /    │
              │ Streaming Storage / Caches      │
              └──────────────────────────────────┘
                              ↓
                     Raw Ingredients
              ┌──────────────────────────────────┐
              │ Disk / SSD / RAM / Networking   │
              │ Compression / Serialization     │
              └──────────────────────────────────┘
```

 Each layer builds on the layer underneath it.

---

 # Layer 1 — Raw Storage Ingredients

 At the lowest level we have the physical and infrastructure components.

```
Disk
SSD
RAM
Networking
CPU
Serialization
Compression
Caching
```

 As a data engineer, I may not directly manage these components.

 However, understanding them helps me understand why a storage system behaves the way it does.

---

 # Layer 2 — Storage Systems

 On top of the raw infrastructure, we have actual storage systems.

 Examples include:

```
Databases
Object Storage
File Storage
Streaming Storage
Memory-Based Storage
```

 For example:

```
Physical Infrastructure
        ↓
Storage System
        ↓
Amazon S3
```

 Or:

```
Physical Infrastructure
        ↓
Database Management System
        ↓
Relational Database
```

 These systems provide interfaces that allow applications and data pipelines to store and retrieve data without directly managing physical hardware.

---

 # Layer 3 — Storage Abstractions

 At the highest level are broader storage architectures and abstractions.

 Examples include:

 - Data warehouses
- Data lakes
- Data lakehouses

 These systems combine multiple underlying technologies to provide a higher-level interface for solving data-engineering problems.

 The key idea is:

 > **The higher I operate in the storage hierarchy, the less I need to worry about individual physical storage components.**

---

 # Object Storage

 One important storage system introduced earlier in the course is object storage.

 A common AWS example is:

```
Amazon S3
```

 Instead of thinking about individual disks or servers, I interact with objects and buckets.

 Conceptually:

```
Bucket
  │
  ├── market_data/
  │     ├── 2025-01-01.csv
  │     ├── 2025-01-02.csv
  │     └── 2025-01-03.csv
  │
  ├── fundamentals/
  │     ├── apple.json
  │     └── microsoft.json
  │
  └── transactions/
        └── transactions.parquet
```

 The underlying infrastructure is abstracted away.

 This makes object storage particularly useful for large-scale data platforms.

---

 # Data Warehouse

 A **data warehouse** is another important storage abstraction.

 A warehouse is generally designed to make structured data available for:

 - Analytics
- Reporting
- Business intelligence
- Aggregations
- SQL queries
- Downstream applications

 A simplified architecture might look like:

```
Source Systems
      ↓
Ingestion
      ↓
Data Warehouse
      ↓
SQL Analytics
      ↓
Reports / Models
```

 In the AWS ecosystem, an example is Amazon Redshift.

---

 # Data Lake

 A **data lake** generally provides a way to store large amounts of data in a relatively flexible form.

 It can contain:

```
Structured Data
Semi-Structured Data
Unstructured Data
Historical Data
Raw Data
Processed Data
```

 A simplified architecture might be:

```
Sources
   ↓
Ingestion
   ↓
Data Lake
   ↓
Processing
   ↓
Analytics / ML
```

 This makes data lakes particularly useful as a central repository for large-scale raw and processed datasets.

---

 # Data Lakehouse

 The lecture also introduces a more recent concept:

 > **Data Lakehouse**

 The lakehouse attempts to combine useful characteristics of data lakes and data warehouses.

 Conceptually:

```
Data Lake
    +
Data Warehouse Capabilities
    ↓
Data Lakehouse
```

 The exact implementation depends on the technology, but the broader idea is to provide flexible large-scale storage together with stronger data-management and analytical capabilities.

---

 # Storage Abstraction

 One of the concepts I want to remember is **abstraction**.

 When using a high-level storage system, I do not need to know:

```
Which physical disk?
Which server?
Which data center?
Which storage controller?
Which hardware component?
```

 Instead, I interact with a higher-level interface.

 For example:

```
My Data Pipeline
       ↓
Amazon S3
       ↓
AWS Infrastructure
       ↓
Physical Storage
```

 The lower-level complexity is hidden from me.

 This abstraction is one of the major advantages of cloud computing.

---

 # But Abstraction Does Not Mean Ignorance

 This is one of the most important lessons from the lecture.

 It is easy to say:

 > "The cloud handles storage, so I don't need to understand storage."

 That would be a mistake.

 Even though cloud providers abstract away the hardware, the underlying characteristics still affect:

 - Performance
- Cost
- Scalability
- Latency
- Reliability

 Therefore:

 > **I do not need to manage every storage component, but I should understand the characteristics and limitations of the storage system I am using.**

---

 # Why Storage Knowledge Matters

 The lecture gives a very practical example.

 A team needed to move a large dataset into a data warehouse.

 Instead of using a bulk-loading approach, they inserted data:

```
Row 1 → Warehouse
Row 2 → Warehouse
Row 3 → Warehouse
Row 4 → Warehouse
...
```

 This meant they were performing individual row inserts.

 The result was:

```
Very Slow
     +
Very Expensive
```

 Eventually, they changed the architecture to use bulk ingestion.

```
Large Dataset
      ↓
Bulk Load
      ↓
Data Warehouse
```

 This was much more appropriate for the workload.

---

 # My Financial Modelling Interpretation

 This example is extremely relevant to financial data engineering.

 Imagine I have:

```
10 Years of Historical Market Data
```

 containing millions or billions of records.

 A poor ingestion approach might be:

```
Record 1 → Database
Record 2 → Database
Record 3 → Database
...
Record N → Database
```

 A better approach could involve:

```
Historical Files
      ↓
Bulk Ingestion
      ↓
Storage / Warehouse
```

 The difference can be enormous in terms of:

 - Runtime
- Infrastructure usage
- Cost
- Reliability
- Operational complexity

 This is why understanding the characteristics of the storage system matters.

---

 # Row-by-Row vs Bulk Processing

 The basic principle is:

```
❌ Individual Writes

Data
 ↓
Row
 ↓
Database
 ↓
Row
 ↓
Database
 ↓
Row
 ↓
Database
```

 Versus:

```
✅ Bulk Write

Data
 ↓
Large Batch
 ↓
Database
```

 For large financial datasets, bulk operations are often far more appropriate than repeatedly making tiny writes.

 The exact optimal strategy depends on the database and workload, but the broader principle is:

 > **Storage systems have access patterns for which they are optimized.**

---

 # Storage and Access Patterns

 Different workloads require different storage characteristics.

 For example:

 | Requirement | Important Storage Characteristic |
| --- | --- |
| Large historical dataset | Capacity + cost |
| Real-time application | Low latency |
| Financial reporting | Efficient analytical queries |
| ML training | High-throughput data access |
| Transaction processing | Fast writes + consistency |
| Real-time risk | Low latency + high availability |
| Long-term archives | Low cost + durability |

This reinforces an idea from earlier lectures:

```
Business Requirement
       ↓
System Requirement
       ↓
Storage Requirement
       ↓
Storage Architecture
```

---

 # Financial Data Storage Is Not One-Size-Fits-All

 A financial platform might contain several different types of storage.

 For example:

```
                    Financial Data Platform
                             │
       ┌─────────────────────┼─────────────────────┐
       ↓                     ↓                     ↓
 Historical Data        Transaction Data       Real-Time Data
       ↓                     ↓                     ↓
 Object Storage          Database             Streaming Storage
       │                     │                     │
       └─────────────────────┼─────────────────────┘
                             ↓
                       Data Warehouse
                             ↓
                    Financial Analytics
```

 Different storage systems can coexist within the same architecture.

---

 # Storage for Historical Market Data

 Historical market data can become extremely large.

 For example:

```
Tick Data
   +
OHLC Data
   +
Order Book Data
   +
Corporate Actions
   +
Fundamental Data
```

 A practical architecture could be:

```
Market Data Provider
        ↓
Batch Ingestion
        ↓
Object Storage
        ↓
Data Lake
        ↓
Transformation
        ↓
Analytical Storage
        ↓
Backtesting / ML
```

 Here, low-cost scalable storage is particularly valuable.

---

 # Storage for Transactional Data

 Transactional data has different requirements.

 For example:

```
Trade
Account
Portfolio
Order
Position
```

 These datasets often require structured schemas and reliable updates.

 A relational database may therefore be appropriate:

```
Application
    ↓
Relational Database
    ↓
Transactions
```

 Later, the data can be moved into analytical storage:

```
Database
    ↓
Ingestion
    ↓
Data Warehouse
    ↓
Analytics
```

---

 # Storage for Real-Time Data

 Real-time financial systems may have a different architecture.

 For example:

```
Market Events
      ↓
Streaming System
      ↓
Real-Time Processing
      ↓
Real-Time Storage / Cache
      ↓
Risk Monitoring
```

 Here, latency becomes more important.

 This is another example of why a single storage system may not be appropriate for every stage of the architecture.

---

 # Storage and Cost

 One of the strongest lessons from the lecture is that storage decisions can have major financial consequences.

 A technically functional system can still be a poor system if it is unnecessarily expensive.

 For example:

```
Solution A
Fast
Complex
Expensive

Solution B
Slightly Slower
Simpler
Much Cheaper
```

 If the business requirement can be satisfied by Solution B, it may be the better architecture.

 This is especially relevant in cloud environments because infrastructure usage is often directly connected to cost.

---

 # Storage and Performance

 Cost is only one side of the equation.

 Storage architecture can also have a major effect on performance.

 For example:

```
Poor Storage Choice
       ↓
Slow Reads
       ↓
Slow Transformation
       ↓
Slow Financial Model
       ↓
Poor User Experience
```

 Conversely:

```
Appropriate Storage
       ↓
Efficient Data Access
       ↓
Faster Processing
       ↓
Faster Analytics / Models
```

 Therefore, storage should be considered as part of the entire system rather than as an isolated component.

---

 # Storage and the Financial Model

 This is particularly important for my goal of applying data engineering to financial modelling.

 A financial model is ultimately limited by the quality and accessibility of its inputs.

```
Storage
   ↓
Data Retrieval
   ↓
Data Processing
   ↓
Features / Inputs
   ↓
Financial Model
   ↓
Prediction / Valuation / Risk
```

 If the storage layer is poorly designed, the model can suffer from:

 - Slow data retrieval
- Stale data
- Missing data
- High infrastructure costs
- Difficult historical analysis
- Poor scalability

 So data storage is part of the foundation of a production-quality financial modelling system.

---

 # A More Complete Financial Data Architecture

 I can now combine the previous lectures into a broader architecture:

```
                    Financial Data Sources
                            │
          ┌─────────────────┼─────────────────┐
          ↓                 ↓                 ↓
        APIs            Databases           Files
          │                 │                 │
          └─────────────────┼─────────────────┘
                            ↓
                       Ingestion
                    ┌───────┴───────┐
                    ↓               ↓
                 Batch          Streaming
                    │               │
                    └───────┬───────┘
                            ↓
                       Data Storage
                    ┌───────┼────────┐
                    ↓       ↓        ↓
                 Object   Database   Stream
                 Storage  Storage    Storage
                    │       │        │
                    └───────┼────────┘
                            ↓
                Data Lake / Warehouse
                            ↓
                     Transformation
                            ↓
                  Curated Financial Data
                            ↓
              ┌─────────────┼─────────────┐
              ↓             ↓             ↓
          Analytics      ML Models    Financial Models
```

 This architecture is starting to connect the individual concepts from the course into one system.

---

 # The Storage Design Mindset

 The main lesson I take from this lecture is that I should not ask:

 > "Which storage technology should I use?"

 Instead, I should first ask:

```
What data am I storing?
        ↓
How much data?
        ↓
How frequently does it change?
        ↓
How quickly must it be accessed?
        ↓
Who will access it?
        ↓
How long must it be retained?
        ↓
What is the cost constraint?
        ↓
What storage architecture fits?
```

 This follows the same principle introduced earlier in the course:

```
❌ Tool → Problem

Instead:

✅ Problem
    ↓
Requirements
    ↓
Architecture
    ↓
Storage Characteristics
    ↓
Technology
```

---

 # Storage as a Trade-Off

 There is rarely a universally "best" storage system.

 Instead, I need to balance different dimensions:

```
              Performance
                   ▲
                   │
                   │
       Cost ◄──────┼──────► Scalability
                   │
                   │
                   ▼
               Complexity
```

 Improving one characteristic may negatively affect another.

 For example:

```
Higher Performance
        ↓
Potentially Higher Cost
```

 or:

```
Greater Flexibility
        ↓
Potentially Greater Complexity
```

 Good data engineering is therefore about finding the appropriate balance for the business requirement.

---

 # What I Want to Remember

 The key ideas from this lecture are:

 - Almost every digital interaction involves some form of data storage.
- Storage decisions affect the performance, scalability, reliability, and cost of data systems.
- Physical storage includes **magnetic disks, SSDs, and RAM**.
- RAM provides very fast access but is expensive and generally volatile.
- Disk storage provides large capacity at relatively low cost.
- SSDs provide faster access than traditional magnetic disks.
- Modern cloud storage is built from distributed infrastructure across servers and data centers.
- Networking, compression, serialization, and caching are also important parts of modern storage systems.
- Data engineers generally interact with higher-level storage systems rather than individual physical disks.
- Storage systems include databases, object storage, streaming storage, and memory-based systems.
- Higher-level storage abstractions include **data warehouses, data lakes, and data lakehouses**.
- Abstraction hides infrastructure complexity, but understanding the underlying characteristics is still important.
- Poor understanding of storage access patterns can result in serious performance and cost problems.
- Bulk ingestion can be much more appropriate than individual row-by-row inserts for large datasets.
- Storage architecture should be selected based on **business and system requirements**, not simply technology preference.

---

 # My Financial Engineering Mental Model

 The main idea I take from this lecture is:

 > **Data storage is not just about keeping data somewhere. It is about designing how data will be stored, accessed, scaled, and paid for throughout its lifecycle.**

 For financial modelling, I can think about the problem like this:

```
Financial Data
      ↓
How much?
      ↓
How frequently does it arrive?
      ↓
How quickly must it be accessed?
      ↓
How long should it be retained?
      ↓
Who needs access?
      ↓
What processing will be performed?
      ↓
What storage system fits?
      ↓
Financial Analytics / Models
```

 This gives me another important principle for the repository:

```
❌ Choose Storage Technology
       ↓
Try to Fit the Problem

Instead:

✅ Understand Data
       ↓
Understand Access Pattern
       ↓
Understand Business Requirement
       ↓
Understand Performance / Cost Requirements
       ↓
Design Storage Architecture
       ↓
Choose Technology
```

---

 # Connecting Storage to the Data Engineering Lifecycle

 At this point, the lifecycle is becoming much clearer:

```
1. Data Generation
        ↓
2. Source Systems
        ↓
3. Data Ingestion
        ↓
4. Data Storage
        ↓
5. Data Transformation
        ↓
6. Serving / Analytics
        ↓
7. Financial Models / ML / Applications
```

 The next stage is **data transformation**.

 Once the data has been ingested and stored, the next question becomes:

 > **How do we turn raw stored data into clean, structured, reliable data that downstream users and financial models can actually use?**

 This leads naturally into the next stage of the data engineering lifecycle: **Data Transformation**.
This lecture fits directly after your storage section. I’ve kept the same README style and emphasized **financial modelling, market data, portfolio analytics, risk, and feature engineering** so the course notes progressively connect to your goal.

 ## Data Transformation — Turning Raw Data into Useful Data

 After understanding **data generation, source systems, ingestion, and storage**, the next major stage of the data engineering lifecycle is **data transformation**.

 This is where data engineering starts to create significant value for downstream users.

 The overall purpose of a data engineer can be summarized as:

```
Raw Data
   ↓
Ingest
   ↓
Store
   ↓
Transform
   ↓
Useful Data
   ↓
Analytics / ML / Financial Models
```

 The important distinction is that simply storing raw data does not necessarily make it useful.

 A database may contain millions of records, but if those records are difficult to query, inconsistent, poorly structured, or missing important business logic, downstream users still cannot effectively use them.

 Therefore:

 > **Data engineering is not just about moving and storing data. It is about turning raw data into reliable, useful, and accessible data.**

---

 # Transformation as the Value-Creation Stage

 Consider a simple business example.

 A business analyst wants to understand daily sales.

 The raw source systems may contain:

```
Customer Table
Product Table
Order Table
Transaction Table
Payment Table
```

 The analyst does not necessarily want to understand all the relationships between these tables.

 Instead, they may want something like:

```
Date
Customer
Product
Quantity
Price
Revenue
```

 The data engineer's job is to transform the raw source data into something that makes this analysis easy.

```
Raw Source Data
       ↓
Cleaning
       ↓
Joining
       ↓
Aggregation
       ↓
Business Logic
       ↓
Analytical Dataset
       ↓
Business Analyst
```

 This is where the data engineer starts to directly enable downstream decision-making.

---

 # My Financial Modelling Perspective

 This concept becomes even more important in financial modelling.

 Financial data is rarely delivered in exactly the format required by a model.

 For example, a raw market-data source might contain:

```
Timestamp
Symbol
Price
Volume
Exchange
Trade ID
```

 But a financial model might need:

```
Daily Return
Volatility
Moving Average
Momentum
Volume Change
Market Beta
Drawdown
Rolling Correlation
```

 Therefore:

```
Raw Market Data
       ↓
Transformation
       ↓
Financial Features
       ↓
Financial Model
```

 The transformation layer effectively becomes the bridge between **raw financial data** and **model-ready financial information**.

---

 # The Three Components of Transformation

 The lecture breaks this stage into three important components:

 1. **Queries**
2. **Data Modeling**
3. **Data Transformation**

 These concepts are closely related, but they represent different responsibilities.

```
             Data Transformation Stage
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
      Queries       Modeling     Transformation
        │              │              │
        ↓              ↓              ↓
     Retrieve       Structure       Modify
      Data           Data            Data
```

 All three can have a significant impact on the quality and performance of the final data system.

---

 # 1\. Queries

 A query is essentially a request to retrieve data from a storage system.

 In modern data engineering, one of the most important query languages is **SQL — Structured Query Language**.

 A simplified example might look like:

```
SELECT
    customer_id,
    product_id,
    quantity,
    price
FROM sales
WHERE sale_date >= '2026-01-01';
```

 The purpose of the query is to retrieve the data required for downstream processing or analysis.

---

 # SQL as a Data Engineering Skill

 SQL is particularly important because data engineers frequently work with structured and semi-structured data stored in:

 - Relational databases
- Data warehouses
- Analytical databases
- Cloud storage systems
- Lakehouse platforms

 A typical workflow might be:

```
Storage
   ↓
SQL Query
   ↓
Filtered Data
   ↓
Transformation
   ↓
Analytical Dataset
```

 SQL therefore becomes one of the main tools for interacting with stored data.

---

 # Queries Are Not Just About Getting Data

 One thing I found important in this lecture is that writing a query is not enough.

 A query can be logically correct and still be a poor query.

 Poorly designed queries can cause:

 - Slow execution
- Excessive compute usage
- High infrastructure costs
- Delays in downstream pipelines
- Excessive data movement
- Performance problems in source systems

 This is especially important in cloud environments where compute usage can directly translate into cost.

---

 # Query Performance

 Consider two approaches.

 ### Approach 1

```
Source
  ↓
Read Entire Dataset
  ↓
Filter Later
```

 ### Approach 2

```
Source
  ↓
Filter Early
  ↓
Read Only Required Data
```

 If the dataset contains billions of financial records, these approaches can have very different costs.

 For example, suppose I have:

```
10 Years of Tick Data
       ↓
Billions of Records
```

 and I only need:

```
AAPL
2025
```

 It would be inefficient to process the entire dataset if the storage/query system can filter the data earlier.

 This leads to a broader principle:

 > **Good data engineering considers not only what data a query returns, but also how much data the system has to process to return it.**

---

 # The Problem of Row Explosion

 Another important issue mentioned in the lecture is **row explosion**.

 This can happen when joining tables incorrectly.

 Suppose I have:

```
Customers
   ↓
1,000 rows
```

 and:

```
Transactions
   ↓
100,000 rows
```

 A properly designed join might produce a meaningful relationship between customers and transactions.

 But if the join condition is incorrect, the result can become dramatically larger than expected.

 Conceptually:

```
Table A
   ×
Table B
   ↓
Unexpectedly Large Result
```

 This can consume significant compute and storage resources.

 In extreme cases, it can cause downstream systems to fail.

---

 # Financial Example — Joining Market Data

 Imagine I have:

```
Prices
```

 and:

```
Corporate Actions
```

 I want to adjust historical prices based on events such as:

 - Stock splits
- Dividends
- Other corporate actions

 A poorly defined join could duplicate price records.

 For example:

```
Price Record
     +
Multiple Matching Corporate Actions
     ↓
Multiple Output Rows
```

 Instead of:

```
AAPL | 2026-01-10 | $250
```

 I might accidentally produce:

```
AAPL | 2026-01-10 | $250
AAPL | 2026-01-10 | $250
AAPL | 2026-01-10 | $250
```

 This could silently corrupt downstream calculations.

 Therefore, understanding joins and query behavior is extremely important for financial data pipelines.

---

 # 2\. Data Modeling

 The second major component is **data modeling**.

 A data model represents how data relates to the real world.

 In simple terms:

 > **Data modeling is the deliberate process of deciding how data should be structured so that it represents the business correctly and can be used efficiently.**

 This is more than simply deciding which columns belong in a table.

 It involves understanding:

 - Entities
- Relationships
- Definitions
- Business rules
- Processes
- Workflows
- Analytical requirements

---

 # Why Data Modeling Matters

 Imagine a financial organization using the word:

 > "Customer"

 This could mean:

 - A person with a brokerage account
- A legal entity
- An investment account
- A beneficial owner
- A trading client

 Different teams may use the same word differently.

 Therefore, a data model cannot be designed purely from a technical perspective.

 The data engineer needs to work with stakeholders to understand what the data actually represents.

---

 # Data Modeling and Business Definitions

 A useful model should reflect:

```
Business Processes
       +
Business Definitions
       +
Business Relationships
       +
Business Rules
       ↓
Data Model
```

 This is one of the areas where data engineering connects directly back to the first lecture.

 We started with:

```
Business Need
     ↓
Requirements
     ↓
Architecture
```

 Now we are seeing that those requirements also influence:

```
Data Model
```

---

 # Normalization

 The lecture introduces the idea of **normalized data**.

 Relational databases often store information in separate tables.

 For example:

```
Customers
---------
customer_id
customer_name
country
```

```
Products
--------
product_id
product_name
category
price
```

```
Orders
------
order_id
customer_id
product_id
quantity
order_date
```

 This structure reduces unnecessary duplication and makes relationships explicit.

 Conceptually:

```
Customer
    │
    └──── Order
             │
             └──── Product
```

 This is useful for transactional systems.

---

 # Denormalization

 However, the structure that is ideal for a transactional system may not be ideal for analytics.

 An analyst may prefer something like:

```
Order Date
Customer
Product
Category
Quantity
Price
Revenue
```

 Instead of repeatedly joining several tables, the data engineer might create a denormalized analytical structure.

```
Normalized Source
        ↓
      Joins
        ↓
   Denormalization
        ↓
Analytical Dataset
```

 The objective is to make downstream analysis simpler and more efficient.

---

 # Financial Data Modeling

 This idea is particularly important for financial analytics.

 A transactional system might contain:

```
Accounts
Trades
Orders
Securities
Clients
Portfolios
```

 But a portfolio analyst may want:

```
Date
Portfolio
Security
Quantity
Price
Market Value
Currency
Sector
Asset Class
PnL
```

 Therefore, the data engineering layer may need to combine and model the underlying data into a structure designed for analysis.

```
Trading Systems
      ↓
Normalized Data
      ↓
Data Modeling
      ↓
Portfolio Dataset
      ↓
Risk / Performance Analytics
```

---

 # A Model Should Represent the Real World

 A good data model should not simply be technically convenient.

 It should represent the actual business concepts.

 For example, a portfolio might contain:

```
Portfolio
    ↓
Positions
    ↓
Securities
    ↓
Prices
```

 But a position is not simply a security.

 It may depend on:

```
Portfolio
Security
Quantity
Price
Timestamp
Currency
```

 Understanding these relationships is necessary before designing the model.

 This is why data modeling requires both **technical knowledge and domain knowledge**.

---

 # 3\. Data Transformation

 The third component is the actual manipulation and enhancement of data.

 This can include:

 - Cleaning
- Type conversion
- Standardization
- Joining
- Filtering
- Aggregation
- Enrichment
- Calculating new fields
- Restructuring schemas
- Feature engineering

 Conceptually:

```
Raw Data
   ↓
Clean
   ↓
Standardize
   ↓
Join
   ↓
Enrich
   ↓
Aggregate
   ↓
Model
   ↓
Useful Data
```

---

 # Transformation Can Happen at Multiple Stages

 One of the most important points from this lecture is that transformation does not happen only once.

 It can occur throughout the data engineering lifecycle.

```
Source System
      ↓
Transformation
      ↓
Ingestion
      ↓
Transformation
      ↓
Storage
      ↓
Transformation
      ↓
Warehouse
      ↓
Transformation
      ↓
Analytics / ML
```

 Therefore:

 > **Transformation is a continuous activity throughout the lifecycle rather than a single isolated step.**

---

 # Transformation Before Ingestion

 Some transformations can happen directly in the source system.

 For example, a source system might add:

```
created_at
updated_at
transaction_id
```

 before the data leaves the system.

---

 # Transformation During Ingestion

 Data may also be transformed while it is moving through the pipeline.

 For example:

```
Source
   ↓
Streaming Pipeline
   ↓
Add Metadata
   ↓
Standardize Fields
   ↓
Destination
```

 A streaming pipeline could enrich incoming events with:

```
event_timestamp
source
processing_timestamp
data_version
```

---

 # Transformation Immediately After Ingestion

 Another common approach is to first land raw data and then perform basic transformations.

 For example:

```
Raw Data
   ↓
Ingestion
   ↓
Raw Storage
   ↓
Type Conversion
   ↓
Schema Standardization
   ↓
Clean Data
```

 Suppose a market-data source sends:

```
price = "250.50"
```

 as a string.

 The transformation layer might convert it to:

```
price = 250.50
```

 as a numeric value.

---

 # Financial Example — Standardizing Market Data

 Imagine I receive market data from several providers.

 Provider A:

```
ticker
timestamp
price
volume
```

 Provider B:

```
symbol
time
last_price
vol
```

 Provider C:

```
security_id
event_time
close
quantity
```

 These datasets represent similar concepts but use different schemas.

 A transformation layer can standardize them:

```
Provider A ──┐
Provider B ──┼──→ Standardization ──→ Common Market Data Model
Provider C ──┘
```

 Result:

```
security_id
timestamp
price
volume
```

 This is extremely valuable because downstream models no longer need to understand the quirks of every individual data provider.

---

 # Data Enrichment

 Transformation can also add information that was not present in the original record.

 For example:

```
Trade
 ↓
Security Reference Data
 ↓
Enriched Trade
```

 A raw trade might contain:

```
security_id
quantity
price
timestamp
```

 After enrichment:

```
security_id
quantity
price
timestamp
sector
country
asset_class
currency
exchange
```

 This creates much more useful analytical data.

---

 # Financial Feature Engineering

 This is where transformation becomes particularly interesting for my financial modelling goal.

 A raw price series might look like:

```
Date       Price
2026-01-01 100
2026-01-02 102
2026-01-03 101
2026-01-04 105
```

 A financial model may not use the raw price directly.

 Instead, I might calculate:

```
Daily Return
Rolling Return
Volatility
Moving Average
Momentum
Drawdown
Beta
Sharpe Ratio
Rolling Correlation
```

 For example:

```
Price
 ↓
Transformation
 ↓
Returns
 ↓
Rolling Statistics
 ↓
Features
 ↓
Financial Model
```

 This is a perfect example of how data engineering and financial modelling connect.

---

 # Transformation vs Feature Engineering

 There is an important distinction I want to maintain.

 **Data transformation** is the broader process of modifying data so it becomes usable.

 **Feature engineering** is more specifically focused on creating useful variables for analytical or machine-learning models.

 Conceptually:

```
Data Transformation
        │
        ├── Cleaning
        ├── Standardization
        ├── Joining
        ├── Aggregation
        ├── Enrichment
        │
        └── Feature Engineering
                 ↓
          Model Inputs
```

 Therefore, feature engineering can be viewed as one specialized use of transformation.

---

 # Transformation for Financial Models

 Suppose I want to build a model predicting future returns.

 Raw data:

```
Price
Volume
Market Index
Interest Rate
Company Fundamentals
```

 Transformation might produce:

```
Return_1D
Return_5D
Return_20D
Volume_Change
Volatility_20D
Beta_60D
Market_Return
Interest_Rate_Change
PE_Ratio
```

 Then:

```
Raw Financial Data
        ↓
Transformation
        ↓
Feature Engineering
        ↓
Feature Store / Analytical Dataset
        ↓
Machine Learning Model
```

 This is the point where data engineering becomes directly useful to quantitative finance.

---

 # Transformation and Data Quality

 Transformation is also where many data-quality problems can be detected and corrected.

 For example:

```
Raw Data
   ↓
Missing Values
   ↓
Invalid Types
   ↓
Duplicate Records
   ↓
Incorrect Timestamps
   ↓
Outliers
   ↓
Inconsistent Symbols
```

 The transformation layer can apply rules to identify and handle these problems.

 For financial data, this becomes especially important because seemingly small data-quality issues can affect model outputs significantly.

---

 # Example — Duplicate Market Data

 Suppose the source accidentally sends the same market event twice:

```
Timestamp       Price
10:00:01        100
10:00:02        101
10:00:02        101
10:00:03        102
```

 If I calculate returns without detecting the duplicate:

```
100 → 101 → 101 → 102
```

 the resulting dataset may not represent the true market sequence.

 A transformation step could identify duplicate events and apply an appropriate rule.

```
Raw Events
    ↓
Deduplication
    ↓
Clean Events
    ↓
Return Calculation
```

---

 # Transformation and Time

 Time is particularly important in financial data.

 A financial pipeline may need to deal with:

 - Time zones
- Trading sessions
- Market holidays
- Timestamps
- Event ordering
- Late-arriving data
- Different market calendars

 Therefore, transformation is not simply about changing column names.

 It may require domain-specific financial logic.

---

 # Transformation and Historical Data

 Another important consideration is that financial data often needs to be reproducible.

 Suppose I calculate a feature today:

```
20-Day Volatility
```

 I may later need to reproduce exactly how that feature was calculated for historical model training.

 Therefore, transformation pipelines should ideally be:

 - Consistent
- Documented
- Reproducible
- Version-controlled
- Testable

 This becomes increasingly important when building production financial models.

---

 # The Transformation Layer as a Contract

 I can think of a transformation pipeline as creating a contract between raw data and downstream users.

```
Raw Source
     ↓
Transformation Layer
     ↓
Standardized Dataset
     ↓
Data Analyst / Data Scientist / Model
```

 The downstream user should not need to understand every problem in the source systems.

 Instead, the transformation layer should provide a predictable dataset.

 For example:

```
security_id
timestamp
price
volume
currency
return_1d
volatility_20d
```

 with clearly defined meanings.

---

 # Data Lineage

 This also introduces the idea of **data lineage**.

 If a model uses:

```
volatility_20d
```

 I should ideally be able to trace where it came from:

```
volatility_20d
      ↓
20-Day Price Window
      ↓
Daily Returns
      ↓
Clean Market Prices
      ↓
Raw Market Data
      ↓
Market Data Provider
```

 This becomes extremely valuable for debugging, auditing, and financial model governance.

---

 # Transformation Architecture

 Combining the concepts from this lecture gives me a more complete architecture:

```
                  Raw Data
                     │
                     ↓
                Data Storage
                     │
                     ↓
                  Queries
                     │
                     ↓
              Data Modeling
                     │
                     ↓
               Transformation
                     │
        ┌────────────┼────────────┐
        ↓            ↓            ↓
    Cleaning     Enrichment    Aggregation
        │            │            │
        └────────────┼────────────┘
                     ↓
              Curated Dataset
                     │
        ┌────────────┼────────────┐
        ↓            ↓            ↓
    Analytics        ML       Financial Models
```

---

 # From Raw Data to Model-Ready Data

 For my particular objective, I can simplify the transformation process as:

```
Raw Financial Data
        ↓
Data Cleaning
        ↓
Data Standardization
        ↓
Data Validation
        ↓
Data Modeling
        ↓
Data Enrichment
        ↓
Feature Engineering
        ↓
Model-Ready Dataset
        ↓
Financial Model
```

 This is becoming the foundation of the architecture I want to build throughout this course.

---

 # The Importance of Understanding the Business

 Another major lesson from this lecture is that transformation cannot be designed purely from the technical side.

 I need to understand what the downstream user actually needs.

 For example, a portfolio manager may ask:

 > "I need portfolio performance."

 That statement is not yet a technical requirement.

 I need to clarify:

 - What does performance mean?
- Absolute return or relative return?
- Which benchmark?
- Which time period?
- Gross or net of fees?
- How should cash be treated?
- How should corporate actions be handled?
- How should currency conversion be performed?

 Only after understanding these questions can I design the correct transformations.

 This connects directly to the principle from the first lecture:

```
Business Need
      ↓
Requirements
      ↓
Data Requirements
      ↓
Transformation Logic
      ↓
Useful Dataset
```

---

 # Transformation Is Where Business Logic Enters the Data

 This is perhaps the most important concept I take from this lecture.

 Raw data represents what happened.

 Transformation applies the organization's interpretation of what that data means.

 For example:

```
Raw Transactions
      ↓
Business Rules
      ↓
Positions
      ↓
Portfolio Value
      ↓
Portfolio Return
```

 Therefore, transformation is not merely technical data manipulation.

 It is also the implementation of **business logic**.

---

 # My Financial Engineering Mental Model

 I now think about transformation as the layer that converts:

```
"What happened?"
```

 into:

```
"What does it mean?"
```

 For example:

```
Raw Trade
    ↓
Trade Classification
    ↓
Position Update
    ↓
Portfolio Exposure
    ↓
Risk Metrics
```

 Or:

```
Raw Price
    ↓
Clean Price
    ↓
Return
    ↓
Rolling Return
    ↓
Momentum Feature
    ↓
Model Input
```

 This is where raw financial data becomes information that can actually support decisions and models.

---

 # Queries, Modeling, and Transformation — Together

 These three components should not be thought of independently.

```
             Data
              │
              ↓
           Queries
              │
              ↓
       Retrieve Required Data
              │
              ↓
       Data Modeling
              │
              ↓
      Organize the Data
              │
              ↓
        Transformation
              │
              ↓
        Improve / Enrich
              │
              ↓
       Useful Dataset
```

 Together, they create the foundation for downstream analytics and machine learning.

---

 # What I Want to Remember

 The key ideas from this lecture are:

 - Transformation is where data engineering begins to create significant value for downstream users.
- Raw data is not automatically useful data.
- SQL is one of the most important tools for querying data.
- Queries can affect performance, cost, and reliability.
- Poor joins can cause **row explosion** and unexpectedly large datasets.
- Data modeling defines how data represents real-world entities and relationships.
- Good data models require understanding business definitions and stakeholder needs.
- Normalized data is often useful for transactional systems.
- Denormalized data can be useful for analytical workloads.
- Data transformation includes cleaning, standardization, enrichment, aggregation, and restructuring.
- Transformation can happen at multiple points throughout the data engineering lifecycle.
- Financial data often requires domain-specific transformations.
- Feature engineering is a specialized form of transformation focused on producing useful model inputs.
- Data transformation is closely connected to data quality.
- Good transformation pipelines should be reproducible, testable, and understandable.
- Data lineage helps trace model inputs back to their original sources.
- Transformation is where much of the organization's business logic gets implemented into the data platform.

---

 # Connecting Everything Learned So Far

 The lifecycle is now becoming much more concrete:

```
1. Data Generation
        ↓
2. Source Systems
        ↓
3. Data Ingestion
        ↓
4. Data Storage
        ↓
5. Queries
        ↓
6. Data Modeling
        ↓
7. Data Transformation
        ↓
8. Curated Data
        ↓
9. Analytics / ML / Financial Models
```

 And from my financial modelling perspective:

```
Market / Financial Sources
          ↓
       Ingestion
          ↓
     Raw Storage
          ↓
     Data Cleaning
          ↓
    Data Standardization
          ↓
      Data Modeling
          ↓
     Feature Engineering
          ↓
   Model-Ready Dataset
          ↓
   Financial Model
          ↓
Prediction / Valuation / Risk / Portfolio Analytics
```

 The key lesson I want to carry forward is:

 > **A data engineer does not simply move data from one system to another. The goal is to transform raw data into reliable, meaningful, and accessible information that downstream users can actually use.**

 For financial modelling, this means the data engineering pipeline ultimately becomes the foundation on which the quality of the financial model depends.

---

 # Looking Ahead

 So far, the lifecycle has covered:

```
Generate
   ↓
Ingest
   ↓
Store
   ↓
Transform
```

 The next question is:

 > **Once we have transformed data, how do we make it available to the people, applications, analytics systems, and models that need it?**

 This leads to the next stage of the data engineering lifecycle:

 **Serving Data for Downstream Use Cases.**
## Data Engineering Undercurrents

 The data engineering lifecycle is not just about moving data through a sequence of stages.

 The lifecycle we have seen so far can be summarized as:

```
Source Systems
      ↓
   Ingestion
      ↓
   Storage
      ↓
Transformation
      ↓
    Serving
      ↓
Downstream Users
```

 However, modern data engineering involves much more than the tools used to implement these stages.

 As the field has matured, data engineers have increasingly moved **up the value chain**. The role now includes practices such as security, data management, cost optimization, operational reliability, architecture, and software engineering.

 These practices apply across the entire data engineering lifecycle and influence how the systems are designed, built, and operated.

---

 ## From Technology-Focused to Value-Focused Data Engineering

 A decade ago, data engineering was often heavily focused on the technology layer.

 The primary questions might have been:

 - Which database should we use?
- Which processing framework should we use?
- How should we build the pipeline?
- Where should the data be stored?
- How do we move data from A to B?

 Modern data engineering has expanded beyond these questions.

 The role increasingly involves understanding:

 - How data should be managed
- How systems should be secured
- How pipelines should be monitored
- How infrastructure costs should be controlled
- How systems should be designed for reliability
- How workflows should be orchestrated
- How software engineering principles should be applied to data systems

 This represents a shift from simply **building data pipelines** toward **building reliable data systems that create business value**.

---

 ## The Data Engineering Lifecycle

 The lifecycle provides the main stages through which data moves:

```
Data Generation
      ↓
    Ingestion
      ↓
    Storage
      ↓
Transformation
      ↓
    Serving
```

 But these stages do not operate independently.

 There are cross-cutting concerns that influence **every stage** of the lifecycle.

 These are referred to as the **undercurrents of data engineering**.

---

 ## What Are Data Engineering Undercurrents?

 I think of the undercurrents as the principles and practices that run underneath the entire data engineering lifecycle.

 Instead of thinking about them as additional pipeline stages, it is better to think of them as **layers that affect every stage**.

```
                 Data Engineering Lifecycle
 ┌─────────────────────────────────────────────────┐
 │ Generation → Ingestion → Storage → Transform → Serve │
 └─────────────────────────────────────────────────┘
                       ↑
              Cross-Cutting Practices
                       │
       ┌───────────────┼────────────────┐
       │               │                │
    Security      Data Management    Data Ops
       │               │                │
    Architecture   Orchestration   Software Engineering
```

 The major undercurrents introduced in this lecture are:

 1. **Security**
2. **Data Management**
3. **DataOps**
4. **Data Architecture**
5. **Orchestration**
6. **Software Engineering**

 These concepts will become increasingly important as the course progresses.

---

 ## 1\. Security

 Security is not something that should be added at the end of a data pipeline.

 It needs to be considered throughout the lifecycle.

 For example:

 - Who can access the source data?
- Who can access the storage layer?
- Who can modify the data?
- Is sensitive data encrypted?
- How are credentials managed?
- How long should users retain access?
- What happens when someone's access should be revoked?

 This connects directly with the AWS **Shared Responsibility Model** discussed earlier.

 As a data engineer, security becomes part of the architecture rather than simply an operational task.

---

 ## 2\. Data Management

 Data management is concerned with how an organization manages its data as an important organizational asset.

 This includes areas such as:

 - Data quality
- Data governance
- Data ownership
- Metadata
- Data discovery
- Data lineage
- Data retention
- Data accessibility

 For example, having a pipeline that successfully moves data from a database into a data warehouse does not necessarily mean that the resulting data is useful.

 We also need to know:

 > **What does this data mean, where did it come from, who owns it, and can we trust it?**

 This becomes especially important in financial modelling.

 A financial model might depend on fields such as:

```
revenue
cost
EBITDA
net_income
shares_outstanding
debt
cash
```

 But before using these fields, we need to understand their definitions.

 For example, two datasets may both contain a field called `revenue`, while using different accounting definitions or reporting periods.

 Therefore:

```
Data Management
       ↓
Understanding Meaning
       ↓
Data Quality & Governance
       ↓
Reliable Financial Analysis
```

---

 ## 3\. DataOps

 DataOps applies operational and engineering practices to data systems.

 The objective is to make data systems:

 - Reliable
- Repeatable
- Observable
- Testable
- Maintainable
- Easier to deploy and operate

 Instead of manually running a data pipeline and hoping that everything works, DataOps encourages automation and operational discipline.

 For example:

```
Code Change
    ↓
Automated Tests
    ↓
Pipeline Deployment
    ↓
Pipeline Execution
    ↓
Monitoring
    ↓
Alerts
```

 This becomes particularly important when financial models depend on regularly updated data.

 A valuation model that works perfectly on your laptop is not necessarily a reliable production system.

---

 ## 4\. Data Architecture

 Data architecture concerns how the different components of a data system fit together.

 It answers questions such as:

 - Where should data be stored?
- How should data flow through the system?
- Which systems should communicate with each other?
- Which workloads should be batch versus streaming?
- How should the architecture scale?
- How should reliability be achieved?
- What are the cost implications of different design choices?

 This connects directly to the earlier principle:

```
Business Need
      ↓
Requirements
      ↓
Architecture
      ↓
Technology
      ↓
Implementation
```

 Architecture should therefore be driven by requirements rather than by simply choosing technologies that happen to be popular.

---

 ## 5\. Orchestration

 Data engineering systems often contain many different tasks.

 For example:

```
Extract Market Data
        ↓
Validate Data
        ↓
Store Raw Data
        ↓
Transform Data
        ↓
Calculate Metrics
        ↓
Update Warehouse
        ↓
Refresh Financial Model
```

 Someone or something needs to coordinate these tasks.

 This is where **orchestration** becomes important.

 An orchestration system can help manage:

 - Task dependencies
- Scheduling
- Retries
- Failures
- Monitoring
- Execution order
- Workflow status

 Instead of manually running each step, we can define the workflow and allow an orchestration system to manage it.

---

 ## 6\. Software Engineering

 Modern data engineering is also increasingly connected to software engineering.

 Data pipelines are software systems.

 Therefore, data engineers benefit from practices such as:

 - Version control
- Testing
- Modular code
- Documentation
- Code review
- CI/CD
- Error handling
- Logging
- Reusable components

 This is particularly relevant to my approach of building financial modelling projects.

 If I create a financial data pipeline that downloads market data, transforms it, calculates financial metrics, and feeds a model, I should treat that pipeline as **production software**, rather than simply as a collection of notebooks.

 For example:

```
Raw Data
   ↓
Python / SQL Code
   ↓
Tests
   ↓
Transformation
   ↓
Validated Dataset
   ↓
Financial Model
```

 The goal is not merely:

 > "The code runs."

 The better goal is:

 > **"The system is reliable, reproducible, testable, and understandable."**

---

 ## My Perspective: Applying the Undercurrents to Financial Modelling

 This is where I see a strong connection between data engineering and financial modelling.

 A financial model is ultimately dependent on data.

 For example, consider a simple valuation workflow:

```
Financial Statements
        +
Market Data
        +
Company Information
        ↓
     Ingestion
        ↓
      Storage
        ↓
 Data Cleaning & Validation
        ↓
 Financial Transformations
        ↓
 Financial Metrics
        ↓
 Valuation Model
        ↓
 Investment Analysis
```

 But the quality of the final model depends on much more than the transformation logic.

 We also need to consider:

 | Undercurrent | Financial Modelling Application |
| --- | --- |
| Security | Protect financial and sensitive company data |
| Data Management | Define financial metrics and maintain data quality |
| DataOps | Make model-data pipelines reliable and repeatable |
| Data Architecture | Design how market and financial data flows through the system |
| Orchestration | Schedule data updates and model refreshes |
| Software Engineering | Version, test, document, and maintain modelling code |

This makes the undercurrents particularly relevant to the financial-data projects I want to build.

---

 ## From Financial Model to Financial Data System

 One important shift in my thinking is that I don't want to treat financial modelling as simply:

```
Excel / Python
      ↓
Financial Model
      ↓
Output
```

 Instead, I want to think about the complete data system behind the model:

```
External Sources
       ↓
    Ingestion
       ↓
   Raw Storage
       ↓
Data Validation
       ↓
Transformation
       ↓
Financial Data Model
       ↓
Financial Calculations
       ↓
Valuation / Risk / Analytics
       ↓
    End Users
```

 And running across all of these stages:

```
Security
Data Management
DataOps
Architecture
Orchestration
Software Engineering
```

 This is a much more complete way of thinking about financial modelling.

---

 ## The Bigger Picture

 The lifecycle tells us **what happens to data**.

 The undercurrents tell us **how we should build and operate the systems that make it happen**.

 So I can think about the two concepts together:

```
                 DATA ENGINEERING
                       │
        ┌──────────────┴──────────────┐
        │                             │
    Lifecycle                    Undercurrents
        │                             │
        ▼                             ▼
 Generation                      Security
 Ingestion                       Data Management
 Storage                         DataOps
 Transformation                  Architecture
 Serving                         Orchestration
                                  Software Engineering
```

 The combination is what turns a collection of data pipelines into a **reliable data platform**.

---

 ## Key Takeaway

 The biggest takeaway from this lecture for me is that data engineering is no longer simply about moving data from one system to another.

 The field is moving **up the value chain**.

 A strong data engineer needs to understand not only how to build pipelines, but also:

 - Why the system exists
- Who depends on it
- How the data should be managed
- How the system should be secured
- How it should be monitored
- How it should scale
- How it should be orchestrated
- How the code should be maintained
- How much the system costs
- How reliable the resulting data is

 For my financial modelling projects, this gives me a useful framework:

```
Business / Investment Question
             ↓
       Data Requirements
             ↓
      Data Architecture
             ↓
         Lifecycle
             ↓
        Undercurrents
             ↓
     Reliable Financial Data
             ↓
       Financial Models
             ↓
    Decision / Investment Insight
```

 The goal is therefore not just to **build a financial model**.

 It is to build the **data engineering system that can reliably feed, maintain, validate, and support financial models**.
## Security as a Core Principle of Data Engineering

Data engineering is not just about collecting, transforming, storing, and serving data. It is also about ensuring that the data remains secure throughout its lifecycle.

Organizations often work with sensitive information, including personal customer data, financial records, proprietary business information, and confidential operational data. When a data engineer builds pipelines and infrastructure to process this information, they also become responsible for helping protect it.

The central lesson from this lecture is:

> **Security should not be treated as an additional feature added after building a data system. It should be a fundamental consideration throughout the design, implementation, and operation of that system.**

This becomes particularly important in financial modelling, where data may include portfolio holdings, transaction histories, client information, trading strategies, financial statements, and proprietary model assumptions.

---

## The Data Engineer's Responsibility for Security

A data engineer is entrusted with building systems that allow data to move between different sources, storage systems, applications, and users.

Every connection between these components introduces potential security considerations.

A simplified view is:

```
Data Sources
     ↓
Data Ingestion
     ↓
Data Transformation
     ↓
Data Storage
     ↓
Data Access & Delivery
     ↓
Analytics / ML / Financial Models
```

At every stage, we need to consider:

- Who can access the data?
- What information are they allowed to see?
- Which system resources can they use?
- How is sensitive information protected?
- What happens if credentials are compromised?
- Could data accidentally become publicly accessible?
- How can we prevent unauthorized access or data leakage?

The responsibility of a data engineer therefore extends beyond making a pipeline work correctly.

A pipeline may successfully ingest, transform, and deliver data while still being fundamentally insecure.

For example, a financial data pipeline might calculate portfolio returns accurately but store its output in a database that allows unauthorized users to access client-level information.

From a technical perspective, the pipeline works. From a business and security perspective, the system has failed.

This distinction reinforces an important principle:

> **A reliable data system must protect not only the accuracy and availability of data, but also its confidentiality.**

---

## Principle 1 — The Principle of Least Privilege

One of the key security concepts introduced in this lecture is the **principle of least privilege**.

The principle states that users, applications, and systems should receive only the permissions necessary to perform their responsibilities, and only for as long as those permissions are required.

In other words, access should be limited by both **scope and duration**.

For example, a data analyst who needs to calculate portfolio performance may require access to historical prices, portfolio weights, and transaction records. They may not need permission to modify production databases, administer cloud infrastructure, or access unrelated client information.

A simplified view is:

```
User / Application
        ↓
  Required Task
        ↓
 Identify Necessary Access
        ↓
 Grant Minimum Permissions
        ↓
 Review / Revoke When Needed
```

### Why excessive permissions are dangerous

Suppose every employee in a financial analytics team has administrator access to the production data platform.

This creates unnecessary risk.

- An accidental command could delete important data.
- A compromised account could expose the entire database.
- An application vulnerability could be exploited to access unrelated resources.
- A user could modify data outside their responsibilities.
- A temporary permission could remain active long after it is needed.

The principle of least privilege reduces the potential impact of these situations.

The lecture also emphasizes that this principle applies to the data engineer personally.

For example, having administrator permissions available does not mean they should be used for every task. Routine development and data processing should use appropriately restricted accounts wherever possible.

### Applying least privilege to financial modelling

Imagine that I am building a portfolio analytics platform.

Different users might require different permissions:

| User / System | Required Access |
| --- | --- |
| Market-data ingestion pipeline | Write access to the designated market-data tables |
| Financial analyst | Read access to approved historical market data |
| Portfolio manager | Access to authorized portfolio analytics and performance reports |
| Risk model | Read access to the specific portfolio and market inputs required for calculations |
| Data engineer | Limited development access, with separately controlled production privileges |
| Platform administrator | Elevated permissions for infrastructure administration when required |

These permissions should be designed around actual responsibilities rather than convenience.

The key idea is that **access should be granted because a task requires it, not simply because granting access is easier**.

---

## Principle 2 — Minimize the Sensitive Data You Collect

Another important lesson is that security begins before data enters the system.

The lecture makes a particularly useful point: one of the best ways to protect sensitive data is to avoid collecting it when it is not necessary.

If sensitive information is never ingested or stored, it cannot be exposed through a breach of that particular system.

This introduces the concept of **data minimization**.

The process can be represented as:

```
Business Requirement
        ↓
Identify Required Data
        ↓
Determine What Is Necessary
        ↓
Exclude Unnecessary Sensitive Data
        ↓
Ingest and Store Only What Is Needed
```

For example, suppose a financial model only needs daily security prices, portfolio weights, and benchmark returns to calculate historical portfolio performance.

There may be no reason to ingest client names, personal addresses, account identifiers, or other personally identifiable information into the modelling environment.

Instead, the model could operate using internal portfolio identifiers or appropriately pseudonymized records.

This reduces the amount of sensitive information exposed to the system.

### Why this matters

Collecting unnecessary sensitive data creates additional responsibilities:

- Access controls must protect it.
- Storage systems must be secured.
- Retention and deletion policies must be applied.
- Data transfers introduce additional exposure.
- Monitoring and auditing become more complicated.
- A potential breach may affect more information.

This leads to an important design principle:

> **Before deciding how to secure a piece of data, first ask whether the system needs that data at all.**

For financial modelling, this is particularly useful when separating the data required for quantitative calculations from the personal or commercially sensitive information associated with the underlying business.

---

## Principle 3 — Security in Cloud-Based Data Systems

Modern data engineering frequently relies on cloud infrastructure.

Cloud platforms make it possible to build scalable pipelines, store large datasets, and deliver data to applications and analytics systems. However, they also introduce additional security considerations.

The lecture specifically highlights three important areas:

- Identity and Access Management (IAM)
- Encryption
- Networking protocols and configuration

### Identity and Access Management (IAM)

IAM determines which users, applications, and services can access particular resources and what actions they can perform.

For example, an AWS-based financial data platform might use IAM policies to control which services can read market data, write transformed datasets, or access production storage.

The goal is to enforce least privilege through explicit and appropriately scoped permissions.

### Encryption

Encryption helps protect data from unauthorized disclosure.

Two important situations are:

- **Encryption at rest:** Protecting data stored in databases, data warehouses, object storage, or backup systems.
- **Encryption in transit:** Protecting data as it moves between systems, typically using secure communication protocols such as TLS.

For example, historical market data transferred from an external provider to a cloud-based data platform should be protected during transmission. Sensitive datasets stored in the platform should also be protected through appropriate storage encryption and access controls.

Encryption is important, but it does not replace authorization. An encrypted database can still be exposed if unauthorized users receive valid access credentials or excessive permissions.

### Networking and exposure

Cloud resources should be reachable only through the network paths required for their intended purpose.

For example, a financial data warehouse used by internal analytics applications should not automatically be accessible from the public internet.

A simplified secure architecture might look like this:

```
External Market-Data Provider
             ↓
       Secure Ingestion
             ↓
     Controlled Cloud Network
             ↓
       Protected Storage
             ↓
     Authorized Applications
             ↓
       Financial Analytics
```

The objective is to reduce unnecessary exposure while allowing legitimate data flows to operate.

### A practical AWS example

The lecture mentions cases where engineers unintentionally leave an AWS S3 bucket, server, or database publicly accessible.

In a financial modelling environment, this could expose historical transactions, portfolio information, model outputs, or confidential research.

Preventive measures include:

- Blocking public access to S3 buckets unless explicitly justified.
- Using appropriately scoped IAM roles and policies.
- Avoiding hard-coded credentials in source code.
- Restricting network access to authorized systems.
- Encrypting sensitive data at rest and in transit.
- Auditing permissions and monitoring suspicious activity.
- Separating development, testing, and production environments.

These controls should be implemented deliberately rather than relying on the assumption that cloud infrastructure is secure by default.

---

## Security Is Also About People

An important aspect of this lecture is that security is not purely a technical problem.

Even a well-designed architecture can be compromised by human mistakes or irresponsible behaviour.

The lecturer highlights examples such as:

- Sharing passwords insecurely.
- Falling victim to phishing attacks.
- Revealing confidential information to unauthorized individuals.
- Misconfiguring cloud resources.
- Forgetting to apply basic security practices.
- Using privileged accounts unnecessarily.

A phishing attack, for example, may involve an attacker impersonating a trusted person or organization to persuade an employee to reveal credentials.

If those credentials provide access to a production data platform, a single mistake can create consequences far beyond the individual account.

This is why security must become part of the working habits of everyone involved in a data system.

### Developing a defensive mindset

The lecture encourages data engineers to anticipate how systems could fail or be attacked.

Instead of asking only:

> "How do I make this pipeline work?"

We should also ask:

> "How could this pipeline expose data, and what would happen if someone gained unauthorized access?"

For a financial modelling pipeline, this might involve considering:

- What happens if an API key is leaked?
- What happens if an object-storage bucket becomes public?
- What happens if an analyst accidentally overwrites production data?
- What happens if a third-party data provider sends malicious or unexpected input?
- What happens if a compromised application accesses data outside its intended scope?
- What happens if confidential model outputs are shared with the wrong users?

Thinking through these scenarios helps identify weaknesses before they become incidents.

Security therefore involves both preventive controls and the ability to detect, investigate, and respond to problems.

---

## Security Theater vs. a Genuine Security Culture

One of the most interesting concepts introduced in this lecture is **security theater**.

Security theater occurs when an organization appears secure because it follows checklists, documents policies, or demonstrates compliance, but its everyday practices do not meaningfully protect its systems and data.

For example, an organization might require employees to complete annual security training while still allowing:

- Excessive administrator permissions.
- Shared credentials.
- Publicly accessible storage containing sensitive data.
- Unreviewed access to production systems.
- Weak monitoring of critical data infrastructure.

In such an environment, security exists in documentation but not necessarily in operational practice.

The distinction can be represented as:

```
Security Theater
       ↓
Policies + Checklists + Compliance
       ↓
Limited Practical Protection
```

Compared with:

```
Genuine Security Culture
       ↓
Policies + Technical Controls + Awareness
       ↓
Consistent Secure Behaviour
       ↓
Reduced Security Risk
```

Compliance requirements remain important, particularly in financial services. However, compliance alone should not be treated as proof that a system is secure.

A genuine security culture requires individuals and teams to understand their responsibilities, recognize vulnerabilities, and consistently apply appropriate controls.

Security must be supported by both technology and organizational behaviour.

---

## My Perspective: Applying Security to Financial Modelling

Financial modelling often involves bringing together market data, company financials, portfolio information, transaction records, economic indicators, and proprietary assumptions.

Although not every financial dataset is confidential, many financial systems contain information that must be protected against unauthorized access, modification, or disclosure.

This means that security should be considered alongside data quality, performance, reproducibility, and model accuracy.

### Example — Building a Portfolio Analytics Pipeline

Imagine I am developing a system that collects market data, calculates portfolio returns, and generates risk reports.

The pipeline might look like this:

```
Market-Data APIs
       ↓
Data Ingestion
       ↓
Raw Market Data
       ↓
Data Validation & Transformation
       ↓
Portfolio / Risk Calculations
       ↓
Analytics Database
       ↓
Dashboards & Reports
```

At each stage, security introduces specific design questions.

| Pipeline Stage | Security Consideration |
| --- | --- |
| Data ingestion | Protect API credentials and restrict which services can access external providers |
| Raw storage | Restrict access and protect confidential or licensed datasets |
| Data transformation | Prevent unauthorized modification and isolate execution permissions |
| Model execution | Give models access only to the required inputs and outputs |
| Analytics database | Enforce user-specific permissions and appropriate data visibility |
| Reporting | Ensure reports are available only to authorized recipients |
| Operations | Monitor access, review permissions, and investigate unusual activity |

### Step 1 — Identify sensitive information

Before building the pipeline, determine which data is public, commercially sensitive, personally identifiable, or subject to licensing and contractual restrictions.

For example, publicly available historical stock prices have a different confidentiality profile from identifiable client holdings or proprietary investment strategies.

### Step 2 — Minimize data collection

Collect only the information needed for the intended calculations.

If portfolio returns can be calculated using pseudonymous portfolio identifiers, there may be no need to expose client identities to the modelling environment.

### Step 3 — Define access permissions

Determine which users and services need to read, write, or administer each dataset.

For example, a risk model may need permission to read portfolio holdings and market prices but should not automatically receive permission to modify the source data or administer the cloud platform.

### Step 4 — Protect data and credentials

Use appropriate encryption, secure credential management, controlled networking, and restricted storage access.

Credentials should not be committed to a GitHub repository, even if the repository is private.

### Step 5 — Monitor and review

Security is not a one-time configuration task.

Permissions can become excessive, infrastructure configurations can change, and new applications can introduce additional access paths.

Regular reviews and monitoring help ensure that security controls remain effective as the system evolves.

The broader lesson is that **a financial model should not be considered production-ready simply because its calculations are correct**. Its surrounding data infrastructure must also protect the information on which the model depends.

---

## Security, Data Quality, and Model Reliability

Security is closely related to other important properties of a data system.

For financial modelling, I find it useful to distinguish between three dimensions:

| Dimension | Core Question | Financial Modelling Example |
| --- | --- | --- |
| Data quality | Is the data accurate and fit for purpose? | Are prices, dates, and corporate actions correct? |
| Security | Is the data protected from unauthorized access or modification? | Can only authorized users access confidential portfolio data? |
| Reliability | Does the system operate consistently as expected? | Can the pipeline recover from failures and produce reproducible outputs? |

These dimensions are different, but they reinforce one another.

For example, unauthorized modification of historical prices could compromise the integrity of a backtest. A model might execute successfully and produce plausible results while relying on data that has been maliciously altered.

Similarly, a security breach could expose proprietary trading signals or investment strategies even if every numerical calculation is correct.

This suggests that secure data engineering is not separate from quantitative research. It is part of creating trustworthy analytical systems.

---


For my GitHub-based learning projects, I also want to maintain a clear distinction between source code and sensitive data. Example datasets, synthetic financial records, and environment-variable templates can be used to demonstrate the architecture without exposing real credentials or confidential information.

---

## Key Takeaways

This lecture reinforces several principles that I want to carry into future data engineering projects.

1. **Security begins with system design.** It should not be postponed until after the pipeline has been implemented.
2. **Apply the principle of least privilege.** Users, applications, and engineers should operate with only the access they require.
3. **Minimize sensitive data.** Avoid collecting information that has no clear purpose in the system.
4. **Understand cloud security fundamentals.** IAM, encryption, networking, and storage permissions are essential parts of cloud-based data engineering.
5. **Adopt a defensive mindset.** Anticipate potential attacks, configuration errors, credential leaks, and accidental data exposure.
6. **Build a genuine security culture.** Security depends on consistent behaviour across the organization, not just policies and compliance checklists.
7. **Treat security as part of financial-model reliability.** Correct calculations are not enough if the underlying data or model outputs are exposed or compromised.

The most important shift in my thinking is that a data engineer is not simply responsible for moving data from one place to another. The engineer also helps determine who can access that data, how it is protected, and how the organization can use it responsibly.

For financial modelling, this means treating security as a foundational requirement alongside data quality, reproducibility, and analytical accuracy.

---

## Looking Ahead — Data Management

The lecture concludes by introducing the next underlying concept in the data engineering lifecycle: **data management**.

Security focuses on protecting data and controlling access. Data management takes a broader view of how data is governed, organized, maintained, documented, and made useful throughout its lifecycle.

These concepts are closely connected.

For example, managing a financial dataset involves more than storing historical prices in a database. It also involves understanding where the data came from, how it has been transformed, who owns it, how reliable it is, how long it should be retained, and who is authorized to use it.

This creates a natural progression:

```
Business Requirements
        ↓
Data Architecture
        ↓
Data Collection & Processing
        ↓
Security & Access Control
        ↓
Data Management & Governance
        ↓
Trustworthy Financial Analytics
```


## Data Architecture: Designing Systems for Evolving Needs

In the earlier lectures, we explored how to understand stakeholder requirements, identify business value, manage data, and protect sensitive information. Data architecture brings these concepts together by defining how a data system should be structured to achieve its objectives.

The central idea is that data architecture is not simply about choosing databases, cloud platforms, or processing frameworks. It is about designing a system that satisfies business requirements while remaining flexible, reliable, secure, and cost-effective as those requirements evolve.

The lecture defines data architecture as:

> **The design of systems to support the evolving data needs of an enterprise, achieved through flexible and reversible decisions and a careful evaluation of trade-offs.**

This definition highlights three important ideas:

- **Evolving needs:** A good architecture should support the organization's future requirements, not just its immediate needs.
- **Flexible and reversible decisions:** Components should be designed so that changes can be made without rebuilding the entire system.
- **Trade-offs:** Architectural decisions require balancing performance, scalability, reliability, security, and cost.

These principles are particularly relevant to financial modelling because financial data systems often evolve from simple analytical scripts into larger platforms supporting portfolio analytics, risk management, backtesting, and business reporting.

---

## Thinking Like a Data Architect

The lecture makes an important distinction between the roles of a data engineer and a data architect.

A data architect is often responsible for defining the overall design of a data system, while a data engineer implements and maintains the pipelines and infrastructure that make the design work.

However, these responsibilities can overlap, especially in smaller organizations or startups.

Even when a data engineer is not directly responsible for architectural decisions, understanding how systems are designed makes it easier to implement solutions effectively and recognize potential problems before they become expensive to fix.

A simplified view is:

```
Business Needs
      ↓
Stakeholder Requirements
      ↓
System Requirements
      ↓
Data Architecture
      ↓
Technology Selection
      ↓
Implementation
      ↓
Monitoring & Improvement
```

This builds on an idea introduced earlier in the course: technology selection should follow an understanding of the problem.

For example, suppose I want to build a financial modelling platform.

A technology-first approach might immediately lead me to choose a cloud provider, database, orchestration framework, and processing engine.

An architecture-first approach would begin with different questions:

- What financial problems should the system solve?
- Which datasets are required?
- How frequently must those datasets be updated?
- How much historical data must be retained?
- How many models and users will the system support?
- What are the requirements for security and reproducibility?
- How should the system behave when a pipeline fails?
- What are the budget and performance constraints?

Only after understanding these requirements can I make informed architectural decisions.

The objective is not to build the most sophisticated system possible. It is to build a system that is appropriate for the problem and can evolve as the problem changes.

---

## Principle 1 — Choose Common Components Wisely

Common components are the parts of a data architecture used by multiple teams, applications, or projects.

Examples include:

- Shared databases and data warehouses
- Centralized data ingestion pipelines
- Data catalogs and metadata systems
- Authentication and access-control services
- Common data transformation frameworks
- Shared monitoring and logging infrastructure

Choosing common components wisely can reduce duplicated work, improve consistency, and make collaboration easier.

However, a shared component should not be selected simply because it is already available. It must provide the capabilities required by the different users and systems that depend on it.

### Applying this to financial modelling

Imagine that I am building three projects:

1. A historical stock-price analysis system
2. A portfolio performance calculator
3. A financial risk analytics platform

All three projects may need access to historical market data.

Instead of independently downloading and storing the same information in each project, I could establish a common market-data layer.

```
                 Market-Data Providers
                          ↓
                  Shared Ingestion
                          ↓
                 Historical Data Store
                    /      |      \
                   ↓       ↓       ↓
              Stock      Portfolio   Risk
              Analysis   Analytics   Models
```

This approach creates a consistent source of market data and reduces unnecessary duplication.

However, the shared component should have clearly defined data contracts, access permissions, quality checks, and ownership.

For example, if one project requires adjusted daily prices while another requires intraday observations, the architecture must support those differences rather than forcing every project into an unsuitable format.

**The key lesson:** Reuse common components where they create genuine value, but design them around the requirements of their users.

---

## Principle 2 — Plan for Failure

A good data architecture must account for situations where components stop working as expected.

Failures can occur because of:

- Network interruptions
- API rate limits
- Cloud-service outages
- Invalid or incomplete input data
- Database connection failures
- Programming errors
- Expired credentials
- Unexpected increases in workload

A system that works only when every component behaves perfectly is not sufficiently robust for important business processes.

Planning for failure means designing systems that can detect problems, recover from them, and prevent failures from silently corrupting downstream results.

A simplified failure-aware pipeline might look like this:

```
Data Source
    ↓
Ingestion Pipeline
    ↓
Validation Checks
    ↓
Storage
    ↓
Financial Model
    ↓
Output Validation
    ↓
Reports
```

At each stage, the system should have appropriate monitoring, error handling, and recovery mechanisms.

For example, if an external market-data API becomes unavailable, the pipeline should not silently replace missing prices with zeros and continue calculating portfolio returns.

Depending on the requirements, it could retry the request, use an approved historical snapshot, quarantine incomplete data, or stop the calculation and raise an alert.

The correct response depends on the use case.

### Applying this to financial modelling

Consider a daily portfolio valuation pipeline.

If the pipeline fails to retrieve prices for several securities, the system must recognize that the resulting portfolio valuation may be incomplete.

Possible safeguards include:

- Retrying temporary API failures
- Detecting missing instruments or dates
- Recording failed ingestion attempts
- Preserving the last successfully validated dataset
- Preventing incomplete inputs from being published as valid results
- Alerting the responsible person or team
- Supporting safe recovery and reruns

An important distinction is that **technical failure and data-quality failure are not the same thing**.

A pipeline may run successfully while receiving incorrect prices. Therefore, the architecture must handle both operational failures and invalid data.

---

## Principle 3 — Architect for Scalability

Scalability refers to a system's ability to handle changes in workload without requiring a complete redesign.

A scalable system can accommodate increased demand and, where supported, reduce resource usage when demand decreases.

This matters because data workloads rarely remain constant.

A financial modelling project may initially process a few securities using daily observations. Over time, it might expand to thousands of instruments, longer historical periods, multiple portfolios, and more complex risk calculations.

A system that is appropriate for the initial workload may become inefficient as the project grows.

### Two important approaches

**Vertical scaling** means increasing the resources available to a single system, such as providing a server with more memory or processing power.

**Horizontal scaling** means distributing work across additional machines or processing units.

The appropriate approach depends on the workload, the technology, and the complexity of the problem.

### Example: Scaling a financial data pipeline

Suppose I initially calculate daily returns for 20 stocks using a local Python script.

As the project develops, I want to process:

- Thousands of financial instruments
- Multiple years of historical data
- Several portfolios and benchmarks
- Daily portfolio rebalancing
- Large-scale backtests
- Multiple risk scenarios

The architecture may need to evolve from a simple local script into a pipeline with scheduled ingestion, persistent storage, incremental transformations, and more powerful processing infrastructure.

```
Initial Project
Local Python Script
        ↓
Growing Workload
        ↓
Scheduled Data Pipeline
        ↓
Structured Historical Storage
        ↓
Incremental Processing
        ↓
Scalable Analytics Platform
```

However, scalability does not mean using distributed computing from the beginning.

For a small dataset, a well-designed Python script using pandas may be entirely sufficient.

Introducing distributed processing too early can increase cost, complexity, and maintenance effort without delivering meaningful benefits.

**The objective is to make the system capable of evolving when the workload justifies it, rather than building unnecessary complexity into the initial design.**

---

## Principle 4 — Architecture Is Leadership

The lecture introduces the idea that architecture is also a form of leadership.

Architectural decisions influence how teams work together, how responsibilities are divided, and how easily other people can understand and maintain a system.

A good architecture can make it easier for different teams to collaborate. A poorly designed system can create dependencies, duplicated work, unclear ownership, and unnecessary technical complexity.

Even as a junior data engineer, I can develop architectural thinking by:

- Understanding why a system was designed in a particular way
- Documenting important design decisions
- Asking questions about trade-offs
- Seeking feedback from experienced engineers and architects
- Considering how other users will interact with my pipelines
- Designing components that are easier to test and maintain

### Applying this to financial modelling

A financial modelling project may eventually involve data engineers, quantitative researchers, analysts, risk managers, and software developers.

Each group has different requirements.

For example, a quantitative researcher may want flexible access to historical data, while a risk team may require reproducible calculations, controlled inputs, and documented validation procedures.

A good architecture provides a structure that allows these users to work effectively without compromising the needs of others.

Thinking like an architect therefore means looking beyond the code being written today and considering how the system will be understood, used, and maintained by other people.

---

## Principle 5 — Always Be Architecting

Data architecture is not a one-time activity.

An architecture that satisfies an organization's needs today may become unsuitable as its business requirements, workloads, data sources, or technologies change.

The lecture emphasizes that architects should continually evaluate their systems and update the design when necessary.

For example, a financial analytics platform may initially rely on one market-data provider. Later, the organization may need additional exchanges, alternative data sources, or more frequent updates.

The original architecture might need to accommodate new ingestion pipelines, additional storage requirements, or revised data-quality checks.

A useful way to think about this process is:

```
Understand Requirements
         ↓
Design Architecture
         ↓
Build the System
         ↓
Monitor Performance
         ↓
Identify New Requirements
         ↓
Evaluate Trade-offs
         ↓
Improve the Architecture
         ↺
```

This creates a continuous feedback loop between business needs and technical implementation.

### Applying this to financial modelling

Suppose my initial project calculates historical returns for a single portfolio.

Later, I want to support multiple portfolios, benchmark comparisons, transaction costs, portfolio rebalancing, and risk attribution.

These changes may require improvements to the data model, processing pipeline, and storage design.

Instead of treating the initial implementation as permanent, I should review the architecture whenever important requirements change.

This does not mean constantly rewriting the system. It means recognizing when a design decision no longer serves its intended purpose and making deliberate improvements.

---

## Principle 6 — Build Loosely Coupled Systems

A loosely coupled architecture consists of components that interact through well-defined interfaces without depending excessively on one another's internal implementation.

This makes it easier to change one component without redesigning the entire system.

For example, a financial data pipeline might contain separate components for:

- Data ingestion
- Data validation
- Data transformation
- Data storage
- Financial calculations
- Reporting

Each component should have a clear responsibility and a defined way of exchanging information with the others.

```
Market-Data Source
        ↓
   Ingestion Layer
        ↓
 Validation Layer
        ↓
  Storage Layer
        ↓
 Calculation Layer
        ↓
 Reporting Layer
```

If the storage technology changes, the financial calculation logic should not necessarily need to be rewritten.

Similarly, replacing one market-data provider should not require redesigning every downstream model, provided the new provider can be integrated through the existing interface.

### Applying this to financial modelling

Imagine that my portfolio analytics project initially obtains prices from one API.

Later, I decide to switch providers because the original service becomes too expensive or no longer meets the project's requirements.

If the data-fetching logic is tightly embedded throughout the modelling code, the change could require extensive modifications.

A better design separates provider-specific logic from the rest of the system.

For example:

```
Provider A ──┐
             ├──> Standardized Market-Data Interface
Provider B ──┘                  ↓
                         Validation & Storage
                                  ↓
                          Financial Models
```

The standardized interface could produce a consistent structure containing fields such as instrument identifier, observation date, price, currency, and source.

The downstream model then consumes that standardized structure rather than depending directly on the details of a particular provider.

This separation improves maintainability and makes future changes easier.

---

## Principle 7 — Make Reversible Decisions

The lecture connects loose coupling with another architectural principle: **make reversible decisions whenever practical**.

A reversible decision is one that can be changed without excessive cost or disruption.

Not every architectural decision can be reversed easily. However, good design reduces unnecessary dependence on decisions that may become unsuitable in the future.

For example, choosing a cloud provider, storage format, database, or orchestration framework can influence a system for years.

The more tightly the system depends on a particular technology, the more difficult it may be to replace that technology later.

### Applying this to financial modelling

Suppose I build a market-data pipeline that stores historical prices in a structured format and exposes them through a clearly defined interface.

My financial models depend on the interface rather than on provider-specific APIs or storage details.

If I later change the underlying storage technology, I may be able to preserve most of the modelling logic.

By contrast, if every model directly queries a particular database using custom queries and provider-specific assumptions, migrating the system may become much more difficult.

Reversibility can be encouraged through:

- Well-defined interfaces
- Modular code
- Standardized data schemas
- Configuration separated from application logic
- Documented data contracts
- Automated tests
- Avoiding unnecessary dependence on proprietary features

However, flexibility has a cost.

Trying to make every component interchangeable can introduce additional abstractions and complexity. The objective is not to eliminate all dependencies, but to make important future changes manageable.

---

## Principle 8 — Prioritize Security

Security is a foundational architectural requirement rather than a feature that should be added after implementation.

Earlier lectures introduced the principle of least privilege, data minimization, encryption, and the importance of a genuine security culture.

This lecture reinforces that security must be considered throughout the design of the architecture.

For example, a financial analytics platform may contain market data, confidential portfolio holdings, proprietary model outputs, and API credentials.

The architecture should determine how these resources are protected and which users or services can access them.

Important considerations include:

- Identity and access management
- Appropriate permissions for users and services
- Encryption at rest and in transit
- Secure credential management
- Network isolation where appropriate
- Separation of development and production environments
- Monitoring and auditing
- Protection against accidental public exposure

The lecture also mentions the zero-trust principle, which broadly encourages systems to verify access explicitly rather than automatically trusting users or applications because of their network location.

### Applying this to financial modelling

A financial modelling pipeline might require permission to read historical prices and portfolio weights, but it should not automatically have administrator access to the entire cloud environment.

Similarly, a reporting application should receive only the information it needs to display authorized results.

These decisions should be reflected in the architecture itself.

Security is particularly important when moving a project from local development into shared infrastructure or production environments, where more users, services, and sensitive datasets may be involved.

---

## Principle 9 — Embrace FinOps

The final principle introduced in this lecture is **FinOps**, which brings financial accountability into cloud and technology operations.

Cloud platforms often operate on a pay-as-you-go model. Resources can be provisioned quickly, scaled when needed, and released when no longer required.

This flexibility creates opportunities, but it also introduces the possibility of unnecessary spending.

A poorly designed pipeline might repeatedly process the same historical data, keep expensive computing resources running when they are idle, or store multiple redundant copies of large datasets.

FinOps encourages teams to consider cost as part of their architectural decisions.

The goal is not simply to minimize expenditure. It is to balance cost against the business value generated by the system.

### Applying this to financial modelling

Imagine that I build a cloud-based backtesting system that processes historical data across many securities and parameter combinations.

Different design choices can produce very different cost profiles.

For example:

- Running a small daily calculation on an appropriately sized resource may be cheaper than maintaining a large server continuously.
- Processing only newly arrived data can reduce repeated computation.
- Using suitable storage formats and partitioning can reduce unnecessary data scans.
- Scheduling expensive backtests when they are needed can prevent idle resource costs.
- Monitoring cloud expenditure can reveal inefficient jobs or unexpected usage.

A simplified decision framework is:

```
Business Requirement
        ↓
Estimate Workload
        ↓
Evaluate Architecture Options
        ↓
Compare Performance & Cost
        ↓
Choose an Appropriate Design
        ↓
Monitor Actual Usage
        ↓
Optimize When Necessary
```

A more powerful architecture is not automatically a better architecture.

For a small financial modelling project, local processing and inexpensive storage may provide the best balance of simplicity, performance, and cost.

As the workload grows, cloud-based processing may become more appropriate.

The key is to evaluate the trade-offs rather than assuming that the most advanced technology is necessarily the best solution.

---

## Bringing the Principles Together: A Financial Modelling Architecture

The nine principles can be combined into a practical example.

Suppose I want to develop a financial data platform that collects market prices, prepares historical datasets, calculates portfolio performance, and produces risk reports.

The architecture could evolve as follows:

```
                Market-Data Providers
                         ↓
                  Ingestion Layer
                         ↓
                 Validation Layer
                         ↓
                  Historical Storage
                         ↓
               Standardized Data Layer
                         ↓
                 Financial Calculations
                    /           \
                   ↓             ↓
           Performance         Risk
            Analytics        Analytics
                   \             /
                    ↓           ↓
                    Reports & APIs
```

Each principle influences the design:

| Principle | Architectural Application |
| --- | --- |
| Choose common components wisely | Reuse market-data ingestion and standardized datasets across projects |
| Plan for failure | Retry transient failures, validate inputs, and prevent incomplete outputs from being published |
| Architect for scalability | Support growing datasets and workloads without unnecessary redesign |
| Architecture is leadership | Document decisions and provide a system that different teams can understand |
| Always be architecting | Revisit the design as financial modelling requirements evolve |
| Build loosely coupled systems | Separate ingestion, validation, storage, calculations, and reporting |
| Make reversible decisions | Use well-defined interfaces and avoid unnecessary technology dependencies |
| Prioritize security | Restrict access, protect credentials, and secure sensitive financial data |
| Embrace FinOps | Balance processing requirements, performance, and cloud expenditure |

These principles are interconnected rather than independent.

For example, loose coupling can make decisions more reversible, planning for failure can improve reliability, and scalability decisions can affect both performance and cost.

The objective is to create an architecture in which the components work together to meet the organization's requirements without introducing unnecessary complexity.

---

## My Perspective: How I Want to Apply These Principles

As I continue learning data engineering and applying it to financial modelling, I want to distinguish between building a model and building the data system that supports the model.

A financial model might begin as a Python script that downloads prices and calculates returns. This is a reasonable starting point for experimentation.

However, as the project grows, additional requirements may emerge:

- Historical data must be retained consistently.
- Data quality must be validated automatically.
- Calculations must be reproducible.
- Pipelines must recover from failures.
- Multiple models should reuse the same datasets.
- Credentials and sensitive information must be protected.
- Processing costs must remain manageable.
- New data sources should be integrated without rewriting the entire system.

Thinking architecturally helps me anticipate these requirements and make deliberate decisions about the structure of the project.

I do not need to build a large cloud platform for every financial modelling problem. Instead, I want to start with the simplest architecture that satisfies the requirements while keeping future improvements practical.

My preferred approach is:

```
Understand the Financial Problem
              ↓
Identify Data Requirements
              ↓
Design the Simplest Suitable Architecture
              ↓
Implement Modular Components
              ↓
Validate Data & Model Outputs
              ↓
Monitor Reliability, Security & Cost
              ↓
Evolve the Architecture as Needed
```

This approach combines the business-oriented mindset introduced earlier in the course with the architectural principles covered in this lecture.

It also provides a way to avoid two common mistakes: choosing tools before understanding the problem, and building unnecessary complexity before there is a clear need for it.

---

## Key Takeaways

This lecture introduces several principles that I want to carry into future data engineering and financial modelling projects.

1. **Architecture is a blueprint for evolving business needs.** A good design should support current requirements while making future changes manageable.
2. **Architectural decisions involve trade-offs.** Performance, reliability, scalability, security, flexibility, and cost must be evaluated together.
3. **Plan for failure.** Data systems should detect problems, handle errors, and recover safely rather than assuming everything will work perfectly.
4. **Design for appropriate scalability.** Systems should be able to grow when required without introducing unnecessary complexity at the beginning.
5. **Use loose coupling and reversible decisions.** Modular components and clear interfaces make systems easier to maintain and adapt.
6. **Treat security as foundational.** Access controls, credential management, and data protection should influence the architecture from the start.
7. **Consider FinOps.** Cloud expenditure is an architectural concern because the cost of operating a system affects the value it delivers.
8. **Keep architecting over time.** Architecture should evolve as requirements, workloads, and organizational priorities change.

The most important lesson I take from this lecture is that **good data architecture is not about predicting every future requirement; it is about making thoughtful decisions today without unnecessarily limiting the choices available tomorrow**.

For financial modelling, this means designing systems that can begin simply, produce trustworthy results, and evolve into more sophisticated analytical platforms as the requirements grow.

---

## Looking Ahead — DataOps

The lecture concludes by introducing the next undercurrent of the data engineering lifecycle: **DataOps**.

Data architecture defines how a data system should be structured. DataOps focuses on the practices and processes that help teams develop, deploy, monitor, and maintain data systems reliably.

For example, a financial data pipeline may have a well-designed architecture, but it still needs automated testing, deployment processes, monitoring, and operational procedures to work consistently.

This creates a natural progression:

```
Business Requirements
        ↓
Data Architecture
        ↓
Data Engineering Implementation
        ↓
DataOps & Operational Practices
        ↓
Reliable Data Pipelines
        ↓
Trustworthy Financial Analytics
```


## DataOps: Building Reliable and Automated Data Systems


DataOps draws inspiration from DevOps, which emerged to reduce the separation between software development and software operations. Traditionally, developers wrote and tested code while separate operations teams were responsible for deploying and maintaining it. This separation often created bottlenecks, delayed releases, and made it harder to identify problems quickly.

DevOps introduced practices that emphasize automation, collaboration, continuous improvement, and rapid iteration. DataOps applies similar principles to the development and operation of data systems.

The central lesson from this lecture is:

> **Building a data pipeline is not enough. A data engineer must also ensure that the pipeline can be executed, monitored, tested, and maintained reliably over time.**

This is particularly important in financial modelling. A Python script that calculates portfolio returns may work perfectly when executed manually, but a production-quality system must also handle new data, detect failures, validate outputs, and recover when something goes wrong.

---

## Understanding DataOps

DataOps aims to improve both the development process and the quality of the data products delivered to end users.

A data product can be a dataset, a data pipeline, a data warehouse, an analytics platform, or another data system that provides value to its users.

For example, a financial data product could be a validated historical market-data dataset used by portfolio managers, quantitative researchers, and risk analysts.

DataOps combines two important dimensions.

### 1\. Cultural practices

DataOps encourages teams to:

- Collaborate with business stakeholders.
- Communicate problems openly.
- Learn from successes and failures.
- Improve systems through rapid iteration.
- Reduce unnecessary manual work.
- Identify bottlenecks and eliminate waste.

These practices are closely related to Agile, which emphasizes delivering work incrementally and improving solutions through feedback.

### 2\. Technical capabilities

The lecture identifies three core pillars of DataOps:

1. Automation
2. Observability and monitoring
3. Incident response

Together, these capabilities help create data systems that are repeatable, measurable, and recoverable.

```
                  DataOps
                     |
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
  Automation    Observability   Incident
                    &            Response
                Monitoring
       |             |             |
       ↓             ↓             ↓
 Repeatable     Early Problem   Faster &
 Processes      Detection       Reliable Recovery
       └─────────────┼─────────────┘
                     ↓
             Reliable Data Products
```

The objective is not simply to automate everything. It is to build a working process that consistently delivers trustworthy data while reducing operational effort and risk.

---

## Pillar 1 — Automation

Automation is the first pillar of DataOps.

In the early stages of a project, manually running individual pipeline tasks may be reasonable. It allows a data engineer to prototype the system quickly and understand how the different components interact.

However, as the pipeline grows, manual execution becomes increasingly inefficient and error-prone.

Imagine a financial data pipeline that requires the following steps:

1. Download market data from an API.
2. Load the data into storage.
3. Validate the incoming records.
4. Transform and standardize the data.
5. Calculate financial metrics.
6. Store the results.
7. Generate reports.

If each step must be started manually, the engineer needs to remember the correct order, wait for each process to finish, inspect the results, and launch the next process.

This becomes difficult to maintain as the number of datasets and calculations increases.

### From manual execution to automation

The lecture describes three approaches to executing data pipelines.

#### Approach 1 — Manual execution

Each task is started manually after the previous task finishes.

```
Run Ingestion
     ↓
Check Results
     ↓
Run Transformation
     ↓
Check Results
     ↓
Run Financial Calculations
     ↓
Generate Reports
```

This can work for experimentation and early prototypes.

However, it becomes problematic when the pipeline must run regularly or contains many dependent tasks.

#### Approach 2 — Pure scheduling

In a scheduling-based approach, tasks are configured to start at predetermined times.

For example:

```
12:00 AM → Ingest Market Data
12:30 AM → Transform Data
01:00 AM → Calculate Returns
01:30 AM → Generate Reports
```

This reduces manual effort, but it introduces an important limitation.

The schedule assumes that the previous task will finish within the expected time.

If market-data ingestion takes longer than usual, the transformation task might start before ingestion has completed. If ingestion fails, downstream tasks may still run unless additional safeguards have been implemented.

Scheduling automates when a task starts, but does not inherently guarantee that its dependencies have been satisfied.

#### Approach 3 — Orchestration

Orchestration frameworks manage the execution of tasks based on their dependencies, execution status, and configured schedules.

Instead of simply starting a task at a particular time, an orchestrator can wait for upstream tasks to complete successfully before allowing downstream tasks to proceed.

```
Ingest Market Data
        ↓
Validate Input Data
        ↓
Transform Data
        ↓
Calculate Portfolio Returns
        ↓
Generate Reports
```

If validation fails, the system can prevent the return calculation and reporting tasks from running with invalid inputs.

Depending on the framework and configuration, an orchestrator can also support retries, failure notifications, execution history, and recovery procedures.

The lecture introduces Apache Airflow as an example of an orchestration framework.

The distinction is important:

- **Scheduling:** Determines when a task should run.
- **Orchestration:** Coordinates when and how tasks run, considering dependencies and execution outcomes.

Scheduling is often part of orchestration, but orchestration provides broader control over the workflow.

---

## Automation Through CI/CD

The lecture also connects DataOps with Continuous Integration and Continuous Delivery (CI/CD).

CI/CD automates important parts of the software development and deployment process.

In a data engineering environment, these practices can help validate and deploy changes to pipeline code, configuration, and supporting infrastructure.

For example, suppose I modify a Python function that calculates daily portfolio returns.

Before deploying the change, an automated workflow could:

1. Check the code for errors.
2. Run unit tests.
3. Validate the expected output using sample data.
4. Check that the pipeline configuration is valid.
5. Deploy the change to a testing environment.
6. Promote the change to production after the required checks and approvals.

A simplified workflow is:

```
Code Change
     ↓
Automated Tests
     ↓
Validation
     ↓
Deployment
     ↓
Monitoring
```

This reduces the risk of introducing changes that break existing functionality.

### Applying this to financial modelling

Suppose I change the logic used to calculate portfolio returns.

The modification might appear small, but an error could affect thousands of historical observations or alter the results of a backtest.

Automated tests can help verify properties such as:

- Returns are calculated using the intended formula.
- Missing prices are handled according to the defined policy.
- Duplicate observations are detected.
- Portfolio weights satisfy the expected constraints.
- Output schemas remain consistent.
- Previously validated test cases continue to pass.

For example, a simple-return calculation can be expressed as:

$$
R_t=\frac{P_t-P_{t-1}}{P_{t-1}}
$$

A test can verify that the implementation produces the expected result for known input prices.

CI/CD does not prove that a financial model is economically correct, but it helps detect unintended changes and makes the development process more repeatable.

**The objective is to make changes safer, easier to test, and easier to deploy.**

---

## Pillar 2 — Observability and Monitoring

The second pillar of DataOps is observability and monitoring.

The lecture emphasizes a fundamental reality of data engineering:

> **Every data pipeline will eventually encounter a failure or unexpected condition.**

Failures may result from unavailable APIs, expired credentials, infrastructure problems, malformed records, changes in source schemas, or errors in transformation logic.

The challenge is not to assume that failures can be eliminated completely. It is to detect problems before they create significant downstream consequences.

### Why monitoring matters

Imagine a market-data pipeline that stops receiving updated prices but continues to publish its existing dataset.

The pipeline may appear to be functioning because its scheduled tasks still execute. However, the data becomes progressively stale.

A portfolio analytics dashboard may then display outdated returns, while risk reports may rely on historical prices that no longer reflect the intended observation period.

If nobody detects the problem, incorrect or misleading outputs could remain in circulation for days or weeks.

This demonstrates why successful task execution does not necessarily mean that the data is correct.

### Monitoring versus observability

These concepts are closely related but serve different purposes.

**Monitoring** involves tracking known indicators of system health and alerting when predefined conditions are violated.

Examples include:

- Did the pipeline complete successfully?
- How long did the ingestion task take?
- How many records were processed?
- Did the latest dataset arrive on time?
- How many records failed validation?

**Observability** is the broader ability to understand a system's internal state from the information it produces, helping engineers investigate unexpected behaviour.

Logs, metrics, execution histories, and data-quality results can help explain why a pipeline behaved unexpectedly.

For example, monitoring might alert me that a market-data pipeline loaded 40% fewer records than usual. Observability helps me investigate whether the cause was an API failure, an unexpected source response, or a validation rule rejecting records.

### What should I monitor in a financial data pipeline?

I would monitor at least four categories.

| Category | Example Checks |
| --- | --- |
| Operational health | Task failures, execution duration, retries, resource usage |
| Data freshness | Latest available date, expected delivery time, delayed updates |
| Data quality | Missing values, duplicate records, invalid prices, unexpected schema changes |
| Business outputs | Number of instruments covered, portfolio valuation completeness, unexpected changes in reported metrics |

These categories should be adapted to the system's requirements.

For example, a daily historical research pipeline may tolerate several hours of processing time, while a market-monitoring application may require much faster detection of stale data.

### Example: Detecting stale market data

Suppose a daily pipeline is expected to load market prices for the latest completed trading session.

A basic validation process could check whether the dataset contains the expected trading date.

```
Pipeline Completes
        ↓
Check Latest Data Date
        ↓
Is Data Fresh Enough?
       / \
     Yes  No
      ↓    ↓
 Continue  Alert / Investigate
```

The expected date should be based on the relevant exchange calendar, time zone, holidays, and data-provider delivery schedule rather than simply assuming that a new record must exist every calendar day.

This is an example of why effective monitoring combines technical measurements with an understanding of the business context.

---

## Pillar 3 — Incident Response

The third pillar of DataOps is incident response.

Incident response is the process of identifying, investigating, and resolving problems that affect a data system.

Monitoring helps detect issues, but detection alone does not restore the system.

When an incident occurs, the team must determine what happened, understand its impact, correct the problem, and verify that the system is operating as expected.

A simplified incident-response workflow is:

```
Incident Detected
        ↓
Assess Impact
        ↓
Identify Root Cause
        ↓
Resolve the Problem
        ↓
Validate Data & Outputs
        ↓
Restore Normal Operations
        ↓
Document Lessons Learned
```

### Example: Incorrect portfolio returns

Imagine that a pipeline produces unusually high portfolio returns because a transformation step accidentally combines adjusted and unadjusted stock prices.

The problem might not cause a technical failure. The pipeline could complete successfully and generate a report.

However, monitoring detects a significant deviation in the output, and an investigation reveals the inconsistent price conventions.

A suitable response might involve:

1. Identifying which datasets and reports were affected.
2. Preventing further publication of the affected outputs.
3. Correcting the transformation logic.
4. Reprocessing the affected historical data.
5. Comparing the corrected results with expected values.
6. Reissuing affected reports where necessary.
7. Adding validation checks to reduce the likelihood of recurrence.

The key point is that incident response must address both the technical system and the integrity of its outputs.

Simply restarting a failed task is not sufficient if the underlying data remains incorrect.

### Incident response is also a cultural practice

The lecture emphasizes that incident response is not only about technology.

It also requires communication, coordination, and a willingness to discuss mistakes openly.

A blameless approach focuses on understanding why the system allowed a problem to occur rather than simply assigning fault to the person involved.

For example, if an engineer accidentally deploys a faulty transformation, the team should investigate whether automated testing, review procedures, deployment controls, or monitoring could have prevented the issue or reduced its impact.

This approach encourages learning and continuous improvement.

**The objective is to fix the immediate problem while making the system more resilient against similar failures in the future.**

---

## My Perspective: Applying DataOps to Financial Modelling

Financial modelling is a useful setting for applying DataOps because the reliability of analytical outputs depends on both the quality of the data and the consistency of the processes that produce those outputs.

Consider a system that calculates daily portfolio performance using market prices, portfolio holdings, and benchmark data.

The pipeline may initially be implemented as a Python script. However, as the project grows, it may need to process multiple portfolios, update historical datasets, calculate risk metrics, and produce scheduled reports.

At that point, the challenge is no longer just writing the calculation code.

The system also needs reliable execution, automated validation, monitoring, and recovery procedures.

### Example — An Automated Portfolio Analytics Pipeline

```
Market-Data APIs
       ↓
Automated Ingestion
       ↓
Data Quality Checks
       ↓
Validated Historical Storage
       ↓
Portfolio Calculations
       ↓
Performance & Risk Metrics
       ↓
Reports / Dashboards
```

DataOps introduces operational safeguards at each stage.

| Pipeline Stage | DataOps Application |
| --- | --- |
| Market-data ingestion | Schedule and orchestrate retrieval from external providers |
| Data validation | Automatically check schemas, missing values, duplicates, and freshness |
| Historical storage | Track processing status and preserve validated datasets |
| Portfolio calculations | Run automated tests and validate model inputs and outputs |
| Report generation | Publish reports only after required upstream tasks succeed |
| Monitoring | Alert on failures, stale data, and unexpected output changes |
| Incident response | Investigate issues, correct the cause, and safely rerun affected tasks |

The purpose is to make the analytical process repeatable rather than dependent on someone remembering to execute a series of scripts in the correct order.

### Step 1 — Automate the workflow

Instead of manually downloading prices and running calculations, I would create a repeatable workflow that ingests the data, validates it, and executes the required calculations.

### Step 2 — Define dependencies

Portfolio calculations should depend on validated market data and the correct portfolio holdings.

Report generation should depend on successful calculations.

If an upstream task fails, downstream tasks should not publish results that rely on incomplete or invalid inputs.

### Step 3 — Monitor the pipeline

I would track execution status, processing duration, data freshness, record counts, and important data-quality metrics.

This helps identify both technical failures and silent data problems.

### Step 4 — Respond to incidents

When something goes wrong, I would investigate the cause, determine which outputs are affected, correct the problem, and rerun the necessary tasks.

The recovery process should also verify that the corrected results are valid before they are used downstream.

### Step 5 — Improve continuously

Every incident or unexpected result provides an opportunity to improve the system.

For example, a recurring API failure might justify better retry logic, while repeated schema errors might justify stronger input validation or earlier alerts.

This reflects the continuous-improvement mindset underlying DataOps.

---

## Starting Small: A Practical Learning Path

One important lesson from this lecture is that DataOps does not require implementing a sophisticated orchestration platform immediately.

A reasonable progression for my financial modelling projects would be:

### Stage 1 — Manual prototype

- Write a Python script to retrieve and process financial data.
- Understand the data sources and calculations.
- Test the outputs manually.

### Stage 2 — Repeatable execution

- Separate the code into reusable functions and modules.
- Add logging and exception handling.
- Create automated tests for important calculations.
- Store configuration separately from the code.

### Stage 3 — Scheduled processing

- Run the pipeline automatically at the required frequency.
- Track whether each execution succeeds.
- Validate that the expected data has arrived.

### Stage 4 — Orchestration and monitoring

- Define task dependencies.
- Use an orchestration framework such as Apache Airflow when the workflow justifies it.
- Add failure notifications and data-quality monitoring.
- Prevent downstream tasks from running on invalid inputs.

### Stage 5 — CI/CD and operational maturity

- Run automated tests when code changes.
- Deploy pipeline changes through controlled workflows.
- Monitor production performance and data quality.
- Document incident-response and recovery procedures.

```
Prototype
    ↓
Repeatable Scripts
    ↓
Automated Tests
    ↓
Scheduled Pipelines
    ↓
Orchestration & Monitoring
    ↓
Controlled Deployment & Recovery
```

This progression avoids unnecessary complexity while creating a path toward more reliable systems.

For a small personal project, the first two or three stages may be sufficient. More advanced infrastructure becomes useful as the requirements, number of dependencies, and operational importance of the system increase.

---

## Key Takeaways

This lecture introduces several principles that I want to carry into future data engineering and financial modelling projects.

1. **DataOps combines culture and technology.** Collaboration, communication, continuous learning, and automation work together to improve data systems.
2. **Automation reduces manual effort and operational errors.** Repeatable workflows are easier to maintain than long sequences of manually executed tasks.
3. **Scheduling and orchestration are different.** Scheduling determines when tasks start, while orchestration also manages dependencies and execution outcomes.
4. **CI/CD makes changes safer.** Automated testing and controlled deployment help prevent changes from breaking existing pipelines.
5. **Monitoring must cover both systems and data.** A pipeline can complete successfully while producing stale or incorrect data.
6. **Observability supports investigation.** Logs, metrics, execution histories, and validation results help explain unexpected behaviour.
7. **Incident response is essential.** Problems should be identified, investigated, corrected, and followed by improvements that reduce recurrence.
8. **DataOps is a continuous-improvement process.** Every failure and unexpected result can reveal opportunities to strengthen the system.

The most important lesson I take from this lecture is that **a data pipeline should be designed not only to produce the right results, but also to demonstrate that those results were produced reliably and to make failures visible when something goes wrong**.

For financial modelling, this means moving beyond scripts that work when executed manually toward repeatable, monitored, and testable workflows that can support trustworthy analysis.

---

## Looking Ahead — Orchestration

The lecture concludes by introducing **orchestration** as the next undercurrent of the data engineering lifecycle.

Orchestration is particularly important because modern data pipelines often contain multiple tasks with dependencies between them.

For example, a financial analytics pipeline may need to retrieve market data, validate it, store the results, calculate portfolio returns, and generate reports in a specific order.

An orchestration framework coordinates these tasks, tracks their execution, and helps ensure that downstream processes run only when their dependencies have been satisfied.

This creates a natural progression:

```
Data Architecture
       ↓
DataOps Principles
       ↓
Automation & Monitoring
       ↓
Orchestration
       ↓
Reliable Data Pipelines
       ↓
Trustworthy Financial Analytics
```
## Orchestration: Coordinating Reliable Data Pipelines

The instructor compares orchestration to conducting an orchestra. Just as a conductor coordinates different instruments to produce a coherent musical performance, a data engineer coordinates different processing tasks to produce reliable data outputs.

A data pipeline often consists of multiple stages, including data ingestion, transformation, storage, validation, and serving data to downstream users. These tasks must execute in the correct order, and some tasks can run only after others have completed successfully.

The central lesson from this lecture is:

> **A data pipeline is not simply a collection of scripts. It is a coordinated workflow in which task dependencies, execution order, and failure handling determine whether the final data can be trusted.**

This concept is particularly relevant to financial modelling, where market-data ingestion, data validation, portfolio calculations, risk analysis, and report generation depend on one another.

---

## Understanding Orchestration

Orchestration is the process of coordinating and managing the execution of tasks within a data pipeline.

In a simple pipeline, tasks might be executed manually. As the system grows, however, manual execution becomes difficult to maintain because each task must be triggered at the appropriate time and in the correct sequence.

Consider a financial analytics pipeline:

```
Market Data Sources
        ↓
Data Ingestion
        ↓
Data Validation
        ↓
Historical Storage
        ↓
Financial Calculations
        ↓
Portfolio Analytics
        ↓
Reports & Dashboards
```

Each stage depends on the output of the previous stages.

For example, portfolio returns cannot be calculated reliably if the required market prices have not been ingested and validated.

Orchestration coordinates these dependencies so that the workflow executes as intended.

### The role of the data engineer

The data engineer is responsible for designing and maintaining the workflow that connects individual processing tasks.

This involves determining:

- Which tasks need to run.
- The order in which tasks should execute.
- Which tasks depend on other tasks.
- When or under what conditions tasks should start.
- What should happen when a task fails.
- How execution status should be monitored.
- When alerts should be generated.

Orchestration therefore connects the individual components of a data system into a coordinated process.

---

## From Manual Execution to Orchestration

The lecture describes three approaches to managing data pipelines.

### Approach 1 — Manual execution

In the early stages of a project, a data engineer might execute each task manually.

For example:

```
Run Ingestion Script
        ↓
Check the Data
        ↓
Run Transformation Script
        ↓
Check the Results
        ↓
Run Financial Model
        ↓
Generate Report
```

This approach is useful during prototyping because it allows the engineer to test individual components and understand how the system works.

However, it becomes inefficient as the number of tasks increases.

Manual execution also introduces operational risks:

- Tasks may be executed in the wrong order.
- An engineer may forget to run a required step.
- A failed task may go unnoticed.
- Processing may become dependent on an individual's availability.
- Repeating the same workflow can consume unnecessary time.

For a small financial modelling experiment, this may be acceptable. For a recurring portfolio analytics process, it becomes increasingly difficult to manage.

### Approach 2 — Pure scheduling

The next step is to automate task execution using a predefined schedule.

For example:

```
12:00 AM → Ingest Market Data
12:30 AM → Validate Data
01:00 AM → Calculate Returns
01:30 AM → Generate Reports
```

This removes the need to trigger every task manually.

However, pure scheduling relies on assumptions about when tasks will finish.

Suppose market-data ingestion usually takes 20 minutes, so the transformation task is scheduled to start 30 minutes after ingestion begins.

If the data provider experiences a delay and ingestion takes 45 minutes, the transformation task might start before all the data has arrived.

The result could be an incomplete dataset and incorrect downstream calculations.

Similarly, if ingestion fails entirely, scheduled tasks may still run unless additional checks prevent them from doing so.

**Scheduling automates task timing, but timing alone does not guarantee that the required data is ready.**

### Approach 3 — Orchestration

Orchestration provides a more sophisticated way to coordinate pipeline execution.

Instead of relying entirely on predetermined times, an orchestration framework can manage task dependencies and execution states.

For example:

```
Ingest Market Data
        ↓
Validate Data
        ↓
Store Validated Data
        ↓
Calculate Portfolio Returns
        ↓
Generate Reports
```

The portfolio-return calculation can be configured to wait until the required upstream tasks have completed successfully.

If data validation fails, downstream tasks can be prevented from running.

An orchestration framework may also support:

- Time-based scheduling.
- Task dependencies.
- Event-triggered execution.
- Retries and failure handling.
- Execution monitoring.
- Notifications and alerts.
- Tracking task status and history.

The exact capabilities depend on the framework and how it is configured.

The important distinction is that orchestration coordinates the workflow based on more than just the clock.

---

## Orchestration Frameworks

The lecture introduces several open-source orchestration frameworks that can be used to build and manage data pipelines.

- **Apache Airflow** — A widely used framework for defining, scheduling, and monitoring workflows.
- **Dagster** — A data orchestrator that emphasizes data assets, dependencies, and testing.
- **Prefect** — A workflow orchestration framework designed to manage and monitor data workflows.
- **Mage** — A framework for developing and orchestrating data pipelines.

These tools address similar high-level problems, but they differ in their programming models, abstractions, and operational features.

For my learning journey, I want to understand the underlying orchestration concepts before focusing on the differences between individual frameworks.

The fundamental ideas of task dependencies, execution order, monitoring, and failure handling remain relevant regardless of which tool is selected.

---

## Understanding Directed Acyclic Graphs (DAGs)

One of the most important concepts introduced in this lecture is the **Directed Acyclic Graph (DAG)**.

Many orchestration frameworks represent workflows as DAGs.

A DAG describes how tasks relate to one another and the order in which dependencies must be satisfied.

The term has three components.

### 1\. Directed

A directed graph has edges that point in a specific direction.

In a data pipeline, arrows represent the direction of task dependencies or data flow.

```
Ingestion → Validation → Transformation
```

The arrows indicate that validation depends on ingestion, and transformation depends on validation.

### 2\. Acyclic

Acyclic means that the graph contains no directed loops.

A task cannot lead through a sequence of dependencies back to itself.

For example:

```
Task A → Task B → Task C
```

is a valid acyclic sequence.

However:

```
Task A → Task B → Task C
    ↑                 |
    └─────────────────┘
```

contains a cycle and is not a DAG.

If a process requires repeated execution, an orchestrator can generally handle this through scheduled runs, retries, or other supported mechanisms rather than by defining a circular dependency within a DAG.

### 3\. Graph

A graph consists of nodes and edges.

- **Nodes** represent tasks or workflow steps.
- **Edges** represent dependencies between those tasks.

For example:

```
           Market Data API
                  |
                  v
             Ingestion
                  |
                  v
             Validation
                  |
                  v
             Raw Storage
                  |
             +----+----+
             |         |
             v         v
       ML Transform  Analytics
             |         |
             v         v
        ML Storage  Analytics Storage
```

This example shows how a pipeline can branch into separate downstream workflows.

One branch prepares data for machine learning, while another prepares data for analytics.

The branches may run independently after their shared upstream dependencies have been satisfied.

### Why DAGs are useful

DAGs make complex workflows easier to understand and manage.

They allow engineers to define dependencies explicitly instead of relying on manually coordinated execution.

A DAG also helps identify which tasks can run in parallel, which tasks must wait, and which downstream tasks are affected when a particular task fails.

**A DAG is a representation of the workflow; the orchestration framework is responsible for executing and managing that workflow.**

---

## Applying Orchestration to Financial Modelling

Financial modelling provides a practical example of why orchestration is important.

Consider a system that calculates portfolio performance and risk metrics using historical market prices, portfolio holdings, and benchmark data.

The final report depends on several upstream processes completing correctly.

### Example — Portfolio Analytics DAG

```
Market Data API          Portfolio Holdings
       |                         |
       v                         v
Price Ingestion          Holdings Ingestion
       |                         |
       v                         v
Price Validation         Holdings Validation
       |                         |
       +------------+------------+
                    |
                    v
            Portfolio Calculations
                    |
                    v
          Performance & Risk Metrics
                    |
                    v
             Output Validation
                    |
                    v
              Final Reports
```

This DAG illustrates an important principle: portfolio calculations require more than one input.

The calculations should begin only after both market prices and portfolio holdings have been retrieved and validated.

The report should be generated only after the calculations and output checks have completed successfully.

### Step 1 — Define the tasks

I would begin by identifying the individual steps in the financial modelling process.

For example:

- Retrieve historical prices.
- Retrieve portfolio holdings.
- Validate both datasets.
- Calculate portfolio returns.
- Calculate benchmark-relative performance.
- Calculate risk metrics.
- Validate the results.
- Publish reports.

Each step should have a clear responsibility and a well-defined input and output.

### Step 2 — Define dependencies

Next, I would determine which tasks depend on other tasks.

Portfolio-return calculations require both price data and holdings data.

Risk calculations may require a sufficiently long history of validated returns.

Report generation depends on the successful completion of the relevant calculations.

These dependencies should be explicitly represented rather than assumed.

### Step 3 — Configure execution

The workflow might run once each trading day after the required market data becomes available.

Alternatively, an event could trigger ingestion when a new data file arrives or a source system reports that new data is ready.

The correct approach depends on the business requirement and the capabilities of the data source and orchestration framework.

### Step 4 — Handle failures

Suppose market-data ingestion fails because the external API is unavailable.

The orchestration framework can be configured to retry the task, notify the engineer, and prevent dependent calculations from running until the necessary data is available.

This avoids generating a report from an incomplete update.

### Step 5 — Monitor completion

Finally, I would monitor whether the pipeline completed on time and whether the resulting data and calculations passed their validation checks.

A successful execution should mean more than simply reaching the end of the workflow. The outputs must also satisfy the relevant data-quality and business requirements.

---

## Event-Driven Orchestration

Another important concept in this lecture is that tasks do not always need to start at a predetermined time.

Orchestration frameworks can also support event-driven execution.

In a time-based workflow, ingestion might start at midnight every day.

In an event-driven workflow, ingestion might start when a new file arrives, a source system signals that data is ready, or another configured event occurs.

The difference can be represented as follows:

```
Time-Based Execution
        |
        v
Scheduled Time Reached
        |
        v
Start Task
```

```
Event-Driven Execution
        |
        v
New Data Becomes Available
        |
        v
Detect Event
        |
        v
Start Task
```

For financial data pipelines, event-driven execution can be useful when data availability varies or when processing should begin as soon as a required input is ready.

However, receiving a new file does not automatically mean that the file is complete or valid. Appropriate validation is still necessary before downstream calculations begin.

---

## Orchestration, DataOps, and Reliability

In the previous lecture, I learned that DataOps has three major technical pillars:

1. Automation.
2. Observability and monitoring.
3. Incident response.

Orchestration brings several of these capabilities together.

It automates task execution, tracks dependencies and task states, and can integrate with monitoring and alerting systems.

For example, if a financial data transformation fails, the orchestrator can record the failure, trigger a notification, and prevent dependent tasks from executing.

The engineer can then investigate the cause and rerun the appropriate part of the workflow once the issue has been resolved.

This creates a relationship between orchestration and DataOps:

```
                 DataOps
                    |
                    v
              Orchestration
                    |
        +-----------+-----------+
        |           |           |
        v           v           v
    Scheduling  Dependencies  Monitoring
        |           |           |
        +-----------+-----------+
                    |
                    v
          Coordinated Execution
                    |
                    v
            Reliable Data Flow
```

Orchestration does not replace testing, data-quality controls, or incident-response procedures. Instead, it provides a framework within which these practices can be coordinated.

---

## My Learning Approach: From Scripts to Workflows

I want to apply the concepts from this lecture progressively in my financial modelling projects.

Rather than immediately introducing an orchestration framework into every project, I would first build a clear understanding of the workflow itself.

### Stage 1 — Build individual Python scripts

Create separate scripts or functions for:

- Retrieving financial data.
- Validating inputs.
- Calculating returns.
- Calculating risk metrics.
- Generating reports.

At this stage, the focus is on understanding the calculations and ensuring that each component works correctly.

### Stage 2 — Define the dependencies

Determine the order in which the components must execute.

For example, returns should not be calculated before the relevant price data has been validated.

Represent the workflow using a simple diagram before introducing an orchestration tool.

### Stage 3 — Automate execution

Introduce a scheduler or a simple automated workflow to remove unnecessary manual execution.

Add logging, error handling, and validation checks so that failures can be identified.

### Stage 4 — Introduce orchestration

When the workflow becomes sufficiently complex, use a framework such as Apache Airflow to define task dependencies, coordinate execution, and monitor task status.

This allows the system to grow beyond a collection of manually executed scripts.

### Stage 5 — Add recovery and monitoring

Configure appropriate retries, notifications, data-quality checks, and recovery procedures.

The objective is to make the pipeline easier to operate and troubleshoot, not simply to make it run automatically.

This progression follows the broader principle introduced throughout the course:

**Understand the problem and design the workflow before choosing the technology.**

---

## Key Takeaways

This lecture introduces several concepts that I want to carry into my data engineering and financial modelling projects.

1. **Orchestration coordinates a pipeline's tasks.** It manages the order and conditions under which individual processing steps execute.
2. **Manual execution is useful for prototyping but difficult to scale.** Repeated workflows benefit from automation.
3. **Scheduling and orchestration are not equivalent.** Scheduling controls timing, while orchestration also manages dependencies and execution outcomes.
4. **DAGs describe workflow dependencies.** Nodes represent tasks, and directed edges represent relationships between tasks.
5. **Dependencies protect downstream calculations.** A task should not proceed when its required inputs have not been produced successfully.
6. **Event-driven execution can reduce unnecessary waiting.** Tasks can start when required inputs or other configured events become available.
7. **Monitoring and failure handling are essential.** Automated execution is valuable only when problems can be detected and handled appropriately.
8. **Orchestration is part of the wider DataOps approach.** It supports automation, monitoring, and coordinated incident response.

The most important lesson I take from this lecture is that **reliable financial analytics requires not only correct calculations, but also a carefully designed workflow that ensures those calculations execute in the right order using the right inputs.**

A portfolio model may produce accurate results when executed manually, but orchestration helps turn that model into a repeatable process that can be operated and maintained reliably.

---

## Looking Ahead — Software Engineering

The lecture concludes by introducing software engineering as the final undercurrent of the data engineering lifecycle.

Software engineering practices are important because data pipelines are themselves software systems. They need to be designed, tested, version-controlled, maintained, and improved over time.

For financial modelling, this means treating analytical code as part of a maintainable software system rather than as a collection of isolated scripts.

The progression so far is:

```
Understand Stakeholder Needs
           ↓
Design Data Architecture
           ↓
Apply DataOps Principles
           ↓
Orchestrate Pipeline Tasks
           ↓
Apply Software Engineering Practices
           ↓
Build Reliable Data Systems
           ↓
Deliver Trustworthy Financial Analytics
```


## Software Engineering: Writing Production-Grade Data Systems

Throughout the previous lectures, we explored several concepts that influence how data systems are designed and operated, including security, data management, data architecture, DataOps, and orchestration.

Software engineering connects these concepts by focusing on how we write, test, deploy, and maintain the code that powers data systems.

The instructor emphasizes an important distinction: being able to write code that works is not the same as being able to write production-grade code.

A script might successfully retrieve market prices or calculate portfolio returns, but a reliable data system requires code that is also readable, testable, maintainable, and deployable.

> **The goal is not simply to write code that works today, but to build software that can be understood, tested, maintained, and trusted over time.**

This distinction is particularly relevant to financial modelling, where calculations must be reproducible, data transformations must be consistent, and changes to analytical logic should not silently introduce errors.

---

## Understanding Software Engineering

Software engineering is the discipline of designing, developing, deploying, and maintaining software applications.

Historically, many data-processing responsibilities were handled by software engineers as part of their broader work. As the volume, diversity, and business importance of data increased, these responsibilities became more specialized and eventually developed into the field of data engineering.

Today, data engineers have access to managed services, open-source frameworks, and cloud platforms that simplify many infrastructure and data-processing tasks.

This allows engineers to spend more time solving business problems instead of building every component from scratch.

However, access to these tools does not eliminate the need for strong programming skills.

### Moving up the value chain

Modern data engineers can use existing tools to handle tasks that previously required substantial custom development.

For example, instead of building a complete distributed processing engine, an engineer can use an existing framework such as Apache Spark.

Instead of manually coordinating every pipeline task, an engineer can use an orchestration framework such as Apache Airflow.

Instead of implementing database operations from scratch, an engineer can use SQL and managed database services.

This changes the nature of the work:

```
Build Everything from Scratch
              ↓
      Use Existing Tools
              ↓
    Focus on Business Logic
              ↓
   Improve Reliability & Quality
              ↓
       Deliver More Value
```

The key lesson is that tools help us work more efficiently, but we still need to understand how to use them correctly and how to write high-quality code around them.

---

## Why Coding Remains Essential for Data Engineers

The lecture identifies coding as a fundamental skill throughout the data engineering lifecycle.

Data engineers work with code across several stages:

- **Ingestion:** Retrieving data from APIs, databases, files, and other sources.
- **Transformation:** Cleaning, validating, joining, and restructuring datasets.
- **Storage:** Loading data into databases, warehouses, and data lakes.
- **Serving:** Preparing data for analytics, machine learning, and applications.
- **Orchestration:** Defining workflows and coordinating the execution of tasks.
- **Infrastructure:** Automating the deployment and configuration of data systems.

Even when managed services handle much of the underlying infrastructure, engineers still need to configure those services, implement business logic, validate results, and troubleshoot problems.

### Languages and technologies introduced in the lecture

| Language or Technology | Typical Role in Data Engineering |
| --- | --- |
| SQL | Querying, joining, aggregating, and transforming structured data |
| Python | Data processing, automation, API integration, and analytical logic |
| Bash | Command-line operations and scripting |
| Apache Spark | Distributed data processing |
| Apache Kafka | Event streaming and real-time data pipelines |
| Java / Scala | Application development and distributed data processing |
| R | Statistical computing and analytics |
| Go / Rust | Systems programming and infrastructure-related applications |

The course focuses primarily on **SQL, Python, and Bash** in its practical exercises.

I want to prioritize these foundational skills before expanding into additional languages and frameworks.

The broader lesson is that strong programming fundamentals make it easier to learn new technologies when a project requires them.

---

## What Does Production-Grade Code Mean?

One of the most important ideas in this lecture is the difference between code that works in a single situation and code that is suitable for a production environment.

Consider a simple Python script that downloads stock prices and calculates daily returns.

The script might work correctly when executed manually on a small dataset. However, problems may emerge when the source API becomes unavailable, a stock has missing prices, or the script needs to process several years of data.

Production-grade code should be designed to handle these situations appropriately.

The lecture emphasizes four important qualities.

### 1\. Clean code

Clean code is organized logically and avoids unnecessary complexity.

Functions should have clear responsibilities, variable names should communicate their purpose, and repeated logic should be reduced where appropriate.

For example, a function called `calculate_daily_returns()` is easier to understand than a generic function called `process_data()` when the task is specifically to calculate returns.

### 2\. Readable code

Readable code allows another person, or the same engineer several months later, to understand how the system works.

This involves meaningful naming, consistent formatting, clear structure, and documentation where necessary.

Readability is particularly important in financial modelling because the implementation of a calculation should be understandable enough to review against its intended financial definition.

### 3\. Testable code

Testable code is structured so that its behaviour can be verified independently.

For example, a return-calculation function can be tested using a small dataset with known prices and expected results.

Testing helps detect errors before they affect downstream pipelines or reports.

### 4\. Deployable code

Deployable code can be incorporated into a controlled environment and executed consistently.

This requires more than writing the main calculation. Depending on the project, it may also involve configuration management, dependency management, automated tests, logging, deployment procedures, and environment-specific settings.

Together, these qualities help transform a prototype into a maintainable data system.

```
          Production-Grade Code
                    |
        +-----------+-----------+
        |           |           |
        v           v           v
      Clean      Readable    Testable
                    |
                    v
                Deployable
                    |
                    v
          Maintainable Systems
```

These characteristics overlap and reinforce one another. They should be treated as ongoing engineering goals rather than separate boxes that can be checked only once.

---

## My Perspective: Applying Software Engineering to Financial Modelling

Financial modelling often begins with exploratory analysis in notebooks or standalone scripts.

For example, I might download historical prices, calculate returns, construct a portfolio, and evaluate its performance.

This is a useful way to explore an idea. However, the implementation can become difficult to maintain when I introduce additional instruments, benchmarks, risk metrics, and reporting requirements.

The next step is to separate the analytical logic into reusable components.

### Example — From a Financial Script to a Reusable System

A basic financial modelling workflow might look like this:

```
Retrieve Market Data
         ↓
Clean & Validate Data
         ↓
Calculate Returns
         ↓
Construct Portfolio
         ↓
Calculate Performance
         ↓
Calculate Risk Metrics
         ↓
Generate Reports
```

Instead of implementing every stage in one large script, I can organize the logic into independent functions and modules.

For example:

```
def calculate_daily_returns(prices):
    return prices.pct_change()

def calculate_portfolio_returns(asset_returns, weights):
    return asset_returns.mul(weights, axis=1).sum(axis=1)
```

These functions illustrate how individual calculations can be separated into reusable components.

The portfolio-return function assumes that the asset returns and weights are aligned correctly and that the weighting convention is appropriate for the model. Those assumptions should be validated in a real implementation.

The advantage of this structure is that each component can be tested, reviewed, and modified independently.

### Step 1 — Separate data processing from financial logic

I would distinguish between retrieving market data, validating it, calculating financial metrics, and generating reports.

This separation makes it easier to identify where an error originates.

### Step 2 — Make calculations reusable

Rather than copying the same return-calculation logic into multiple notebooks, I would implement it once in a reusable function or module.

This reduces duplication and makes it easier to maintain consistency across projects.

### Step 3 — Add tests

I would verify that the functions produce expected results for known inputs and behave appropriately when they encounter invalid or missing data.

### Step 4 — Add operational safeguards

I would introduce logging, exception handling, input validation, and configuration management where appropriate.

This helps make the system more predictable when it interacts with external data sources and automated workflows.

### Step 5 — Integrate the components

Finally, I would connect the functions into a repeatable pipeline and, when necessary, use an orchestration framework to manage its execution.

The objective is to preserve the correctness of the financial logic while making the surrounding system easier to maintain and operate.

---

## Testing: An Essential Skill for Financial Data Systems

Although this lecture does not explore testing in detail, its emphasis on testable code suggests an important practical direction for my learning.

Financial calculations should not be trusted simply because a script executes without errors.

A program can run successfully and still produce incorrect results because of a formula error, misaligned dates, missing observations, or incorrect assumptions.

For example, simple daily returns are calculated as:

$$
R_t=\frac{P_t}{P_{t-1}}-1
$$

Suppose the previous closing price is 100 and the current closing price is 105.

The expected simple return is:

$$
R_t=\frac{105}{100}-1=0.05=5\%
$$

A unit test can verify that the implementation produces this result.

Other useful tests for financial modelling include:

- Checking that returns match known examples.
- Verifying that date indexes are correctly aligned.
- Detecting duplicate instrument-date observations.
- Ensuring portfolio weights satisfy the intended constraints.
- Testing the handling of missing prices and zero denominators.
- Checking that changes to one function do not break other calculations.

The correct tests depend on the financial model and its assumptions.

For example, a portfolio with cash holdings or short positions may legitimately have weights that do not follow the constraints of a fully invested long-only portfolio.

**Testing should verify the model's intended behaviour, not impose assumptions that are inappropriate for the model.**

---

## Software Engineering and the Other Data Engineering Undercurrents

Software engineering connects directly with the concepts introduced in the previous lectures.

### 1\. Security

Code must handle credentials and sensitive information responsibly.

For example, API keys should not be embedded directly in source code or committed to a public repository.

Access permissions, configuration, and secret management should be designed with the system's security requirements in mind.

### 2\. Data management

Software should help maintain data quality, consistency, and integrity.

This includes implementing validation rules, documenting data definitions, and handling changes to schemas and source systems.

### 3\. Data architecture

Code implements the design decisions made when building a data system.

Well-structured modules and clear interfaces make it easier to evolve individual components without unnecessarily changing the entire system.

### 4\. DataOps

Software engineering supports automation, testing, continuous integration, and controlled deployment.

These practices reduce the risks associated with changing data-processing logic.

### 5\. Orchestration

Orchestration frameworks coordinate the execution of software components.

For example, Python functions and SQL transformations can be organized into tasks with explicit dependencies.

The relationship can be summarized as follows:

```
Software Engineering
        |
        +── Security Controls
        |
        +── Data Quality Logic
        |
        +── Architecture Implementation
        |
        +── Automated Testing & Deployment
        |
        +── Orchestrated Workflows
        |
        v
 Reliable Data Engineering Systems
```

Software engineering is therefore not an isolated programming topic. It supports the implementation and maintenance of nearly every other aspect of the data engineering lifecycle.

---

## Open-Source Contributions and Infrastructure as Code

The instructor also introduces two additional areas where data engineers apply software engineering skills.

### Open-source development

Data engineers often use existing open-source frameworks to solve practical problems.

During implementation, they may discover a limitation or develop an improvement that could benefit other users.

Contributing a fix or enhancement to an open-source project requires code that is understandable, testable, and consistent with the project's development practices.

Even if I do not immediately contribute to public projects, learning how to work with existing codebases is valuable because data engineering frequently involves integrating and extending existing tools.

### Infrastructure as Code and Pipeline as Code

Infrastructure as Code (IaC) means managing infrastructure through version-controlled, machine-readable definitions rather than relying entirely on manual configuration.

Pipeline as Code applies a similar idea to data workflows, where pipeline definitions and execution logic are maintained as code.

These approaches make infrastructure and pipeline configurations easier to review, reproduce, test, and deploy.

For example, a cloud-based financial data pipeline might require:

- Storage resources.
- Access permissions.
- Data-processing services.
- Workflow definitions.
- Monitoring and alerting configurations.

Managing appropriate parts of this setup as code can reduce configuration inconsistencies and make the system easier to recreate.

These practices also connect directly to the previous lectures on DataOps, architecture, and orchestration.

---

## My Learning Priorities

Based on this lecture, I want to build a strong foundation in software engineering before moving toward increasingly complex data infrastructure.

My initial priorities are:

1. **Python fundamentals:** Functions, modules, data structures, exceptions, and reusable code.
2. **SQL:** Querying, joining, aggregating, and transforming structured data.
3. **Bash and the command line:** Running scripts, navigating environments, and automating routine tasks.
4. **Testing:** Writing unit tests and validating financial calculations.
5. **Version control:** Using Git and GitHub to track changes and maintain a clear development history.
6. **Code organization:** Separating data ingestion, transformations, financial calculations, and reporting.
7. **Logging and error handling:** Making problems visible and easier to investigate.
8. **Automation and deployment:** Gradually integrating the code into repeatable workflows.

I do not need to master every framework or programming language immediately.

The more useful objective is to build transferable skills that will help me understand and maintain increasingly complex systems.

---

## Key Takeaways

This lecture completes the discussion of the undercurrents of the data engineering lifecycle.

The main lessons I want to retain are:

1. **Software engineering is fundamental to data engineering.** Writing and reading code are everyday responsibilities.
2. **Working code is not necessarily production-grade code.** Readability, testability, maintainability, and deployability also matter.
3. **Modern tools reduce infrastructure work but do not eliminate the need for coding skills.** Engineers still need to implement business logic and ensure that systems behave correctly.
4. **Strong fundamentals make learning new languages easier.** SQL, Python, and Bash are useful starting points for this course.
5. **Financial calculations should be independently testable.** Successful execution does not guarantee mathematical or financial correctness.
6. **Reusable components improve maintainability.** Separating ingestion, validation, calculations, and reporting makes systems easier to understand and modify.
7. **Software engineering supports the other undercurrents.** Security, architecture, DataOps, and orchestration all depend on well-designed and maintainable implementations.

The most important lesson I take from this lecture is that **I want to approach financial modelling as both a quantitative discipline and a software engineering discipline**.

Understanding financial theory helps me determine what should be calculated. Software engineering helps me implement those calculations in a way that is reproducible, testable, and maintainable.

Combining these skills is essential as I move from individual analytical experiments toward automated financial data systems.

---

## Looking Ahead — Bringing the Lifecycle to the Cloud

The lecture concludes the discussion of the undercurrents of the data engineering lifecycle and introduces the next stage of the course: applying these concepts in practical exercises on AWS.

This represents a transition from understanding the principles behind data engineering to seeing how those principles operate in a real cloud environment.

The concepts covered so far provide a foundation for these exercises:

```
Business Requirements
        ↓
Data Architecture
        ↓
Data Management & Security
        ↓
DataOps & Orchestration
        ↓
Software Engineering
        ↓
Cloud-Based Data Pipelines
        ↓
Reliable Analytics & Financial Models
```
