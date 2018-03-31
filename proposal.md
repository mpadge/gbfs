
Project Proposal: Bikeshare 1
=============================

#### *Kaelyn Rosenberg & Simon Couch*

#### General theme

Several years ago Portland introduced a bikeshare program called Biketown. In this system, bikes are available to rent from stations throughout the city and can be returned to another station, with the transaction conducting via smartphone, resulting in a rich trail of data. We plan to develop an R package to assist in making use of this data.

#### Specific questions

What functions can be written to query and organize this data based on user arguments?

What kinds of questions are people asking about this data, and how can that visualization process be automated?

#### Relevant work

The following works help us to understand the structure of bike sharing programs and what kinds of questions people are asking about bike sharing, which can help guide us in thinking about what types of functions would be most useful to people trying to analyze bike sharing data.

Bike-sharing: History, Impacts, Models of Provision, and Future (DeMaio)

Bikesharing in Europe, the Americas, and Asia: Past, Present, and Future (Shaheen et. al)

Shared Bicycles in a City: A Signal Processing and Data Analysis Perspective (Borgnat et. al)

#### Clients/stakeholders and their contact information

For further information on biketown data storage, these contacts might be useful:

<customerservice@biketownpdx.com> - (866) 512-2453

To get in touch with someone at the Portland Bureau of Transportation:

503-823-5185 (Note: this is a general referral line--numbers of specific departments listed online do not seem relevant to this work)

#### The data

The data is stored in a json feed in a standardized data format for bikeshare data (gbfs). Links to each dataset can be found at <http://biketownpdx.socialbicycles.com/opendata/gbfs.json/>. The data is stored in 9 different files: system information, station information, station status, free bike status, system hours, system calendar, system regions, system pricing plans, and system alerts. All of this data is real-time, and is not aggregated over a larger time span. Accordingly, these individual files are small (100kb at most). Each of the files has its own observational unit and variable types.

For this reason, we need a data source that encompasses data since the project began and/or data with query-specified time ranges. There is a promising source that needs to be looked into further here: `https://app.socialbicycles.com/developer` It seems like this is a paid, subscription-based program, and it's not entirely clear the data they are offering.

Privacy concerns are minimal for this study; the released data does not have names or unique identifiers attached to it, and all rides start and end at the same, public places.

#### Vision for deliverable

Our main vision for the deliverable of this project is an R package. We would first like this R package to query bikeshare data, save it as .csvs, and organize it intuitively and in a way that can easily interact with similar data pulled with different arguments. Next, we would like to develop a function that develops a sort of "suite" of visualizations based on what the user would like to know about (i.e. which datasets to consider, around what time frame, and in what location).