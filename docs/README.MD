# Hosting a Full-Stack Application

## Udagram

## Dependencies

```bash
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

## Infrastructure

s3 bucket: <http://udagram712.s3-website-us-east-1.amazonaws.com>
RDS host: database-1.cam7rgpjid44.us-east-1.rds.amazonaws.com
RDS PORT : 5432
Elastic Beanstalk: <http://udagram-env.eba-znuh8gun.us-east-1.elasticbeanstalk.com/>

## Environment Variables Set via Circleci

### APP

PORT  

### JWT

- JWT_SECRET

### Database (RDS)

- POSTGRES_HOST
- POSTGRES_USERNAME
- POSTGRES_DB
- POSTGRES_PASSWORD

### AWS

- AWS_SECRET_ACCESS_KEY
- AWS_ACCESS_KEY_ID
- AWS_REGION
- AWS_PROFILE  
- AWS_BUCKET
- URL

## Pipeline : Circleci

- Configure elastic beanstalk
- Setup aws-cli
- install node and checkout code
- Install Front-End Dependencies
- Install API Dependencies
- Front-End Build
- Build API
- deploy website to s3
- deploy server to elastic beanstalk

Check diagrams folder for more details about archticture and pipeline.
