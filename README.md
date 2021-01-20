# testitorgmgnt-infra


## Purpose

This is an IaC project setup to manage an organization accouunt
and its members accounts using [org-formation][1] and [sceptre][2]

## Deployments


### org-formation

Deploy resources to management and all member accounts

* install [nodejs][3]
* cd org-formation
* npx org-formation print-tasks --profile management-profile --verbose --print-stack organization-tasks.yaml

### sceptre

Deploy resources to all member accounts

* install [lerna][4]
* cd sceptre
* npx lerna run deploy --stream

We use lerna to recursively execute deployment `scripts` (in package.json files) in all sub directories.

[1]: https://github.com/org-formation/org-formation-cli
[2]: https://github.com/Sceptre/sceptre
[3]: https://nodejs.org/en/download/package-manager/
[4]: https://lerna.js.org/
