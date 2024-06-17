## Data Sourcing Challenge

#### The application will import data via online APIs, and do the following:

* Will exercise understanding of accessing online APIs for data sourcing
* Formatting data (json)
* Converting data to Pandas DataFrames for analysis and calculations
* Cleaning, merging, and final Export of data to .csv format.

Sample of a complex query from NYT

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

Sample of complex query for movie details from The Movie Database

Found: Love & Taxes; id: 1248795
{
    "adult": false,
    "backdrop_path": "/9JNsAIFMu4o37AgnU1JVtR6AWsK.jpg",
    "belongs_to_collection": null,
    "budget": 0,
    "genres": [
        {
            "id": 10749,
            "name": "Romance"
        },
        {
            "id": 28,
            "name": "Action"
        },
        {
            "id": 18,
            "name": "Drama"
        }
    ],
    "homepage": "[https://www.netflix.com/title/81689799](https://www.netflix.com/title/81689799)",
    "id": 1248795,
    "imdb_id": "tt28355490",
    "origin_country": [
        "TR"
    ],
    "original_language": "tr",
    "original_title": "Romantik H\u0131rs\u0131z",
    "overview": "After learning that the art thief she has been chasing is her ex-lover, an officer working for Interpol concocts a plan to catch him red-handed.",
    "popularity": 85.682,
    "poster_path": "/niVtvS9Kf8G1VDPSqurqHkaSSwm.jpg",
    "production_companies": [],
    "production_countries": [
        {
            "iso_3166_1": "TR",
            "name": "Turkey"
        }
    ],
    "release_date": "2024-03-13",
    "revenue": 0,
    "runtime": 99,
    "spoken_languages": [
        {
            "english_name": "Turkish",
            "iso_639_1": "tr",
            "name": "T\u00fcrk\u00e7e"
        }
    ],
    "status": "Released",
    "tagline": "",
    "title": "Art of Love",
    "video": false,
    "vote_average": 6.495,
    "vote_count": 111
}
