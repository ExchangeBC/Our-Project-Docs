#API Owner Engagement Level
(service scenarios using BCdevExchange):
----
---

<table>
  <tr>
    <th>Engagement Level  in Ascending Order</th>
    <th>Self Serviceable?</th>
    <th>Provider Activity</th>
    <th>Feature Needed</th>
  </tr>
  <tr>
    <td>Advertisement Only</td>
    <td>Yes</td>
    <td>supply swagger URL</td>
    <td>API explorer;<br>search;<br>code snippet;</td>
  </tr>
  <tr>
    <td>Extended Channel</td>
    <td>Yes</td>
    <td>compose swagger</td>
    <td>+ API gateway;<br>swagger composer</td>
  </tr>
  <tr>
    <td>Exclusive Channel<br>(Migrate Domain)</td>
    <td>Yes</td>
    <td>+ supply SSL cert files<br>change existing DNS to a CNAME</td>
    <td>+ dynamic SSL cert selector</td>
  </tr>
  <tr>
    <td>Simple hosted repo with CRUD operation</td>
    <td>Yes</td>
    <td>Create data model via GUI</td>
    <td>+ modeler</td>
  </tr>
  <tr>
    <td>Complex hosted repo <br>(custom code to transform data)</td>
    <td>No</td>
    <td>+ supply custom code via PR</td>
    <td>GitHub!</td>
  </tr>
</table>


###Advertisement only
	* beyond shallow integration (tags, links, and description)
	* provide API explorer (no dependancy on gateway)
	* Self service
#####Builder Activity:
	* Swagger and URL
#####Feature needed by DevExchange
	*  API Explorer
	*  Search
	*  Code Snippets

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

## Other Common Services
* Analytics & Reporting
* Logging
* APM
