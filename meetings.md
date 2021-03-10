# Jenkins Cloud Native SIG Meetings

:::info
## Quick links

* [Logistics](#Logistics)
* [Meeting Recordings](https://www.youtube.com/playlist?list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG)
* Jenkins Roadmap: https://www.jenkins.io/project/roadmap/
* [Agenda and Notes](#Agenda-and-Notes)
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
