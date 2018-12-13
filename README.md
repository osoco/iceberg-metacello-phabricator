# iceberg-metacello-phabricator

An Iceberg and Metacello repository to use our Phabricator's Git service.

## Use

To load the project from GitHub you can execute the following expression:

```
Metacello new
	repository: 'github://osoco/iceberg-metacello-phabricator/src';
	baseline: 'IcebergMCPhabricator';
	load
```

Once you have loaded this project in a Pharo image with Iceberg, a new `phabricator` prefix will be
available to use with Iceberg and Metacello.

The repository parameter to load a project from the Phabricator's Git service takes this form:

`phabricator://{projectName}:{version}/{subFolder}`

where:

- `{projectName}`: Name of the project.
- `{version}`: This parameter is optional (it will take master by default). It can be: the name of a branch, a tag like 'v1.2.0' or 'v1.x.x', or a the SHA of a commit
- `{subfolder}`: This parameter is optional in case the code is at the root of the project. It should point to the subfolder containing the code.

**Note that currently this repository is configured to use the internal OSOCO's repository.**

In the future we will release a more generalized version of the project to be used with any Phabricator server.