# Improving Testing Through Operability

[![license](https://img.shields.io/github/license/:user/:repo.svg)](LICENSE)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

## Background

Reliability, handling failure gracefully and recovering quickly are becoming increasingly important as the software development world adopts DevOps culture and practices. Outages and security failures are big news and many companies are investing heavily to avoid these challenges. Operable systems are easy to deploy and test, provide actionable information about their state and behave more predictably in adverse conditions. 

Testers on development teams are often used to testing changes to the functionality of an application but less so testing how operable a system is. My recent experience has seen testers on teams charged with improving operability for systems through better logging, monitoring and system control measures (such as feature flags) to emit better information. This information on system stability and state is critical to testing and we can influence its creation profoundly.   

### Why it is important for testers

* As the operability of systems becomes a greater focus, testers need to be equipped with models to think about how to add value in this context.
* As testers, we strive to add value and testing for reliability enables us to use our risk analysis skills to explore for failures and how to recover.
* If we get involved with helping our system to emit better information from an operability standpoint, testability through observability and control will likely be enhanced.
* Rather than having shallow status checks, testers can contribute to meaningful monitoring of customer journeys and how reliability and recovery are measured.

### Takeaways

* Recognise the key terminology pertaining to logging, monitoring and system control measures and their role in operability. 
* Understand how to test systems for the quality of operational information that they emit and how this can help improve information gained through testing.
* Apply the understanding of operational insights to testing deployment pipelines and operational hooks to enhance overall operability.

### Table of Contents

- [Background](#background)
- [Usage](#usage)
- [API](#api)
- [Contributing](#contributing)
- [License](#license)

## Usage

This repo is to gather together resources and exercises for operability testing and enhancing testing through operability.

## Contributing

PRs accepted.

## License

[MIT © Ash Winter.](./LICENSE)
