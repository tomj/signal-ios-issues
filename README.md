# A collection of suggestions to clean up the [Signal iOS repo](https://github.com/signalapp/Signal-iOS).

## Rationale
* I recently became a user of Signal, and wished to contribute to the project
* I noticed that there were a large number of issues in the backlog (400+)
* I am a clean freak when it comes to software projects - while simultaneously acknowledging that [real artists ship](https://www.folklore.org/StoryView.py?story=Real_Artists_Ship.txt)
* I have previously worked on large scale secure mobile applications and the one thing which helped to have the projects run efficiently was a commitment to organisation
* Considering the above I realised the project would benefit more from the contribution of backlog management and documentation rather than opening up a PR to move some scrolling logic off the main thread

## Areas of focus
### Backlog management (aka: get Signal-iOS from 400+ open issues to 0)
* Grab all of the issues and put them into a workable format (this ended up being [Airtable](https://airtable.com/shrMaRrnrQCzxoNs8))
* Classify all of the issues 
* Move the feature requests into a new repo/project/tracking system
* Create a pipeline or strategy to test bugs

### [Create strategy for creation of new issues](https://github.com/tomj/signal-ios-issues/issues/1)
* Right now there appears to be a bit of friction when adding a new issue to the upstream repo, in addition to the potential for issues to be created which should not be created in the first place (feature requests, e.g.).  Using the new GitHub [issue template feature](https://help.github.com/en/articles/about-issue-and-pull-request-templates#issue-templates) will likely reduce that somewhat

### Git repo hygiene
* At time of writing there are 229 unmerged and 119 merged git branches in the upstream repo.  At a minimum the merged release branches should have their merge commits tagged and then the branches deleted.  The unmerged branches should be triaged and deleted as necessary.  Clean repo's are much easier to work on as they reduce cognitive overhead when onboarding
* Create and institute basic branching strategy.  It would help if contributors of all flavors stuck to forking and then running PR's from their fork to the upstream as this would solve the merged/unmerged branch issue

### Contribution guidelines
* Right now there are limited guidelines on how contributions should be made.  Is Swift ok, or should contributors stick to Obj-C?  Is there a coding standard?  A linting template?  etc etc

### Specifications
* Currently when filing an issue the question is asked: "I am submitting a bug report for existing functionality that does not work as intended"
* The question then is then what _is_ the intended functionality of the Signal iOS app?  There are some specs in `Signal/test` however actually documenting the expected behaviour of the app would be extremely helpful in preventing redundant issues being filed, in addition to providing the basis for quality documentation for the app.

## This sounds great, how can I help?
* Raise an issue in this repo with your email address and I'll add you to the Airtable to help classify the outstanding tickets
* PR any adjustments to this README.md you think are warranted
* Create any issues you think should be created
