# Google_Analytics_Certification
I learned the course on Udemy to prepare for Google Analytics Individual Qualification Certification. (https://www.udemy.com/google-analytics-certification/). Thanks to Daragh Walsh, I passed the test and got the certification! Here is a summary of the basic knowledge points.


## View
1. You can use filters to limit or modify the data in a view.
2. Filters allow you to limit and modify the data that is included in a view. 
	* **If a filter excludes data from a view, that data can not be recovered for that view.** The data from after the filter was created is affected.
	* (exclude data from a view/ include data from a view/ modify how data appears in reports)
	* Google Analytics Filters: By default, view filters are applied to the data in the order in which the filters were added. So, if there are existing filters for a view, your new filter is applied after them.
3. **A view is permanently deleted 35 days after being moved** to the Trash Can. Once deleted, the view is gone, and we are not be able to retrieve any historical data or reinstate the reports. 
 This includes any setting and configuration preferences, like Goals and user permissions, but does not include data saved at the property or account level.

## Goals 
1. Goals in Google Analytics fall into one of 4 types: **Destination, Event, Duration, Pages/Screens per Session**
   - Events are user interactions with content that can be tracked independently from a web page or a screen load. 
     - An event hit for reporting can include which **four parameters: Category, Action, Label, Value** 
     - The term "Non-interaction" applies to the final, and optional, Boolean parameter that can be passed to the method that sends the Event hit. This parameter allows you to determine how you want bounce rate defined for pages on your site that also include event tracking.  If a user opens a single page on your site and then exits without clicking on anything, Google Analytics will count this session as a bounce.
	
2. **Goals are configured at the view level.** Goals can be applied to specific pages or screens your users visit, how many pages/screens they view in a session, how long they stay on your site or app, and the events they trigger while they are there. [If you’ve defined a goal of downloading a PDF, and the user downloads the PDF five times in five separate sessions, how many Goal conversions will Google Analytics count? ---5]
3. Creating a goal--> Goal Name, Goal Type, Goal Slot ID

## Data Table
* Percentage: displays a pie chart, showing the contribution to the total for the selected metric.
* Performance: displays a horizontal bar chart, showing the relative performance for the selected metric.
* **Comparison**: displays a bar chart plotting the performance of the selected metrics relative to the site average.
* Pivot: rearranges the information in the table for certain reports by pivoting your data on a second dimension.
* Term cloud: displays a visual representation of the performance of keywords (not available for all reports)

## Dimensions and Metrics
1. Metrics are quantitative measurements. The metric Sessions is the total number of sessions. The metric Pages/Session is the average number of pages viewed per session.    i.e. 'Users' means the users that had at least one session on your site in the given data range
2. **Custom Dimensions can not be shared in the Solution Gallery.**
You can share Dashboards, Custom Reports, Segments, Goals, and Custom Attribution Models in the Solutions Gallery. Only configuration data is shared through the Solutions Gallery. When you create and share an asset, your personal information and Analytics data stays private in your account. And when you import an asset from the Solutions Gallery, only the template is imported into your account.
3. **Custom dimensions** can appear as primary dimensions in Custom Reports. You can also use them as Segments and secondary dimensions in standard reports.
4. You can **only apply a Custom Dimension to data that was collected after you created the dimension.** You’ll have to create the Custom Dimension first and let it be applied to your data during processing in order to use it in reports. 
5. Custom metrics can produce more flexible and more readable custom reports and as such are a convenient way to track your most important metrics. 
6. Not every metric can be combined with every dimension. **Each dimension and metric has a scope: user-level, session-level, or hit-level.** In most cases, it only makes sense to combine dimensions and metrics that share the same scope.
7. **Custom metrics** can have different scopes. Hit-level custom metrics get associated with all the hit level dimensions with which it was sent. Similarly, product-level custom metrics are associated only with the product with which it was sent.
8. Sessions and Bounce Rate come under metrics. That's why "Sessions / Bounce rate" is not a valid metric-dimension combination.
9. By default, Source and Medium dimensions does Google Analytics capture for each user that visits your website.
		* Email comes under “Medium”.
	
## Medium
3 default medium in Google Analytics
* **Organic** [It represents traffic that comes from organic, or unpaid, search results]
* **Referral** [Any traffic that comes to your site from another website that's not a search engine will show up in your reports as a "referral."]
* **None** [This medium is applied only for users that come directly to your site by either typing your URL into a browser or clicking on a bookmark.].  cpc

## Hierarchy of organizations, accounts, users, properties, and views
organizations > accounts > users > properties > views

## Session
1. A session is a group of interactions that take place on your website within a given time frame. **By default, a session lasts until there's 30 minutes of inactivity, but you can adjust this length so a session lasts a few seconds or several hours.** A session can be as short as a few seconds or as long as several hours. A single user can open multiple sessions.
2. In Analytics, a bounce is calculated specifically as a session that triggers only a single request to the Analytics server, such as when a user opens a single page on your site and then exits without triggering any other requests to the Analytics server during that session.
3. Google Analytics will **only count 1 unique event per session.**

## Segment 
1. A segment is a subset of your Analytics data. **Segments let you isolate and analyze those subsets of data** so you can examine and respond to the component trends in your business. You can also use segments as the basis for audiences. 
2. A segment is made up of one or more non-destructive filters (filters that do not alter the underlying data). Those filters isolate subsets of users, sessions, and hit.
3. 4 segments may be applied at once
4. Custom Segments can be created using Dimensions, Metrics, Session Dates, Sequences od user actions. **Custom Segments CANNOT be created using Ad type** [Ad type relates to Google AdWords and is not available as a filter in the Google Analytics segment builder to build segments]
5. The children of users cannot be use in Custom Segment
6. **Segments are applied after it samples the property-level data**, and after it applies filters, which can also reduce the number of sessions included in a sample. [Google Analytics applies segments after it samples the data in reports.]

## Report

- Pairing metrics and dimensions of different scopes is not possible in any report. **<Same Scope!>**
	
- Channel: The default system channel definitions reflect Analytics' current view of what constitutes each channel in the Default Channel Grouping. Default channels are Direct, Organic Search, Social, Email, Affiliates, Referral, Paid Search, Other Advertising and Display.
	- Assist interaction is any interaction that is on the conversion path but is not the last interaction. If a channel appears anywhere—except as the final interaction—on a conversion path, it is considered an assist for that conversion. The higher these numbers, the more important the assist role of the channel.
	
- **Landing Pages report** indicates where visitors entered your website.
- **Exit Pages report** can determine the pages where users left your site.
	
- **Goal Flow report** can determine where users start or exit the conversion funnel.
	
- **New vs Returning report** can determine the percent of your site traffic that has visited previously.
	
- **All Pages report** can determine which pages on your site get the most traffic and highest engagement. [allows you to view the Average Time on Page and Pageviews to determine which pages are the most popular.]
	
- **All Traffic report** can determine which websites send traffic to your pages.

- **Active Users Report**: The metrics in the Active Users Report are relative to the last day in the date range you are using for the report. (Over 1-day, 7-day, 14-day, and 30-day periods)
	
- **The Browser & OS report** can determine which browsers may have had problems/issues with your website.
	
- **Content DrillDown Report:** You can see the performance of your website’s specific sections under the “Content Drill Down” dimension in Google Analytics.
	
- **The Lifetime Value report** lets you understand how valuable different users are to your business based on lifetime performance. This is not just a number but a complete metrics. That's why it could not be tracked in Goal.
	
- **The Time Lag report** counts the number of days from the first user interaction (e.g., impression, click, direct session) to conversion. __Time lag between page views in the goal funnel can be determined.__
	
- **By activating Advertising Features**, in **Demographics and interests report** can you collect additional information about your users (need to update Analytics to support Advertising Reporting Features)
	
- **Behavior Flow report** visualizes the users interactions on your website. This report can help you discover what content keeps users engaged with your site. [visual representation of the path users traveled from one page or Event to the next on your website]

- **Cross Device report are only available within a User-ID view.** There are three Cross Device reports: Device Overlap, Device Paths, and Acquisition Device. These reports display data collected during sessions in which a User ID is sent to Analytics
	- **Without a User-ID view, when the session happen in different browsers on the same device Google Analytics NOT be able to identify sessions from the same user.**

- View Type	
	- Explorer: The standard Analytics report. Includes a line graph and a data table that includes dynamic elements like a search/sort option and secondary dimensions.
	- Flat Table: A static, sortable table that displays data in rows.
	- Map Overlay: A map of the world. Different regions and countries display in darker colors to indicate traffic and engagement volume.

- Custom Reports
	- Use multiple dimensions together in the same report
	- Create a report with Custom Metrics
	- Use a Custom Dimension as a primary dimension
	- Prevent data from appearing in a custom report
		- A filter that filters out all data 
		- Dimensions and metrics of different scopes

- Multi-Channel Funnels reports
	- Goals or Ecommerce transaction must be set up in order to generate Multi-Channel Funnel reports( generated from conversion paths, the sequences of interactions)
	- **By default, the channel labels that you see in Multi-Channel Funnels reports (Paid Search, Organic Search, Social Network, etc.)** are defined as part of the MCF Channel Grouping. 
	- If you have specific analysis requirements, you may wish to create your own Custom Channel Grouping(s), each with its own set of labels. When you share a Custom Channel Grouping, only the configuration information is shared. 
		
	  - When you create a Custom Channel Grouping you can 
			- immediately select it in reports
			- **apply it retroactively and see historical data classified by your new channel definitions**
			- Change how reports display your data, without changing the data itself [ Your data remains private]
			
 	- The Multi-Channel Funnels reports show how previous online referrals and searches contributed to your sales. All the channels are credited according to the roles they play in conversions—how often they assisted and/or completed sales and conversions. 
  - Multi-Channel Funnels reports can show you the sequence of interactions that led up to each conversion and transaction. 

## User ID
1. What would happen if a user clears the Google Analytics cookie from their browser?
		a. Analytics will not be able to associate user behavior data with past data collected
		b. Analytics will set a unique ID the next time a browser loads a tracked page
		c. Analytics will set a new browser cookie the next time a browser loads a tracked page
		
2. [The analytics.js library accomplishes this via the **client ID field, a unique, randomly generated string that gets stored in the browsers cookies**, so subsequent visits to the same site can be associated with the same user.]
3. **The User ID lets you associate engagement data from multiple devices and different sessions with unique IDs.**

## Data 
- **Google Analytics can only collect user behavior data from internet-connected systems by default.**
- Data Import lets you join the data generated by your offline business systems with the online data collected by Analytics.
- Measurement Protocol lets you send data to Analytics from any internet-connected device. It's particularly useful when you want to send data to Analytics from a kiosk, a point of sale system, or anything that is not a website or mobile app

## Google Ads
1. When you link your Google Ads account to Google Analytics[Linking your Google Ads account to your Analytics property lets you see the full customer cycle, from how they interact with your marketing]: 
		a. View AdWords click and cost data alongside your site engagement data in Google Analytics
		b. Import Analytics goals and transaction into Google Ads as conversions
		c. Create remarking lists in Analytics to use in Google Ads campaigns
	
2. Bid adjustments allow you to show your ads more or less frequently based on where, when, and how people search.
3. The following user characteristic may be used to change keyword bids in AdWords: device, time of day, location.
4. AdWords let users advertise : Google search. Google Display Network

## Track campaign
1. **The URL Builder** has six fields, but you generally need to use only **Campaign Source, Campaign Medium, and Campaign Name**.(required by the Google Analytics URL Builder to generate campaigns URLS)
2. Medium, Source and Campaign --> accurate campaign tracking
3. **Common hit types include page tracking hits, event tracking hits, and ecommerce hits.** Each time the tracking code is triggered by a user's behavior  [Each interaction is packaged into a hit and sent to Google's servers.]
4. Analytics tracking code send an event hit to Google Analytics **whenever a user performs an action with event tracking implemented**.
5. By adding campaign parameters to your URLs, you can identify the campaigns that send traffic to your site. When a user clicks a referral link, these parameters are sent to Analytics, so you can see the effectiveness of each campaign in your reports. Google Adwords gives you an option to track campaign using auto-tagging.
	 - Auto-tagging is the recommended approach and ensures that you get the most detailed AdWords data.(automatically collect data)
	 - Auto-tagging automatically adds **'gclid='** campaign tag to your Google Ads destination URLs.
	
6. Which of these campaigns requires you to manually add campaign parameters to your URLs for tracking? -- Email campaigns
7. **Site Search** lets you understand the extent to which users took advantage of your site's search function, which search terms they entered, and how effectively the search results created deeper engagement with your site.
8. Should Paste your Analytics tracking code snippet just after the opening <head> tag in your web pages.
9. The default setup of the tracking code is designed to make it easy for you to track traffic to a single domain or subdomain (e.g. a single website URL) that does not share user data with other domains or sub-domains.
	[if you don't set up cross-domain tracking and instead install the same default tracking code on separate domains e.g. an ecommerce site and a separate shopping cart site, Analytics will associate these users and sessions with their respective domains]
	
## Remarketing
- Show customized ads to customers who have previously visited your site
- Create remarketing lists based on custom segments and targets
- Create remarketing lists without making changes to your existing Analytics snippet
- You **create remarketing audiences based on user behavior on your site or app**, and then use those audiences as the basis for remarketing campaigns in your ad accounts like Google Ads and Display & Video 360. 
-  Dynamic Remarketing (Encourage purchasing)
	 - You can implement Dynamic Remarketing by using the preconfigured All Users list, creating more narrowly targeted lists lets you focus your ad content and budget where it will have the most impact. For example, users who have already added items to their shopping carts might need just a reminder or incentive to complete their transactions, while users who have only viewed the products may need more convincing about the overall value of the products. By following the same procedure you use to create Remarketing Audiences, you can build segment-based Dynamic Remarketing Audiences using your new dimensions.

## Extra 

- Smart Goals uses machine learning to examine dozens of signals about your website sessions to determine which of those are most likely to result in a conversion. Smart goals allow you to automatically optimize your Google Ads performance even if you don’t have goals or ecommerce tracking set up.

- **Cohort analysis** helps you understand the behavior of component groups of users apart from your user population as a whole. [can compare the behavior and performance of groups of users over a series of weeks]

- Personally identifiable information - The Google Analytics terms of service, which all Google Analytics customers must adhere to, prohibit sending personally identifiable information (PII) to Google Analytics. PII includes any data that can be used by Google to reasonably identify an individual, including (but not limited to) names, email addresses, or billing information.

- A pageview is defined as a view of a page on your site that is being tracked by the Analytics tracking code. If a user clicks reload after reaching the page, this is counted as an additional pageview. If a user navigates to a different page and then returns to the original page, a second pageview is recorded as well.

- Assigning a monetary value to a goal gives you a way to compare conversions and measure changes and improvements to your site or app. All goal types except Smart Goals let you assign a value during the setup process. There are special considerations when setting up an Event goal or a goal that involves Ecommerce Tracking.

- When a dashboard is shared, users can edit the dashboard configuration.

- Choose **'Greater precision'** in the sampling pulldown menu --> can the amount of data in a sampled Google Analytics report be increased.

