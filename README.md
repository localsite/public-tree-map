# public-tree-map

Public Tree Map uses open datasets to document publicly owned park + street trees in Santa Monica, California. We're also working to add coverge in other parts of LA County (based on [data](https://github.com/stiles/data/tree/master/los-angeles-street-trees) collected by Matt Stiles). For details about how we process data, please see the [data pipeline repository](https://github.com/Public-Tree-Map/public-tree-map-data-pipeline). For more information about the project, please see our [project page](https://public-tree-map.github.io/) and join our [slack workspace](https://join.slack.com/t/publictreemap/shared_invite/zt-dzhrivk4-m8gaZ3wrZBE_leo_oeepPw). 

We primarily use javascript.
Our test site is https://publictreemap.org/

## Contributing
```bash
git clone https://github.com/Public-Tree-Map/public-tree-map.git
```
No other setup is required. Access the index.html file in your browser to see the application. 

**iOS Debug Notes:**

To debug Geolocation related functionalities on iOS, use Safari Web Inspector following [these instructions](https://medium.com/better-programming/debugging-your-iphone-mobile-web-app-using-safari-development-tools-71240657c487).

Additionally, Safari does not allow location service over HTTP. In order to debug and test on iOS, the website must be served over HTTPS. The following steps and terminal commands are provided for using [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) in [VS Code](https://code.visualstudio.com/):

- create private key and certificate

        openssl genrsa -aes256 -out localhost.key 2048   
        openssl req -days 3650 -new -newkey rsa:2048 -key localhost.key -x509 -out localhost.pem
        

- create `.vscode/settings.json` in project folder, add following:

            {
            "liveServer.settings.https": {
            "enable": true,
            "cert": "{some path}/localhost.pem", //certificate, absolute path
            "key": "{some path}/localhost.key", //private key file, absolute path
            "passphrase": "12345" //passphrase used in private key creation
            }
    (see [here](https://github.com/ritwickdey/vscode-live-server/blob/master/docs/settings.md) )


## Protocol for pull requests + code review

- Please review open issues and link your pull request to the relevant issue. 
- Please create a new branch!
- Please determine if your contribution is part of the [la county expansion milestone](https://github.com/Public-Tree-Map/public-tree-map/milestone/1). If your work is part of this milestone, please make your PR to the ["la-expansion"](https://github.com/Public-Tree-Map/public-tree-map/tree/la-expansion) branch.
- In your pull request, please list and explain all proposed changes to the code base (additions, deletions). If you reuse code from elsewhere, please make sure you've attributed it.
- Please apply all relevant labels to your pull request.
- Please request a review (either from a specific person or from the appropriate [slack channel](https://join.slack.com/t/publictreemap/shared_invite/zt-dzhrivk4-m8gaZ3wrZBE_leo_oeepPw)).
- Reviewers: please review all proposed changes, write comments and questions in line notes. Please review all updates made at your request.
- Reviewer and requester: please confirm with each other that the PR is ready to merge. Please make sure that the PR branch name documents the new changes.

## Related projects/inspiration
- [A Very Detailed, Interactive Map of Chicago’s Tree Canopy (Atlas Obscura)](https://www.atlasobscura.com/articles/chicago-tree-canopy-map-2017)
- [Arnold Arboretum map explorer](https://arboretum.harvard.edu/explorer/?utm_source=topnav&utm_medium=nav&utm_campaign=top-menu-map)
- [Canopy](https://github.com/seeread/canopy) and descriptive [blog post](http://www.datakind.org/projects/out-on-a-limb-for-data) from DataKind
- [Canopy Tree Plotter](https://pg-cloud.com/Canopy)
- [The effects of urban trees on air quality - USDA 2002 PDF](https://www.nrs.fs.fed.us/units/urban/local-resources/downloads/Tree_Air_Qual.pdf)
- [Friends of the Urban Forest - SF (FUF)](https://www.fuf.net/)
- [i-Tree](https://www.itreetools.org/)
- [Increased home size and hardscape decreases urban forest cover in Los Angeles County’s single-family residential neighborhoods PDF](http://johnwilson.usc.edu/wp-content/uploads/2018/03/Increased-home-size-and-hardscape-decreases-urban-forest-cover-in-Los-Angeles-Countys-single-family-residential-neighborhoods.pdf)
- [Jill Hubley's NYC street tree map](https://github.com/jhubley/street-trees)
- [Melbourne - Urban Forest Visual](http://melbourneurbanforestvisual.com.au/)
- [Minimum Requirements for an Arborist Report - City of Atlanta PDF](https://www.atlantaga.gov/home/showdocument?id=20151)
- [NYC Parks' New York City Street Tree Map](https://tree-map.nycgovparks.org/)
- [The Need to Standardize At-planting Data PDF](https://urbanforestry.indiana.edu/doc/publications/2015-need-to-standardize.pdf)
- [Pasadena Beautiful Foundation's Endangered Trees List](http://www.pasadenabeautiful.org/green-links/endangered-trees-list/)
- [Rancho Santa Ana Botanic Garden - app (Guru LLC)](https://itunes.apple.com/us/app/rancho-santa-ana-botanic-garde/id1389785599?mt=8)
- [RegisTree](http://www.vision.caltech.edu/registree/)
- [Santa Monica's Top 15 Tree Speices PDF (2010)](http://csmgisweb.smgov.net/docs/mapcatalog/trees.pdf)
- [TreeMapLA](https://www.opentreemap.org/latreemap/map/)
- [Urban Tree Growth & Longevity (UTGL) Working Group - Urban Tree Monitoring Protocols Field Guide](http://www.urbantreegrowth.org/field-guide.html)
- [West Coast Arborists (WCA)](https://westcoastarborists.com/services) - see the description of ArborAccess, WCA's GPS tree inventory service for their clients
- [We calculated how much money trees save for your city - The Conversation](http://theconversation.com/we-calculated-how-much-money-trees-save-for-your-city-95198)
