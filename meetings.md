# Jenkins Cloud Native SIG Meetings

:::info
## Quick links

* [Logistics](#Logistics)
* [Meeting Recordings](https://www.youtube.com/playlist?list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG)
* Jenkins Roadmap: https://www.jenkins.io/project/roadmap/
* [Agenda and Notes](#Agenda-and-Notes)
    * [2021-02-12 Meeting](#February-12-2021)
    * [2021-02-05 Meeting](#February-5-2021)
    * [2021-02-26 Meeting](#February-26-2021)
   

## Logistics

* **Meeting notes on HackMD.io**: https://hackmd.io/@cdf-sig-interoperability/ry3TTB5DL
* **When**: Fridays at 14:00UTC (*See your timezone [here](https://time.is/1400_in_UTC)*).
* **Zoom Meeting Link**: https://zoom.us/j/91266012072?pwd=OWJZSGVuY2s3aHhHbitPVnIwNDBIUT09
* **Meeting Recordings**: [Jenkins Cloud Native Playlist](https://www.youtube.com/playlist?list=PLN7ajX_VdyaOFG9hTrswbO-ZK_n4B8CaG)
* **Jenkins Events Calendar**: [here](https://www.jenkins.io/events/)
* **2020 Meeting Minutes**: [Google doc containing minutes of meetings in 2020](https://docs.google.com/document/d/13zeaKgtud5jZ5RqZEh1lrwjDXJRm7j31scPymlrMpfo/edit#heading=h.jlsdrmbt2n8j)

## Agenda and Notes

Meeting agenda and notes are kept on [HackMD.io](https://hackmd.io/7uB6FuEqQAOp_-blPGykzA) where everyone can add new topics to the agenda for upcoming meetings or take notes during the meetings. Please click edit button to edit the document.

If you are looking for 2020 minutes of meetings, please take a look at [2020 Meeting Minutes document](https://docs.google.com/document/d/13zeaKgtud5jZ5RqZEh1lrwjDXJRm7j31scPymlrMpfo/edit#heading=h.jlsdrmbt2n8j), which is a Google doc containing past meeting minutes.

:::

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
* 


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
* 

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
CloudEvents metadata 
CloudEvents SDK -- excellent to explore and use to understand CloudEvents better. Do not need K8s knowledge to get started with this. GSoC students interested in CloudEvents plugin proposal, may find this a good initial step to understanding the proposed project.
Need to find endpoints that can be subscribed to. Related to consuming endpoints.
How would we consume CloudEvents => convert to Jenkins metadata?
Gareth: initially could be a webhook handler that we post CloudEvents to.
Plugins out there that have similar functionality -- good to look into (see Vibhav action item below)

First prototype to understand how CloudEvents work, from producer point of view: 
create (poc) global plugin configuration for Jenkins

Github-autostatus-plugin-- reports events for stage changes/promotions: https://github.com/jenkinsci/github-autostatus-plugin
Gareth: would be interesting to consider how it is listening to the Jenkins internals

Figure out extent to which to bootstrap the CloudEvents plugin project for GSoC students:
 Possibly need to bootstrap the global plugin configuration. 

[GSOC Tekton Client Plugin](https://docs.google.com/document/d/1_mS0gLgM7oz7PanE0X_SkJ8iUo-BPVCixXMSDO7-VMk/edit#heading=h.vn4ec3wsbisx)  -- read over, review, give feedback
		
Action items:
Vibhav: Metadata table 
Vibhav: Look at generic-webhook-trigger for understanding basis for consuming cloudevents
Vibhav: Github-autostatus-plugin
Create doc for Cloudevents Metadata Table for Jenkins
Research on Tekton-asa-code:  https://github.com/chmouel/tekton-asa-code
How would this work with Tekton Client Plugin. May want to research and look at Lighthouse and how it is implemented. 




#### Action Items


#### Meeting Recording