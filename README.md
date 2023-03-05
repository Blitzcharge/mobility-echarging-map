# webcomp-mobility-echarging-map

This project contains the map web component for the Green Mobility project.

[![CI/CD](https://github.com/noi-techpark/webcomp-mobility-echarging-map/actions/workflows/main.yml/badge.svg)](https://github.com/noi-techpark/webcomp-mobility-echarging-map/actions/workflows/main.yml)

[Green Mobility South Tyrol](https://www.greenmobility.bz.it/it/) wants to split the existing functionalities of the website into reusable and independent components. Using these webcomponents, a developer can easily integrate the functionality of the single components into any website.
The data source for the components is the [Open Data Hub](https://opendatahub.bz.it/) project.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [webcomp-mobility-echarging-map](#webcomp-mobility-echarging-map)
  - [Usage](#usage)
    - [Options](#options)
      - [Translations](#translations)
      - [Logo](#logo)
    - [Styling](#styling)
  - [Getting started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Source code](#source-code)
    - [Dependencies](#dependencies)
    - [Build](#build)
  - [Deployment](#deployment)
  - [Docker environment](#docker-environment)
    - [Installation](#installation)
    - [Dependenices](#dependenices)
    - [Start and stop the containers](#start-and-stop-the-containers)
    - [Running commands inside the container](#running-commands-inside-the-container)
  - [Information](#information)
    - [Support](#support)
    - [Contributing](#contributing)
    - [Documentation](#documentation)
    - [Boilerplate](#boilerplate)
    - [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Usage

Include the Javascript file `dist/map_widget.min.js` in your HTML and define the web component like this:

```html
<e-mobility-map-widget></e-mobility-map-widget>
```

### Options

#### Translations

Add `language` as attribute, if you want to translate the web component.

```html
<e-mobility-dashboard-widget language="en"></e-mobility-dashboard-widget>
```

Possible values are currently `en`, `de`, `it`, `nl`, `cs`, `pl`, `fr`, `ru` (see [/src/translations.js](/src/translations.js)).

#### Logo

URL of an icon, that will be shown in the lower left corner.

```html
<e-mobility-map-widget logo="https://www.example.com/your-logo.png"></e-mobility-map-widget>
```

### Styling

This web component has only one style variable, namely
`--e-mobility-widget-map-height`, which sets the height of the widget.

For example:
```html
<style>
  e-mobility-map-widget.YOUR_CLASS_NAME {
    --e-mobility-widget-map-height: 200px;
  }
</style>

<e-mobility-map-widget class="YOUR_CLASS_NAME" logo="logo.png" language="it"></e-mobility-map-widget>
```

The width of this component reacts on regular css rules. Configure the `display`
property accordingly, for instance, as `display: block`, if you want to hardcode
the dimensions.


## Getting started

These instructions will get you a copy of the project up and running
on your local machine for development and testing purposes.

### Prerequisites

To build the project, the following prerequisites must be met:

- Node 12 / NPM 8.1.2

For a ready to use Docker environment with all prerequisites already installed and prepared, you can check out the [Docker environment](#docker-environment) section.

### Source code

Get a copy of the repository:

```bash
git clone https://github.com/noi-techpark/webcomp-mobility-echarging-map.git
```

Change directory:

```bash
cd webcomp-mobility-echarging-map/
```

### Dependencies

Download all dependencies:

```bash
npm install
```

### Build

Build and start the project:

```bash
npm run start
```

The application will be served and can be accessed at [http://localhost:8000](http://localhost:8000).

## Deployment

To create the distributable files, execute the following command:

```bash
npm run build
```

## Docker environment

For the project a Docker environment is already prepared and ready to use with all necessary prerequisites.

These Docker containers are the same as used by the continuous integration servers.

### Installation

Install [Docker](https://docs.docker.com/install/) (with Docker Compose) locally on your machine.

### Dependenices

First, install all dependencies:

```bash
docker-compose run --rm app /bin/bash -c "npm install"
```

### Start and stop the containers

Before start working you have to start the Docker containers:

```
docker-compose up --build --detach
```

After finished working you can stop the Docker containers:

```
docker-compose stop
```

### Running commands inside the container

When the containers are running, you can execute any command inside the environment. Just replace the dots `...` in the following example with the command you wish to execute:

```bash
docker-compose run --rm app /bin/bash -c "..."
```

Some examples are:

```bash
docker-compose run --rm app /bin/bash -c "npm run build"
```

## Information

### Support

ToDo: For support, please contact [help@opendatahub.bz.it](mailto:help@opendatahub.bz.it).

### Contributing

If you'd like to contribute, please follow the following instructions:

- Fork the repository.

- Checkout a topic branch from the `development` branch.

- Make sure the tests are passing.

- Create a pull request against the `development` branch.

A more detailed description can be found here: [https://github.com/noi-techpark/documentation/blob/master/contributors.md](https://github.com/noi-techpark/documentation/blob/master/contributors.md).

### Documentation

More documentation can be found at [https://opendatahub.readthedocs.io/en/latest/index.html](https://opendatahub.readthedocs.io/en/latest/index.html).

### Boilerplate

The project uses this boilerplate: [https://github.com/noi-techpark/webcomp-boilerplate](https://github.com/noi-techpark/webcomp-boilerplate).

### License

The code in this project is licensed under the GNU AFFERO GENERAL PUBLIC LICENSE Version 3 license. See the [LICENSE.md](LICENSE.md) file for more information.
