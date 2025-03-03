# Digital (/web) Analytics Masterclass

A project based learning path for becoming an expert digital analytics practitioner.

__Digital Analytics practitioner__: a professional who applies data analysis and statistical techniques to help organizations make informed business decisions. Typically 
using data collected by Analytics tools about user behaviour on digital platforms such as websites and apps.

At the core of this curriculum is having a website and analytics tracking on it. This is a must!

Each of the other 3 areas can be thought of as a buffet. They do not rely on each other and can be approached in any order.

For someone interested in developing data analysis skills, they might do areas 0, 1, 2 and 2a. Spending a considerable portion
of time in 2a (Advanced Data Analysis) answering various questions about the data, maybe some of those questions are AI generated.

Use of Generative AI is encouraged to help fill any knowledge gaps. Getting error messages along the way means you're learning.



## 0. Create a website [CORE]

By any means necessary create a website. There are many free and low cost platforms to achieve this.

- [Github pages](https://pages.github.com/)
- [Wordpress on Digital Ocean](https://www.digitalocean.com/solutions/wordpress-hosting).
- [Wordpress on Hostinger](https://www.hostinger.com/wordpress-hosting)
- [Static site on Digital Ocean app platforms](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-static-website-to-the-cloud-with-digitalocean-app-platform)

Skills:

- git
- github
- server access and management


## 1. Add web analytics tracking [CORE]

__Default: Google Analytics 4__

Learn how to implement web analytics tracking technology on a website by adding (simple page view) tracking to your website. 

Verify the analytics tracking is working through debugging (browser dev tools or (Omnibug)[https://marquinsmith.com/2023/08/06/omnibug-part-1/]) in the browser. Also verify by monitoring stats in the platform.

Using multiple platforms to track usage of your website is fine, even encouraged! Eg Google Analytics and Matomo.

There are free options or self hosted options for this such as

- Google Analytics 4 [FREE - 14 months of history retention]
- Matomo / Piwik [SAAS | Self hosting]
- [Mixpanel](https://mixpanel.com/home/) [FREE UP TO 1M events per month]
- Plausible [SAAS | Self hosted]
- Umami [FREE UP TO 100k events per month]

Self hosted resources:
- https://www.pikapods.com/apps#analytics
- https://github.com/awesome-selfhosted/awesome-selfhosted?tab=readme-ov-file#analytics
- https://caprover.com/
- https://apps.yunohost.org/catalog?search=analytics


Skills developed:

- HTML
- Javascript
- Web tracking debugging (Omnibug)
- Browser developer tools
- Server management (if self hosted)


### 1a. Advanced tracking [OPTIONAL]

__Implementation specialist track (HTML + Javascript).__ Dive deep on this side quest to become an expert in web tracking implementation.

Add further tracking to the website to record more detailed interactions:

- button click tracking - Capture how many times and on what pages buttons are clicked
- conversion tracking - Enable conversion tracking on some action eg. downloading a PDF
- scroll depth - Track how far down a page users scroll.

Use a tag management system like Google Tag Manager or Matomo Tag Manager. Trigger events and analytics tracking from within the Tag Management system.




## 2. Create various reports using the web analytics platform.

In the web analytics platform you have chosen, have a poke around and build different kinds of reports if 
the platform offers that.


### 2a. Advanced Data Analysis

__Data analysis track__ Deep dive on this side quest to develop data analysis skills. Bonus points for creating a powerpoint deck (or video) 
explaining the findings of the analysis.

- Identify key themes in the most popular pages
- Create a forecast for daily visits over the next 30 days.
- Is there any correlation with daily page views and the daily weather in your home town / city?
- How does my website perform in terms of mobile vs. desktop traffic, and are there opportunities for improvement?


## 3. Query raw data directly

Gain access to the raw data that is being collected by your web analytics platform of choice.


- Google Analytics :: export data to BigQuery
- Other Web Tracking tool :: If self hosted query database directly (access server or docker container). If a SAAS web analytics tool was chosen, the raw data will likely need to be exported before being able to access.


Skills

- SQL
- Python (recommended)


### 3a. Advanced data access and manipulation

__Data engineer track (SQL + Python)__ Deep dive on this side quest to develop skills aligned with Data Engineering or Analytics Engineering

__Google Analytics__

Model the Google Analytics export data to make potential reporting and analysis easier. Dataform in BigQuery is a good tool choice for this.

__Other Web Analytics Tool__

Set up regular data exports to a data warehouse of your choosing (Extract Transform Load). Popular modern cloud data warehouse choices include:
- BigQuery
- Clickhouse
- Snowflake

Alternatively the data can be extracted to a SQLite or DuckDB database for local analysis and storage.

Make the automated export idempotent and self healing. Will duplicate extracts result in duplicate data? What happens if an export fails on a particular day. will the gap be filled on subsequent runs?


## 4. Visualise data

Once access to raw data has been established, start building visualisations and reports based on the data

- LookerStudio
- PowerBI
- Tableau
- Redash
- Excel or Google Sheets
- Streamlit
- Evidence
- Observable
