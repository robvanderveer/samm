Agile notes explain to the SAMM reader how topic specifically works for agile. They also provide best practices and pitfalls.

Rob van der Veer and Michael Kuipers agreed with the SAMM group that they would start adding agile notes to SAMM’s core model.  Just to imagine how they would work:  in the 2.0 core PDF, these notes could for example be presented in rectangles marked ‘Agile note’ and then contain the note text. That way they are not part of the method-agnostic core text but at the same time they provide information that can easily be found or skipped.

There are three main reasons for these agile notes:
1. They correct for any misinterpretation by sensitive agile-minded readers who tend to think that the model is ‘too much waterfall’. This is mainly a language thing.
2. They provide specifics on how the activity is (slightly) different for agile, on the same detail level as the core model
3. They can provide more detail on how to implement activities in agile (for example how you make code reviews incremental)

# TODO
Link texts to identifiers in the core model using https://github.com/OWASP/samm/blob/master/v2.0/summit-201810-Minneapolis/SAMM1.5-SAMM2.0%20Mapping%20Minneapolis%20v20181014.xlsx  
# The notes
No particular order and all quick draft.
## General:
Agile is quick and quality assurance is traditionally bureaucratic and slower than you want for agile. The trick is to attain quality at speed. Security needs to be built in fluently. The key is to prevent and to fight mistakes with maximum efficiency, so to minimize manual work and the burden on developers.

Prevent:
-using solid technologies/frameworks/components that do part of the security
-clear requirements
-insight and understanding of security principles with all people involved 
-doable and therefore situational instructions for developers. No stacks of books but clear short lists based on what is needed for the specific task at hand
-good changeability of code (maintainability) to minimise errors
-everybody feels security responsibility, including the product owner

Fight:
-by checks that need to be automated as much as possible and the manual part needs to be performed in a smart incremental and risk-based way, focusing only on changes and their impact.

“Careful with red tape.
A maturity model seems conflicting with the agile manifesto, because Agile holds people over process and working software over documentation. Therefore, in an agile environment, it is important to take extra care for making the process and tracking maturity as lightweight as possible. Please note that agile does not disqualify process or documentation - it wants to minimise it where possible.”
## Topic: Strategy & Metrics
### “Team autonomy”
In most agile environments, team autonomy is important, which means that it can be a challenge to work on process maturity on an organisation-wide scale. If team-autonomy is important, than a maturity program should embrace that different teams can have different maturities. At the same time it is advisable to let teams learn from each other, so sharing of practices between teams is a best practice for maturity programs.”
### Responsibilities in agile
In some organisations, security is organised in such a way that the ‘security department’ verifies the software and then needs to convince the ‘business’ to fix the issues found. In an agile environment there is no time for this approach of ‘we will figure it out once we see what the issues are’ because you would need to do that every sprint. In agile, security needs to be owned by everyone including the product Owner - according to specified requirements. This puts security professionals much more in an advisory and supportive role than in a restricting role.

## Topic: Education & Guidance - Organisation&culture
### Comment
I’m not sure if it’s a good idea to have the security group ensure that developers are applying best practices. This would nurture an us vs them situation where the security group would be the security police. Instead, security should be everybody’s responsibility. My guess is that SAMM agrees to that standpoint, but it is not reflected in the text on the security group.
## Design-Threat assessment
### TODO: Something on incremental threat modelling based on new features
-Include a reference to Irene Michlin - incremental threat modeling

## Security requirements - A. Software requirements:
### “Iterative requirements”
Agile requirements are done iteratively. Typical waterfall development assumes all requirements can be defined upfront and changes are handled as exceptions. Agile, on the other hand, believes requirements are situational and situations change. Also, Agile believes customer requirements should not be trusted to be complete and correct. 

PITFALL: The key to agile security is to apply the right requirements at the right time. If this process fails, then Agile is focused too much on delivering functions, ignoring important non-functional requirements.

### “Classifying requirements assurance”
A functional security requirement (e.g. a login feature) has its own user story and a non-functional requirement needs to be ensured in another way. Per non-functional requirement, the following assurance classification can be made at the very start of development:
 -Not applicable in the context
 -Covered by the technology used (e.g. framework)
 -Needs to be included in general instructions and tested for
 -Needs to be included in instructions per story and tested for
During classification, the type of required test(s) can also be specified: automated static or dynamic test, peer code review, pentest.
Of course this classification can be revisited when necessary (e.g. testing has been extended, new framework choices).
### “Requirements in stories”
Stories need to be equipped with the relevant non-functional requirements, to be put in the acceptance criteria of the story, based on the type of work expected in the story. This informs developers what should be taken into account and it should lead to the required tests.
Equipping the stories is done during creation of the story and during backlog refinement. There are different ways to collect the criteria: using triggers, using abuse stories and/or using the help of an expert. 

PITFALL: Doing this during sprint planning is not recommended because all the time will be needed to plan.

PITFALL: In case the team works with the “conditions of satisfaction” these should not be used for security requirements because these are typically functional and also not in the definition of done because these are user story independent.
### “Triggers”
A list of triggers can help the team to find relevant instructions and criteria based on what is being build. Triggers are words or patterns that describe types of functionality or architecture that need specific sets of requirements. These requirements can then be put in acceptance criteria.
There are commercial and open source tools to support this process.
“Security Triggers”
The list of subjects can be created by the organisation, or by the team and improved when required. One way to review this is during a sprint retrospective. 
