Harry and Ginny are getting married! Yay

They've decided to use Github to coordinate their wedding plans, and are concurrently working on a seating arrangement. They've got most of the important people covered, but just need to fill in a few gaps...

Divide into pairs, one assumes the role of Ginny and one assumes the role of Harry.

1. Fork the repository REPO_LINK
2. Create one feature branch for each of you - call one Harry and one Ginny
3. Follow the steps below IN ORDER PLEASE:
 
 EXERCISE 1 - complete beginners
 
 LEARNING OBJECTIVES:
  - Create a feature branch
  - Collaborate on a feature branch
  - Switch between branch and master, merging between the two
  - Raise pull requests
  - Stash changes
  - Go back to earlier commit
  
  At first, work off the "Harry" branch together
	a. GINNY: You've been trying and trying to get Harry to speak to his aunt and uncle again, you realise they made his childhood difficult but they were afraid. 
	They care about him in their own unique way, otherwise they wouldn't have risked their lives to save his, so you add the following names to the "extended family" table:
		Vernon Dursley
		Petunia Dursley
		Dudley Dursley
	add then commit your changes with a message explaining yourself lovingly, then push to your feature branch
	b. HARRY: 
	Open the document on the same branch and add a couple of your friends that you'd forgotten last time to the "Mutual Friends" table:
		Cho Chang
		Seamus Finnigan
	DON'T ADD YET! Ginny has been making changes to the seating plan, and you don't want to overwrite her changes with yours or generally cause problems, so you try and make sure you have the latest version of the document first. 
	Pull down her changes to your local branch. If you have trouble, stash the changes you've made, merge, then unstash.
	Check the git log to see what she's done - look at her commit message and sigh deeply - you knew she'd do this eventually...
	Revert her changes by checking the git log and going back to the previous commit. She won't be happy, but there's really no need to invite the Dursleys.
	add then commit your changes with an appropriate message - remember your message shouldn't really explain what you've changed (you can see that by looking at the changes), rather it should be more *why* you've 
	done it to add context for the others.
	Push your changes to your branch, raise a pull request to get it merged into master.
	c. GINNY: Switch to master, pull down Harry's changes and merge to the "Ginny" feature branch to see what he's done.
	Open the document, boil up inside when you realise he's not only reverted your additions, but he had the nerve to invite his former love interest Cho Chang! In a fit of rage, delete her name off the list. 
	How dare he, you talked about this and agreed she wouldn't be there!
	add then commit your changes with a suitably angry message. 
	Push your changes to your branch, raise a pull request to get it merged into master.
	
 EXERCISE 2 - slightly more advanced
 
 LEARNING OBJECTIVES:
 - Resolve conflicts
 - Squashing commits
 - Change commit message
 - Undo local changes 
 - Delete feature branch 

	d. HARRY: You've forgotten one of your favourite professors!
	Pull Ginny's changes from master, merge into your feature branch, and then open the document. Add Filius Flitwick at position 38.
	Add, commit with the following message: 
	"Added Professor Flitwick"
	Do not raise pull request yet.
	e. GINNY: Great minds think alike - You've forgotten one of your favourite professors! open the document, add Pomona Sprout at position 38.
	Add, commit.
	g. GINNY: You realise Harry has spelt Neville's name wrong. Correct the surname to "Longbottom", and commit again.
	There's no point having two separate commits in the history - the spelling mistake is minor and shouldn't ever need to be rolled back by itself. Squash both commits with one commit message that demonstrates 
	the purpose of the change.
	Add, commit, raise pull request, get merged into master.
	h. HARRY: Realise that you've written a commit message that is not really adequate, go back and modify it to explain the reason for the change.
	Raise pull request to merge your change. Ginny got there before you though so you'll have to resolve conflicts first.
	i. GINNY: Pull and merge Harry's changes really late at night, accidentally fall asleep on your keyboard and wipe out the entire document. Your PC crashes and you lose everything (close document :) ) No need to panic though,
	simply restore from the branch.
	Invite yourself and the person you're working with to the wedding - choose which table you'd like to sit on :)
	Add, commit, pull request.
	j. BOTH: Delete your feature branch.