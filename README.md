# Tock management reports

A couple of scripts I use to monitor Tock data.

## Usage

For a given date, use `run.py` with a `YYYY-MM-DD` date. For example:

```sh
python run.py 2016-10-23
```

To check an individual, use `check_user.py` with a `YYYY-MM-DD` date and a username. For example:

```sh
python check_user.py 2016-10-23 vladlen.zvenyach
```

## Docker Usage

The easiest way to use the script is to use Docker.

First, make sure to copy the `.env.example` file into `.env`. Then, use is as simple as:

``` sh
docker-compose run app python run.py <date>
```

## Installation

If you are not using Docker, you'll need to use some sort of strategy to export the environment variables in `.env.` I use [autoenv](https://github.com/kennethreitz/autoenv). Then:

``` sh
git clone https://github.com/18F/tock-management-reports.git
cd tock-management-reports
cp .env.example .env
python -m venv env
source env/bin/activate
pip install -r requirements.txt
```

### Public domain

This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
