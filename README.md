# 👋 Shodunke-Feranmi

### 💻 Data Analyst | Computer Science Student | Aspiring Data Professional

Welcome to my GitHub! I'm a Computer Science student passionate about **Data Analytics, SQL, Excel, Power BI, and turning raw data into meaningful business insights.**

I work on real-world datasets, cleaning and transforming data, performing analysis, and building dashboards that communicate insights clearly.

---

## 🚀 About Me

* 🎓 Computer Science Student
* 📊 Interested in **Data Analytics & Business Intelligence**
* 💡 Currently improving my skills in **SQL, Excel, Power BI, and Data Visualization**
* 🔍 Interested in solving business problems using data
* 📚 Continuously learning and building practical projects

---

## 🛠️ Skills & Tools

### Data Analysis

* Microsoft Excel
* SQL / MySQL
* Power Query
* Data Cleaning

### Data Visualization

* Microsoft Power BI
* Excel PivotTables & PivotCharts
* Dashboard Design

---

## 📂 My Projects

### 🏦 MetroBank Analytics Challenge: A 5-Week Finance Case Study
 
A full walkthrough of a 5-stage analytics project simulating a real bank's data, from who the customer is to where fraud risk sits. Each week is written as its own mini case study: the role I played, the goal, what I did, and what I found.*
 
---
 
### The Premise
 
MetroBank is a fictional retail bank with Retail, Corporate, and Private customers. Real banks don't get one clean dataset to answer every question; different teams (Marketing, Relationship Management, Operations, the COO's office, Risk) each hold a piece of the picture and ask different questions of it. This project was structured the same way: five weeks, five roles, five connected datasets that link together through shared customer and account IDs. My analysis started from week 1 where I was asked  "who is the customer?" all the way to week 5 where I was also asked "where is the bank losing money to fraud?" — with every week building on the one before it.
 
---
 
### Week 1: Customer Profiling & Segmentation
**Role:** Marketing Analyst
**Goal:** Understand who MetroBank's customers actually are, so the marketing team can design better-targeted campaigns instead of marketing to everyone the same way.
 
**What I did:** Worked from `Customers.csv` and built calculated columns to segment the base — age groups (Gen Z, Millennial, Gen X, Boomer) using `IF`/`IFS` logic, income brackets (Low, Medium, High, Premium), and customer tenure using `DATEDIF`. Summarized everything into PivotTables and a one-page dashboard covering region, gender, age, income, and segment.
 
**Findings:**
- 500 total customers: 256 female, 244 male
- Regional spread: South (137), East (133), North (120), West (110)
- **Millennials** are the largest age group (147); **High Income** is the largest income bracket (188)
- **Retail** is the largest customer segment (286 of 500 customers)
- **Private** customers have the highest average income ($118,774), despite Retail being the largest group by volume (286)
**Why it matters:** This week set up the lens for everything after it. Retail is where the *volume* is, but Private is where the *value* is — two very different customer groups that need two very different strategies.
 
---
 
### Week 2: Accounts, Balances & Credit
**Role:** Relationship Management Analyst
**Goal:** Understand what products customers actually hold, how healthy their finances are, and how much risk sits in the loan book — the link between *who* the customer is (Week 1) and *what* they do with the bank.
 
**What I did:** Linked `Accounts.csv` to `Customers.csv` to analyze product penetration (Checking, Savings, Credit Card, Loan), total deposits, the approved loan book, and credit score patterns. Delivered both Pivot Tables and Dashboard Visualization in an Excel workbook.
 
**Findings:**
- Account mix: 303 Savings, 246 Checking, 169 Credit Card, 82 Loan accounts
- Total balances across the bank: **$145,013,181**
- Total approved loan amount: **$3,677,399** — a small fraction of total deposits
- Average credit score: **580**, which sits at the low end of "Fair"
- **Gen Z customers hold higher average balances than Boomers**, a counterintuitive result that challenged the usual assumption that older customers are wealthier
**Why it matters:** The bank is sitting on far more in deposits than it's lending out, and credit quality is a real constraint on how aggressively it can grow that lending. The Gen Z finding also directly updates the Week 1 picture — age doesn't predict value the way you'd expect.
 
---
 
### Week 3: Transaction Behavior & Patterns
**Role:** Operations Analyst
**Goal:** Now that we know what accounts customers hold, understand *how* they actually use them, so operations can tailor offers and optimize resources around real behavior, not assumptions.
 
**What I did:** Enriched `Transactions.csv` with account type and customer segment by linking it to both prior weeks' data. Built PivotTables grouped by transaction type, channel they use during transactions, and merchant, added Slicers and Timelines for interactivity, and grouped the date field by month to surface trends.
 
**Findings:**
- **5,000 transactions** totaling **$25,066,089**, averaging **$5,013** per transaction
- Customers use all four transaction types fairly evenly: Withdrawal and Payment (1,266 each), Deposit (1,244), Transfer (1,224)
- **Withdrawals carry the highest total transaction value**, while **Transfers carry the least**
- **POS is the most popular channel** (1,286 transactions) *and* the channel carrying the highest-value transactions
**Why it matters:** No single transaction type dominates behavior, which meant the bank couldn't just optimize for one use case. But POS clearly stands out as where both volume and value concentrate, making it the highest-leverage channel for partnerships, rewards, and monitoring.
 
---
 
### Week 4: Branch Performance & Efficiency
**Role:** Analyst reporting to the COO
**Goal:** The COO needs to decide where to invest and where to streamline, based on which branches are actually pulling their weight.
 
**What I did:** Analyzed `Branches.csv` as a standalone dataset (deliberately not linked to the earlier weeks), covering 20 branches across 4 regions and 1,951 staff. Built PivotTables and a dashboard around three questions: profitability, efficiency (revenue per staff member), and cost management.
 
**Findings:**
- Across all 20 branches: **$59.4M in revenue**, **$21.2M in operating costs**, and **$38.3M in profit** (a 64% margin)
- **South is the most profitable region** ($14.79M profit, 63% margin), followed by West ($9.47M) and North ($8.84M)
- **East is the least profitable region** ($5.15M profit) and also has the **lowest margin of any region (46.5%)** — its revenue is comparable to North's, but its costs are more than double
- **Two branches are losing money outright**: West Loganmouth (-$652K) and Lake Lynnton (-$534K), the latter in the East region, which explains much of East's weak showing
- **Javiertown has the highest operating cost** of any branch ($1.97M), yet still turns a solid profit ($2.81M) — the opposite of a wasteful branch, since it's simply high-cost *and* high-revenue
- The most efficient branches by revenue-per-employee are **Caldwellburgh** ($198K/employee, just 18 staff) and **Simonland** ($188K/employee, 23 staff) — both small, lean, high-output branches
- The least efficient is **Lake Lynnton** ($7.2K/employee on 193 staff) — the same branch that's losing money, now explained: it's overstaffed relative to what it generates
- Staff count and revenue-per-employee are **negatively correlated** (-0.68): bigger branches are consistently less efficient per employee than smaller ones
**Why it matters:** The instinct to look at "highest operating cost" as a red flag turned out to be wrong for Javiertown — it earns its spend. The real problem branch is Lake Lynnton: high staff count, lowest efficiency, and negative profit all at once. That reframes the COO's decision from "cut costs everywhere" to "streamline specific overstaffed branches like Lake Lynnton and West Loganmouth, while continuing to invest in lean, high-efficiency branches like Caldwellburgh and Simonland."
 
---
 
### Week 5: Customer Experience & Risk Intelligence
**Role:** Strategic Analyst reporting to the Chief Customer Officer and Chief Risk Officer
**Goal:** Move beyond just counting complaints to producing actionable intelligence — diagnosing what's driving service issues, and flagging which fraud cases need action right now.
 
**What I did:** Linked `Complaints.csv` back to both `Customers.csv` and `Accounts.csv` to correlate complaints with segment, region, and account value. Built a priority-flagging system for high-risk fraud cases (for example, any Open fraud case older than 7 days), since a raw complaint count doesn't tell you what needs attention *today*.
 
**Findings:**
- **Charges Dispute** is the most common complaint type having 184 total cases
- Average resolution time is **31 days**; the "Others" category takes the longest to resolve, a possible process gap
- The open backlog is significant: **157 Open** and **172 In Progress** complaints
- **High-value customers complain more than average** — a direct retention risk
- **54 active fraud cases**, out of **145 total ever reported** — meaning over a third of all fraud cases the bank has ever seen are still unresolved
**Why it matters:** This week ties the whole project together. The customers most worth keeping (from Week 1 and Week 2's high-value segments) are the ones filing the most complaints, and over a third of all fraud ever reported is still sitting active. That's not just a service metric, it's a retention and risk exposure problem stacked on top of everything found in the earlier weeks.
 
---
 
### The Full Arc
 
Read start to finish, the five weeks tell one connected story: MetroBank's most valuable customers (Private segment, high balances, often younger than assumed) are also disproportionately represented in the complaint and fraud data, at the same time the bank is sitting on underused deposits, two branches bleeding money (West Loganmouth and Lake Lynnton), and uneven regional performance driven more by staffing efficiency than by cost alone. That's the throughline I lead with in the full README and dashboard.

Tools: Data Analytics | Excel | Data Visualization
 
🔗 [View Project](https://github.com/Shodunke-Feranmi/MetroBank-Analysis-Project/blob/main/README.md)

---
### 🚗 Car45 Sales Analysis
 
*A used-car market analysis built on ~2,900 real listings scraped from Car45, a Nigerian car marketplace, structured around the one question that mattered most: what actually drives price?*
 
---
 
### The Premise
 
Anyone buying or selling a used car in Nigeria is essentially pricing blind — there's no single reference for what a "fair price" looks like across brands, conditions, and locations. This project treats **~2,900 listings** across **47 makes** and **13 states** as a market snapshot, working toward one core question: what actually moves the price of a car in this market?
 
---
 
### Section 1: Market Snapshot & Landscape
**Goal:** Get a baseline read on the market, then map who's selling what, and where.
 
**What I did:** Pulled summary statistics across the full dataset, then grouped listings by make, color, state, and city to see how supply is distributed.
 
**Findings:**
- Average listing price is **~₦5.0M**, but the **median is ~₦3.2M** — a gap of about 1.6x, meaning a handful of premium cars pull the average up. This one number set the rule for the rest of the project: **use the median, not the average**, when talking about a "typical" price.
- **Toyota alone is ~39% of the entire market** (1,126 of ~2,900 listings); together with Honda, Lexus, and Mercedes-Benz it makes up roughly **69%** of all listings.
- **Lagos (50%) and the FCT (23%) account for 73% of all listings** — this is really a two-city market with a long tail, not a national one. Despite that, median price barely differs between them, so location alone doesn't command a premium.
**Why it matters:** Before asking what drives price, it's worth knowing this market isn't evenly spread — it's Toyota-dominated and Lagos/Abuja-concentrated, which shapes how any other finding should be read.
 
---
 
### Section 2: The Real Price Driver — Age, Not Mileage
**Goal:** Answer the core question: what actually moves the price of a car?
 
**What I did:** Compared median price across condition categories (Foreign Used, Nigerian Used, Brand New), then ran a correlation check between price and each numeric spec — manufacture year, mileage, engine size, and horsepower.
 
**Findings:**
- **Foreign Used cars carry a median price ~2.2x higher** than Nigerian Used cars, despite being only 17% of listings.
- **Manufacture year correlates with price at 0.58** — a real, moderate relationship. **Mileage correlates at just 0.07** — essentially no relationship.
- Bucketed by 5-year age bands, price rises steeply with recency: the newest cars (2016+) carry a median price **roughly 11.5x higher** than cars from 2000 or earlier — and the sharpest jump happens once a car crosses into that "recent" band.
**Why it matters:** This is the single most important — and most counterintuitive — finding in the project. The usual instinct is that low mileage should command a premium, the way it does in most used-car markets. Here it barely registers. **Buyers are pricing almost entirely on how old a car is and where it was imported from, not how far it's been driven.** That's the non-obvious insight worth leading with.
 
---
 
### Section 3: Brand and Body Type Premiums
**Goal:** Check whether brand and body type still matter on top of the age effect already found.
 
**What I did:** Compared median price by make and by body type, restricted to brands and categories with meaningful listing volume.
 
**Findings:**
- **Land Rover, Mercedes-Benz, and Lexus** command the highest median prices; **Peugeot and Honda** sit at the bottom.
- **SUVs** average roughly **1.7x** the price of Sedans, and make up the largest share of listings with a known body type.
**Why it matters:** Brand and body type layer on top of age rather than replacing it — a luxury badge or an SUV body still adds a real premium, but the age effect from Section 2 remains the dominant force underneath.
 
---
 
### The Full Picture
 
Read together, this project answers one question cleanly: **in this market, a car's price is set almost entirely by how old it is and where it was imported from — not by how far it's been driven.** That's backed by a correlation check (0.58 for age vs. 0.07 for mileage), not just intuition. Toyota sets the market's center of gravity by sheer volume, Lagos and the FCT are where that market actually lives, and luxury brands and SUVs add a real but secondary premium on top of the age effect. *(Worth flagging: body type and trim are missing for a large share of listings, and a handful of outlier entries — impossible engine sizes, zero mileage on "used" cars — were excluded from the cleaner comparisons above.)*


Tools: Data Analytics | Excel

🔗 [View Project](https://github.com/Shodunke-Feranmi/Car45-Sales/blob/main/README.md)

---
### 🪑 Furniture Sales Excel Project
 
A profitability investigation built on 2,121 order line items across four years (2014–2017) of furniture sales. Structured around one central tension: sales kept growing, but profit didn't — and the dashboard exists to explain why.
 
---
 
### The Premise
 
A business can grow its top line every year and still be quietly dying underneath it, and that's exactly what this dataset showed. Across **2,121 line items**, **1,764 orders**, and **$741,999.80 in total sales**, the company only kept **$18,451.27 in profit** — a **2.5% margin**. This project's job was to find out where that margin was actually going, and it turned out to trace back to a small set of very specific, fixable decisions.
 
---
 
### Section 1: The Growth-Without-Profit Paradox
**Goal:** Start with the headline number leadership actually cares about — is the business getting healthier or weaker year over year?
 
**What I did:** Compared 2017 against 2016 on sales, quantity, and profit, and tracked the margin trend across the full four-year window.
 
**Findings:**
- **2017 sales rose to $215.4K, up 8% from $198.9K in 2016**, and units sold rose **11%**
- **2017 profit fell to $3.0K — down 57% from $7.0K in 2016**
- The overall profit margin dropped from **3.5% in 2016 to just 1.4% in 2017**
**Why it matters:** This is the number that frames the entire project. Growing sales usually reads as good news, but here it's the opposite — the business sold more and made less doing it, which means the problem isn't demand. Something in how those sales were being made (pricing, discounting, product mix) was actively working against the company.
 
---
 
### Section 2: The Discount Leak
**Goal:** Find the actual mechanism behind Section 1's paradox — what's eating the margin on every extra sale?
 
**What I did:** Bucketed every line item by its discount level and compared the resulting profit margin at each level, then measured how many line items were outright unprofitable.
 
**Findings:**
- Full-price line items earn a healthy **22.7% margin**
- Line items discounted **20–30% flip to roughly −11% margin**
- Line items discounted **30–50% collapse to roughly −39% margin**
- **About 34% of all line items lose money**, totaling roughly **$61K in losses** — which wipes out about 77% of the profit earned everywhere else
**Why it matters:** This is the direct answer to the Section 1 paradox. It isn't that the company is selling more low-margin items by accident — it's that a specific, sizeable chunk of transactions are being discounted into losses. A third of all sales activity is actively working against profitability, which is a policy problem (how discounts get approved), not a market problem.
 
---
 
### Section 3: Which Products Are Actually the Problem
**Goal:** Take the discount finding down to the product level — which categories are absorbing the damage, and which are carrying the business?
 
**What I did:** Broke sales and profit down by sub-category, and checked average discount rate alongside profit for each one.
 
**Findings:**
- **Tables**: the second-largest category by sales ($206,966), but **losing $17,725** overall, at an average discount around **26%**, and getting worse in 2017 specifically
- **Bookcases**: also unprofitable, **losing $3,473**
- **Chairs**: the clear winner, generating **$26,590 in profit**, the most of any category
- **Furnishings**: the smallest category by sales but the healthiest, with the best margin at roughly **14.2%**
**Why it matters:** Two categories (Tables and Bookcases) are actively subtracting from the bottom line while two others (Chairs and Furnishings) are carrying the entire profit of the business. This reframes the Section 2 discounting problem into something concrete and actionable: it's not "discounting in general," it's Tables specifically that needs a pricing or supplier-cost review before anything else.
 
---
 
### Section 4: Where the Losses Are Hiding
**Goal:** Check whether the profit problem is evenly spread geographically, or concentrated somewhere specific.
 
**What I did:** Broke sales and profit down by state and city, comparing top-selling locations against their actual profitability.
 
**Findings:**
- **California is the largest single market (about 21% of total sales) but earns only a 6% margin** — high volume, thin profit
- The **Central region loses money outright** (−$2.9K), driven by the heaviest average discounting of any region (about 30%)
- **Philadelphia and Houston — both strong-selling cities — actually lose money** (−$6.8K and −$3.4K respectively) despite their sales volume
**Why it matters:** This is the same pattern as Section 3, just viewed geographically: high sales volume doesn't guarantee profit, and in several of the biggest markets it's masking a loss. A leadership team looking only at a "top markets by revenue" report would miss this entirely — it takes a profit-by-location view to catch it.
 
---
 
### Section 5: Seasonality
**Goal:** Understand when demand actually happens, separate from the profitability question, since it affects staffing and inventory decisions regardless of margin.
 
**What I did:** Grouped sales by month across all four years to find the demand curve.
 
**Findings:**
- **September through December generates about 55% of annual sales**, with **December as the single strongest month**
- **February is the weakest month** by a wide margin
**Why it matters:** This is a genuinely separate lever from everything above — even after fixing the discount and product problems, the business still needs to plan inventory and staffing around a real Q4 surge, and use the slow months (like February) for targeted, controlled promotions rather than the blanket discounting shown in Section 2 to be causing damage.
 
---
 
### The Full Picture
 
Read together, this project traces one thread from a single headline number down to a specific, fixable cause: **sales grew 8% while profit fell 57%, and the reason is that roughly a third of all transactions are being discounted into a loss — concentrated specifically in Tables and Bookcases, and geographically visible even in top-selling markets like Philadelphia, Houston, and Central region.** The fix isn't "sell more" or "discount less everywhere" — it's a targeted discount cap, a pricing review on two specific product categories, and treating California's high volume with appropriate skepticism about what it's actually worth. That's the sentence I'd lead with if asked to summarize the whole project.
Tools: Microsoft Excel

🔗 [View Project](https://github.com/Shodunke-Feranmi/Furniture-sales-excel-Project/blob/main/README.md)

---

## 🗄️ SQL Projects
 
A batch of MySQL projects covering CRM sales, banking fraud risk, academic records, entertainment analytics, and public safety data.
 

 
### 🏦 North Axis Bank: Fraud & Risk Analysis
A public-safety analysis of over 340,000 people involved in road accidents across 37 Nigerian states, built to answer where and when intervention would actually make a difference.
 
---
 
### The Premise
 
Treating every state and every year the same wastes limited road-safety resources — real risk clusters in specific places and specific times, and the job of this project was to find exactly where. Using five years of state-level accident data (2020–2024), it answers three questions: which states are actually the highest risk, whether risk is rising or falling over time, and whether high accident *volume* in a state always means high *severity*.
 
---
 
### Section 1: The National Scale of the Problem
**Goal:** Establish the headline numbers before breaking anything down by state or year.
 
**What I did:** Summed people involved, casualties, deaths, and injuries across all 666 state-quarter records from 2020 to 2024.
 
**Findings:**
- **342,607 people involved** in road accidents nationally, resulting in **179,562 total casualties**
- **25,462 people killed** and **154,137 injured**, across **52,745 total recorded cases**
**Why it matters:** These totals are the scale of the problem before any targeting — every state-level and year-level finding below is a way of asking "where inside this number should attention go first?"
 
---
 
### Section 2: Risk Is Concentrated in a Predictable Cluster
**Goal:** Find out whether accident risk is evenly spread across Nigeria's 37 states, or concentrated in a specific group.
 
**What I did:** Ranked states by people involved, deaths, and total cases, then classified every state into a Low/Mid/High casualty tier.
 
**Findings:**
- **Kaduna (28,721), Ogun (29,175), and the FCT (29,111)** lead in people involved, far ahead of the national spread; **Bayelsa (903)** has by far the fewest
- **Kaduna has the most deaths (2,641)**, ahead of Ogun (1,723) and Niger (1,662)
- Casualty-tier classification puts **7 states in the HIGH-risk tier**: Bauchi, FCT, Kaduna, Nasarawa, Niger, Ogun, and Oyo — versus 10 Mid and 20 Low
- **Kaduna stands out as the single highest-risk state overall** — it leads in deaths, in fatal-severity cases (1,193), and ranks near the top in people involved
**Why it matters:** This directly answers the project's first question — risk is not evenly spread. Seven specific states account for a disproportionate share of harm, and Kaduna alone is worth prioritizing above every other state on the list.
 
---
 
### Section 3: 2022 Was a Clear Outlier Year
**Goal:** Check whether the problem is getting better, worse, or staying flat over the five years of data available.
 
**What I did:** Compared total people involved and average deaths per record, year by year, and repeated the same comparison by quarter to check for seasonal patterns.
 
**Findings:**
- **2022 was the worst year on record**, both in volume (89,143 people involved — the highest of any year) and in severity (43.62 average deaths per record — also the highest)
- 2020, 2023, and 2024 are all noticeably lower than 2022 on both measures
- At the national level, accidents don't show a strong seasonal pattern — **Q1 through Q4 are all within about 5% of each other** in total people involved
- The single worst quarter in the entire dataset is **Q1 2022**, tied to the same outlier year rather than a recurring seasonal spike
**Why it matters:** This rules out a tempting but wrong conclusion — that accidents spike in a predictable season every year. They don't. What actually stands out is a single anomalous year, which raises a different, more useful question: did something specific change in 2022 (enforcement, reporting, travel volume) that's worth investigating directly, rather than planning around a "dangerous quarter" that doesn't really exist nationally.
 
---
 
### Section 4: Volume and Severity Don't Always Match
**Goal:** Check whether the states with the most recorded cases are also the states where those cases are most severe.
 
**What I did:** Compared each state's total case count against its death count and fatal-severity case count directly.
 
**Findings:**
- The **FCT has the most recorded cases of any state (5,779)** — more than Kaduna
- But **Kaduna has more deaths and more fatal-severity cases than the FCT**, despite having fewer total cases
**Why it matters:** This is the most useful nuance in the whole project. A state with more accidents isn't automatically the state where those accidents are deadliest. The FCT's cases, on average, appear to be less severe, while Kaduna's smaller case count is producing a disproportionately high death toll — something worth investigating directly (road type, speed limits, emergency response time) rather than assuming case volume alone tells the full risk story.
 
---
 
### The Full Picture
 
Read together, this project makes a specific, resource-allocation-ready recommendation: **prioritize a cluster of seven HIGH-tier states, with Kaduna as the single highest priority given its death toll and severity, not just its case count; treat 2022 as a flagged anomaly worth investigating on its own rather than assuming a recurring seasonal risk pattern; and remember that case volume and severity are different things — a state with fewer accidents can still be the deadlier one.**

🔗 [View Project](https://github.com/Shodunke-Feranmi/Northaxis-Bank-Risk-analysis)

---
 
### 🎓Student Biodata Database
 
A relational database project built to answer a deceptively simple question: can four linked tables actually stay in sync as students are added, and what does the data say about the cohort itself?
 
---
 
### The Premise
 
Academic records systems fall apart quietly — a student gets added to the main roster but never makes it into the attendance sheet, and nobody notices until a report comes out wrong. This project builds a small but complete version of that system (42 students linked across biodata, department, courses, and attendance, all tied together by student ID) specifically to test whether it holds together, and to profile who the cohort actually is.
 
---
 
### Section 1: Who's in the Cohort
**Goal:** Establish a demographic baseline before checking anything about performance or data integrity.
 
**What I did:** Queried the student biodata table directly for gender, level, age, and department distribution.
 
**Findings:**
- **42 students**: 23 male, 19 female, averaging **19.7 years old** (range 18–22)
- Levels are fairly balanced: **200L is largest (13 students)**, then 300L (11), 100L (10), 400L (8)
- **Computer Science is the largest department (9 students)**, followed by Accounting and Arts (7 each)
- By faculty, **Science leads with 22 students (about 52% of the cohort)**, ahead of Arts (13) and Accounting (7)
**Why it matters:** This is a Science-heavy cohort with no single department overwhelming the picture — useful for anyone using this dataset to plan resourcing (lab space, staffing) proportionally rather than assuming an even split.
 
---
 
### Section 2: Attendance Is a Real Concern
**Goal:** Move past headcounts and check whether the thing the system is meant to track — attendance — actually looks healthy.
 
**What I did:** Aggregated the attendance table by status, and broke it down day by day.
 
**Findings:**
- **Overall attendance rate is 58.5%** (24 present out of 41 recorded)
- Day-by-day attendance swings widely — some sessions show full turnout (3 of 3 present), others show **zero attendance** at all
- One inconsistency in the raw data: a single record uses lowercase `'present'` while every other entry uses `'Present'` — a small thing, but it would silently break an exact-match query
**Why it matters:** A 58.5% attendance rate is low enough to be a genuine finding, not just a data artifact — if this were a real cohort, it would justify a closer look at specific dates with zero turnout rather than assuming the average tells the whole story.
 
---
 
### Section 3: The Integrity Check Actually Caught Something
**Goal:** Test the core premise of the project — do the four linked tables actually stay consistent when a new student is added?
 
**What I did:** Ran anti-join checks (`NOT IN` queries) comparing student IDs across all four tables to find any student missing from a linked table.
 
**Findings:**
- **Student 42 (added in a follow-up `INSERT` after the initial batch) has a department record, but no course enrollment and no attendance record at all**
- Every other student (1–41) is fully consistent across all four tables
**Why it matters:** This is the most important result in the whole project, because it's not a hypothetical — it's a real gap that the integrity queries were specifically designed to catch, and they did. It's direct proof that the checks work, not just that they exist.
 
---
 
### The Full Picture
 
Read together, this project does two things at once: it profiles a Science-leaning, fairly balanced cohort with a genuine attendance problem worth investigating, and it proves out a working data-integrity process by catching a real, late-arriving student who fell through the cracks between tables. That combination — descriptive analysis plus a working integrity check that actually finds something — is the throughline worth leading wit

🔗 [View Project](https://github.com/Shodunke-Feranmi/Student-biodata)


---
 
### 📺 Parks and Recreation: Episode & Ratings Analysis
A SQL analysis of 125 episodes of Parks and Recreation, built around a question that turned out to have a genuinely counterintuitive answer: does a show's live viewership actually match how well it holds up critically?
 
---
 
### The Premise
 
Two tables — one tracking live US viewership per episode, one tracking IMDb ratings — normally get treated as measuring roughly the same thing: "how good was this episode." This project joins them to check whether that assumption holds, using 125 episodes across 7 seasons.
 
---
 
### Section 1: The Viewership Baseline
**Goal:** Establish what a typical episode looked like before comparing seasons or contributors against each other.
 
**What I did:** Aggregated total and average viewership, and pulled the top individual episodes by viewership.
 
**Findings:**
- **125 episodes**, averaging **3.86M US viewers**, for **482.3M total views** across the series
- The **Pilot is the single most-watched episode** (6.77M viewers), followed by Season 3's "Go Big or Go Home" (6.14M) and "Canvassing" (5.92M)
**Why it matters:** The most-watched episode being the Pilot is expected — new-show curiosity usually peaks early — but it sets up the real question in Section 2: did the show's *quality*, not just its audience, peak early too, or did it improve as viewership declined?
 
---
 
### Section 2: Viewership vs. Rating — The Inverse Relationship
**Goal:** Directly test whether high viewership correlates with high critical reception, season by season.
 
**What I did:** Compared average viewership by season against average IMDb rating by season, and ran a correlation check across all matched episodes.
 
**Findings:**
- **Season 1 has the highest average viewership (5.35M per episode)** — despite being the shortest season at just 6 episodes — but the **lowest average IMDb rating (7.23)** of any season
- **Season 3 has the highest average IMDb rating (8.51)**, without ever matching Season 1's viewership
- Across all matched episodes, US viewers and IMDb rating correlate at **−0.16** — a slight negative relationship, not a positive one
**Why it matters:** This is the central finding of the project, and it directly contradicts the assumption from Section 1. The season that pulled in the most live viewers is the one critics and long-term audiences rated the worst, while the season with the best writing (by rating) never had the biggest audience. Live viewership and lasting quality are measuring genuinely different things here.
 
---
 
### Section 3: Who Made the Show, and Did It Decline?
**Goal:** Check the show's trajectory over time, and see whether specific contributors line up with its high points.
 
**What I did:** Counted writing and directing credits, ranked writers by average viewership, and tracked viewership trend across all seven seasons.
 
**Findings:**
- **Michael Schur** holds the most writing credits (12 episodes); **Dean Holland** directed far more episodes than anyone else (27)
- Viewership declined steadily after Season 1, bottoming out in **Season 6 (2.94M average)** — typical of long-running network sitcoms
- **Season 7 has the two highest-rated individual episodes in the entire series** ("One Last Ride" and "Leslie and Ron," both at 9.6), meaning the show's quality held up or even peaked right at the end, opposite to its viewership trend
**Why it matters:** This reinforces Section 2 from a different angle — the show got smaller in audience but didn't get worse in quality, and in fact closed on its two best-rated episodes ever. That's a stronger, more specific version of the same finding.
 
---
 
### The Full Picture
 
Read together, this project's answer to its central question is clear: **live viewership and critical/audience rating are not proxies for each other on this show — they move in opposite directions.** Season 1 won on audience size and lost on quality; the finale won on quality while the show's audience had shrunk to a fraction of where it started. Anyone using viewership alone to judge whether a show "still works" would draw the wrong conclusion here.

🔗 [View Project](https://github.com/Shodunke-Feranmi/Parks-and-Rec-SQL-)

---
 
### 🚧 Road and Transport Accidents Analysis
A public-safety analysis of over 340,000 people involved in road accidents across 37 Nigerian states, built to answer where and when intervention would actually make a difference.
 
---
 
### The Premise
 
Treating every state and every year the same wastes limited road-safety resources — real risk clusters in specific places and specific times, and the job of this project was to find exactly where. Using five years of state-level accident data (2020–2024), it answers three questions: which states are actually the highest risk, whether risk is rising or falling over time, and whether high accident *volume* in a state always means high *severity*.
 
---
 
### Section 1: The National Scale of the Problem
**Goal:** Establish the headline numbers before breaking anything down by state or year.
 
**What I did:** Summed people involved, casualties, deaths, and injuries across all 666 state-quarter records from 2020 to 2024.
 
**Findings:**
- **342,607 people involved** in road accidents nationally, resulting in **179,562 total casualties**
- **25,462 people killed** and **154,137 injured**, across **52,745 total recorded cases**
**Why it matters:** These totals are the scale of the problem before any targeting — every state-level and year-level finding below is a way of asking "where inside this number should attention go first?"
 
---
 
### Section 2: Risk Is Concentrated in a Predictable Cluster
**Goal:** Find out whether accident risk is evenly spread across Nigeria's 37 states, or concentrated in a specific group.
 
**What I did:** Ranked states by people involved, deaths, and total cases, then classified every state into a Low/Mid/High casualty tier.
 
**Findings:**
- **Kaduna (28,721), Ogun (29,175), and the FCT (29,111)** lead in people involved, far ahead of the national spread; **Bayelsa (903)** has by far the fewest
- **Kaduna has the most deaths (2,641)**, ahead of Ogun (1,723) and Niger (1,662)
- Casualty-tier classification puts **7 states in the HIGH-risk tier**: Bauchi, FCT, Kaduna, Nasarawa, Niger, Ogun, and Oyo — versus 10 Mid and 20 Low
- **Kaduna stands out as the single highest-risk state overall** — it leads in deaths, in fatal-severity cases (1,193), and ranks near the top in people involved
**Why it matters:** This directly answers the project's first question — risk is not evenly spread. Seven specific states account for a disproportionate share of harm, and Kaduna alone is worth prioritizing above every other state on the list.
 
---
 
### Section 3: 2022 Was a Clear Outlier Year
**Goal:** Check whether the problem is getting better, worse, or staying flat over the five years of data available.
 
**What I did:** Compared total people involved and average deaths per record, year by year, and repeated the same comparison by quarter to check for seasonal patterns.
 
**Findings:**
- **2022 was the worst year on record**, both in volume (89,143 people involved — the highest of any year) and in severity (43.62 average deaths per record — also the highest)
- 2020, 2023, and 2024 are all noticeably lower than 2022 on both measures
- At the national level, accidents don't show a strong seasonal pattern — **Q1 through Q4 are all within about 5% of each other** in total people involved
- The single worst quarter in the entire dataset is **Q1 2022**, tied to the same outlier year rather than a recurring seasonal spike
**Why it matters:** This rules out a tempting but wrong conclusion — that accidents spike in a predictable season every year. They don't. What actually stands out is a single anomalous year, which raises a different, more useful question: did something specific change in 2022 (enforcement, reporting, travel volume) that's worth investigating directly, rather than planning around a "dangerous quarter" that doesn't really exist nationally.
 
---
 
### Section 4: Volume and Severity Don't Always Match
**Goal:** Check whether the states with the most recorded cases are also the states where those cases are most severe.
 
**What I did:** Compared each state's total case count against its death count and fatal-severity case count directly.
 
**Findings:**
- The **FCT has the most recorded cases of any state (5,779)** — more than Kaduna
- But **Kaduna has more deaths and more fatal-severity cases than the FCT**, despite having fewer total cases
**Why it matters:** This is the most useful nuance in the whole project. A state with more accidents isn't automatically the state where those accidents are deadliest. The FCT's cases, on average, appear to be less severe, while Kaduna's smaller case count is producing a disproportionately high death toll — something worth investigating directly (road type, speed limits, emergency response time) rather than assuming case volume alone tells the full risk story.
 
---
 
### The Full Picture
 
Read together, this project makes a specific, resource-allocation-ready recommendation: **prioritize a cluster of seven HIGH-tier states, with Kaduna as the single highest priority given its death toll and severity, not just its case count; treat 2022 as a flagged anomaly worth investigating on its own rather than assuming a recurring seasonal risk pattern; and remember that case volume and severity are different things — a state with fewer accidents can still be the deadlier one.**

🔗 [View Project](https://github.com/Shodunke-Feranmi/Road-and-Transport-)

---

## 🎧 Spotify 2023 Most Streamed Songs Analysis
 
A Power BI dashboard built on Spotify's most-streamed tracks, structured around one goal: find the real signal in the numbers, and catch the places where the dashboard itself was lying.
 
---
 
### The Premise
 
A five-year streaming dataset (2019–2023) covering top artists, top songs, danceability, and platform distribution sounds straightforward to summarize — until you actually read the numbers closely. This project's real value wasn't just building the dashboard, it was catching two places where the visuals were technically rendering but telling the wrong story.
 
---
 
### Section 1: The Real Trend Behind the Numbers
**Goal:** Establish the streaming trend across 2019–2023 without being misled by a partial final year.
 
**What I did:** Read the "Streams in the Last Five Years" chart and checked each year's total against the others before drawing any conclusion about growth or decline.
 
**Findings:**
- **2022 was the true peak year at 288bn streams**, up 22.6% from 2021 (235bn)
- **2023 shows only 78bn** — but this is a partial year of data, not a real collapse in streaming
- 2020 was the low point (138bn, down 11.5% from 2019), before rebounding sharply in 2021 (+70.3%)
**Why it matters:** The obvious read of this chart is "streaming fell off a cliff in 2023." That's wrong, and saying it out loud in a defense would be an easy point for a panel to catch. The correct read is that 2022 is the real benchmark year, and 2023 needs to be labeled "year to date" everywhere it appears.
 
---
 
### Section 2: Who Actually Dominates
**Goal:** Identify which artists and songs carry the platform's total streaming volume.
 
**What I did:** Read the Top 10 Artists and Top 10 Songs charts and summed them against the five-year total.
 
**Findings:**
- **Ed Sheeran (56bn) and The Weeknd (54bn) lead all artists**, with the top 10 artists combining for **308bn streams**
- **"Blinding Lights" (18.5bn) is the single most-streamed song**, ahead of "Shape of You" (17.8bn)
**Why it matters:** This is a genuinely concentrated market — a small number of artists and songs carry a large share of total volume, which matters for anyone using this kind of data to plan licensing, playlist placement, or marketing spend.
 
---
 
### Section 3: Catching Two Broken Charts
**Goal:** Verify that every chart on the dashboard is actually measuring what its title claims — the most valuable part of this project.
 
**What I did:** Cross-checked the Platform donut chart and the Danceability chart against what a real distribution should look like.
 
**Findings:**
- **The Platform chart shows an exact 20% split across all 5 platform categories** (Apple Charts, Apple Playlists, Deezer Charts, Deezer Playlists, Shazam Charts) — a real streaming split essentially never lands on a perfectly even five-way tie
- **The Danceability chart shows values up to 705** — impossible for a metric that should sit on a 0–100% scale
**Why it matters:** Both point to the same underlying cause: a measure summing a value once per matching row instead of aggregating it correctly (most likely per platform-tag or per duplicate chart appearance). This is the single most defensible finding in the project, because it's not an opinion — it's a chart that's mathematically impossible as labeled, caught by simply reading the axis carefully instead of trusting the visual.
 
---
 
### The Full Picture
 
Read together, this project's real thesis isn't just "here's what's popular on Spotify" — it's "here's what's popular, and here's exactly which two charts on this dashboard can't be trusted until their measures are fixed." That's the sentence I'd lead with if asked to summarize it: **the data tells a real story about artist and song concentration, but two of the six visuals are producing numbers that are mathematically impossible, and I can show exactly why.**
 
📊 Full write-up, dashboard, and workbook: 


🔗 [View Project](https://github.com/Shodunke-Feranmi/Spotify2023-Streams)

---

## 💼 CRM Sales Opportunities Analysis (Excel → SQL → Power BI)
 
A full three-tool pipeline — Excel for cleaning, MySQL for analysis, Power BI for visualization — built around a sales pipeline of 7,375 deals. This is the one where cross-checking one tool's output against another caught a real, systematic bug before it could be presented as fact.
 
 
---
 
### The Premise
 
Most projects stop at "here's the dashboard." This one is structured to show the full chain: Excel cleaned four raw tables, MySQL ran the actual analysis and is the authoritative source of every number, and Power BI turned that analysis into a 5-page interactive dashboard. The most important part of the project turned out to be verifying that the last step (Power BI) still agreed with the first two.
 
---
 
### Section 1: The SQL Analysis — What's Actually True
**Goal:** Establish the ground truth before building anything visual on top of it.
 
**What I did:** Ran the full SQL analysis directly against the cleaned CSVs — revenue, win rate, top accounts, top products, and agent/regional performance.
 
**Findings:**
- **$10.0M in closed revenue** across **7,375 deals**, **4,238 won**, for a **63.15% win rate**
- **Kan-code, Konex, and Condax** are the top three accounts by revenue
- **GTX Pro and the GTX series dominate product revenue** (about 73% of the total)
- Deals close within **±1.5% of list price** — genuine pricing discipline
- **The agent performance gap (70.4% vs. 55.0%) is far wider than the regional gap (63.9% vs. 62.6%)** — coaching matters more than region
**Why it matters:** This is the number set everything else gets checked against. Without this step done first and done carefully, there's no way to know later whether the dashboard is telling the truth.
 
---
 
### Section 2: Building the Dashboard — And Everything Lining Up
**Goal:** Turn the SQL findings into a usable, filterable Power BI report across five pages (Overview, Account Analysis, Product Analysis, Sales Analysis, Sales Team Analysis).
 
**What I did:** Modeled the data in Power BI and rebuilt each SQL question as a corresponding visual, then checked every ranking and percentage against the SQL output.
 
**Findings:**
- **Every ranking and every percentage matched**: Retail as the top sector, Rangreen's 75% win rate, the 84/79/78 regional account split, West's lead on regional win rate — all consistent with the SQL analysis
- The dashboard added real value the SQL couldn't: a **filterable, presentation-ready view** anyone on the team could explore without writing a query
**Why it matters:** Getting the rankings and percentages to match perfectly across two independently-built systems is a strong sign the underlying model was built correctly — which made the next finding stand out even more sharply.
 
---
 
### Section 3: The Numbers That Didn't Match — A Real Bug, Caught
**Goal:** Stress-test the dashboard by checking its absolute totals against the SQL analysis, not just its rankings.
 
**What I did:** Compared specific dollar and count figures — total revenue, individual account revenue, monthly deal counts — directly between the SQL output and the Power BI dashboard.
 
**Findings:**
- **Every absolute number in the dashboard is almost exactly 2.0x the real SQL figure**, to three or more significant figures: $10.0M revenue became $20M, Kan-code's $341,455 became $683K, June's 531 deals sold became 1,062
- **Every percentage-based number stayed correct**, because dividing two doubled numbers cancels the error out — which is exactly why the rankings in Section 2 all looked fine
**Why it matters:** This is the single most valuable finding in the whole project. A fan-out (many-to-many) relationship in the Power BI data model was silently doubling every summed measure, and it was invisible unless someone specifically checked absolute values against an independent source. I traced a plausible root cause too: the SQL script itself has a real bug where two different source CSVs (`CRMEQaccounts.csv` and `CRMEQsales_team.csv`) both load into the same table, which is exactly the kind of duplicate-key setup that produces this failure mode if carried into the Power BI model.
 
---
 
### The Full Picture
 
Read together, this project's real thesis is: **build the SQL analysis first as ground truth, then never trust a dashboard's absolute numbers just because its rankings and percentages look right — check both, because rate-based measures can hide a doubling error that dollar totals will not.** That's a genuinely defensible, technical finding, and it's the direct result of using three tools instead of one and refusing to let the last one go unchecked.
 
📊 Full write-up, SQL script, Excel workbook, and dashboard: 
🔗 [View Project](
 
--

## 👟 Nike Sales Dashboard
 
A Power BI dashboard analyzing Nike's regional profit, monthly trend, sales channels, and product performance — built around finding which numbers were real signal and which were data artifacts.
 
---
 
### The Premise
 
A regional sales dashboard is only as useful as the labels on its axes. This project analyzes Nike's profit and sales data across Indian cities, channels, and products — and a meaningful part of the work was checking whether the dashboard's own regional and time-based groupings actually held up under scrutiny.
 
---
 
### Section 1: Where the Profit Actually Sits
**Goal:** Identify which regions and channels are actually driving Nike's profit.
 
**What I did:** Read the Regional Profits chart and the Sales Channel donut, and summed both against their stated totals.
 
**Findings:**
- **Mumbai leads all regions in profit (₹115K)**, followed by Kolkata (₹110K) and Delhi (₹95K) — the top three account for over half of the ₹552K total across all seven listed regions
- **Retail (52.84%) narrowly outsells Online (47.16%)** — close enough that neither channel should be deprioritized
**Why it matters:** Profit is concentrated in a handful of cities, which is useful for prioritizing investment, but the channel split is close enough that this isn't a "shut down Online" or "shut down Retail" story — both are pulling real weight.
 
---
 
### Section 2: A Duplicate Hiding in Plain Sight
**Goal:** Verify that every labeled category in the dashboard represents a genuinely distinct entity.
 
**What I did:** Checked the Regional Profits chart's seven city labels against real-world geography.
 
**Findings:**
- **"Bangalore" and "Bengaluru" both appear as separate regions** in the same chart — but these are the same city, renamed officially in 2014
**Why it matters:** This is the kind of error that's easy to miss because the chart still renders and looks plausible, but it means one real market's profit is very likely being split across two labels, understating that region's true rank. Catching this before presenting regional rankings is the difference between a dashboard that looks right and one that is right.
 
---
 
### Section 3: Growth That Isn't What It Looks Like
**Goal:** Check whether the year-over-year unit sales trend is a real growth story.
 
**What I did:** Compared 2023, 2024, and 2025 unit sales directly rather than accepting the jump at face value.
 
**Findings:**
- **2024 (338 units) and 2025 (332 units) are close to each other**, but **2023 shows only 51 units** — a jump so large (over 500%) that it's a strong signal of a partial year, not real year-over-year growth
**Why it matters:** Presenting all three years side by side without flagging this would tell an inflated growth story that isn't real. The honest comparison is 2024 vs. 2025 — both strong, roughly flat — with 2023 excluded or clearly labeled as partial.
 
---
 
### The Full Picture
 
Read together, this project makes a specific, calibrated claim: **Mumbai, Kolkata, and Delhi are the real profit centers; Retail and Online are close enough to both deserve investment; and two of the dashboard's own labels (the Bangalore/Bengaluru split and the 2023 partial year) need fixing before any of the regional or growth numbers are presented as final.** That combination — real business insight plus caught labeling errors — is the same pattern I look for on every dashboard before trusting what it shows.
 
📊 Full write-up, dashboard, and workbook: 
🔗 [View Project](
--
## 🎯 Current Goals

* Build more real-world data analytics projects
* Improve my SQL skills
* Become more confident with Power BI Visualization
* Learn Python for data analysis
* Develop stronger data storytelling skills
* Build a professional data analytics portfolio

---


## 🤝 Let's Connect

I'm always open to connecting with other students, analysts, developers, and professionals interested in technology and data.

* 📧 Email: [shodunkeferanmi@gmail.com](mailto:shodunkeferanmi@email.com)
* 🐙 GitHub: [Shodunke-Feranmi](https://github.com/Shodunke-Feranmi)

---

 Feel free to explore my repositories and follow my journey as I continue learning, building, and growing in the world of data.
