# The Graph Tooling

Monorepo for various tools used by subgraph developers.

This repository houses the following tools:

<!-- prettier-ignore-start -->
| NPM | Name | 
| --- | --- | 
|[![npm (scoped)](https://img.shields.io/npm/v/@graphprotocol/graph-cli.svg?color=success)](https://www.npmjs.com/package/@graphprotocol/graph-cli)[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FYaroShkvorets%2Fgraph-tooling.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FYaroShkvorets%2Fgraph-tooling?ref=badge_shield)
| [`@graphprotocol/graph-cli`](./packages/cli) |
[![npm (scoped)](https://img.shields.io/npm/v/@graphprotocol/graph-ts.svg?color=success)](https://www.npmjs.com/package/@graphprotocol/graph-ts)|[`@graphprotocol/graph-ts`](./packages/ts)|

<!-- prettier-ignore-end -->

## Release process

We use `changeset` to manage releases. Every PR should include a changeset file. The release process
is as follows:

1. Author creates the PR with changes and runs `pnpm changeset` to create a changeset file to
   summarize the changes.
2. When the PR is merged to `main`, a Github Action will run and create a PR with the version bump
   and changelog.
3. We will merge the bot generated PR to `main`.
4. A Github Action will run and publish the new version to npm.

Helpful links:

- [Semver official docs](https://semver.org/)
- [Changesets](https://github.com/changesets/changesets)
- [Snapshot release](https://github.com/changesets/changesets/blob/main/docs/snapshot-releases.md)

### Stable release example

When PRs are merged and to `main` we can choose to merge the bot generated changeset PR to `main`
and it will publish a new version to npm.

Example of a `graph-client` release: https://github.com/graphprotocol/graph-client/pull/295

### Alpha release example

Every PR to `main` that includes a changeset file will create a new alpha version.

Example of `graph-client` snapshot release:
https://github.com/graphprotocol/graph-client/pull/178#issuecomment-1214822036

## License

Copyright &copy; 2018-2019 Graph Protocol, Inc. and contributors.

The Graph CLI is dual-licensed under the [MIT license](LICENSE-MIT) and the
[Apache License, Version 2.0](LICENSE-APACHE).

Unless required by applicable law or agreed to in writing, software distributed under the License is
distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either expressed or
implied. See the License for the specific language governing permissions and limitations under the
License.


[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FYaroShkvorets%2Fgraph-tooling.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FYaroShkvorets%2Fgraph-tooling?ref=badge_large)