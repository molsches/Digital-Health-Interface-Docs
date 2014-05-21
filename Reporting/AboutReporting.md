#About Reporting#

##Discretion is the better part of valor##
While it seems like getting an API or an interface setup might be a breeze, it can often incur the difficulties of involving folks to plug interfaces together. Interface folks may be busy, booked, or otherwise indisposed to help you out on your project. You might also get involved with a level of organizational approval or budgeting with interfaces that will extend your project timelines to an undesirable level.

One good alternative, if real-time push/pull data is not required for a application workflow, is to use an EMR's built in reporting tools to query for data and save the results to a location that can be accessed via VPN or SSH.

This isn't quite a silver bullet, but it provides an option that may be more amenable to an organization. This may be particularly true if you can supply the expertise or personnel to handle the report writing. Many healthcare organizations are already automating and distributing daily reports; you would simply need to hook into their existing batch distribution workflows.

###Epic###

Epic can save and export batch data via either it's Clarity Reporting Module or through batch reporting run directly on Chronicles RDMS. Most Epic sites run a "Shadow" or reporting server that mirrors real-time data for reporting purposes. You would write reports on those servers which would be saved somewhere on those UNIX servers or some other agreed upon network location. Most Epic sites have some data that is grabbed from 3rd party vendors this way, be it .wav files for transcription or reports distributed to downstream systems.

###Cerner###

Most Cerner applications interact with the Cerner database layer through CCL, the Cerner Command Language. CCL is similar to SQL, and can be used to declaratively query for data within Cerner. Cerner organizations have the ability to script reporting using CCL, and it's not uncommon for a large Cerner organization to have a few CCL wizards on staff (often former Cerner employees).

(http://en.wikipedia.org/wiki/Cerner_CCL "Wikipedia Page on CCL")

(http://www.cerner.com/uploadedFiles/Content/Solutions/Customer_Stories/Childrens_national_medcenter_casestudy.pdf "A white paper where Cerner talks about automating reports used for improving adverse event identification")

###Allscripts###

Most Allscripts EHR Applications (Professional, Enterprise, Sunrise Inpatient) have some reporting infrastructure built on MS-SQL technologies. Some of this may be exposed via CLinical Analytics or may be available simply by tapping into the SQL Server on a non-production environment through either SSRS or Crystal Reports. Be forewarned, the data models are supposedly hairy. You may be better off using Allscripts APIs if they better meet your needs.

###NextGen###

You can use SSRS or Crystal Reports to query objects on the MS SQL server. There are a few consulting shops that currently do this.

###Meditech###

You can automate reports through the (https://www.meditech.com/ProductBriefs/presentations/quality_reporting/report_scheduler.htm "Report Scheduler")
