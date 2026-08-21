# Welcome to the IP-XACT open source community!

The goal of this GitHub organization is to build and share free and open-source tools around [Accellera's IP-XACT standard](https://www.accellera.org/downloads/standards/ip-xact), following the latest version (IEEE 1685-2022). [^1]

## XactFlow Application

**XactFlow** is our main tool: a Python-based application for reading, manipulating, and generating IP-XACT descriptions. It is inspired by how PeakRDL works for SystemRDL, and aims to become a similar reference toolchain for the IP-XACT ecosystem.

### Planned architecture

At its core, XactFlow will be built around an **ipxact-compiler**, a library that reads IP-XACT XML files and translates them into a structured Python object model. The rest of the ecosystem (importers, exporters, and integrations) will build on top of that shared object model instead of each tool re-parsing IP-XACT XML on its own. On top of the compiler, we plan to grow a collection of standalone importer and exporter applications: generating IP-XACT components from SV source paired with a metadata file, simplifying the creation of an IP-XACT design file through a new, custom way of describing it, and exporting HTML documentation or SV files from an IP-XACT design file.

### Scope

For the initial phase, XactFlow will focus on the following IP-XACT object types:

- **Component** descriptions
- **Design** descriptions
- **Bus** related definitions (bus definitions / abstraction definitions)

Support for additional IP-XACT object types (catalogs, generators, etc.) may follow once this core is solid.

## License

Unless otherwise noted, projects in this organization are released under the [GNU Lesser General Public License v3.0 (LGPL-3.0)](https://www.gnu.org/licenses/lgpl-3.0.html).

[^1]: This IP-XACT GitHub group is not affiliated with Accellera.