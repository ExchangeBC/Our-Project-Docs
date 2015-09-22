#API Owner Engagement Level 
(service scenarios using BCdevExchange):
----
---
###Advertisement only
	* shallow integration (tags, links, and description)
	* provide API explorer (no dependancy on gateway)
	* Self service
#####Builder Activity:
	* Swagger and URL
#####Feature needed by DevExchange
	*  API Explorer
	*  Search
	*  Code Snipits

---	
###Extended Channel: (gateway plus self hosted API)
#####Feature needed by DevExchange
	* Needs everything above plus a Swagger composer.

---
###Exclusive Channel (gateway and migrate domaine to bcdevexchange)
	* Fully Self serve
#####Builder Activity:
	* Supply SSL cert
	* change DNS to Cname
#####Feature needed by DevExchange
	* requires dynamic SSL cert selector

---
###Simple Hosted Repo (basic CRUD)
	* Self servicable
#####Builder Activity:
	* need to create data model that API is based via GUI
	* Expose the database
#####Feature needed by DevExchange
	* All above features plus modeler
	* Hosting policy

---
###Complex Hosted Repo (need custom code to transform data)
	* Supply custom code via PR (no longer self serve)
	* Uses github for code managment

---	
Loosely coupled features is a bonus

Tool Kit:

	* API explorer: core Swagger ui
	* Search:
	* Swagger Composer:
	* Dynamic SSL cert: NodeJS package
	* Modeler:
	* Code Repos: GitHub
