# testproof

Status: proposal stage. Applied to the Research Software Catalyst Fund (Exploratory track); no code yet.

## What it is


When an agent writes both the code and the tests, a green test suite proves very little: the tests were written to match the code, so they pass by construction. testproof is an open-source command-line tool and GitHub Action that measures how much an agent-written test suite constrains the code it claims to test, by mutating the code and checking which tests notice, by cross-checking generated tests against property-based tests derived from the function signatures, and by recording, per commit, which tests an agent wrote, from what prompt, and what the tool found. It runs on Rust and Python projects first, since those cover most research software written with AI help today. At the end of five months there is a working tool under Apache-2.0, a GitHub Action anyone can add in one line, a CC BY report on 25 real open research repositories, and the dataset behind that report on Zenodo.


## Planned deliverables

- testproof CLI (Rust, Apache-2.0) plus a Python shim on PyPI
- A GitHub Action that posts one pull request comment with the mutation score and the tests that never fail
- A written guide (CC BY) for researchers without an RSE
- A report and dataset (CC BY) on 25 public research repositories, archived on Zenodo

License: Apache-2.0 (software), CC BY 4.0 (report, guide, dataset).

Maintainer: Matthew Busel, mattbusel@tensorust.com
