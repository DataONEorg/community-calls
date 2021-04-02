# 2021-04-01 DataONE Community Call

[![hackmd-github-sync-badge](https://hackmd.io/vUhA2UV2QkOJNuFEmtXs7w/badge)](https://hackmd.io/vUhA2UV2QkOJNuFEmtXs7w)


**Topic:** Science on Schema.org Guidelines and Experiences

**Time:**
2021-04-01 at 8pm Eastern US time. Other time zones:
```
US/Eastern        2021-04-01 20:00:00 -0400
US/Central        2021-04-01 19:00:00 -0500
US/Mountain       2021-04-01 18:00:00 -0600
US/Pacific        2021-04-01 17:00:00 -0700
US/Alaska         2021-04-01 16:00:00 -0800
Pacific/Tahiti    2021-04-01 14:00:00 -1000
Pacific/Auckland  2021-04-02 13:00:00 +1300
Australia/Sydney  2021-04-02 11:00:00 +1100
```

**Description:** 

Schema.org provides a simple mechanism to include machine readable, structured metadata in human readable web pages, including descriptions of Dataset entries on dataset landing pages. The metadata is readily accessible using common web tools, and is actively harvested by large scale, generalist, commercial indexers (e.g. Google). DataONE will soon be indexing schema.org metadata as an alternative pathway for repositories to participate in the DataONE federation. The flexibility of schema.org means it can be used to describe many resources including scientific datasets, but that flexibility also enables potentially incompatible approaches for constructing such metadata. The ESIP Science-On-Schema.org group has produced an evolving set of guidelines to assist with consistent implementation of scientific dataset descriptions using the schema.org vocabulary. This community call will introduce the Science-on-schema.org guidelines, highlight additional resources available for working with schema.org, and include experiences of some that have implemented the guidelines for their repositories.

**Invited Panelits:**

* Jeff Horsburgh
* Daniella Lowenberg
* Adam Shepherd
* Chantelle Verhey
* Dave Vieglais

**Participants**

* Amber Budden, DataONE/NCEAS/Arctic Data Center aebudden@nceas.ucsb.edu
* Harrison Dekker, URI/Project STEEP, hdekker@uri.edu
* Adrienne Canino
* Ashley Orehek, University of Tennessee, aorehek@vols.utk.edu
* Becca Scully
* Bryce Mecum
* David Tarboton, Utah State University, david.tarboton@usu.edu
* Frank Nitsche
* Jing Tao
* Julian Gautier, Dataverse/IQSS juliangautier@g.harvard.edu
* Karl Benedict
* Madison Burrus
* Marcelo Morandini, University of Sao Paulo, m.morandini@usp.br
* Martin Seul
* Matt Jones, DataONE/NCEAS/Arctic Data Center jones@nceas.ucsb.edu
* Meghan Eyler
* Michael Bobak
* Neil Davies, UC Berkeley, ndavies@berkeley.edu
* Peter Pulsifer
* Philip Murphy
* Rajesh Kalyanam
* Ramona Walls
* Sean Gordon
* Stepehn Richard
* Stott (maybe Don Stott?)
* Thomas Thelen
* Steve Diggs
* Stevan Earl, CAP LTER, stevan.earl@asu.edu

**High-Level Agenda**

1. Brief introduction (5min, Karl)
2. Introductions from panelists (20-30min)

   1. `Schema.org` primer (Chantelle)
   2. `Science-on-schema.org` (Adam, [slides](https://docs.google.com/presentation/d/1zejEJjbHmEOuqNzi79w5C0Tnnzc-l3jsk1Z0CV6QMKE/edit#slide=id.gce444d0463_0_0))
   3. BCO-DMO (Adam)
   4. Data Dryad (Daniella)
   5. HydroShare (Jeff)
   6. DataONE support (Dave)

3. Discussion, Q/A

    Chantelle Verhey - schema.org primer
    - designed for data managers, current resources distributed and siloed. Intent of primer is to bring materials together into one-stop-shop. 
    
    Adam Shepherd
    - History - ESIP cluster started by programmers sitting at repositories. Up tick in web publishing using schema.org. Wanted to apply to science use cases. Shared pattern - reliable, consistent federation. Guidlines released 4/1/20, 2nd revision coming in July 2021. 
    - BCO-DMO implementation. Website is drupal based. Schema.org implemented on the back end, php, json-ld serialization. 
    
    Daniella Lowenberg
    - Dryad implementation of schema.org was simple. 'Super easy'. Did find that making adjustments to schema.org would create issues with google datasets, but these may ve resolved in v3? 
    
    Jeff Horsburgh
    - HydroShare is a repository operated by CUASHI. Data and models. A place where researchers can link models and data to journal publications. Uses dublin core metadata to describe resources. Implementation pretty straight forward to map dublin core elements to schema.org. Useful to have the science on schema.org recommendations/ guidelines was very helpful. Embedded in html code of resource landing pages. (there is guidance on where this should be placed within soso). Some differences - expressiveness of metadata did not always enable the soso guidelines to be followed. e.g. roles - only had contributors and creators. Google dataset search is picking up hydroshare resources; dates, licenses etc. Excited for hydroshare to join the DataONE network using schema.org.

    Dave Vieglais
    - DataONE status: now have member node implementaiton, indexing rules in place for coordinating nodes. Need to move to a test instance for evaluation and then more to produciton. Offers a relatively straight forward way for repositories to participate in DataONEinfrastructure. Determination of whether a resource has changed. Currently look at site map, points to landing page, extract json-ld. Having time stamps of when things have changed is very helpful. And having this information upfront to save complete download. Google structured data testing tools are useful but oriented twds google needs and doesn't align with richness desired for science datasets. 2-way street - can provide feedback to soso group and to google implementers to help make it as useful as possible.


    Implementation list
    - BCO-DMO: Drupal backend, php implementation
    - Dryad
    - HydroShare



Questions:

* There seems to have been a convergence towards the JSON-LD serialization as a recommended approach - what are the pros and cons that folks have encountered with the different options for serialization?
    * Multiple ways to embed schema.org content in webpages - comes down to effective tagging and markup. Community is settling on json-ld as most appropriate way for expressing machine readable markup. 
    * From hydroshare perspective, was able to do mapping, hand over to developer who did the serialization and add to html without impacting the rest fo the web page. 
    * Steve Richard - this is one of the bog resasons that schema.org has become popular. With json-ld there is one scipt, an applicaiton, at one place in the document enabling easy injection, maintenance and debugging.
* Folks spoke about the strengths and things that worked.  What were the things missing or that did not work smoothly?
    *   JH: 4 things. 1) representation of license (they allow as an option custom license terms, so a URL alone was insufficient) 2) funding element - still unresolved. funder/funding/monetary grants - terms suggested but no consistency 3) provenance information to related resources. 
    *   MJ: prioritize the omnetary grant issue to 1.3 release?
    *   SR: In earthcube geocodes interface, trying to integrate linkages btn data and tools. Need conventions around how relationships are consistently described. A few different ways that people are describing how they get the data. The flexibility (inconsistency) has been a challenge. 
    *   DV: encoding geospatial information has been a challenge but some consistency being developed there. 
    *   DV: Two namespaces for schema.org (http://schema.org versus https://schema.org)
* What's the difference between sameAs and url elements? I've had trouble deciphering them.
    * JH: In hydroshare every resource gets a hydroshare id. When published it gets a DOI so for URL they give the DOI encoded URL and the same as they will use the hydroshare ID. 
    * MJ: URL is primarily meant to be a locator to let you know where you will get the item on a web. Same as is for other resources that are instances of the same dataset at other locations. This might also be a URL but not always. Its saying that two things are equivalent. URL is telling you were to go. A lot of subtlties and likely a lot of variability in implementation.
* I'm working with data that has several types of keywords, like GCMD. What's a strategy to incorporate keywords like GCMD?
    * DV: Is there a recommendation in soso?
    * SR: There's a defined element
    * AS: https://schema.org/keywords accepts "DefinedTerm"
    * AMO: GCMD also follows a hierarchy too, so I want to avoid redundancies
    * AS: There is an issue for this and will look at this for v1.3. (https://github.com/ESIPFed/science-on-schema.org/issues/125)
* Favored tooling / resources? Is it an issue for developers to be able to test?
    * JH: Used GSDTT (Google Structured Data Testing Tool) to test. Some issues missed that a developer would have identified given time
* How many people are getting ready to implement schema.org - have been looking at it but weren't / aren't quite ready.
    * AMO: Practicum with NCAR EOL and working with them to implement 
    * AC: Yes
    * RW: We implemented in CyVerse a few years ago, and found it pretty straightforward. We will implement it soon in iSamples, I hope!
* Have there been observed benefits from implementation?
* AC: are the search engines other than google that benefit from schema.org
    * DV: Yes, other engines (bing, duckduckgo, few others), DataONE ... Hard to say how richly they are expressing the informaiton and what they are using it for. 
    * AC: Commercial indexers too? e.g. Web of Science (as was named), Mendeley
    * DL: They were scraping from DataCite vs schema.org. Doesn't help with non DataCite DOIs
    * DV: Can be used for much more than describing datasets - organizaitons, researchers ... linked data approach enables you to repeatedly list investigators in multiple locations. 