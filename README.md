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
