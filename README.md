# Valheim game server on AWS

## CDK commands

- `cdk ls` list all stacks in the app
- `cdk synth` emits the synthesized CloudFormation template
- `cdk deploy` deploy this stack to your default AWS account/region
- `cdk diff` compare deployed stack with current state
- `cdk docs` open CDK documentation

## Deployment commands

- Activate virtual environment
  - `source .venv/bin/activate`
- Install requirements
  - `pip install -r requirements.txt`
  - `pip install -r requirements-dev.txt`
- Deploy infra using CDK
  - `make bootstrap`
  - `make synth | less`
  - `make deploy`
- While deploying the `ValheimAwsStack`, to upload files to S3
  - make sure the S3 bucket has been provisioned before running this
  - `make upload`

## venv commands

To manually create a virtualenv on MacOS and Linux:

```bash
python3 -m venv .venv
```

After the init process completes and the virtualenv is created, you can use the following
step to activate your virtualenv.

```bash
source .venv/bin/activate
```

If you are a Windows platform, you would activate the virtualenv like this:

```bash
% .venv\Scripts\activate.bat
```

Once the virtualenv is activated, you can install the required dependencies.

```bash
pip install -r requirements.txt
```
