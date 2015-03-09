<a rel="research" href="https://github.com/BCDevExchange/docs/wiki/Project-States"><img alt="An idea being explored and shaped. Open for discussion, but may never go anywhere." style="border-width:0" src="https://img.shields.io/badge/BCDevExchange-Research-red.svg" title="An idea being explored and shaped. Open for discussion, but may never go anywhere." /></a>

##GitHub as a Data Source 

To support the principle of relying on external data, it is proposed that GitHub be used as a source of data for BCDevExchange.org. Some proposed ideas are discussed below. 

**Release 1:** To help avoid having to build out a backend or store data on BCDevExchange, it’s proposed that we utilize GitHub as a ‘back end’ / database. This could theoretically be used to store information for any of the elements discussed in this document (Profiles, Organizations, Resources, Interests, or Projects), but would probably be initially used just for [[Resources|resources]] and [[Projects|projects]].
 
An idea being discussed is tagging a Repo’s readme.md with an identifier flagging it as a Project (BCDevExchange-Project) or a Resource (BCDevExchange-Resource), and having BCDevExchange search functionality return these as part of relevant queries. Some sort of structure within a Project Repo may also be useful for displaying a Project backlog to users via BCDevExchange, such as an associated issues list, which can be retrieved by BCDevExchange post query. 

To become available for search by BCDevExchange, a repo would need to be registered by a user who has created an account with BCDevExchange via an existing GitHub account. 

1.	Register with BCDevExchange with a GitHub account
2.	BCDevExchange pulls and displays a list of GitHub Repos associated to the account (those associated directly with the account, and those associated with associated Organizations where the account has an Owner role)
3.	For each Repo returned, the user can select a desired State (Research, Discovery, Delivery), and Type (Resource, Project, possibly others) 
4.	An Activate button (or other function) will display for each displayed Repo. Pressing this button will initiate the following automated process (done through GitHub / GitHub APIs) - 
    1. BCDevExchange Organization forks the Readme.md from the selected Repo
    2. Appends the Readme.md with a BCDevExchange identifier, state, type, and URLs for relevant badges
    3. A pull request sent to the Repo owner 
5.	Once the pull request is accepted, then the Repo will be returned by calls to the GitHub API from the BCDevExchange search functionality

GitHub has an API available for querying its repos and files. There are some limitations that require an account name or repo name to be identified when using the API. This would require users to register with BCDevExchange.org with a GitHub account (thereby registering their GitHub account with BCDevExchange), which can then be used when calling the GitHub API and querying its data. 

###Conversations

**Future State:** GitHub supports Repo specific Wikis and Issue reporting / tracking. These existing tools are being considered as mechanisms to support conversations, discussions, and feedback on Projects or Resources shared on BCDevExchange through GitHub. Projects and Resources stemming from other locations (such as BCDC) would require different tools to support discussions or feedback. As mentioned previously, issue lists can be used to store and track a project backlog.

###Organizations

**Future State:** [[Organizations|organizations]] maintained in GitHub could be identified through the presence of an associated .md (with naming convention or content) or specific keywords in their description, and used to populate search results from BCDevExchange.org.
