# NRQL_Queries

A collection of generic/sample NRQL Queries which can be used on the New Relic Monitoring Platform.

<details>
  <summary> Ajax Related </summary>
  
    1. View time in seconds from start of request to when all resulting callbacks   
    (including subsequence Ajax callbacks) are complete - request URL  
    
      ````
      SELECT average(timeToSettle) FROM AjaxRequest FACET requestUrl SINCE 180 MINUTES AGO TIMESERIES
           
      
    2. View time in seconds from start of request to when all resulting callbacks (including subsequence Ajax callbacks) are complete - Page URL
      
      SELECT average(timeToSettle) FROM AjaxRequest FACET pageUrl SINCE 180 MINUTES AGO TIMESERIES
      ```           
      
  </details>

<details>
  <summary> Window Load </summary>

    3. View Average Window Load in milliseconds for Page URL
    
      ````        
      SELECT average(windowLoad) FROM PageViewTiming FACET pageUrl SINCE 180 MINUTES AGO TIMESERIES
      ```        
      
  </details>


