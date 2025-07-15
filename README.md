## Installing
### Linux
* You must have [Go v1.24.3](https://go.dev/doc/install) (or higher), [PostgreSQL](https://www.postgresql.org/download/), [goose](https://github.com/pressly/goose/releases) and [sqlc](https://docs.sqlc.dev/en/stable/overview/install.html) installed on your system
* Clone this repo to your desired location
* Run ```go build``` on your local machine in cloned repository
### Windows
* You can repeat the linux steps, it will work just fine
* Or alternatively you can [download an executable from release page](https://github.com/lackingworth/Go-Gator/releases)

## Info
 Gator us a simple RSS feed aggregator in Go. It makes use of PostgreSQL as its database, goose for db migration and sqlc for safe SQL query handling

## Available commands
* ```register <name>``` - registers you in local config file ```~/gatorconfig.json```
* ```login <name>``` - switches users
* ```reset``` - resets database to its blank state
* ```users``` - lists all users
* ```agg <time_between_requests>``` - scrapes rss feeds
* ```addfeed <name> <url>``` - adds feed to database (and follows it)
* ```feeds``` - list all feeds
* ```follow <feed_url>``` - follows specified feed 
* ```following``` - lists all following feeds
* ```unfollow <feed_url>``` - unfollows specified feed
* ```browse``` - browse through all feeds that you follow
> [!NOTE]  
> 
> The default config file ```~gatorconfig.json``` is located in your home directory and looks like this:
> ```json
>{
>   "db_url":"<protocol>://<login>:<password>@<domain>:<port>/<dbname>?sslmode=disable"
>}
> ```

## Version History

* v0.0.1:

    * Initial Release
