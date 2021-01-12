---
layout: article
title: Billing for Cloud SIEM accounts 
permalink: /user-guide/billing/billing-siem
flags:
  admin: true
  logzio-plan: community
tags:
  - accounts
  - sub-accounts
  - main-account
  - timeless-accounts
contributors:
  - yberlinger
---

# DRAFT Content

Logz.io Cloud SIEM works with your logs to boost your security observability with enriched and aggregated security log and alerts data, excellent prebuilt security content, and more than 10 of the most useful external Threat Intelligence feeds.

We take you to the next level with a Dedicated Customer Success Engineer and a dedicated Security Analyst for your Enterprise level Cloud SIEM account.  

Your Security Analyst will help you manage your onboarding process, and be on tap to help you create custom dashboards and ship additional security products.

+  If you’re a new customer who wants a complete Cloud SIEM solution, the pricing is presented on the <a href = "https://logz.io/pricing/" target="_blank"> Pricing page</a>, when you click  **Cloud SIEM**.
  
  ![Logz.io plan selection](https://dytvr9ot2sszz.cloudfront.net/logz-docs/billing-charges/product-selection.png)

+ If you’re an existing Pro or Enterprise account customer who wants Cloud SIEM, you must have a Log Management plan in place. 

Because Cloud SIEM uses the logs from your Log Management plan, the maximum storage available for your Cloud SIEM plan is the capacity you purchased for your Log Management plan.

For example, if you want to buy 50GB of SIEM, your Log Management plan storage should be at least 50GB.

For Cloud SIEM, you’ll be charged a flat rate per indexed GB. The greater the volume of logs you send us, the less you pay per indexed GB.

## Cloud SIEM Billing FAQs

Q: Is there a self-service option to upgrade my Logz.io account? <br>
A: Yes! If you already have a Cloud SIEM account, you can upgrade your account on our own. From your Log Management account, go to the cog wheel in the top right corner of the app, hover over settings, and then go down to ‘Usage and Billing’. 

This will bring you to a page showing the amount of log data you’re currently indexing per day. You’ll also see the option to upgrade your account so you can index more logs for longer periods. All you need is your credit card.

Q: How do I know how much data is being used in my account?<br>
A: Hit the cog wheel in the top right corner of the app, hover over settings, and then go down to **Usage and Billing**’**. This will bring you to a page that shows the average amount of data you’ve indexed per day during your log retention period (For example: You’ve used an average of 10 indexed GBs of log data per day, over the last 14 days). Note that you'll be billed according to your account plan, and we'll notify you if you go over plan capacity. 

Q: Are archived logs held against my Logz.io costs? <br>
A: No. You only pay for what you index. In fact, you can save costs by archiving your log data in an S3 Bucket or Azure Blob to store logs for cheap, while maintaining access to them if you need to index and analyze them later. Note that restoring archived logs won't trigger Security rules: The logs still include our threat enrichment, but the actual threat rules will not longer be triggered.

Q: Will I be charged for dropping data before it's indexed?<br>
A: For now, no. Not all logs are very interesting - use Logz.io’s Drop Filters to filter out unneeded logs before they are indexed and held against your Logz.io price. We won’t charge you for using the feature.  <!-- This will be changed in the future, we will charge for dropping data-->

Q: Does Customer Support cost extra? <br>
A: No! Our heroic 24/7 Customer Support team will help you get started and be successful with Logz.io at no extra cost - regardless of your plan.
