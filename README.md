# net.loadbang.web

![Screengrab][grab]

This package is an embedded web server for MaxMSP, written in Java and
using [Jetty][jetty]. The system supports static data and JSPs. The
server is packaged into an MXJ object, and can serve files from any
directory in MaxMSP's search path. It implements two-way communication
with Max: the object reports web requests into the Max world, and Max
can create attribute bindings for JSPs.

## Installation

The following files (there are rather a lot of them) are needed in Max's
`Cycling '74/java/lib` directory:

- `net.loadbang.web-0.0.1-SNAPSHOT.jar`
- `jetty-6.1.26.jar`
- `jetty-util-6.1.26.jar`
- `net.loadbang.lib-1.8.0.jar`
- `jsp-2.1-6.0.2.jar`
- `jsp-api-2.1-6.0.2.jar`
- `ant-1.8.4.jar`
- `ant-launcher-1.8.4.jar`
- `log4j-1.2.16.jar`

These files are all included in `distribution.zip` in
[downloads][downloads], alongside the test patchers.

## Usage

The directory `examples` contains Max patchers (written originally for
Max 4!) which bring up the web server. `examples/WebServer.mxt` is a
good place to start, but the real party is happening in
`examples/max5/cassiel.JWebFun.maxpat`.

## Building

The `net.loadbang` support projects, all hosted in GitHub, are written
in Java and can be built in Maven. They need to be built in sequence
since they aren't centrally hosted. The `max.jar` file also needs to be
pushed into a local Maven repository. See the `README` for
[net.loadbang.lib][loadbang-lib] for details.

## Acknowledgements

Thanks to [Adam Murray][adam] for contributions to the JSP support.

## License

Distributed under the [GNU General Public License][gpl].

Copyright (C) 2012 Nick Rothwell.

[grab]: https://github.com/downloads/cassiel/net.loadbang.web/grab.png
[jetty]: http://jetty.codehaus.org/jetty/
[loadbang-lib]: https://github.com/cassiel/net.loadbang.lib
[downloads]: https://github.com/cassiel/net.loadbang.web/downloads
[adam]: http://compusition.com/web/about
[gpl]: http://www.gnu.org/copyleft/gpl.html
