# cdk-template

Snapshot-only repository for scanning a synthesized CloudFormation template generated from CDK source.

## Source
- Source repository:   - Local path:     -       /Users/bottens/git/cdkgoat
- Source commit SHA:   -     c6c0278a49083526c462c80d6ff95e32db83f6a8
- Synthesis command used in source repo:

```bash
cd /Users/bottens/git/cdkgoat
cdk synth
```

## Scan Target
- Primary scan file:   -         templates/cdkgoat.template.json

## Update Procedure
```bash
cd /Users/bottens/git/cdkgoat
cdk synth

cp cdk.out/cdkgoat.template.json /Users/bottens/git/cdk-template/templates/cdkgoat.template.json

# Update README source commit SHA
cd /Users/bottens/git/cdk-template
git add templates/cdkgoat.template.json README.md
git commit -m "Update CDK template snapshot"
```

## Notes
- This repository intentionally excludes other `cdk.out` metadata files to minimize scan noise and diff churn.
- CI scanner configuration can be added later without restructuring this repository.
