---
title: Contributing to Linaro release Kernel for HiKey boards
permalink: /documentation/consumer/hikey/contribute/
---
# Contributing to Linaro release Kernel for HiKey boards

This page provides instructions for developers willing to contribute to the
Linaro release kernel for HiKey boards.

# How to contribute

The following mailing list has been created to contributions:

[HiKey-Kernel mailing list]

This is a public mailing open to any developer.

# General recommendations

* This mailing list is not a substitute for proper upstreaming. We are willing to accept patches against our release (e.g. generally that means against a stable/LTS branch), if the submitters are also willing to upstream their changes. We will not be maintaining orphaned patches forever.
* It is recommended to upstream your changes first into mainline kernel, and then send a backport for inclusion into our release branch. When sending backport patches, please use `git cherry-pick -x <commit>` to make sure that we keep a record about the upstream commit in the commit log.
* Patches should be sent to the mailing list, as inline patches.
* When we do kernel upgrade we might not carry external patches, and they will have to be sent and tested again, if they have not been upstreamed in between.
* The mailing list is for patches and code. Regular support will continue to be on the 96boards forum
* We expect all discussions to be held on the public mailing list and discourage private discussions over emails as much as possible.
* Of course any patches will be reviewed by the maintainers of the involved sub projects, and these developers are responsible to accept or refuse any contribution.
