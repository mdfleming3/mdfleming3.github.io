---
layout: post
title: "How to Build a Free Content Marketing Automation Tool with Google"
date: 2020-07-14
author: Mark Fleming
description: Learn how to create a free content automation tool with Google that 
image: doc-automation.png
image-alt: "build-free-content-marketing-automation-tool-google"
category: blog
meta: content automation, Google Sheets, Google Docs, Document Studio, Content Workflow
tags: content-marketing automation digital-marketing workflow
---

If your content marketing strategy is not powered by automation, your team is likely wasting too much time on repetitive writing tasks. For many organizations, this hinders productivity, drives risk for error, and increases costs. As so, many firms weigh whether to invest in high-priced automation software or maintain the status quo. However, with a little elbow grease and Google savvy, you can solve your content marketing woes by building a free content automation tool.

Before we begin, think of a written piece of content you want automated. This can be marketing materials, webinar invites, digital ads, you name it. Got an idea -- Good! Let’s use this for the demo.

Below are the free web-based tools we will use:
* Google Sheets
* Google Docs
* Document Studio (free Google Sheets add-on)

####Step 1: Installing Document Studio into Google

Log into your [Google Account](https://accounts.google.com/signin/v2/identifier?continue=https%3A%2F%2Fwww.google.com%2F&hl=en&flowName=GlifWebSignIn&flowEntry=ServiceLogin), and download the free Google Sheets Add-on, “[Document Studio](https://gsuite.google.com/marketplace/app/document_studio/429444628321)” from the G Suite Marketplace. 

We will come back to this later.

####Step 2: Creating the Google Doc Template

Open [Google Docs](https://docs.google.com/), and create a new document. 

In this file, we will build our template that can be automated in the future. For my example, I will create two simple examples of frequent time sinks for marketers at professional service firms -- a web biography and a social media post.

Here is the content I wrote:

>> 
Bio:

{{first-name}} {{last-name}} is a {{job-title}} in the firm’s {{practice}} practice at the {{location}} office. {{he-she}} specializes in the practice of {{specialty}}. {{his-her}} clients typically include {{clients}}. 

Tweet: 

The firm is pleased to welcome {{first-name}} {{last-name}} to our {{location}} office. {{he-she}} is a {{practice}} attorney with a specialty in {{specialty}}. #newfirmhire
>>

The text enclosed in the curly brackets is the variable that will be automated. In writing your document, you can create any variable you want, as long as it fits within a spreadsheet cell. Examples may include simple values such as names, job titles, locations, number values, etc. Variables may also be full chunks of text (i.e. value propositions, specialties, quotes, etc.). 

**Note:** Variables can be used as many times as possible, but they require exact formatting (i.e. {{first-name}} {{First-name}} {{first_name}} are considered different variables). As so, I prefer to use all lowercase letters and hyphens. 

Once you have created your document, save your document.

####Step 3: Creating Google Sheets Document:

Go to [Google Sheets](https://docs.google.com/spreadsheets/?usp=mkt_sheets), and open a new document. 

You can now import a spreadsheet by clicking: **File > Import**. If you do not have existing data, you can manually create a spreadsheet, and the process will work just fine. 

My initial data looks like this: 

![build-free-content-marketing-automation-tool-google-one]({{ site.baseurl }}/assets/doc-auto-1.png)

As highlighted, my top row labels match the variables from the Google Doc. Similar to a mail merge, the rows below will be merged with the template.

Now is a good time to clean your data (i.e. missing values, capitalization, periods, etc.). I am missing the {{he-she}} and {{his-her}} variables used in the template, so I will add these now. This is an easy fix. I can use an IF function to output these into new columns (i.e. =IF($F$2="Male","He","She")). My output is now ready to be merged:

![build-free-content-marketing-automation-tool-google-one-two]({{ site.baseurl }}/assets/doc-auto-2.png)

Save your Google Doc for now by renaming “Untitled Document” in top left.

####Step 4: Using Document Studio Export

In your Google Sheets menu, click:  **Add-ons > Document Studio > Open**. The Document Studio side panel will appear. 

![build-free-content-marketing-automation-tool-google-one-three]({{ site.baseurl }}/assets/doc-auto-3.png)

Set “Enable” to “Yes” 

Under “Select a template in Google Drive,” select Google Document and then select the Google Doc template you created. 

The Markers field will show variables that have correctly synced. If any variables are missing, check your formatting to ensure variables match in both documents. 

From here, you will want to name the merged file. I encourage including a bracketed variable that will help distinguish the merged documents. This is essential if you are working with many documents.

Choose an Export format. I selected Microsoft Word, but there are several other options.

Once all options are selected, you can choose when you want to merge. I haven chosen Merge Documents Now, which will output three separate documents immediately.

####Step 5: Reviewing Output

Document Studio has created several new columns in the Google Sheet. These are links to the files that have been saved on our Google Drive. To access the individual files, simply click the link.

![build-free-content-marketing-automation-tool-google-one-four]({{ site.baseurl }}/assets/doc-auto-4.png)

My output looks like this:

![build-free-content-marketing-automation-tool-google-one-five]({{ site.baseurl }}/assets/doc-auto-5.png)

Looks good to me! If you have further changes, you can edit accordingly. To create corrected output, delete the links from the columns Doc Studio created and re-run the export. This will overwrite the old documents.

####Takeaways

Once your Google Doc template is created, you can reuse this countless times or repurpose it into new templates. This makes creating new content or updating dated content a breeze. For example, I can build templates for several other standard Tweets. If I re-run the Document Studio Export, I can have a complex suite of social media content in just several minutes.

Have any questions on how this process can be integrated into your marketing strategy? Questions on troubleshooting. [Let’s Connect](https://www.linkedin.com/in/markdfleming/). 

**Further Reading**:
* [Use Cases - What can you do with Document Studio](https://www.labnol.org/document-studio-use-cases-5844)
* [Example Google Doc](https://docs.google.com/document/d/1O-9Y49aclklnX8hF6Byl8BmwECrxiWzwdMKd3nj_ELE/edit?usp=sharing)
* [Example Google Sheet](https://docs.google.com/spreadsheets/d/1Q3EdPFD-kNh4SQthB1Q-NA6-retufnsaqZ39jeL12B4/edit?usp=sharing)
* [Exported Document](https://drive.google.com/file/d/1WLT19C89oI7m9p1RIZ4l8S_jhApbMeRm/view?usp=sharing)
