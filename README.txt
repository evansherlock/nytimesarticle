===========
nytimesarticle
===========

nytimesarticle is a fully-functional Python wrapper for the New York Times Article Search API. 


Installation
=========

With pip::

    $ pip install nytimesarticle

or easy_install::

    $ easy_install nytimesarticle


Dependencies
=========

nytimesarticle requires the `requests <https://pypi.python.org/pypi/requests>`_ package.


Usage
=========

Simply import and initialize the API with your developer key::

    $ from nytimesarticle import articleAPI
    $ api = articleAPI('*Your Key*')

And call the 'search' function with your desired search parameters/values::

    $ articles = api.search( q = 'Obama', fq = {'headline':'Obama', 'source':['Reuters','AP', 'The New York Times']}, begin_date = 20111231, facet_field = ['source','day_of_week'], facet_filter = True )

The search function returns a dictionary of the search results.

You can specify multiple filters by using a dictionary::
    fq = {'headline':'Obama', 'source':['Reuters','AP', 'The New York Times']}

And multiple values by using a list::
    facet_field = ['source','day_of_week']

More examples::

    $ articles = api.search( q = 'Obama' )

    $ articles = api.search( q = 'Obama', begin_date = 20111231, page=2 )


For a complete overview of the available search parameters, please refer to the NYTimes Article Search API `Documentation <http://developer.nytimes.com/docs/read/article_search_api_v2>`_.

