---
layout: post
title:  "Ontology for Java"
date:   2015-09-22 16:00:00
categories: Review
comments: true
---

*In object-oriented languages, an API usually includes a description of a set of class deﬁnitions, with a set of behaviors associated with those classes. A behavior is the set of rules for how an object, derived from that class, will act in a given circumstance. Although, API documents provide invaluable information regarding the legal usage of API, they are in natural language text. A human mind is trained to extract the knowledge from natural language text. However, it is not trivial for computers to do the same owing to the ambiguity of natural language text. Thus, there is a need for representing the knowledge in API documents in a machine understandable format. In this project we take the ﬁrst step towards documenting the knowledge API documents in machine understandable format. In particular, this project presents an methodology to write ontologies from API documents. We document our experience of writing ontologies for JAVA or C# .NET API.*

####INTRODUCTION

In object-oriented languages, an API usually includes a description of a set of class deﬁnitions, with a set of behaviors associated with those classes. A behavior is the set of rules for how an object, derived from that class, will act in a given circumstance. This abstract concept is associated with the real functionalities exposed, or made available, by the classes that are implemented in terms of class methods (or more generally by all its public components hence all public methods, but also possibly including any internal entity made public, like ﬁelds, constants, nested objects, enums...). The API in this case can be conceived as the totality of all the methods publicly exposed by the classes (usually called the class interface). This means that the API prescribes the methods by which one interacts with/handles the objects derived from the class deﬁnitions.

Although, API documents provide invaluable information regarding the legal usage of API, they are in natural language text. A human mind is trained to extract the knowledge from natural language text. However, it is not trivial for computers to do the same owing to the ambiguity of natural language text. Thus, there is a need for representing the knowledge in API documents in a machine understandable format. Recently ontologies have been shown to be an effective way of representing knowledge.

In computer science and information science, an ontology formally represents knowledge as a set of concepts within a domain, and the relationships between those concepts. It can be used to reason about the entities within that domain and may be used to describe the domain. In theory, an ontology is a “formal, explicit speciﬁcation of a shared conceptualisation”. An ontology renders shared vocabulary and taxonomy which models a domain with the deﬁnition of objects and/or concepts and their properties and relations.

In this project we take the ﬁrst step towards documenting the knowledge API documents in machine understandable format. In particular, this project presents an methodology to write ontologies from API documents. However, it is not trivial to write ontologies from API documents because of the disconnect between description logic and object oriented systems primarily related to completeness and satisﬁability. We document our experience in dealing with such situations and the measures taken to resolve such situations.

In summary, this paper makes the following contributions:

1. A methodology to write ontologies from API documents.
2. Ontologies for JAVA or C# .NET API
	
####APPLICATIONS

Automated program synthesis has far reaching implications. First, it holds potential for easing the task of a developer by taking care of program generation and allowing the developer to concentrate on design tasks. Second, synthesized programs would be correct by construction. Third, owing to mechanical nature of synthesis, the task of programming itself would be repeatable. Finally, such programs would be free from the errors introduced by developers owing to human factors involved.

Recently there has been some exciting work [1]–[10] in this direction. Srivastava et. al. [1]–[3], [8] addresses the problem by leveraging speciﬁcations in the form of pre/post conditions and invariants to achieve synthesis. There is also some work [5]–[7], [9], [10] in literature that addresses the problem of program synthesis by leveraging the state of the art constraint solving.

Sumit Gulwani describes program synthesis as “Program Synthesis is the task of discovering an executable program from user intent expressed in the form of some constraints.” Program synthesis is different from compilation as synthesis can accept a wide range of constraints (natural language, input out examples etc...), in contrast a compiler only accepts a structured program and performs syntax directed translations.

An ideal synthesis system would mimic a human in synthesizing program. For instance, consider a scenario where a developer has to write a method to add to numbers. Following are considerations that a developer generally addresses:

1. How the method accepts inputs? Are they method parameters or accepted as console input?
2. What is the nature of numbers? Is it integer, ﬂoat, double ...?
3. How the addition operation is actually achieved?Does it involve a method invocation or an arithmetic operator?
4. How is the output handled? Does the method return the output or does it display it on Console?

Some of the considerations are explicit developer choices. For instance, a developer explicitly chooses how the method accepts inputs and outputs. However, some considerations are bound to the target programming language. For instance, what is the support for representing numbers and what is the addition operator or the method call. These second set of concerns are usually resolved by reading the API documentation. Our ontologies can can be subjected to machine manipulation to assist in program synthesis.

####METHODOLOGY

For Example the type hierarchy of Integer API in Java is shown in Figure 1. It can be directly converted into the ontology as shown in Figure 2.


{% highlight java %}
java.lang.Object
	|-> java.lang.Number
		|-> java.lang.Integer
{% endhighlight %}
Figure 1. Type Hierarchy of `Integer` API in Java


{% highlight xml %}
<owl:Class rdf:ID="Number">
	<rdfs:subClassOf rdf:resourse="#Object" />
</owlClass>
<owl:Class rdf:ID="Integer">
	<rdfs:subClassOf rdf:resourse="#Number" />
</owlClass>
{% endhighlight %}
Figure 2. OWL equivalent of `Integer` API in Java



Open problem how do we model the methods within a Class.

####REFERENCES

1. S. Srivastava, S. Gulwani, and J. S. Foster, “From program veriﬁcation to program synthesis,” in Proc. 37th POPL,January 2010, pp. 313–326.
2. S. Gulwani, V. Korthikanti, and A. Tiwari , “Synthesizing geometry constructions,” in Proc. PLDI,2011.
4. S. Gulwani, S. Jha, A. Tiwari, and R. Venkatesan, “Synthesis of loop-free programs,” in Proc. PLDI, 2011.
5. S. Gulwani, “Automating string processing in spreadsheets using input-output examples,” in Proc. POPL, 2011.
6. S. Gulwani, S. Jha, A. Tiwari, and R. Venkatesan, “Spreadsheet table transformations from examples,” in Proc. PLDI,2011.
7. S. Jha, S. Gulwani, S. Seshia, and A. Tiwari, “Synthesizing switching logic for safety and dwell-time requirement,” in Proc. ICCPS, 2010.
8. S. Gulwani, S. Seshia, A. Tiwari, and S Jha , “Oracle-guided component-based program synthesis,”in Proc. ICSE, 2010.
9. S. Srivastava, S. Gulwani, S. Chaudhuri, and J. Foster, “Pathbased inductive synthesis for program inversion,” in Proc. PLDI, 2011.
10. S. Itzhaky, S. Gulwani, N. Immerman, and M. Sagiv, “Asimple inductive synthesis methodology and its applications,”in Proc. OOPSLA, 2010.
11. A. Taly, S. Gulwani, and A. Tiwari, “Synthesizing switching logic using constraint solving,” in Proc. VMCAI, 2009.