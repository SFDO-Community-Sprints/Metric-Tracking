### Metric Tracking
Better understanding of the data collected for clients/students at an organization.

### Project Description
Identify and develop metrics that organizations can use to track their outcomes and answer questions such as:
  * Is the client/student at risk?
  * How effective is our support to the client or students?
  * Which client/student should we focus on?
  * How to measure the performance of an initiative against defined parameters (e.g., budgetary, etc)


### Project Audience
Anyone who wants a system to collect data about a program with key indicators, results and targets.

### Project Team

* Team Leader:
* List of Contributors: Christopher Littlefield (clittlefield3@une.edu), Carol Le (cle2@une.edu), Ashima Saigal (ashima@databasesherpa.com), Jason Vance (vancejas@msu.edu), Heath Parks (heathparks@cincinnatiworks.com), William Corkill ()

### Project Team Accomplishments
What did the Project Team accomplished during the Sprint?
Discussing the two of tracking data:

  * Specific data at the object level (i.e. Contact, Account, Campaigns, etc)
  * Aggregating of specific data to better understand the outcomes
  
We created a data model and method for tracking the indicators and outcomes for those indicators. We discussed ways to collect the data for the results. Initially it would be entered into the system manually using reporting data or existing roll up data, eventually code could be written to grab data from a report or a field to fill in the results data.

### Contributing
If someone were to contribute to this project at the next Sprint what would you want them to work on to move this project forward?
* Talk to the team about how program data is currently being collected
* Being willing to push and pull on the model designed here, keeping in mind this is a simple prototype to begin

### Project Roadmap
What is the ultimate vision for this project?
* Create a data model for collecting data for programmatic purposes

### Reference:
* Verasolutions.org - Solutions: Amp Impact

### Schema
Objects:
* Initiative - Object to hold the results of each related benchmark. Has a master-detail relationship with the Benchmark object.
* Benchmark -  Object to hold each of the various initiatives.
* Indicator - Object that holds the key measurements to track for the organization. Has master-detail relationship with the Outcome object.
* Outcome - Object to hold the outcomes which compare the target data and the actual results for a specific indicator. This is a junction object for Indicator and Benchmark.

Initiative Fields:
* Name (text)
* Category (picklist)
* Start Date (date)
* End Date (date)
  
Indicator Fields:
* Name (text)
* Result Type (picklist)

Outcome Fields:
* Indicators (lookup)
* Targets (numbers)
* Results (numbers)
