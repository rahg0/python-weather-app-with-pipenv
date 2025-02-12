# python-weather-app-with-pipenv

## Installation
- Clone the repo:
```sh
$ git clone https://github.com/rahg0/python-weather-app-with-pipenv.git
$ cd python-weather-app-with-pipenv
```

- Install `Pipenv` tool (if not present already):
```sh
/python-weather-app-with-pipenv$ pip install pipenv
```

- Install all the dependency packages locked in `Pipefile.lock` file:
```sh
/python-weather-app-with-pipenv$ pipenv install 
```

- Activate this project's virtualenv:
```sh
/python-weather-app-with-pipenv$ pipenv shell 
```

- Create an [OpenWeather](https://openweathermap.org/) account and generate an API Key.

- Assign the API Key for **api_key** in `app.py` file. 

- Run the application:
```sh
(python-weather-app-with-pipenv) /python-weather-app-with-pipenv$ python app.py
Enter the city name: bengaluru
Weather in Bengaluru:
Temperature: 30.6°C
Condition: Broken clouds
```

## Scan for Security Issues
```sh
(python-weather-app-with-pipenv) /python-weather-app-with-pipenv$ orca-cli fs scan ./
✓ Performing file system scanning for security risks
✓ Performing results analysis and policy decision (via Orca Cloud)
========================================================================
VULNERABILITIES
pipenv (./Pipfile.lock)
[TOTAL: 8 | CRITICAL: 2 | HIGH: 3 | MEDIUM: 3 | LOW: 0 | UNKNOWN: 0]
╭──────────┬──────────────────┬───────────────────┬───────────────┬──────────┬───────┬───────┬────────╮
│ PACKAGE  │ VULNERABILITY ID │ INSTALLED VERSION │ FIXED VERSION │ SEVERITY │ CVSS2 │ CVSS3 │ STATUS │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ agpt     │ CVE-2024-6091    │ 0.2.2             │               │ CRITICAL │       │ 9.8   │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ gradio   │ CVE-2025-23042   │ 5.10.0            │ 5.11.0        │ CRITICAL │       │       │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ flask    │ CVE-2023-30861   │ 1.0.2             │ 2.3.2, 2.2.5  │ HIGH     │       │ 7.5   │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ waitress │ CVE-2022-24761   │ 2.0.0             │ 2.1.1         │ HIGH     │ 5     │ 7.5   │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ waitress │ CVE-2024-49769   │ 2.0.0             │ 3.0.1         │ HIGH     │       │ 7.5   │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ requests │ CVE-2023-32681   │ 2.26.0            │ 2.31.0        │ MEDIUM   │       │ 6.1   │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ requests │ CVE-2024-35195   │ 2.26.0            │ 2.32.0        │ MEDIUM   │       │ 5.6   │ FAILED │
├──────────┼──────────────────┼───────────────────┼───────────────┼──────────┼───────┼───────┼────────┤
│ waitress │ CVE-2024-49768   │ 2.0.0             │ 3.0.1         │ MEDIUM   │       │ 4.8   │ FAILED │
╰──────────┴──────────────────┴───────────────────┴───────────────┴──────────┴───────┴───────┴────────╯
```
