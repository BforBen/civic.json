**UNDER DEVELOPMENT**

This standard is still being refined.

---

Civic.json is a metadata standard for civic technology projects that is intended to complement project information in a github repository.  This repo contains documents that specify the keys and values that make up the civic.json data standard, and provides information about the scope, mission, and background of the standard.

civic.json exists to create an api-accessible set of project attributes that complements the attributes already associatd with a github repository.  These can be used to power an API-driven community projects list like http://lgprojects.herokuapp.com/

civic.json looks like this:

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
