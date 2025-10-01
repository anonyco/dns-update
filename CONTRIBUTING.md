# Contributing

## Rust Environment

First, its reccomended you develop dns-update on a Linux distro such as [Linux Mint](https://linuxmint.com/download.php). If you don't already have Linux, head to that link, follow the steps, and you'll have Linux Mint up and running on your computer in no time. MacOS is also a possible editing environment, although expect more issues and troubleshooting.

Second, install Rust and Cargo. Be sure to select the Nightly release of Cargo, which is required for the dev dependencies testing this project. (Note: dns-update can be used in other projects on Rust 2021 Stable; nightly is only reccomended for development of dns-update.)

```
wget -O- https://sh.rustup.rs | sh -s
```

Next, use the `tool` executable file in this repo to run all the right cargo commands. Namely, the most important command is:

```
./tool dev
```

* Notice: this runs `cargo fmt` if the tests succeed, which reformats all your changes to conform to standard Rust styling conventions, e.g. tabs are converted to spaces. Don't be alarmed: Rust's standard styling is enforced/required for contributions to this project.
* Notice: this also runs `cargo clippy` if the tests succeed, which has a tendency to yell all kinds of errors at you. Its important to distinguish rustc error messages about *invalid* Rust code versus Clippy warnings about *bad code*. (Do note that neither are tolerated in this project. Please resolve all warnings and errors before making any commit.)

Finally, after you make your changes, use git commands such as:

```
git add /src/lib.rs
git commit --signoff
```

* **IMPORTANT:** Do not commit any changes unless the project builds successfully! It's crucial to `git bisect` (used to find bugs) and `git rebase` (used to update old branches) that all commits ever committed must standalone and compile on their own.
* The `--signoff` adds `Signed-off-by: Your Real Name <your.email@email-server.com>` to the bottom of the commit, which is a best project and required for contributions to this project.
* Its highly reccomended you [setup gpg signing](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits) so that your commits on GitHub come across with big green checkmarks validating that the commits correspond to your GitHub account.
* As long as `./tool dev` doesn't give any warnings or errors, you're good to go!

## Code of Conduct

Please note we have a code of conduct, please follow it in all your interactions with the project.

## Licensing

This project is licensed under either of

 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option. By contributing to this project, you agree that your contributions will be licensed under the AGPL-3.0 license.

## Fiduciary Contributor License Agreement

Before making any contributions, all contributors are required to sign the Fiduciary Contributor License Agreement (FLA). The FLA is a legal agreement that assigns the copyright of contributions to a designated fiduciary, who manages these rights on behalf of the project. This arrangement ensures that the software remains free and open, even as contributors come and go.

Key points of the FLA:

- Ensures the software remains free and open source
- Protects the project from potential copyright issues
- Includes a reversion clause: if the fiduciary violates Free Software principles, rights revert to the original contributors

For more details about FLA, please refer to the [FLA FAQ](https://fsfe.org/activities/fla/fla.en.html).

## Pull Request Process

1. Ensure any install or build dependencies are removed before the end of the layer when doing a 
   build.
2. Update the README.md with details of changes to the interface, this includes new environment 
   variables, exposed ports, useful file locations and container parameters.
3. Increase the version numbers in any examples files and the README.md to the new version that this
   Pull Request would represent. The versioning scheme we use is [SemVer](http://semver.org/).
4. You may merge the Pull Request in once you have the sign-off of two other developers, or if you 
   do not have permission to do that, you may request the second reviewer to merge it for you.

## Code of Conduct

We as members, contributors, and leaders pledge to make participation in our community a harassment-free 
experience for everyone, regardless of age, body size, visible or invisible disability, ethnicity, sex 
characteristics, gender identity and expression, level of experience, education, socio-economic status, 
nationality, personal appearance, race, religion, or sexual identity and orientation.
We pledge to act and interact in ways that contribute to an open, welcoming, diverse, inclusive, 
and healthy community.

You can read the full Code of Conduct [here](https://github.com/stalwartlabs/.github/blob/main/CODE_OF_CONDUCT.md).
