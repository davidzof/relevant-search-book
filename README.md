# Relevant Search

Code and Examples for [Relevant Search](http://manning.com/turnbull) by [Doug Turnbull](http://github.com/softwaredoug) and [John Berryman](http://github.com/jnbrymn). Published by [Manning Publications](http://manning.com).

Relevant Search is all about leveraging Solr and Elasticsearch to build more intelligent search applications with intuitive results!

# How to run

## Install Elasticsearch

The examples expect Elasticsearch to be hosted at localhost:9200. So you'll need to install Elasticsearch to work with the examples.

   ```
1. Confirm Elasticsearch is running

  ```
  curl -XGET http://localhost:9200
  ```
  
  or visit this URL in your browser. 
  
  You should see JSON returned from the Elasticsearch instance. Something like:

   ```json
      {
        "name" : "Mary Zero",
        "cluster_name" : "elasticsearch",
        "version" : {
          "number" : "2.0.0-rc1",
          "build_hash" : "4757962b01a4d837af282f90df9e1fbdb68b524e",
          "build_timestamp" : "2015-10-01T10:06:08Z",
          "build_snapshot" : false,
          "lucene_version" : "5.2.1"
        },
        "tagline" : "You Know, for Search"
      }
   ```

## Running The Python Examples on Windows

The examples are written in Python 2.7 (which was EOLed in Jan 2020) in [jupyter notebook](http://ipython.org/notebook.html) depending only on a few basic libraries. The only external library needed is the [requests](http://docs.python-requests.org/en/latest/) HTTP library. Some of the external APIs require API keys (for example TMDB, you can obtain one [here](https://www.themoviedb.org/faq/api)).


1. Install Miniconda with Python 2.7

Miniconda is a free minimal installer for conda. Conda is an open source package management system and environment management system . Miniconda is a small, bootstrap version of Anaconda that includes only conda, Python, the packages they depend on, and a small number of other useful packages, including pip, zlib and a few others. 

see: https://docs.conda.io/en/latest/miniconda.html

Conda needs to access the internet. If you are behind a corporate proxy with ntlm authentication install a local proxy such as px and configure the proxy environment variables
```
  C:\> setx https_proxy http://127.0.0.1:3128/
  C:\> setx http_proxy http://127.0.0.1:3128/
  
2. Install jupyter notebook (to run the examples)

Run Conda Powershell from the Start menu install jupyterlab and notebook
```
(base) PS C:\> conda install -c conda-forge notebook
(base) PS C:\> conda install -c conda-forge jupyterlab
(base) PS C:\> conda install -c conda-forge notebook
```

2. Then use the following commands to install the exercuses
  ```
  git clone https://github.com/davidzof/relevant-search-book.git
  cd relevant-search-book
  
  cd ipython/
  ```

5. Launch!

  ```jupyter notebook```

6. Play!

Switch to your default browser where the Ipython examples are ready for you to experiment with. Keep in mind many examples are order dependent, so you can't just jump to an interesting listing and run it. Indexing commands with certain settings and what not need to be run. Be sure to run the prior ipython notebook commands too!

Happy Searching!

