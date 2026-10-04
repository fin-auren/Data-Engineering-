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
