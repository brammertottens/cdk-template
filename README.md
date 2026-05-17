# cdk-template

Synthesized CloudFormation template used for deployment and infrastructure validation.

## Scan Target
- Primary scan file: `templates/cdkgoat.template.json`

## Update Procedure
```bash
cd /Users/bottens/git/cdkgoat
cdk synth

cp cdk.out/cdkgoat.template.json /Users/bottens/git/cdk-template/templates/cdkgoat.template.json

# Update README metadata as needed
cd /Users/bottens/git/cdk-template
git add templates/cdkgoat.template.json README.md
git commit -m "Update synthesized CloudFormation template"
git push
```

## Notes
- This repository intentionally excludes other `cdk.out` metadata files to minimize scan noise and diff churn.
- CI scanner configuration can be added later without restructuring this repository.
