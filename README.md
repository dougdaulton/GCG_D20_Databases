# d20 Databases

**d20-databases** is an expanding set of open-source tools and datasets written in Python that leverage generative AI and structured data to support the creation, conversion, and publication of *Adventure Paths*, campaigns, monsters, spells, and more across a wide range of D20 tabletop roleplaying game systems.

The project began with the excellent work of the [`5e-database`](https://github.com/bagelbits/5e-database) and aims to broaden its scope to include content from systems like **Pathfinder 1E and 2E**, **D&D 1st through 5th Edition**, and emerging open ecosystems such as those licensed under **ORC**, **Creative Commons**, or **GCL** (Game Content License).  

All data will include structured metadata for **license type**, **data provenance**, and **usage rights**, ensuring respectful treatment of intellectual property, including attribution and license compliance—without use of protected trade dress or proprietary content.

## 📚 System Databases (Planned and In Progress)

This repository is designed as a hub for interoperable databases across D20 systems:

- [x] **D&D 5th Edition (SRD-based)** — Original 5e-database  
- [ ] **D&D 5E+** — For post-2024/OneD&D public materials  
- [ ] **D&D 3rd Edition**  
- [ ] **D&D 3.5 Edition**  
- [ ] **D&D 4th Edition**  
- [ ] **D&D 2nd Edition (AD&D)**  
- [ ] **D&D 1st Edition (OD&D / BECMI)**  
- [ ] **Pathfinder 1st Edition** *(Placeholder: PyZO Pathfinder 1E)*  
- [ ] **Pathfinder 2nd Edition** *(Placeholder: PyZO Pathfinder 2E)*  

Each database will eventually include normalized schemas and conversion tools for monsters, spells, classes, feats, items, and more—enabling remixing and publication under compatible license frameworks.

## D&D 5th Edition (SRD-based): Original 5e-database  

## 🚀 How to Run

### With Docker

You can build and run the 5E database locally using Docker:

docker run ghcr.io/5e-bits/5e-database:latest

![Build Status](https://github.com/bagelbits/5e-database/workflows/5e%20Database%20CI/badge.svg?branch=main)
[![Discord](https://img.shields.io/discord/656547667601653787)](https://discord.gg/TQuYTv7)

Holds the database for the D&D 5th Edition API at http://dnd5eapi.co/

Talk to us [on Discord!](https://discord.gg/TQuYTv7)

## How to run

### With Docker

You should be able to build locally and then run the local Docker image. This can be done one of two ways:

1. If you just need an image and you aren't running an M1:

```bash
docker run ghcr.io/5e-bits/5e-database:latest
```

2. If you're running an M1 or you want to test changes that you've made to the Database:

```bash
docker build -t 5e-database .
docker run -i -t 5e-database:latest
```

### Without Docker

First you need to make sure you have [MongoDB installed locally.](https://docs.mongodb.com/manual/installation/)

You can load this data locally by running:

```bash
MONGODB_URI=mongodb://localhost/5e-database npm run db:refresh
```

## API Issues

If you see anything wrong with the API and not the data, please open an issue or PR over [here](https://github.com/bagelbits/5e-srd-api).

## Contributing

* Fork this repository
* Create a new branch for your work
* Push up any changes to your branch, and open a pull request. Don't feel it needs to be perfect — incomplete work is totally fine. We'd love to help get it ready for merging.
* We use Semantic Release so here are the PR naming convetions:

| Commit message                                                                                                                                                                             | Release type                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| fix(pencil): stop graphite breaking when too much pressure applied                                                                                                                         | Patch Fix Release                                                                                        |
| feat(pencil): add 'graphiteWidth' option                                                                                                                                                   | Minor Feature Release                                                                                    |
| perf(pencil): remove graphiteWidth option<br><br>BREAKING CHANGE: The graphiteWidth option has been removed.<br>The default graphite width of 10mm is always used for performance reasons. | Major Breaking Release<br><br>(Note that the BREAKING CHANGE: token must be in the footer of the commit) |

## Code of Conduct

The Code of Conduct can be found [here.](https://github.com/5e-bits/5e-database/wiki/Code-of-Conduct)

## License

This project is licensed under the terms of the MIT license. The underlying material
is released using the [Open Gaming License Version 1.0a](https://www.wizards.com/default.asp?x=d20/oglfaq/20040123f)

## Contributors

<a href="https://github.com/5e-bits/5e-database/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=5e-bits/5e-database" />
</a>
