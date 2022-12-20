---
layout: default
title: General Microproject Information
---

## Introduction

It is strongly recommended that people who want to apply to the Git
project for the Google Summer of Code (GSoC), Outreachy, or other such
mentoring programs, called "applicants" in this document, submit a
small code-related patch to the Git project as part of their
application.

People who want to get involved in Git development outside mentoring
programs can also benefit from information on this page to get
started, though it might be a bit less relevant to them. If they want,
they can use something like "[FirstTimer]", "[Newbie]", "[Newcomer]"
instead of "[GSoC]" or "[Outreachy]" in the emails they send.

Think of these microprojects as the "Hello, world" of getting involved
with the Git project; the coding aspect of the change can be almost
trivial, but to make the change the applicant has to become familiar
with many of the practical aspects of working on the Git project.

Git development is based on sending successive versions of patches or
patch series to the mailing list until they are considered good and
correct by the reviewers and Junio Hamano, the maintainer, who will
merge them. This process usually takes quite some time. By sending
drafts of your microproject patches to the mailing list long before
the deadline, you can show us that you are willing and able to work
well using the Git development process.

It is *expected* that what you send will need several rounds of
reviews and discussions. If you are not sure at all about a patch you
can put "[GSoC][RFC/PATCH]" or "[Outreachy][RFC/PATCH]", depending on
the mentoring program you are applying for, at the beginning of its
subject.

Consider [a sample email thread](http://public-inbox.org/git/1386590745-4412-1-git-send-email-t.gummerer@gmail.com/T/#u),
which shows how a developer proposed a change and a patch to implement
it. The problem being solved, the design of the proposed solution,
and the implementation of that design were all reviewed and discussed,
and after several iterations an improved version of the patch was
accepted into our codebase. As a GSoC contributor, or Outreachy intern,
you will be playing the role of the developer and engaging in a
similar discussion. Get familar with the flow, need for clarity on
both sides (i.e. you need to clearly defend your design, and need to
ask for clarifications when questions/suggestions you are offered are
not clear enough), the pace at which the discussion takes place, and
the general tone of the discussion, to learn what is expected of you.

To complete a microproject, you will have to go through approximately
the following steps:

* Download the source code: clone the repository using the
  [Git via Git](http://git-scm.com/downloads) instructions and read
  the `README` file.

* Build the source code: this is described in the file `INSTALL`.

* Glance over our coding guidelines in the file
  `Documentation/CodingGuidelines`. We take things like proper code
  formatting very seriously.

* Read about the process for submitting patches to Git: this is
  described in `Documentation/SubmittingPatches`. A more detailed
  step-by-step guide could be found in [`Documentation/MyFirstContribution.txt`](https://git-scm.com/docs/MyFirstContribution).

* The "[Hacking Git](https://git.github.io/Hacking-Git/)" page
  could also serve as a handy resource. It points to resources
  on various topics related to working on Git.

* Select a microproject and check that it has not yet been taken or
  discussed by searching the mailing list.
  [Public Inbox](http://public-inbox.org/git/) is your friend.

* Send an email to the mailing list where you describe the
  microproject you want to work on, the way you want to do it, and
  maybe talk a bit about yourself. Make sure the email you send has a
  subject that starts with "[GSoC]" or "[Outreachy]".

* **Make the actual change.** (Funny, this is the only part they teach
  you about in college.)

* Run the test suite and make sure it passes 100%: this is described
  in the file `t/README`.  (If you have added new functionality, you
  should also add new tests, but most microprojects will not add new
  functionality.)

* Commit your change. Surprise: we use Git for that, so you will need
  to gain at least
  [a basic familiarity](http://git-scm.com/documentation) with using
  Git. Make sure to write a good commit message that explains the
  reason for the change and any ramifications. You can find information
  on writing a good commit message in the
  ["Describe your changes well" section of the `SubmittingPatches` document](https://git-scm.com/docs/SubmittingPatches#describe-changes).
  Remember to make sure
  that you agree with our "Developer's Certificate of Origin" (whose
  text is contained in `Documentation/SubmittingPatches`), and to
  signify your agreement by adding a `Signed-off-by` line.

* *Optional, but recommended:*
  With an account at GitHub, you can use GitHub CI to test your changes
  on Linux, Mac and Windows. See
  [examples](https://github.com/git/git/actions/workflows/main.yml)
  of recent CI runs.

  To run these tests against your own branch,
  [create a fork](https://help.github.com/articles/fork-a-repo/)
  of [Git](https://github.com/git/git) on GitHub and switch to it. At the
  top bar select [Actions tab](https://github.com/git/git/actions)
  and perform the initial setup to enable it for your fork. After enabling it,
  CI will run for a specific branch of your fork whenever you push new changes
  to it in GitHub. You can monitor the test state of all your branches in the
  same [Actions tab](https://github.com/git/git/actions) of your fork.

  If a branch did not pass all test cases then it is marked with a red cross. In
  that case you can click on the failing job and navigate to
  "ci/run-build-and-tests.sh" and/or \
  "ci/print-test-failures.sh". You can also
  download "Artifacts" which are tarred (or zipped) archives with test data
  relevant for debugging. Fix the problem and push your fix to your GitHub fork.
  This will trigger a new CI build. Ensure all tests pass.

* Submit your change to the Git mailing list. For this step you
  probably want to use the commands `git format-patch` and `git
  send-email`. Make sure that your email is formatted correctly: send
  a test version of the email to yourself and see if you can apply it
  to your repository using `git am`. Alternatively you may use
  [GitGitGadget](https://gitgitgadget.github.io/) or
  [submitGit](https://submitgit.herokuapp.com/).

  When you submit your patch, please mention that you plan to apply
  for the GSoC or Outreachy. You can use "[GSoC][PATCH ...]" or
  "[Outreachy][PATCH ...]" in the subject of the emails you send for
  that purpose. This will ensure that we take special care not to
  overlook your application among the large pile of others.

* Expect feedback, criticism, suggestions, etc. from the mailing list.

  *Respond to it!* and follow up with improved versions of your
  change.  Even for a trivial patch you shouldn't be surprised if it
  takes two or more iterations before your patch is accepted.  *This
  is the best part of participating in the Git community; it is your
  chance to get personalized instruction from very experienced peers!*

The coding part of the microproject should be very small (say, 10-30
minutes). We don't require that your patch be accepted into the
"master" branch by the time of your formal application; we mostly want
to see that you have a basic level of competence and especially the
ability to interact with the other Git developers.

## Only ONE quality focused microproject per applicant

Applicants please attempt only **ONE** microproject. We want quality,
not quantity! (Also, it takes work to collect the ideas, and it would
be nice to have enough microprojects for everybody.)

This means that for a microproject that consists in refactoring or
rewriting a small amount of code, your patch should change only
**ONE** file, or perhaps 2 files if they are closely related, like
"foo.c" and "foo.h".

If you change a test file, the title of your patch (after the
"[GSoC][PATCH ...]" or "[Outreachy][PATCH ...]" part) should start
with "tXXXX: " where tXXXX is the start of the filename of the test
script you change. If you change "foo.c" or "foo.h", the title of your
patch should probably start with "foo: ".

In general it's a good idea to check on the mailing list archive what
other GSoC or Outreachy applicants attempting a microproject have
already been told this year or any previous year, as hopefully it will
help you avoid some mistakes. As some microproject ideas haven't
changed for years, some similar microprojects might have been
attempted many times already and you can learn a lot from these
attempts.

The more you research your microproject and take advantage of that,
the more confident we can be that you will be able to solve many
problems when working on your real GSoC or Outreachy project. So it's
a very good thing to show that you have researched your microproject
and taken into account what you have found.

If you've already done a microproject and are itching to do more, then
get involved in other ways, like finding and fixing other problems in
the code, or improving the documentation or code comments, or helping
to review other people's patches on the mailing list, or answering
questions on the mailing list or in IRC, or writing new tests, etc.,
etc. In short, start doing things that other Git developers do!
Alternatively you can of course focus on your project proposal.

## How to find other ideas for microprojects

First check the specific page(s) or information about Git
microprojects related to your program that should have been published
on this site or on the GSoC or Outreachy site. But then still read on
everything below!

Any small code-related change would be suitable. Just remember to keep
the change small! It is much better for you to finish a small but
complete change than to try something too ambitious and not get it
done.

Though we don't require that your patch be accepted into the "master"
branch by the time of your formal application, we still expect that a
good number of iterations between discussions and improvements has
happened. Don't be surprised if we reject your application after you
send something out of the blue just before the deadline, even if what
you did is very significant and/or of high quality!

If you don't like for some reason the microprojects that are proposed
related to your program, or if you just want more choice, you may find
other ideas for microprojects by searching the mailing list
(<https://public-inbox.org/git/>) or the code base itself. In the code
base you could search the code itself or the tests (in the "t"
directory).

When you find something you are interested to work on, please ask
first on the mailing list if it's worth doing and if it's appropriate
for a microproject before starting to work on what you find. Even if
it looks straightforward, there could be hidden reasons why it is too
difficult or just inappropriate.

You can also always send an email to the mailing list to ask if people
have other microproject ideas, but before that please check that
someone participating in the same program as you has not already done
that recently.

### Searching for bug reports

Git has no official bug tracker or bug list. On
<https://git-scm.com/community> we recommend that people report bugs
directly on the Git mailing list.

On the mailing list people sending bug reports are likely to use
things like "[BUG]", "bug", "issue" or "crash" in the subject of their
emails. So it can be a good idea to search for that.

Most bugs are usually fixed soon after they are reported or are well
known behaviors or limitations though. So don't expect too much.

[GitGitGadget](https://gitgitgadget.github.io/), which can be used to
send patches from a GitHub repository to the Git mailing list, has its
own list of Git issues on:

<https://github.com/gitgitgadget/git/issues>

There are even a couple ideas marked as #leftoverbits, i.e. curated
and copied from the Git mailing list see:

<https://github.com/gitgitgadget/git/issues?q=is%3Aissue+is%3Aopen+label%3Aleftoverbits>

And there are a couple of project ideas marked as "good first issue":

<https://github.com/gitgitgadget/git/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22>

that might be interesting to look at.

There is another non official bug tracker dedicated to Git issues on:

<https://crbug.com/git>

Git for Windows also has it's own issue tracker:

<https://github.com/git-for-windows/git/issues>

But of course the Git for Windows issues might not apply to Git
itself. Please check that before talking about them on the Git mailing
list.

In general it's a very good idea to check that you can reproduce the
bug on the latest version of Git before working on it.

### Searching for #leftoverbits in the mailing list

People have recently started to add "#leftoverbits" to their emails
when they think further small work on the topic could be useful.

You can easily search that using:

<https://public-inbox.org/git/?q=leftoverbits>

But don't forget to search to check if what you find has already been
addressed. If it has not been addressed, please ask first on the
mailing list if it's a good idea to work on that.

### Searching the code base itself

Your best bet is probably to search for strings like "FIXME", "TODO",
"NEEDSWORK", or maybe "NEED-WORK", and "BUG" (though not the "BUG()"
macro).

You can also search (`git grep` is your friend) for common patterns in
the code and try to find or create a function to refactor them.

### Searching the tests

Tests are in the "t" directory and can be run by launching "make" in
this directory. Doing that you will see that there are a number of
tests that are marked with "# TODO known breakage", like for example:

"not ok 28 - git checkout -f: replace submodule with a directory must fail # TODO known breakage

These tests start with "test_expect_failure" instead of
"test_expect_success". They document that something is not working as
it should perhaps be working. And it might be an interesting
microproject to fix that.

Note that it is especially wise to first search the mailing list and
then ask on the list before working on one of these
"test_expect_failure", because if we bothered to document a failure
but not fix it, that is often because the fix is non-trivial.

You could also check if some commands have no test for some of their
options and it could be an interesting microproject to add a test for
one of those options.

### Searching the mailing list for other ideas

You can search the mailing list for words like "low hanging fruit", or
"low-hanging fruits", "hint, hint", "later", "we should", "I plan
to"...

## How to introduce yourself to the community

It's likely that you will introduce yourself to the community around
the same time you are going to start working on a micro-project.

We don't require you to send us a special introductory email or to
tell us about your skills, interests, experience, background,
etc. Feel free to tell us what you want about yourself if you wish
though.

But please, make it clear that you are interested in a specific
mentoring program and use the right tag, like [GSoC], [Outreachy], etc
at the beginning of the subject of your emails.

As we usually don't know your interests, skills, experience,
background, etc, it's hard for us to select a micro-project for
you, and it's part of your job as an applicant to research a good
micro-project for you. It will show us that you will be able to
select a good project for you and properly research it.

You can ask for help if there are things you don't understand in a
micro-project description, or if you have some trouble working on your
micro-project or even finding a micro-project. But please be very
specific in your questions and tell us in detail what you searched or
tried, what you expected and what didn't work as you
expected. Something like "I couldn't find a good micro-project for
me", for example, doesn't tell us much, and doesn't give us any idea
about how we could help you.

## Some conventions and tips

It can be intimidating to introduce yourself or send your first patch
to the mailing list, but we hope that the following conventions and
tips will help you get properly started.

### Start your own email thread

When you introduce yourself to the Git mailing list, please start your
own email thread instead of replying to a thread where someone else
introduced themself, or worse a completely unrelated thread.

### Use a tag, like [GSoC], [Outreachy], etc, in your subject

Yeah, we insist on this because many applicants don't do it despite
the fact that it helps everyone, especially themselves.

It helps because efficiently searching the mailing list is not so
easy. Having such a tag at the start in the subject makes it much
easier to find what applicants or contributors from a program have
done. And applicants should be very interested in searching for what
other applicants or contributors participating in GSoC or Outreachy
have been doing in the past, for example what kind of microproject
they have chosen, how their proposal looked like, etc.

### Reply inline

Many people these days use the "top posting" posting style, but we
usually reply inline instead, which is also called the "interleaved
posting" posting style. See
https://en.wikipedia.org/wiki/Posting_style for more information about
these styles.

So please don't just reply on top of the email you are replying
to. Instead, just expand the email you are replying to and put your
comments in it.

### Put ALL the co-mentors in To: or Cc:

When emailing about something related to your program (GSoC or
Outreachy or ...) and when you know who are your possible
(co-)mentors, put them all in To: or Cc:. If you email or reply and
forget to put one of your (possible) co-mentors in the loop, it can
only create confusion or additional useless synchronization work for
your mentors and ultimately make it harder for them to help you.

If you have something personal to say to only one of your mentors,
it's Ok to not put others in To: or Cc:, but otherwise, please, make
it a habit to put them all in the loop when you contact them.

Tip: just use "Reply-all" when you reply to an email.

### Don't be formal

We are used to not using titles, like "Sir", "Mr", etc, and not being
formal. Yeah, it can be difficult, as in some areas or countries,
people are supposed to be formal with mentors, professors or people
older or more experienced than themself. But please try to be as
informal as us.

### Tell us your first name or how you want to be called

Most people on the mailing list like to call each other and to be
called using their first name, or sometimes a nickname. So that's how
we would like to call you. So let us know your firstname or how you
want to be called.

Yeah, sometimes it seems obvious, but sometimes it's really not, as
for example in some countries people commonly have 4 different names,
in others they usually mention their first name after their last name
(instead of before), in yet others, first names are usually
abbreviated in non obvious ways, etc.

So please make it clear.

### Tell us the pronouns we should use

Again, yeah, it's often obvious, but often it's not. So please tell us
if we should use "He/him/his", "She/her/her(s)", "They/them/their(s)",
or another pronoun to talk about you.

### Confirm that you pass the requirements

Programs like Outreachy or GSoC usually have requirements for
applicants. Sometimes applicants have to be accepted by the program
after they have shown they satisfy the requirements.

In any case it's interesting for us to know soon how you currently
stand regarding the requirements and maybe the acceptance process.

### Tell us what steps you have already taken

We can better help you and suggest the next steps for you to take if
we know what steps you have already taken.

So if you have read this documentation, tell us. If you have already
started or finished a Git tutorial, tell us too. If you have only
built Git from source, tell us. If you have already sent patches on
the Git mailing list to improve Git, tell us.

We don't need to know about the computer science knowledge or C or
shell language programming experience you have, but telling us where
you are regarding developing Git is definitively helpful.
