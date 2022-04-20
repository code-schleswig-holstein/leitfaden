# Open-Data-Leitfaden Schleswig-Holstein

This is the source for the "Open-Data-Leitfaden Schleswig-Holstein". From the source, different targets can be generated. See the [Makefile](/Makefile) for details. 
The workflow is based on the procedure used for the [Berliner Open-Data-Handbuch](https://github.com/berlinonline/open-data-handbuch).

The following versions exist:

- A PDF document generated directly from the source via [pandoc](https://pandoc.org) (and additional processing - see [Makefile](/Makefile) for details).
- An HTML version generated directly from the source via the static website generator [Hugo](https://gohugo.io) - available online here: https://opendata.zitsh.de/leitfaden/

## Building

You need a few prerequisites to build the _Open-Data-Leitfaden Schleswig-Holstein_. On a Ubuntu 20.04 LTS system the following packages have to be installed:

```bash
sudo apt install make librsvg2-bin poppler-utils pandoc pdflatex hugo
```

You can create the PDF document:

```bash
git clone https://code.schleswig-holstein.de/opendata/leitfaden.git
cd leitfaden
make pdf
```

The resulting PDF document will be called `leitfaden-opendata.pdf`.

To generate the HTML version:

```bash
git clone https://code.schleswig-holstein.de/opendata/leitfaden.git
cd leitfaden
make web
```

The resulting HTML files can be found in the `public/` directory. 

You can also run Hugo in _live mode_ and serve the content at http://localhost:1313/leitfaden/ by using the command `make serve-web`.

## License

The text, all markdown sources and PDF artifacts of the _Open-Data-Leitfaden Schleswig-Holstien_ are published under [Creative Commons Namensnennung 4.0 International Lizenz](https://creativecommons.org/licenses/by/4.0/deed.de) (CC BY 4.0).

For the licenses to the images contained in the _Open-Data-Leitfaden Schleswig-Holstein_, please refer to the [Bildverzeichnis](https://berlinonline.github.io/open-data-handbuch/#bildverzeichnis).

All code, including the `Makefile` and the source code in `/bin` is published under the [MIT License](/LICENSE).
