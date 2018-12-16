# Introduction
A ruby parser using [linkeddata](https://github.com/ruby-rdf/linkeddata) and [rdf](https://github.com/ruby-rdf/rdf) to interpret the [Semantic Web for Earth and Environmental Terminology (SWEET)](https://github.com/ESIPFed/sweet) ontology suite. Additonally this program loads SWEET into [Neo4J](https://neo4j.com) for cool graph queries and examination.

# Installation
Ensure you have the most recent version of Ruby installed. If you need to upgrade, you can run 

```
$ \curl -sSL https://get.rvm.io | bash -s stable --ruby
```
Then install some Ruby Gems (you may need to be root)
```
$ gem install rdf linkeddata neography activesupport
```
Finally, ensure that you have a local version of Neo4j running.
```
$ brew install neo4j
$ neo4j start
```
Ensure that your username and password are set. The default username and password for Neo4j is 'neo4j' and 'neo4j' respectively. You can change these from the GUI the first time you use Neo4j. You can navigate to http://localhost:7474/browser/ to set it.

# Configuration
Before running the program, make sure the following properties are set in **parser.rb**

```ruby
# Set the following variables in parser.rb and let the magic happen
NEO4J_USER = "${your.username}"
NEO4J_PASSWORD = "${your.password}"
SWEET_URL = "https://raw.githubusercontent.com/ESIPFed/sweet/master/src/sweetAll.ttl"
```

![Alt text](graph.png?raw=true "Sweet Neo4J")
