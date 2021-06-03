# Spatial Data Package Profile

- Start Date: 2021-06-03
- Author: [cividi people](https://github.com/orgs/cividi/people)
- Target Major Version: (2.x / 3.x)
- Reference Issues: (fill in existing related issues, if any)
- Implementation PR: (leave this empty)
- Status: **Draft** (Approved, Review, Wontfix, Implemented)

# Summary

Support a Spatial Data Package profile and geographic resource types as part of the Frictionless Data specification. Reconsider the use of GeoJSON/Geopoint field types, or at least expand the guidance around publishing geospatial datasets. Reference Spatial Data Packages where relevant in other specs. 

# Basic example

- A proposed schema and examples: https://github.com/cividi/spatial-data-package
- A proposed Framework extension to add GeoJSON read and write support: https://github.com/cividi/frictionless-geojson
- Early alpha of a Create (datapackage-ui) tool with spatial features: https://create.cividi.ch/ ([source](https://github.com/n0rdlicht/datapackage-ui/tree/spatial-data-package))

# Motivation

Creating a proof of concept for Frictionless Data has been a very important aspect of cividi, our civic tech pioneer project, where we have been working at the intersection of the open-source-geospatial, city-planner-architect and data-engineering communities. We have identified compelling needs for referencing geodata that are not covered by the [Geopoint and Geodata](https://specs.frictionlessdata.io/table-schema/#types-and-formats) field types. These include a standard and render-neutral way of referencing base map layers and projections, supporting alternative coordinate and indexing systems, and interfacing with openly supported styling grammars. We would like to explore future scenarios for spatial datasets in the Frictionless Data ecosystem in conversation with the broader community. 

# Approach

The cividi tech team - @n0rdlicht @bkarolina @brieden and @loleg - had a workshop to dive into the draft [Spatial Data Package](https://github.com/cividi/spatial-data-package) profile that we have been working on for over one year. It is already built into our projects, most notably [Spatial Data Platform](https://github.com/cividi/spatial-data-package-platform) (Gemeindescan.ch) and [Spatial Data Package Export](https://github.com/cividi/spatial-data-package-export) (QGIS plugin). We have presented our intention and mentioned progress several times in the Frictionless Data forums and community calls. This RFC represents our striving towards a roadmap for actual incorporation into the Specifications. 

We have built our work off where the 2017 [investigation by Steve Bennett](https://research.okfn.org/spatial-data-package-investigation/) ended, and would like to see stronger support for geodata co-developed and co-funded within the network. This development should anchor, as do most of the existing Use Cases, in clear business + activism use cases. To this end we would like to try to bring in at least one relevant project/pilot from Switzerland.

We still need to clarify the process for incorporating new Profiles into the [Frictionless Registry](https://specs.frictionlessdata.io/schemas/registry.json), start a Pull Request of an update to the documentation, a Forum discussion and get help reaching out through other channels for feedback. We are well aware that other people are doing similar work elsewhere, have already had some validation and questions on our Issues and Discussion topics, and aim to keep this whole process as open as possible.

Additional activities that we have brainstormed are:

- Run a [cividi.tech workshop](https://medium.com/cividi) with the Frictionless Data community on advanced publication and analysis of geospatial data.
- Propose CKAN features and build on [ckanext-geoview](https://github.com/ckan/ckanext-geoview) and [ckanext-spatial](https://github.com/ckan/ckanext-spatial), e.g. for deeper indexing and flexible rendering previews.
- Propose an extension of [datapackage-ui](https://github.com/frictionlessdata/datapackage-ui) and [data-cli](https://datahub.io/docs/features/data-cli) with geospatial support. 
- Write an overview of some of the diverse ways that [GeoJSON](https://geojson.org/) ([RFC7946](https://datatracker.ietf.org/doc/html/rfc7946)) is referenced and catalogued in geospatial-focused portals.
- Propose a Data Package import for [geojson.io](http://geojson.io/), [OpenLayers](https://openlayers.org/en/latest/examples/index.html?q=geojson), [Cesium](https://cesium.com/docs/cesiumjs-ref-doc/GeoJsonDataSource.html) and other popular geodata visualisers.
- Extend the [QGIS export plugin](https://github.com/cividi/spatial-data-package-export) with import functionality.
- Create lightweight (statically-rendered) examples and write a developer tutorial. Note the existing [GeoJSON tutorial](https://datahub.io/examples/geojson-tutorial#javascript) on Datahub.
- Investigate and respond to the question of compatibility with existing geometadata packaging, e.g. [Geopackage](https://github.com/opengeospatial/geopackage).

# Drawbacks

Why should we *not* do this? Please consider:

- implementation cost, both in term of code size and complexity
- whether the proposed feature can be implemented in user space
- the impact on teaching people to use this spec
- integration of this feature with other existing and planned features
- cost of migrating existing applications (is it a breaking change?)

There are tradeoffs to choosing any path. Attempt to identify them here.

# Alternatives

What other designs have been considered? What is the impact of not doing this?

# Adoption strategy

If we implement this proposal, how will existing developers adopt it? Is this a breaking change? Can we write a codemod? Can we provide a runtime adapter library for the original API it replaces? How will this affect other projects in the CKAN ecosystem?

# Unresolved questions

Optional, but suggested for first drafts. What parts of the design are still TBD?
