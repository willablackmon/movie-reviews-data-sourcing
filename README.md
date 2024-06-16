## Data Sourcing Challenge

#### The application will import data via online APIs, and do the following:

* Will exercise understanding of accessing online APIs for data sourcing
* Formatting data (json)
* Converting data to Pandas DataFrames for analysis and calculations
* Cleaning, merging, and final Export of data to .csv format.


Sample of a complex query from

https://ashar180.medium.com/crawling-ny-times-api-for-relevant-articles-b6134b651054




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
