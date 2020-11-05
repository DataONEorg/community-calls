# 2020-11-05 DataONE Community Call

[![hackmd-github-sync-badge](https://hackmd.io/DJM08xWQQc6B2qy3dby0fw/badge)](https://hackmd.io/DJM08xWQQc6B2qy3dby0fw)

Nov 5, 2020 9am Pacfic time

## Participants (please add your name, email, and affiliation)

- Matt Jones, jones@nceas.ucsb.edu, [DataONE](https://dataone.org)
- Amber Budden, aebudden@nceas.ucsb.edu, [DataONE](https://dataone.org)
- Erin McLean, mclean@nceas.ucsb.edu, [Arctic Data Center](https://arcticdata.io)
- Jasmine Lai, jasminelai@nceas.ucsb.edu, [Arctic Data Center](https://arcticdata.io)
- Dave Vieglais, vieglais@ku.edu, [DataONE](https:/dataone.org/)
- Karl Benedict, kbene@unm.edu, [DataONE Community Board Co-Chair, UNM](https://www.dataone.org/community/)
- Adrienne Canino, adrienne@axiomdatascience.com, Axiom Data Science in Anchorage, AK
- Jeff Horsburgh, jeff.horsburgh@usu.edu, Utah State University 
- Martin Seul, mseul@cuahsi.org, CUAHSI
- Rob Crystal-Ornelas, rcrystalornelas@lbl.gov, Berkeley Lab
- Stevan Earl, stevan.earl@asu.edu, [CAP LTER](https://sustainability.asu.edu/caplter/)
- John Porter, jhp7e@virginia.edu, [VCR LTER](https://www.vcrlter.virginia.edu)
- Dominic J Bordelon
- Karen Payne
- Kathe Todd-Brown, ktoddbrown@ufl.edu, Univ of Florida
- Mark Schildahuer
- Meghan Eyler, meghan_eyler@fws.gov, USFWS
- Steve Aulenbach, saulenbach@usgs.gov, USGS
- Terri Velliquette

## DataONE [Object Format Vocabulary](https://github.com/DataONEorg/community-calls/issues/1)


### Agenda

- Introducing DataONE Community calls (Budden)
    - Call for community call ideas
- Object Format Registry Discussion
    - Background and overview (Jones)
    - LTER Network member use cases and needs (Porter)
    - Discussion and Q&A

### Notes
- Introducing DataONE Community Calls
    - Details
        - Held monthly, on the first Thursday of each month
        - Alternates monthly between 1700 and 2400 UTC to support global engagement
        - Calls last one hour with approximately 15 minutes for presentation and 45 minutes for discussion

    - Resources
        - Community Call [webpage](https://www.dataone.org/community-calls/)
        - Community Call [repo](https://github.com/DataONEorg/community-calls)
        - Community call [topics (GitHub issues)](https://github.com/DataONEorg/community-calls/issues)



### Object Format Registry Discussion
- Overview by Matt Jones. 
    - DataONE publish own object formats vocab, allowing for level of granularity to allow differentiation of different formats. Variants of EML, FGDF, other standards. Underlying XML, can access through API. Each format has an ID, name, type. Extensible when there is a need.
    - [DataONE format list](https://cn.dataone.org/cn/v2/formats)
    - Conversation on how to make it more open. Moving to GitHub as primary mechanism for sharing. 
    - [Object Formats GitHub repo](https://github.com/DataONEorg/object-formats)
- John Porter: LTER
    - [Slides](https://docs.google.com/presentation/d/1rwQ1iqUL1ttlgRTIZ5mVAJZZjOWPz7Z2mYDAYQ1Wsns/edit#slide=id.p)
    - Went through all LTER documents and looked at the format type.
### Questions and Comments:
- KB: Is there a benefit of separating version information from the format names as a free-standing metadata element?
    - Only if that had a practical impact on the way it is being used. Made a choise to have each version be its own stand alone version type. They're not currently linked (other than by shared family name)
- SE: Do you know how widely the resource is currently being adopted?
    - All objects in DataONE use the format identifier
    - Many repos don't register the different types of data
    - There's a lot of power in having people adopt a common vocabulary. Its been a part of DataONE from the onset but we hadn't previously exposed it as part of the services offered.
- MJ: We currently have a proposal format for how we might extent the vocabulary. Do people see using this? 
    - KB: Seems the proposal process is a reasonable one - tracking, information to feed in
    - JH: I think the GitHub process seems a good way to quickly build it out. Advocate for giving terms URIs and GitHub may not be the best way for that. As long as there's good definition in GitHub of how to build those out it will be useful.
    - MJ: URIs are a sticking point. Started with MIME types and stuck with it. Lots of text csv. Didn't want to reinvent a new term URI for formats that already have a URI. What is the canonical URI for text csv. As a community, who is the authority for these things?
- JP: The issue of the nesting part is potentially a problem. If you can nest once, you can end up nesting a lot of time. e.g. Zip+shape file. Zip>zip>shape...
    - The mime standard provides a mechanism through mime subtypes. We've been focussing on things that are commonly zip as standardized formats (registered as a mime type). e,g, ESRI .., KML files (uncompressed / compressed). Still a question of how to deal with mixed type containers. 
- DV: Format identifier and Mime type are two seperate items that define an object. Need to expand format ID structure a little bit. If we moved away from a single string what would we add in? Profile? e.g. serialized dublin core. 
    - SE: Is this one piece of a broader issue? Should we be looking this more wholistically? We can't be describing other components of the metadata at the zipped level.
    - MJ: lot of heterogeneity acrosss the metadata world, expressing the same concept in different ways. How do we span different communities of practice to increase interop without mandating change existing type descriptions?
- JH: resource model - composite resource is container of aggregations of other things. Aggs are types within a resources, each agg has a metadata file. Formats are identified in metadata files.
- MJ: Issues:
    - Need URI for formats
        - can probably add URIs without being too disruptive
        - MS: strong support for HTTP URIs for formats
    - Dealing with aggregated things




