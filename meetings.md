# Jenkins Cloud Native SIG Meetings

:::info
## Quick links

* [Logistics](#Logistics)
* [Meeting Recordings](https://www.youtube.com/playlist?list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG)
* Jenkins Roadmap: https://www.jenkins.io/project/roadmap/
* [Agenda and Notes](#Agenda-and-Notes)
    * [2021-04-9 Meeting](#April-09-2021)
    * [2021-04-2 Meeting](#April-02-2021)
    * [2021-03-5 Meeting](#March-05-2021)
    * [2021-02-26 Meeting](#February-26-2021)
    * [2021-02-12 Meeting](#February-12-2021)
    * [2021-02-5 Meeting](#February-5-2021)
    * [2021-01-29 Meeting](#January-27-2021)
    * [2021-01-22 Meeting](#January-22-2021)
    * [2021-01-15 Meeting](#January-15-2021)
   

## Logistics

* **Meeting notes on HackMD.io**: https://hackmd.io/@cdf-sig-interoperability/ry3TTB5DL
* **When**: Fridays at 12:00UTC (*See your timezone [here](https://time.is/1200_in_UTC)*).
* **Zoom Meeting Link**: https://zoom.us/j/91266012072?pwd=OWJZSGVuY2s3aHhHbitPVnIwNDBIUT09
* **Meeting Recordings**: [Jenkins Cloud Native Playlist](https://www.youtube.com/playlist?list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG)
* **Jenkins Events Calendar**: [here](https://www.jenkins.io/events/)
* **2020 Meeting Minutes**: [Google doc containing minutes of meetings in 2020](https://docs.google.com/document/d/13zeaKgtud5jZ5RqZEh1lrwjDXJRm7j31scPymlrMpfo/edit#heading=h.jlsdrmbt2n8j)

## Agenda and Notes

Meeting agenda and notes are kept on [HackMD.io](https://hackmd.io/7uB6FuEqQAOp_-blPGykzA) where everyone can add new topics to the agenda for upcoming meetings or take notes during the meetings. Please click edit button to edit the document.

If you are looking for 2020 minutes of meetings, please take a look at [2020 Meeting Minutes document](https://docs.google.com/document/d/13zeaKgtud5jZ5RqZEh1lrwjDXJRm7j31scPymlrMpfo/edit#heading=h.jlsdrmbt2n8j), which is a Google doc containing past meeting minutes.

:::

### April 9, 2021

#### Participants
* Kara de la Marck
* Gareth Evans
* Sagar Khurana
* <GSoC mentees>
* <add your name>

#### Agenda and Notes

* Announcement: Jenkins Contributor Summit on 25 June 2021, https://www.jenkins.io/events/contributor-summit/
    * Free registration
    * Draft Agenda is here: https://docs.google.com/document/d/1JVbWudREipEF5UJn-bBRU5QIjKf8mzFP9iFdwWbgFB0/edit?pli=1#heading=h.quu0wh66oy0i
    * Great opportunity to speak about the work we are doing in Cloud Native SIG
        * Demos welcome :)

* Tekton Client Plugin update
* GSoC updates - as related to Cloud Native initiatives
* Questions from GSoC applicants
    * Discussion on: https://www.jenkins.io/projects/gsoc/2021/project-ideas/semantic-release-version/
    * https://github.com/jenkinsci/jep/blob/master/jep/229/README.adoc

    
* Discuss: https://tech.ebayinc.com/engineering/how-ebay-leverages-kubernetes-helm-charts-and-jenkins-pipelines-to-deliver-high-quality-software/ references plans to leverage Tekton in their Pipelines. Now with Jenkins, so it is a good opportunity for the Tekton Client plugin.

### April 2, 2021

#### Meeting cancelled this week due to holidays around the globe.

### March 19, 2021

#### Participants
* Kara de la Marck
* Vibhav Bobade
* Gareth Evans
* Sagar Khurana
* <add your name>

#### Agenda and Notes

* GSoC mentor invitations to the Continuous Delivery Foundation GSoC mentor org have been sent out -- please check your spam folder as there is a tendency this year for gmail to filter the emails to spam 😂
* Tekton Client Plugin release discussion
* Gareth: have started work 
* Vibhav: what would be the criteria for a release? Anything else wanted in the first release?
* Gareth: the goal of a first realease will be the ability to try it out and test it on non-production pipelines
    * at moment doesn't need to be a 'complete' first release => the point of this release is to be able to test out the plug-in
    * see JEP 229: https://github.com/jenkinsci/jep/blob/master/jep/229/README.adoc
* Vibhav: script: https://github.com/jenkinsci/tekton-client-plugin/blob/master/deploy.sh

* Gareth: https://github.com/jenkinsci/tekton-client-plugin/pull/64
The log-cli plugin implements basic aspects of this proposal from the developer side.

repository-permissions-updater #1747 and repository-permissions-updater #1779 implement changes to infrastructure.

plugin-pom #375 and pom #147 add a POM profile to block MRP in CD mode.

The verify-ci-status Action and the jenkins-maven-cd Action implement most of the logic of the CD process.

* Vibhav: lets run a meetup this month on this plugin


#### Action Items
* Cloud config for tekton client plugin (Vibhav)
* TaskRun async logging (Vibhav)
* Kara to liase with Mark and Oleg on existing Jenkins meetups and if a meetup on this plugin fits with existing schedule or do an additional meetup


### March 12, 2021

#### Participants
* Kara de la Marck
* Gareth Evans
* Mauricio Salatino
* Vibhav Bobade
* Sagar Khurana
* <add your name>

#### Agenda and Notes
* Welcome and thanks to Mauricio for joining us.
    * Mauricio has volunteered as a mentor on the [proposed GSoC CloudEvents plugin for Jenkins project](https://www.jenkins.io/projects/gsoc/2021/project-ideas/cloudevents-plugin/).
    * Mauricio brings a deep interest and expertise as an active member in the [CDF's Event SIG](https://github.com/cdfoundation/sig-events)
    * You can find out more about the Event SIG, its goals, and how to get involved in this post: ['CD Foundation Announces Industry Initiative to Standardize Events from CI/CD Systems'](https://cd.foundation/blog/2021/03/16/cd-foundation-announces-industry-initiative-to-standardize-events-from-ci-cd-systems/)

[pretty much a transcript below, but it was a good discussion. :)]
* Vibhav discuss CloudEvents plugin
    * Overview: 
        Goals are to be able to listen on cloudevents, trigger Jenkins jobs on cloudevents, be able to emit cloudevents for Jenkins jobs and other events created by Jenkins, and have them in the cloudevents format.
    * Plugin: https://github.com/cloudevents/sdk-java/blob/master/examples/basic-http/src/main/java/io/cloudevents/examples/http/basic/BasicHttpServer.java
    * Question on cloudevent subscription and discovery, has this been standardized? 
* Mauricio:
    * Subscription and discovery of cloudevents is work that is getting started.
    * And subsciption and discovery likely is an extension of the scope of this GSoC project.
    * The cloudevents plugin will be a plugin that will emit events when you run this plugin inside Jenkins and also an endpoint that will be exposed to enable the submission of cloudevent notifications to Jenkins itself. These 2 concepts are what the initial scope of the work should be.
    * 'Emiting events' that's usally submitting a post request to url. Once that is provided then can hook that 'thing' to other tools that are going to be able to deal with forwarding cloudevents to other systems, etc.
    * The initial plugin work is pretty well scoped.
    * One outstanding question is the format of the events themselves. This is work that the CDF Events SIG is focused on right now. And also, what events do you emit (standardizing on that).
    * For this plugin we should avoid emitting Jenkins specific events, because if Jenkins specific events are emitted then this can limit interoperability and might limit the usefulness of this plugin to the Jenkins ecosystem.
        * The plugin should avoid emiting Jenkins specific events
    * But if event standard events, then can interop with other tools. And that is what we are trying to acieve in the CDF.
    * How to get started on this plugin work?
        * Start by experimenting with plugin for Jenkins that emits cloudevents. And exposing an endpoint that consumes cloudevents coming from other systems.
        * And then can start focusing on the format of the cloudevents themselves. Start with simple cloud event with minimal data, making sure can emit the events at right times.
        * Then figure out what info is available within the jobs and what can/should be included in the events
        * Need to establish the identifiers for the events you determine should be emitted. Then details become a little more tricky. So best first to see a plugin that can emit and consume events, then we can go into the details of the data.

* Vibhav
    * In [design doc for Cloudevents plugin proposal](https://docs.google.com/document/d/1vJ06K92-2wumfAUAiUEwwx921iR19v4zu7nHPkScrvk/edit#heading=h.txtc8k4mxium), Vibhav has created a table of cloudevents based on the Tekton cloudevents.
    * When Mauricio mentioned the importance of being generic with cloudevents and steering away from emitting Jenkins specific cloudevents, how do we ensure this?
* Mauricio
    * Good! In CDF we are defining generic events for exactly this same reason. If emit Jenkins specific events, other tools (eg, Tekton) will not be able to understand them. So what we are doing is creating essentially a shared language between these tools so they can exchange event data and react based on differnt events.
    * But don't need to focus too much on that right now. If we get a basic plugin created (described above) then we can focus on the data format and event definitions. Goal right now is to be able to emit cloudevents and listen for events.
* Vibahv: one of the goals of this plugin is interoperability between different tools, so wants to ensure from the beginning we have the goal of supporting generic cloudevents.
    * Does Mauricio have an example of what a generic cloudevent would look like?
* Mauricio: Yes. [CDF SIG](https://github.com/cdfoundation/sig-events) PRs have some examples.
    * Note, 'Job' is more of a Jenkins concept, and likely we'll use a phrase like 'step'. So, some of the concepts and how those are labelled needs to be more generic, but the concept, and the way of emitting events, is the same.
    * One of the things we can do in this project is create/define the Java objects that are going to represent the generic events.
    * To clarify: Very likely that Java objects will be created inside the plugin and then we are going to use the [cloudevents sdk in Java](https://github.com/cloudevents/sdk-java/blob/master/examples/basic-http/src/main/java/io/cloudevents/examples/http/basic/BasicHttpServer.java) to emit the events.
    * So, instead of creating the Java objects inside the plugin, we can create a separate library that includes the events definition and then we can plug in the generic ones.
* Vibhav: [Have created a repo](https://github.com/jenkinsci/cloudevents-plugin) to get started on the work.
* Mauricio: Some of the work on creating these definitions of events will be mapping cloudevents to Jenkins events. And when receiving cloudevent notifications, what does the Jenkins plugin do in response. We'll need to think about which kind of events to support and which are not.
* Vibhav: So when a cloudevent is 'received' we should be able to put an cloudevent trigger on a Job which is listening on a specific cloudevent. eg, listening on a Tekton Task completion, and then the Job will be triggered once received.
* Question for Gareth: Where should main the configuration for all this kept? Do we keep all the information regarding what events we should listen on the global configuration or on the Jobs? Should it be global or localised per Job? 
* Gareth: You could do a global configuration for events. You may also want to do it on a Job trigger as well.
* Vibhav: on the Job trigger, we could reference that to the global plugin configuration and choose from there. 
    * The global plugin configuration is more of an admin thing, allowing certain cloudevents to get into the system, reading certain cloudevents, allowing certain projects to listen on certain cloudevents. Am I overthinking the security aspects of this? Would per Job be more secure? 
* Gareth: I can see there being a use in the future on the ability to filter out events of a certain type. For example, if you've got a bad actor in the system that is sending invalid events, etc.
* Kara: if you wanted to control which events were going to be emitted, you could write a policy for that.
    * Gareth: yes
* Kara: Then once events are emitted they are put in some sort of queue and can you put permissions on who has access to that information?
* Mauricio: Yes, but that should be outside of Jenkins. Later we can write more complex components that deal with that, but I wouldn't start with that.
    * Kara: yes, and then additional question on data formats for events.
* Mauricio: Work in proress, PRs are up for a first go at defining the vocabulary.  From there will work on definition of cloudevents using that vocabularly, so at least the metadata of events should be there. From there we can start to create a Java model for events.
    * Also, has done a draft implementation in Go.
* Mauricio: That's one reason why for plugin work, we should focus on first implementation of emitting and receiving events and then move forward from there in terms of determining the exact data format for events.
* Vibhav: Yes. That sounds like a good place to start.
* Mauricio: Eventually, we may want the plugin to be able to emit both Jenkins specific and generic CDF definited cloudevents and then in configuration can decide which events get emitted.
* Vibhav: The Go library that Mauricio has created - we could use that to debug a cloudevents listener.
* Mauricio: yes. In addition, there is the [sockeye.io](https://github.com/n3wscott/sockeye) project that you can use as a sink for events and you can graphically see the events that are arriving.
* Vibhav: yes, very nice for debugging.
* Mauricio: Can we get a Jenkins instance in the cloud where we can put this plugin?
* Vibhav: can spin up Jenkins in minikube, while testing the plugin. 
* Mauricio: running it locally is fine for now. Eventually, would be nice for CloudBees to provide some cloud resources, if we want to connect different tools, etc.
* Kara: when we get to the point where we need that, I can ask.
* all: Thank you, Mauricio for joining today. Awesome discussion :) 
* Sagar: Question on using java cloudevents sdk example to emit cloud events.

#### Meeting Recording
https://www.youtube.com/watch?v=o9aPtZkMyd8&list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG&index=11


### March 5, 2021

#### Participants
* Kara de la Marck
* Gareth Evans
* <add your name>


#### Agenda and Notes
* Add Support for Tekton Catalog to Tekton Client Plugin: https://github.com/jenkinsci/tekton-client-plugin/pull/58
    * Woohoo! 
    * How does this impact potential GSoC student projects?
    * https://github.com/jenkinsci/tekton-client-plugin/blob/master/roadmap.md
    * Gareth: as a PoC James contribution is spot-on.
    * Gareth: James has created a PR on enhancements proposals for Tekton (see James twitter)
    * 
* Dina Graves Portman will present the 4 Key Framework to the Interoperability SIG on 18 March.
    * Link to her presentation and demo at cdCon, Measuring DevOps: https://www.youtube.com/watch?v=rbenCqQCa-4&feature=youtu.be
* CDF Events SIG is now on!
    * https://github.com/cdfoundation/sig-events
    * Meetings are open, meeting info on the above link
    * Excellent reference and resource for our work. 
* [Design Doc: DSL in Tekton Client Plugin](https://docs.google.com/document/d/10n3vgYrjS_M1571OUOYLw4tK2QmxY7kp_wyUT3ke4gY/edit#heading=h.txtc8k4mxium)
    * https://www.jenkins.io/projects/gsoc/2021/project-ideas/tekton-client-plugin/
* In latest Interoperability SIG meeting, we had a presentation of [Project "Piper"](https://www.project-piper.io/) by Oliver Nocon, from SAP
    * Recording: https://www.youtube.com/watch?v=LbdMG0O4m6Y
    * The goal of project "Piper" is to substantially ease setting up continuous delivery in your project using SAP technologies.
    * Most of their pipelines (pipeline templates use Jenkins)
    * Oliver Nocon discussed their need for a DSL such as that of Jenkins X 2.0 DSL (which has now been deprecated, with the Jenkins X project using Tekton syntax)
    

### February 26, 2021

#### Participants
* Kara de la Marck
* Gareth Evans


#### Agenda and Notes
* Announcement: Dina Graves Portman will present the 4 Key Framework to the Interoperability SIG on 18 March.
    * Link to her presentation and demo at cdCon, Measuring DevOps: https://www.youtube.com/watch?v=rbenCqQCa-4&feature=youtu.be
* Also, really interesting discussion/work on defining Events here: https://github.com/cdfoundation/sig-interoperability/pull/64

### February 12, 2021

#### Participants
* Kara de la Marck
* Gareth Evans
* Bartek Antoniak
* Vibhav Bobade
* Sagar Khurana


#### Agenda and Notes
* Bartek to present on history of Jenkins Kubernetes Operator.
* Kara: We welcome GSoC project ideas (final deadline rapidly approaching!) and mentors are welcome to add their name to potentially mentor on project ideas that interest them: https://www.jenkins.io/projects/gsoc/2021/project-ideas/
    * More infor on proposing a Jenkins GSoC project idea: https://www.jenkins.io/blog/2020/12/16/call-for-mentors/
    * Note that this year's GSoC requires less of a time commitment from students: students will be focused on a 175-hour project over a 10-week coding period.
    * Project ideas should be similarly reduced in scope (from previous years) to be appropriate for work undertaken during the new GSoC timeline.
* Sagar shared https://www.youtube.com/watch?v=STKCRSUsyP0 as a resource for understanding Event Driven Architecture.
* Vibhav: Tekton as Code exploratory work -- found it relatively straight forward.
* Outline Tekton Client Plugin aims


#### Action Items
* All: Review and provide feedback on GSOC Tekton Client Plugin  https://docs.google.com/document/d/1_mS0gLgM7oz7PanE0X_SkJ8iUo-BPVCixXMSDO7-VMk/edit#heading=h.vn4ec3wsbisx
 
#### Meeting Recording
* https://www.youtube.com/watch?v=AknUZ0KV_xg&list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG&index=11

### February 5, 2021

#### Participants
* Kara de la Marck
* Gareth Evans
* Bartek Antoniak
* Tracy Miranda
* Vibhav Bobade
* Sagar Khurana
#### Agenda and Notes
* Action Item Review, All
* Jenkins Kubernetes Operator:Open Governance, Trademarks, planning of the next steps
https://groups.google.com/g/jenkinsci-dev/c/OA5nb_SAgh0/m/GrbA8r63BQAJ 
* Cloud Native SIG to help develop technical roadmap for Jenkins K8s Operator

#### Action Items
* Kara to find out information on becoming Jenkins Sub-Project. Understand Jenkins Enhancement Proposal, work with Jenkins Governance Board.
* Bartek will kick off email thread within Jenkins Community on becoming Sub-project - email thread can be found at https://groups.google.com/g/jenkinsci-dev/c/m1epwoehhls/m/vh5_Gku4AwAJ
* Kara: find clear path for Jenkins Kubernetes Operator to participate in GSoC 2021, as it would be a fantastic project. And Virtus Labs likely can commit mentors. 
* Bartek willing to present again on history of Jenkins Kubernetes Operator.



#### Meeting Recording
- [Jenkins Operator Growth Plan Presentation](https://docs.google.com/presentation/d/1Yee66aYmL6A6u-6USUd1UwAorKxPbJLdSOoqQR0zgR0/edit?usp=sharing)

### January 29, 2021

#### Participants
* Kara de la Marck
* Gareth Evans 
* Vibhav Bobade
* Sagar Khurana
* Danilo


#### Agenda and Notes
* Action Item Review, All
* Open items from previous meeting:
* CloudEvents metadata 
CloudEvents SDK -- excellent to explore and use to understand CloudEvents better. 
    * Do not need K8s knowledge to get started with this. GSoC students interested in CloudEvents plugin proposal, may find this a good initial step to understanding the proposed project.
    * Need to find endpoints that can be subscribed to. Related to consuming endpoints.
    * How would we consume CloudEvents => convert to Jenkins metadata?
    * Gareth: initially could be a webhook handler that we post CloudEvents to.
Plugins out there that have similar functionality -- good to look into (see Vibhav action item below)
* First prototype to understand how CloudEvents work, from producer point of view: 
create (poc) global plugin configuration for Jenkins
* Github-autostatus-plugin-- reports events for stage changes/promotions: https://github.com/jenkinsci/github-autostatus-plugin
    * Gareth: would be interesting to consider how it is listening to the Jenkins internals
* Figure out extent to which to bootstrap the CloudEvents plugin project for GSoC students: Possibly need to bootstrap the global plugin configuration. 

#### Action Items
* All: [GSOC Tekton Client Plugin](https://docs.google.com/document/d/1_mS0gLgM7oz7PanE0X_SkJ8iUo-BPVCixXMSDO7-VMk/edit#heading=h.vn4ec3wsbisx)  -- read over, review, give feedback
* Vibhav: Metadata table 
* Vibhav: Look at generic-webhook-trigger for understanding basis for consuming cloudevents
* Vibhav: Github-autostatus-plugin
* Create doc for Cloudevents Metadata Table for Jenkins
* Research on Tekton-asa-code:  https://github.com/chmouel/tekton-asa-code
    * How would this work with Tekton Client Plugin. May want to research and look at Lighthouse and how it is implemented. 


#### Meeting Recording
* https://www.youtube.com/watch?v=wqoqJLYBqYM&list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG&index=10

### January 22, 2021

#### Participants
* Kara de la Marck
* Gareth Evans 
* Vibhav Bobade


#### Agenda and Notes
* Action Item Review, All
* [CDF calendar of events, for meetings on Interoperability and CloudEvents:](https://calendar.google.com/calendar/u/0/embed?src=linuxfoundation.org_mhf0kmgedn67ihni8r129avp24@group.calendar.google.com&ctz=America/Los_Angeles)
* GSoC 2021 Cloud Native Events proposal by Vibhav https://github.com/jenkins-infra/jenkins.io/pull/4079
    * Metadata for CloudEvents for Jenkins -- how to define, what should the metadata contain.  
    * Vibhav: following metadata that is being generated and defined for Tekton is a start.
    * We should make a table on what the metadata looks like. Action item for Vibhav 
* GSoC 2021 Tekton Client Plugin potential  proposal by Vibhav
    * PoC is done
    * A lot that students can do, especially with the GSoC timeline that we now hald (1.5 months rather than 3).
    * Work that needs to be done fits well within the current timeline
    * Vibhav: will create draft to share within gsoc email channel and gitter.
    * Gareth: potential integration between Tekton as Code and Tekton Client plugin.
    * Tekton as Code: https://github.com/chmouel/tekton-asa-code 
Being bootstrapped at Red Hat, will likely be merged into Tekton. Uses Tekton dashboard to visualise Tekton tasks.
    * Related Tekton issue: https://github.com/tektoncd/pipeline/issues/859

#### Action Items
* Research needed on what CloudEvents metadata should contain. 
* Figure out user stories around CloudEvents: what CloudEvents can do. 
* Play with CloudEvents SDK
* Find endpoints that can be subscribed to. 
* First prototype to understand how CloudEvents work.
* Vibah: figure out extent to which to bootstrap the project for GSoC students.
* Vibhav: will create draft on Tekton Client Plugin to share within gsoc email channel and gitter.
* Would be great if the Jameses could attend to discuss Tekton Client Plugin and Tekton as Code, as they have done similar work in Jenkins X.


#### Meeting Recording
* https://www.youtube.com/watch?v=Ezy-Quj4L5Q&list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG&index=9

### January 15, 2021

#### Participants
* Kara de la Marck
* Gareth Evans 
* Vibhav Bobade


#### Agenda and Notes
* Action Item Review, All
* New time for SIG:
    * 2 hours earlier, Friday still works
* Tekton Client Plugin, Status update
    * https://github.com/jenkinsci/tekton-client-plugin/blob/master/roadmap.md
    * Possibility to make this into a GSoC project, to have greater support in moving roadmap forward.
    * Tekton catalogue support is a goal.
    * Gareth interested in having Jenkins support Tekton
    * Vibhav will create GSoC draft proposal and submit to jenkins gsoc mailing list.
    * GSoC proposal for Cloudevents plugin: https://docs.google.com/document/d/1xsI6nkEPzXId5npXLrjz3Ydj7jx9Rf8g7SWnTldpeQc/edit#heading=h.vn4ec3wsbisx

#### Action Items
* Vibhav will create GSoC draft proposal and submit to jenkins gsoc mailing list.
* Kara will propose moving this meeting 2 hours earlier

#### Meeting Recording
* https://www.youtube.com/watch?v=9w9EuUn2zdk&list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG&index=8
