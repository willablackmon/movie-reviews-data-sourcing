# Data Sourcing

### Summary:

This application will import data via online APIs, convert to JSON format, convert to Pandas DataFrames for investigation, cleaning, merging, and export to CSV.

---

### APIs:

* **The New York Times**
  * https://developer.nytimes.com/docs/articlesearch-product/1/routes/articlesearch.json/get
* **The Movie Database**
  * https://developer.themoviedb.org/docs/search-and-query-for-details

## Functions Performed:

* Access online APIs and extract data
* Investigate data and formatting
* Execute multiple different queries
* Format data into JSON
* Convert data to Pandas DataFrames for analysis and calculations
* Clean data
* Merge DataFrames from two different sources of data
* Export final merged, cleaned data to .csv format.

---



## Developer Notes

### Sample querys from NYT

https://api.nytimes.com/svc/search/v2/articlesearch.json?q=election&api-key=yourkey

ref: https://ashar180.medium.com/crawling-ny-times-api-for-relevant-articles-b6134b651054

```
section = "technology"
query_url = f"https://api.nytimes.com/svc/topstories/v2/{section}.json?api-key={apikey}"
query_url = f"https://api.nytimes.com/svc/search/v2/articlesearch.json?api-key={apikey}"r = 

requests.get(query_url)query = "AWS"
begin_date = "20200701"  # YYYYMMDD

filter_query = "\"body:(\"security\") AND body: (\"aws\") AND body:(\"breach\") AND news_desk:(\"Technology\") AND glocations:(\"USA\")\""  # http://www.lucenetutorial.com/lucene-query-syntax.html

page = "1"  # <0-100>
sort = "relevance"  # newest, oldest
response_field = 'abstract,web_url,snippet,source,headline,keywords,pub_date,section_name'

query_url = f"https://api.nytimes.com/svc/search/v2/articlesearch.json?" \
            f"q={query}" \
            f"&api-key={apikey}" \
            f"&begin_date={begin_date}" \
            f"&fq={filter_query}" \
            f"&page={page}" \
            f"&sort={sort}"\
            f"&fl={response_field}"
print(query_url)
r = requests.get(query_url)
pprint(r.json())
```

### Sample queries for The Movie Database

**Search by movie, TV show or person:**

* https://api.themoviedb.org/3/**search/movie?query=Jack+Reacher&**api_key=API_KEY

**Query for a full movie details using movie id:**

* https://api.themoviedb.org/3/**movie/343611?**api_key=API_KEY



```

```
