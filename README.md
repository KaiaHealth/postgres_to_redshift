# PostgresToRedshift

This gem copies data from postgres to redshift. It's especially useful to copy data from postgres to redshift in heroku.

[![Build Status](https://travis-ci.org/kitchensurfing/postgres_to_redshift.svg?branch=master)](https://travis-ci.org/kitchensurfing/postgres_to_redshift)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'postgres_to_redshift', git: 'git@github.com:KaiaHealth/postgres_to_redshift.git'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install postgres_to_redshift

## Usage

Set your source and target databases, as well as your s3 intermediary.

```bash
export DROP_TABLE_BEFORE_CREATE='true'
export POSTGRES_TO_REDSHIFT_EXCLUDE_TABLES='table1,table2'
export POSTGRES_TO_REDSHIFT_INCLUDE_TABLES='table2,table3'
export POSTGRES_TO_REDSHIFT_SOURCE_PASSWORD='source_password'
export POSTGRES_TO_REDSHIFT_SOURCE_URI='postgres://username:password@host:port/database-name'
export POSTGRES_TO_REDSHIFT_TARGET_PASSWORD='target_password'
export POSTGRES_TO_REDSHIFT_TARGET_SCHEMA='production'
export POSTGRES_TO_REDSHIFT_TARGET_URI='postgres://username:password@host:port/database-name'
export S3_DATABASE_EXPORT_BUCKET='some-bucket-to-use'
export S3_DATABASE_EXPORT_ID='yourid'
export S3_DATABASE_EXPORT_KEY='yourkey'

postgres_to_redshift
```
