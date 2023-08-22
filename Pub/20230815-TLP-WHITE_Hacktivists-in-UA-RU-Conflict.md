# Hacktivists in Ukraine-Russia Conflict

## Intro
- Since the beginning of the Ukraine invasion in 2022, we observed multiple hacktivists entities involved in the conflict, this document aims to centralize the information collected and provides a short analysis of their operating methods, financing models and some ideas on how-to report on this threat actor type, Mitre ATT&CK mapping.


## Disclaimer
- The scope encompass my own collection from January 2022 to July 2023 included, it is mostly based on publicly available data, some Telegrams & VK groups were private.
- The following analysis will not contain Hacktivist entities & alliances names to not make them any publicity
- I can be wrong, I'm a human, do not hesitate to comment the analysis


## Hacktivists Persona
### General
- Under this word, a lot is encompassed, sometimes wrongfully, sometimes correctly
- We are going to retain the following definition of Hacktivists here: "ideologically motivated non-state entities using computer-based techniques"

### Hacktivist, Hacktivists, Hacktivists Group, Galaxy (All entities)
- You certainly seen all these terms used in different reports, by both cybersecurity & medias companies
- We have seen during this conflict:
  * the Hacktivist entity being only one physicial entity
  * one entity behind multiple Hacktivists entities
  * multiple entities reported as individual entities when in fact, they were sub-projects of one entity
  * mutiple entities reported as individual entities when in fact, they were divisions / departments of one entity
  * Several reroll (same team) but new entity, changing entity name

### Hacktivists alliances
- The alliancy system is not something new, we already witnessed this during the era of Anonymous attacks against Scientology
- Some link between entities can be compared to a feudal system, where you need to be knighted by the King to be part of the alliances
- Other alliances can be formed because you will support the attack that an entity launched (eg. FCKNATO & RIPGermany)
- One entity coordinating its attacks with others entities, making the attacks more powerful than an isolated one (in the most of the cases, and it's almost always DDoS attacks)
- One entity supported foreign Hacktivists entities DDoS operations to be supported in its own DDoS operations in return

### Fake Hacktivist type persona
- We have seen several entities outed by Cybersecurity companies or Ukraine Government officials as fake hacktivists
- It is something common in the cybersecurity field but you can find this also in classic spy literature where a group or indivual claimed to be independent people and not linked to any state when in the end you will learned they were directed / financed by some state.
- Russia shown their use of Fake hacktivists entities several times during this conflict
- When it is more complicated to established, some Pro-ukrainian hacktivists entities can also be linked to Ukrainian government too
- No big news here, the both side use this fake hacktivist type personas as it is a plausible deniability of their actions

### Anonymous
- Anonymous is an umbrella for ideological motivated movements
- This is not relevant to say "Anonymous attacked Russia" or "Anonymous attacked Ukraine" if you do not mention more identifying element regarding the group origin (Like their Telegram channel)
- Also, in the Ukraine - Russia conflict, several groups claimed to be anonymous, both from Russia & Ukraine


## Hacktivists attacks TTPs in nutshell
- Hacktivists attacks are unsophisticated but some of them have been significant & relevant

### Attacks means seen in the wild
- DDoS attacks (With their own botnet, renting botnets, having alliance or publicity agreement with botnet owners, organizing DDoS attacks contests,..)
- Defacements
- Fake reviews : coordinated mass posting of bad reviews (Google, the targets website and others) | CIB
- Social Network abuse report : coordinated mass report for abuse (suppress profile pages by using mass report mechanisms) | CIB
- Doxxing individual people (Eye of God, nudes, sexual orientation, personal address, email, phone, family or friends mapping, harassment)
- Leaking data & credentials
- Fake bomb email alerts
- Threatening phone calls
- Information Systems Intrusions
- Ransomware & wipers (Modified existing ransomware previously leaked builders, on one hacktivist entity they removed the decryption routine code making the ransomware code a wiper)

### Hacktivists platforms
- Telegram (Mostly used to coordinate operations, operations announcements, short videos, recruitment,automated bots, ...)
- Twitter (operations announcements, recruitments)
- Telegraph (Telegra.ph, used to published long posts with pictures)
- Check-Host (Website Availability service, used by hacktivist to prove that their attacks have been successful, FYI the data retention is under 3 months)
- YouTube (American Video platform, used to disseminate video materials and recruitments)
- VK (Russian Social network, used for communications, recruitment)
- FaceBook (American Social Network, used for communications)
- Instagram (American Social Network, used for communications)
- TikTok (Chinese Social Network, used for communications)
- Other specifics platforms has been seen in the Hacktivist operations, their reach was low...


## How-to assess Hacktivist attack claim
- Until victim or authorities confirm the attack or significant proof of the attack, the hacktivist action is a claim
  
### Hacktivist most used attacks, claim & real effect
#### DDoS
- The most used hacktivist attack TTPs is also the most insignificant one, for the most of the attacks reported
- Sometimes DDoS attack against a company is announced as sucessful when in fact the attack did not affect the company operations because:
  * target was not the good website
  * target enabled GEOIP restriction
  * the anti-DDoS measures cleared the traffic
  * the attack did not happened
- But mostly because DDoS attacks targeted the website of the company which we called the Global company website, other than an image impact, the company operations are not affected, in others words we DGAF
- Also, a very specific hacktivist entity only report sucessful attacks when in reality they attack dozens websites / IP addresses / each day
- Despite this, some attacks has been significant, with real damages, one Hacktivist entity used persistent DDoS attacks with impact to the company

#### Data Leaks
- When hacktivist leaked data, they often overhyping the real data:
- Data coming from previous leaks
- Data publicly available (Support FTP server, unclassified data)
- Some hacktivists groups has been seen with access & data where they did not understood what they had in hand
- We have seen them been excited by accessing to public service IMINT providers and claiming they has access to satellite data
- Translation from English to Russian by some hacktivist group are done with automated translation tools (Wrong context can give you a bad translation eg. CLASSIFIED or UNCLASSIFIED)
- Hacktivists entities here are doing the same job of Ransomware & extortion threat actors, they want publicity of their actions

#### Credentials Leaks
- Hactivist recovered powerful access and burned it without understanding the sensitivity these accounts
- They also published old credentials leaks from big breachs from the past using credentials leaked brokers services
- Becareful, some might still be relevant but mostly not

#### Defacements
- The attack consist in defiguring the target website, with text or by changing/adding pictures to it, often with some slang or bad depicts of the adversary
- The defacements are often done in campaign, meaning dozens, hundreds of websites are defaced in the same time
- But they are often small & medium business, association, old websites not up to date and Hacktivists relaized the intrusion by expoiting N-day (WordPress, Drupal, etc.) vulnerabilities, mostly by using publicly available exploits
- When the title is big in the media, the operational reality impact is low to the mentioned country (no operational impact to services provided by the targeted state)
- But the damage to SME, Association, & old websites is real, it is impactful for them as they are often without dedicated tech employees

#### Information Operation driven attacks
- Some hacktivists actions have the goal to uses the stolen information to create another type of hybrid attack we called Information Operations (IO)
- Information operations and warfare, also known as influence operations, includes the collection of tactical information about an adversary as well as the dissemination of propaganda in pursuit of a competitive advantage over an opponent. (Source: RAND)
  * an entity (A) directs the intrusion in computer networks or information systems
  * documents, mails, pictures, etc; are stolen by an hacktivist entity (B) or another threat actor type (it can be the same entity)
  * the Hacktivist entity analyzes the stolen files (Optional)
  * the Hacktivist entity alter the stolen files (Optional)
  * the same Hacktivist entity (B) or another hacktivist entity (C) disseminate the leak of the files
- When it is the case of informations operations driven attacks, what the hacktivist entity wants above all is media coverage
- We have seen data leaks from Hacktivists entity directly (they claim the hack and released the data) as we have also seen data been hacked by entity (A) & articles based on the leaked data published in such short timeframe by entity (B) & (C) which do not let the possibility of some agreement between entities (A), (B) and (C).


## How Hacktivists financing their attacks
- Donations in Flat currencies, cryptocurrencies (Some supported more than dozens different cryptocurrencies), materials (computers, drones, etc)
- DDoS Extortion: Asking their victims to pays to stop DDoS attack
- Selling botnets attacks
- Telegram revenue: Telegram bots credits to access data, Premium channels
- Training: Some offers trainings to evolve your capabilities (here the objective can be both, make money and train Hacktivist supporters to conduct more evolved attacks)
- Cryptocurrencies schemes: In some case we suspected Hacktivist to have been part of cryptocurrencies schemes, encouraging their supporters to buy specific cryptocurrency
- NFT: At leaset one hacktivist entity tried to make money by selling NFT to their supporters
- Hidden finance sources
- Note: Most Hacktivist has been financed by theses sources, but the financing point is a struggle for a lot of them!


## Reports on Hacktivists actions
- Reports by medias, Situational awareness accounts, cybersecurity companies are used as a promotional materials by Hacktivists (Several examples like CyberKnow Tracker, media articles, Tweets/blogs from cybersecurity companies)
- That is exactly the same problem for Ransomware threat actors
- Not reporting on them would not permit us to assess the right extent of this conflict, reporting on permits them to use it as promotional content
- That is a complex problem, I don't have the solution, maybe the good thing is to reporting on them with an analysis of the event, with confidence level by using admiralty scale

## Mitre ATT&CK TTPs
### Reconnaissance
- T1595: Active Scanning
  * T1595.001: Scanning IP Blocks
  * T1595.002: Vulnerability Scanning
- T1589: Gather Victim Identity Information
  * T1589.001: Credentials
  * T1589.002: Email Addresses
  * T1589.003: Employee Names
  * T1590.002: DNS
  * T1590.001: Domain Properties
  * T1590.005: IP Addresses
  * T1590.006: Network Security Appliances
  * T1590.004: Network Topology
- T1591: Gather Victim Org Information
  * T1591.002: Business Relationships
  * T1591.001: Determine Physical Locations
  * T1591.004: Identify Roles
- T1596: Search Open Technical Databases
  * T1596.005: Scan Databases
  * T1596.002: WHOIS
- T1593: Search Open Websites/Domains
  * T1593.002: Search Engines
  * T1593.001: Social Media
- T1594: Search Victim-Owned Websites
### Resource Development
- T1583: Acquire Infrastructure
  * T1583.005: Botnet
  * T1583.003: Virtual Private Server
- T1586: Compromise Accounts
  * T1586.003: Cloud Accounts
  * T1586.002: Email Accounts
- T1588: Obtain Capabilities
  * T1588.005: Exploits
  * T1588.001: Malware
  * T1588.002: Tool
### Initial Access
- T1190: Exploit Public-Facing Application
- T1133: External Remote Services
- T1078: Valid Accounts
  * T1078.004: Cloud Accounts
  * T1078.002: Domain Accounts
### Execution
### Persistence
- T1133: External Remote Services
### Privilege Escalation
### Defense Evasion
- T1578: Modify Cloud Compute Infrastructure
### Credentials Access
- T1110: Brute Force
  * T1110.004: Credential Stuffing
  * T1110.003: Password Spraying
### Discovery
### Lateral Movement
### Collection
- T1560: Archive Collected Data
  * T1560.003: Archive via Custom Method
- T1530: Data from Cloud Storage
- T1213: Data from Information Repositories
  * T1213.003: Code Repositories
  * T1213.001: Confluence
  * T1213.002: Sharepoint
- T1039: Data from Network Shared Drive
- T1114: Email Collection
  * T1114.001: Local Email Collection
  * T1114.002: Remote Email Collection
- T1113: Screen Capture
### Command and Control
### Exfiltration
- T1011: Exfiltration Over Other Network Medium
- T1567: Exfiltration Over Web Service
- T1537: Transfer Data to Cloud Account
### Impact
- T1485: Data Destruction
- T1486: Data Encrypted for Impact
- T1491: Defacement
  * T1491.002: External Defacement
  * T1491.001: Internal Defacement
- T1561: Disk Wipe
- T1499: Endpoint Denial of Service
  * T1499.003: Application Exhaustion Flood
  * T1499.002: Service Exhaustion Flood
- T1498: Network Denial of Service
  * T1498.001: Direct Network Flood
  * T1498.002: Reflection Amplification




## Errors, typos, something to say ?
  - If you want to add a link, comment or send it to me
  - Feel free to report any mistake directly below in the comment or in DM on Twitter [@SwitHak](https://twitter.com/SwitHak)
