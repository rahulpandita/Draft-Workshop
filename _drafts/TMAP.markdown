---
layout: post
title:  "API Mapping using Text Mining"
date:   2015-09-21 10:44:00
categories: paper presentation
---

Our work on inferring likely method mappings across APIs was accepted in [SCAM 2015]{http://www.ieee-scam.org/2015/}. 

#### Abstract

>Developers often release different versions of their applications to support various platform/programming-language application programming interfaces (APIs). To migrate an application written using one API (source) to another API (target), a developer must know how the methods in the source API map to the methods in the target API. Given a typical platform or language exposes a large number of API methods, manually writing API mappings is prohibitively resource-intensive and may be error prone. Recently, researchers proposed to automate the mapping process by mining API mappings from existing codebases. However, these approaches require as input a manually ported (or at least functionally similar) code across source and target APIs. To address the shortcoming, this paper proposes TMAP: Text Mining based approach to discover likely API mappings using the similarity in the textual description of the source and target API documents. To evaluate our approach, we used TMAP to discover API mappings for 15 classes across: 1) Java and C# API, and 2) Java ME and Android API. We compared the discovered mappings with state-of-the-art source code analysis based approaches: Rosetta and StaMiner. Our results indicate that TMAP on average found relevant mappings for 57% more methods compared to previous approaches. Furthermore, our results also indicate that TMAP on average found exact mappings for 6.5 more methods per class with a maximum of 21 additional exact mappings for a single class as compared to previous approaches.


Sithu presented the work at the venue. Here is link to the presentation slides.

