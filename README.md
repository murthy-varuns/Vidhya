# Vidhya
A search engine to view and order books with a single click

Every time I've tried to buy books online I've encountered the following problems:
1. No one seller has all the books I'm looking for
2. I need to create multiple sessions, each with a different shopping cart, to buy from multiple sites
3. Local bookstores don't update their inventory online and I need to call them to place an order

All of these can be solved with an Amazon/Google-like search engine interface that allows you to simply browse your favorite titles without having to worry about ordering and shipping them to your doorstep. 

## Phase 1
Build a command line tool that given the name of a book, finds available inventory (online and in person) close to you, and can build a valid shipping order (not place it, just build it).
### Design
Crawling [Python]: Needs to be written to schedule crawls across a list of trustworthy hosts and return availability in a tuple format (TITLE, LOCATION, PRICE, AVAILABILITY)
Indexing [Python]: Needs to be written to store availability in a key-value store with TITLE as primary and LOCATION as secondary keys, i.e. (TITlE, LOCATION) could also be a valid key
Retreiving [Python]: Needs to be written to quickly retreive availability of books near user both online and offline with probabilistic guarantee on delivery time

e.g. `$python vidhya.py "Principles by Ray Dalio"`
