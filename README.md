# zotero-bibtex-online-sources
This repository provides the translator for the BibTex format, adapted to provide online sources with an url and access date automatically in LaTex.
It is useful to handle online sources, since [Zotero](https://github.com/zotero/zotero) does not natively support the URL attribute and Access Date. Hence, manual changes have been required in the past. This script solves the mentioned problem. 

## How to use this script
To use this script, just copy the file into the translators directory of the Zotero directory. It should replace the existing BibTeX.js file. Bibliography exports now contain the `howpublished` attribute, as well as the note attribute containing the access date.

## Example 
This is how it looked before:
```
@misc{google_cloud_platform_5_nodate,
	title = {5 years of 100\% renewable energy, and targeting 100\% {CFE}},
	url = {https://cloud.google.com/blog/topics/sustainability/5-years-of-100-percent-renewable-energy},
	abstract = {For five years now, Google has matched all its energy consumption with renewable energy, and is planning to use 100\% carbon-free energy by 2030.},
	language = {en},
	urldate = {2024-03-11},
	journal = {Google Cloud Blog},
	author = {{Google Cloud Platform}},
	file = {Snapshot:/Users/user/Zotero/storage/VL2UG7ZY/5-years-of-100-percent-renewable-energy.html:text/html},
}
```
This is how the updated version looks like:
```
@misc{google_cloud_platform_5_nodate,
	title = {5 years of 100\% renewable energy, and targeting 100\% {CFE}},
	url = {https://cloud.google.com/blog/topics/sustainability/5-years-of-100-percent-renewable-energy},
	abstract = {For five years now, Google has matched all its energy consumption with renewable energy, and is planning to use 100\% carbon-free energy by 2030.},
	language = {en},
	urldate = {2024-03-11},
	note = {[Online: accessed 2024-03-11]},
	journal = {Google Cloud Blog},
	author = {{Google Cloud Platform}},
	howpublished = {https://cloud.google.com/blog/topics/sustainability/5-years-of-100-percent-renewable-energy},
	file = {Snapshot:/Users/tengelma/Zotero/storage/VL2UG7ZY/5-years-of-100-percent-renewable-energy.html:text/html},
}
```

## Customize
To customize the format of the access date, just change line 1408 in the script. This line defines the date format.
