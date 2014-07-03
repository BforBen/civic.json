# civic.json
A standard metadata specification for civic technology projects


## Purpose

Civic.json is a metadata standard for civic technology projects that is intended to complement project information in a github repository.  This document will specify the keys and values that make up the civic.json data standard, and provide information about the scope, mission, and background of the standard.


## Background 

In 2013, civic Technologists at Chicago's Opengov Hacknight created a "hands-off" projects page using the github API.  In the world of civic hacking, projects come and go, and there is a risk of user-maintained projects pages to become stale.  The intent was to make a "stupid simple" projects page, where all of the data came from github repositories, where "...humans will be responsible for one thing: deciding what gets tracked."  

On the 20th June 2014, the LocalGov Digital Makers created an adaptation of civic.json to extend the metadata available and to try and apply more common structure around the categorisation and linking of the data.

In theory, if civic technology groups adopt this standard, it will be possible to aggregate nationwide, regional, or topic-specific lists of civic tech projects.


## File Location and contents
1. `civic.json` shall reside in the root directory of a project's github repository.
2. `civic.json` shall include a single object represented as JSON, with the key/value pairs outlined below.


## Key/Value Specification
1. `status` - text indicating the status of the project.  Any text is allowed, but a selection from the recommended values is advised:

   * `"Ideation"` - Brainstorming phase
   * `"Alpha"` - Brainstorming phase
   * `"Beta"` - Brainstorming phase
   * `"Production"` - Finished Product, development ongoing
   * `"Sunset"` - Finished Product, development ceasing
   * `"Archival"` - Finished Product, development ceased
2. `thumbnailUrl` - a url to an image associated with the project listing
3. `bornAt` - text indicating the name of the event or place the project was conceived at, if any.  Any text is allowed.
4. `geography` - text indicating the town, city, county, or other geographic entity this project is relevant to.  Any text is allowed.

		examples: "UK", "London", "Shorditch"
5. `politicalEntity` - text indicating the political entity the project is relevant to. Any text is allowed.

		examples: "Westminster City Council", "DWP"
6. `type` - text describing the type of project.  Any text is allowed, but a selection from the recommended values is advised:

   * `"Web App"`
   * `"Mobile App"`
   * `"Policy Document"`
   * `"Dataset"`
   * `"Schema"`

7. `needs` - an array of "need" objects.  There is no limit to the number of needs included in a project.
8. `need` - text indicating a need of the project.  This can be a skillset that is needed, or any other resource.  Any text is allowed.

		examples: "Web Designer", "Web Hosting", "Political Sponsorship"

9. `categories` - an array of "category" objects.  There is no limit to the number of categories included in a project.
10. `category` - text indicating the category of the project.  Any text is allowed.

		examples:  "Land Use", "Transportation", "Politics", "Financial", "Open Data"

11. `owner` - object indicating the person or organisation that the project is owned by.

	* `"name"`: the name of the person or organisation

		examples: "Guildford Borough Council", "DCLG", "DWP"

	* `"type"`: the type of organisation 

		examples: "Local council", "Government Agency"
		
	* `"@id"`: the uri of the named resource

		example: "http://somewhere/some#thing"
		
12. `deployments` - array of objects detailing name and uri of where the project is deployed

	* `"name"`: the name of the deployment

		examples: "Guildford Borough Council"
		
	* `"@id"`: the uri of the named deployment

		example: "http://somewhere/some#where"
		
13. `serviceCategories` - array of objects describing associated services for the project

	* `"name"`: the name of the service

		examples: "Planning", "Housing", "Pensions"
		
	* `"@id"`: the uri of the named services

		example: "http://id.esd.org.uk/service/1057"
14. `technologies` - array of objects describing technologies used in the project

	* `"name"`: the name of the tech

		examples: "AngularJS", "Ruby on Rails", "PHP"
		
	* `"@id"`: the uri of the named tech

		example: "http://angularjs.org"

## Example civic.json
```
	{
        "status": "Beta",
        "thumbnailUrl": "https://avatars.githubusercontent.com/u/6362924?s=64",
        "bornAt": "LocalGovDigital Makers Hackday",
        "geography": "UK",
        "politicalEntity":"",
        "type":"Web App",
        "needs": [
                {"need": "Web Designer"},
                {"need": "Node Dev"},
                {"need": "Angularjs Dev"}
        ],
        "categories": [
                {"category": "Community"},
                {"category": "Education"}
        ]
        "owner": {
            "name": "Brighton and Hove Council",
            "type": "Local council"
            "@id": "http://gov.uk/councils/brighton"
        }
        "deployments": [
            {
                "name": "Brighton",
                "@id": "http://budgetsimulator.com/brighton-and-hove"
            }
        ]
        "serviceCategories" [
            {
                "name": "Waste",
                "@id": "http://example.com/services/waste",
            },
        ]
        "technologies" [
            {
                "name": "Ruby on Rails",
                "@id": "http://rubyonrails.org",
            },
        ]
}
```

## Links
 *  [Opengovhacknight's projects page](http://opengovhacknight.org/projects.html)
 *  [Repo for backend of Opengovhacknight's projects page](https://github.com/open-city/civic-json-worker)
 *  [Repo for frontend Opengovhacknight's projects page](https://github.com/open-city/open-gov-hack-night#projects-and-people)
 *  [BetaNYC's projects page](http://projects.betanyc.us)
 *  [Repo for BetaNYC's projects page](https://github.com/chriswhong/betanyc-projects-list)




