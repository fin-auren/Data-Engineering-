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
