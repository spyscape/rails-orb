# rails-orb

## development

Pushing a branch will trigger a workflow on CircleCI. This validates the orb
and publishes it under a temporary development tag.

For example the build https://circleci.com/gh/spyscape/rails-orb/43
Published the orb `spyscape/rails-orb@dev:master-816aee2a2dec49021dde9a451ee9a837738feba0`

This temporary tag can be used in the upstream projects while you're testing
the change works. Once you're happy with the change you can promote the tag to
a full version using:

```
circleci orb publish promote <orb> patch/minor/major
```

For example to promote the previous mentioned tag to the next patch version run:

```
circleci orb publish promote spyscape/rails-orb@dev:master-816aee2a2dec49021dde9a451ee9a837738feba0 patch
```
