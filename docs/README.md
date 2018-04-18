# medium-post-fragile-tests

## Description

This is example code which is a companion to the Medium article, [Zrah](https://lotsofwords.com/*zrah), that describes an automated system that:
- runs a suite of tests several times to reduce the effects of a fragile test system to find truly failing tests
- suppresses the failing tests
- creates a new commit and Github pull request that silences the failing test

## Setting up

[Fork](https://github.com/lyndsey-ferguson/medium-post-fragile-tests#fork-destination-box) this repo and run the following commands from a directory where you store your repos:
```sh
    git clone git@github.com:REPLACE-WITH-YOUR-GITHUB-USERNAME/medium-post-fragile-tests.git
    cd medium-post-fragile-tests
    git remote add lyndsey git@github.com:lyndsey-ferguson/medium-post-fragile-tests.git
    gem install bundler
    bundle install
```

Create a new Github token [here](https://github.com/settings/tokens) and save it as `~/.github-token`.

Run the sample code from the Terminal in this cloned repo:
```
    bundle exec fastlane sweep
```

Observe as the tests run with one consistently failing test. The `fastlane` `sweep` lane will run the tests 3 times, suppress the truly failing tests, make a new commit, and issue a pull request against the main repo.

Use this code sample to add improved logic to your build and test system. Feel free to ask questions or make comments in the Medium post or add Issues to this repo.

Thanks for reading and I hope that you enjoyed it!