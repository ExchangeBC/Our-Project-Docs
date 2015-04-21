
#Programs Goal

The concept of Programs and their accompanying Programs Page is intended to help meet several perceived business needs for Government and BPS – 

- Presenting a description of the Program, and helping to clarify the goals of the Program and related Projects that it encapsulates
- Help illustrate related business processes and business needs, through providing use cases, current and future journey maps, and listing related personas
- Provide some insight into how the program is being delivered, through sharing the perspective of the program owner and its staff, links to question and answer documents, and promoting opportunities for direct engagement
-	Expose related Projects and activities that are currently happening or are planned, including backlogs, epics, and user stories
-	Provide listings of relevant Projects and Digital Resources (APIs, Data, and Applications), helping to provide context for 
-	Show Pathway to Adoption options for the Program

##Programs In BCDevExchange

We are introducing the concept of a Program to BCDevExchange, intended to reflect a set of related projects or activities being sponsored or administered by a government or broader public sector organization. Conceptually, a Program exists at a higher level than a Project, and defines the bigger picture goals, objectives, and principles that individual Projects may work towards or support. A Program may also define the framework against which the Projects will be defined and structured. 

The new Program entity will exist above the existing Project entity, with each Program having zero or more Projects related to it. Each Project will reflect different groupings of activities or initiatives being pursued along their own timelines (possibly consecutively or concurrently within a Program). Currently, Resources are generally related to a Project (with the relationship inherited by the Program), but could also be listed directly against the Program.

#Program Directory

BCDevExchange will be enhanced to include a Program Directory – a page, accessible from the navigation bar (similar to Resources and Project searches), that provides a listing of all of the Programs registered with BCDevExchange. This directory will display each Program’s title, description, tags, and link to the Programs Page on BCDevExchange.
The contents of the Program Directory will be moderated by the BCDevExchange dev team, through the use of a source file in GitHub (a .yml file in the BCDevExchange-Programs repo). The listing in GitHub will include a URL identifying a separate .md file in the same GitHub repo, which will contain further details for the Program, and used to generate the Program Page.

#Program Page

For each Program listed in the Program Directory, a Program Page will be accessible on BCDevExchange. This page will display a breadth of information about the selected Program, and provide (to be determined) functionality for drilling down on Program details, viewing associated Projects, Backlogs, Resources, Links, and other rich content.
 
The contents of the Program Page will be generated from a source .md file in GitHub, which will be converted from markdown to html through new logic added to BCDevExchange. The source .md will be created jointly between the BCDevExchange dev team and the Program owner, and will reside in a BCDevExchange repo, allowing for full moderation control by BCDevExchange, though allowing for modifications to be made by the Program owner, and submitted through pull requests. 

Program Page Structure
Based on an analysis of the wireframe used as a driver for this enhancement, the following structure is proposed as a template for the Program Page. Formatting and fonts will be aligned with as per the existing BCDevExchange.org styles. 
Section Title – The title of a section. Used for the page header / titles and section headers. A Section Title should display in its own row. Interpret markdown Header 1 or 2 as Section Titles. Any Content that follows the Section title should display as full page width. Section Titles should be left aligned.


    #Heading = <h1>Heading 1</h1>
    ##Heading = <h2>Heading 2</h2>
    
Subsection Title – The title of a subsection, to be interpreted into a column style. Interpret any headers in markdown not equal to Header 1 or 2 as Subsection Titles. These titles are intended to support column headers, with multiple columns spanning a page. Subsection Titles should be left aligned. 
    
    ###Heading = <h3>Heading 3</h3>
    ####Heading = <h4>Heading 4</h4>
    #####Heading = <h5>Heading 5</h5>
    ######Heading = <h6>Heading 6</h6> 


**Content** – Words, lists, bullets that are not defined as titles. Need to support ordered and unordered lists, nested lists, bold, italics, Content should be left aligned, and wrapped to fit within its column width. Number of columns / width need to be defined.

    <p>Example content </p>
    <p><strong>bold example content </strong></p>
    <p><em>italicized example content </em></p>

**Creating Rows and Sections** – The BCDevExchange Program Page will utilize custom syntax for defining page structure within the markdown document, which can then be interpreted by BCDevExchange when the markdown is rendered into HTML. All of the below syntax can be commented out in GitHub (only making it visible when editing the document / viewing raw markdown), if a more similar look and feel between the GitHub rendered markdown and the Programs Page in BCDevExchange is desired. Syntax can be commented out by adding a start and stop characters around the string being commented out. 

    <!---[thing to be commented out]--->

[row start] This declares that a row is being created. Page will automatically define the spacing for 2 columns or 3 columns on the page, based on the number of columns that follow. 

[col start] This declares the start of a distinct column. Any Titles or Content that follow will be displayed constrained by the column width. It is recommended that no more than 3 columns be displayed in a single row (this is a style recommendation, not a technical limitation).

[col end] Declares the end of a distinct column. Subsequent [col start] can be declared.

[row end] Declares the end of a distinct row. Unless another row is declared, subsequent content will display in full page width.

**External Resources** - External sites can be linked via standard markdown linking.

    [Link description](www.destinationlink.url)

**Media** - Images, icons, or other (types to be determined) media can also be displayed on the Program Page, but will need a host location, and linked via standard markdown. Images, icons, and other media can be stored in a repo in GitHub, such as the existing Logos directory. Images should be provided by HTTPS instead of HTTP.

    ![Image name](www.contenthostlocation.url)

##How to list your Program

Programs Markdown template file in BCDevExchange – Programs. 

1.	Program owner forks the BCDevExchange - Programs repo
2.	Program owner copies an existing Programs file or template 
3.	Program owner renames the Program file to their Program name
4.	Updates template as per template instructions
5.	Makes pull request back to BCDevExchange 
6.	BCDevExchange accepts pull request
7.	Program owner can view their Program through a dynamically generated URL for the Program Page (available before it is visible on the Programs Directory)
8.	Program owner and BCDevExchange confirm the layout of the Program Page
9.	Once approved, BCDevExchange updates directory.yml to make the Program visible (change visible from ‘no’ to ‘yes’)
