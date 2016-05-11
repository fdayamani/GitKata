### Harry and Ginny are getting married! Yay

They've decided to use Github to coordinate their wedding plans, and are concurrently working on a seating arrangement. They've got most of the important people covered, but just need to fill in a few gaps...

Divide into pairs, one assumes the role of Ginny and one assumes the role of Harry.

Fork the repository https://github.com/fdayamani/GitKata

Create one feature branch for each of you - call one Harry and one Ginny

## EXERCISE 1 - complete beginners

#### LEARNING OBJECTIVES:
* Create a feature branch
* Switch between branch and master, merging between the two
* Collaborate across branches
* Raise pull requests
* Stash changes
* Revert an earlier commit

#### Steps:
In your pairs, decide who will be Ginny and who will be Harry. Then follow the steps below __in order please__. Each person should be working off their own branch at each stage:

1. __GINNY__: You've been trying and trying to get Harry to speak to his aunt and uncle again, you realise they made his childhood difficult but they were afraid. They care about him in their own unique way, otherwise they wouldn't have risked their lives to save his. Switch to the Ginny branch and open GuestList.txt and add the following names to the "extended family" table: 

    * Vernon Dursley 
    * Petunia Dursley 
    * Dudley Dursley 

    add then commit your changes with a message explaining yourself lovingly, then push to your remote feature branch.
    _NB: The feature branch doesn't exist yet. Pushing will automatically create the branch for you, and push your changes_
    Create a pull request to merge to the master branch. This will be your fork.
2. __HARRY__: Switch to the Harry branch, open GuestList.txt and add a couple of your friends that you'd forgotten last time to the "Mutual Friends" table: 
    * Cho Chang 
    * Seamus Finnigan 
    
    Add, but **DON'T COMMIT YET!** Ginny has been making changes to the seating plan, and you don't want to overwrite her changes with yours or generally cause problems, so you try and make sure you have the latest version of the document first:
   * Pull down her changes and merge to your local branch. 
   * If you have trouble, stash the changes you've made, merge, then unstash. 
   * Check the git log to see what she's done - look at her commit message and sigh deeply - you knew she'd do this eventually... 
   * Revert her changes by checking the git log, finding the hash of her change, and reverting that commit. She won't be happy, but there's really no need to invite the Dursleys. 
   * Add then commit your changes with an appropriate message - remember your message shouldn't really explain _what_ you've changed (anyone can see that by simply looking at the changes), rather it should explain _why_ you've done it, to give other collaborators the context for the change. 
   * Push your changes to your remote branch (see NB above), raise a pull request to get it merged into master. 
3. __GINNY__: Let's see what Harry has been up to:
    * Switch to master, pull down Harry's changes and merge to the "Ginny" feature branch to see what he's done. 
    * Open GuestList.txt, boil up inside when you realise he's not only reverted your additions, but he had the nerve to invite his former love interest Cho Chang!
    * In a fit of rage, delete her name off the list. How dare he, you talked about this and agreed she wouldn't be there! 
    * Add then commit your changes with a suitably angry message. 
    * Push your changes to your branch, raise a pull request to get it merged into master.

## EXERCISE 2 - slightly more advanced

## LEARNING OBJECTIVES:

* Resolve conflicts
* Squashing commits
* Change commit message
* Undo local changes
* Delete feature branch

4. __HARRY__: _Switch to the Harry branch_. You've forgotten one of your favourite professors! It wouldn't do to have your wedding without the man who taught you Wingardium Leviosa...
    * Pull Ginny's changes from master, merge into your feature branch, and then open GuestList.txt. 
    * Add Filius Flitwick at position 38. Add, commit with the following message: "Added Professor Flitwick" 
    * _Do not push your changes or raise pull request yet._ 
5. __GINNY__: _Switch to the Ginny branch_. Great minds think alike - You've also forgotten one of your favourite professors! 
    * Open the document, 
    * add Pomona Sproouut (spelt exactly like that) at position 38. 
    * Add, commit. 
6. __GINNY__: You realise you've spelt Professor Sprout's surname wrong. 
    * Correct the surname to "Sprout", and commit again. 
    * There's no point having two separate commits in the history - the spelling mistake is minor and shouldn't ever need to be rolled back by itself. Squash both commits with one commit message that demonstrates the purpose of the change. 
    * Raise pull request, get it merged into master.
    _NB: by rebasing, you are effectively changing the git history, so in practice only proceed with caution! Here we are fine, as this file has not been used by anybody else yet so changing things won't have horrible results. In general, however, pause before rebasing and make sure it is the right course of action_
    * Check the git log to make sure that there's only one commit. 
7. __HARRY__: _Switch back to your branch._ Realise that you've written a commit message that is not really adequate - you've basically summarised WHAT you changed, rather than WHY you changed it. This is unnecessary, as mentioned before, since anyone just needs to look at the git history to figure out WHAT change was made.
    * Go back and modify it to better explain the reason for your change. 
    * Raise pull request to merge your change. Ginny got there before you though so you'll have to resolve conflicts first. 
8. __GINNY__: _Switch to the Ginny branch_ Disaster strikes!
    * Pull and merge Harry's changes really late at night, 
    * Accidentally fall asleep on your keyboard and delete all the text from the entire document (Delete everything in GuestList.txt). Your PC crashes and you lose everything (close document :) )! 
    * Don't panic though, simply restore the document from the branch. 
    * Invite yourself and the person you're working with to the wedding - choose which table you'd like to sit on :) 
    * Add, commit, push, pull request (you know the drill by now..). 
9. __BOTH__: Thankfully, this tedious part of your wedding planning is over, and now you can focus on way more enjoyable parts, like cake selection (plus all the free samples that come with it!). Delete your feature branch.
10. Raise a pull request to merge your fork back into the original master. It probably won't get accepted, no offence - this step is just for completeness :).
