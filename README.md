# NRQL_Queries

A collection of generic NRQL Queries which can be used on the New Relic Monitoring Platform.

<details>
  <summary> Ajax Request - View time in seconds for completion of request URL </summary>

    SELECT average(timeToSettle) FROM AjaxRequest FACET requestUrl SINCE 180 MINUTES AGO TIMESERIES
  </details>

<details>
  <summary> Ajax Request - View time in seconds for completion of page URL </summary>

    SELECT average(timeToSettle) FROM AjaxRequest FACET requestUrl SINCE 180 MINUTES AGO TIMESERIES
  </details>

<details>
  <summary>Window Load - View average window Load in milliseconds for Page URL</summary>

      SELECT average(windowLoad) FROM PageViewTiming FACET pageUrl SINCE 180 MINUTES AGO TIMESERIES

</details>

<details>
  <summary>Javascript - View Javascript error message and the page URL</summary>

    SELECT count(*) FROM JavaScriptError FACET pageUrl, errorMessage SINCE 480 MINUTES AGO TIMESERIES

  </details>

<details>
  <summary>PageView - View Total page views</summary>

    SELECT count(*) FROM PageView FACET pageUrl SINCE 480 MINUTES AGO TIMESERIES

  </details>