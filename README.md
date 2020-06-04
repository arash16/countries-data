# countries-languages
The project contains json data files.
The data is about countries, languages codes and anthems.

## Table of Contents
* [Installation](#installation)
* [Countries Data](#countries-data)
  * [Data Structure](#data-structure)
  * [Example: Iran](#example-iran)
* [Languages Data](#languages-data)
  * [Data Structure](#data-structure-1)
  * [Example: Azerbaijani](#example-azerbaijani)
  * [Example: Malay](#example-malay)
  * [Example: Albanian](#example-albanian)  
* [Anthems Data](#anthems-data)
  * [Data Structure](#data-structure-2)
  * [Example: United States](#example-united-states)
* [Initial Data Source](#initial-data-source)

## Installation
```
npm install countries-data
```

## Countries Data
The countries data based on iso_3166_1_alpha2 (a2) countries codes.

### Data Structure
- `name`
    - `common` - common name in english
    - `official` - official name in english
    - `native` - list of all native names
        - key: three-letter ISO 639-3 language alpha code
        - value: name object
            - key: `official` - official name translation
            - key: `common` - common name translation
- `demonym` - name of residents
- `capital` - capital city
- `iso_3166_1_alpha2` - code ISO 3166-1 alpha-2
- `iso_3166_1_alpha3` -code ISO  3166-1 alpha-3
- `iso_3166_1_numeric` - code ISO 3166-1 numeric
- `currency` - ISO 4217 currency code(s)
    - key: three-letter ISO 4217 currency code
    - value: currency object
        - key: `iso_4217_code` - three-letter ISO 4217 currency alpha code
        - key: `iso_4217_numeric` - three-number ISO 4217 currency numeric code
        - key: `iso_4217_name` - official ISO 4217 currency name
        - key: `iso_4217_minor_unit` - minor currency unit
- `tld` - country code top-level domain
- `alt_spellings` - alternative spellings
- `languages` - list of official languages
    - key: three-letter ISO 639-3 language code
    - value: name of the language in english
- `translations` - list of name translations
    - key: three-letter ISO 639-3 language code
    - value: name object
        - key: `official` - official name translation
        - key: `common` - common name translation
- `geo`
    - `continent` - continents that country lies in
        - key: two-letter continent code
        - value: name of the continent in english
    - `postal_code` - geographical area postal code
    - `latitude` - short form of latitude coordinate point
    - `latitude_dec` - described latitude coordinate point
    - `longitude` - short form of longitude coordinate point
    - `longitude_dec` - described longitude coordinate point
    - `max_latitude` - maximum latitude coordinate point
    - `max_longitude` - maximum longitude coordinate point
    - `min_latitude` - minimum latitude coordinate point
    - `min_longitude` - minimum longitude coordinate point
    - `area` - land area in km²
    - `region` - geographical region
    - `subregion` - geographical sub-region
    - `world_region` - geographical world region
    - `region_code` - geographical region numeric code
    - `subregion_code` - geographical sub-region numeric code 
    - `landlocked` - landlocked status
    - `borders` - land borders
    - `independent` - independent status
- `dialling`
    - `calling_code` - calling code(s)
    - `national_prefix` - national prefix
    - `national_number_lengths` - national number lengths
    - `national_destination_code_lengths` - national destination code lengths 
    - `international_prefix` - international prefix
- `extra`
    - `geonameid` - Geoname ID
    - `edgar` - Electronic Data Gathering, Analysis, and Retrieval system
    - `itu` - Codes assigned by the International Telecommunications Union
    - `marc` - MAchine-Readable Cataloging codes from the Library of Congress
    - `wmo` - Country abbreviations by the World Meteorological Organization
    - `ds` - Distinguishing signs of vehicles in international traffic
    - `fifa` - Codes assigned by the Fédération Internationale de Football Association
    - `fips` - Codes from the U.S. Federal Information Processing Standard
    - `gaul` - Global Administrative Unit Layers from the Food and Agriculture Organization
    - `ioc` - Codes assigned by the International Olympics Committee
    - `cowc` - Correlates of War character
    - `cown` - Correlates of War numeric
    - `fao` - Food and Agriculture Organization 
    - `imf` - International Monetary Fund 
    - `ar5` - Fifth Assessment Report (AR5) 
    - `address_format` - Address forma
    - `eu_member` - European Union Member
    - `vat_rates` - Value-Added Tax
- `population`
    - `count` - population number
    - `worldPercentage` - country population of world population percentage
- `wikiLink` - relative link to country wikipedia page

### Example: Iran
```json
{
  "IR": {
    "name": {
      "common": "Iran",
      "official": "Islamic Republic of Iran",
      "native": {
        "fas": {
          "official": "جمهوری اسلامی ایران",
          "common": "ایران"
        }
      }
    },
    "demonym": "Iranian",
    "capital": "Tehran",
    "iso_3166_1_alpha2": "IR",
    "iso_3166_1_alpha3": "IRN",
    "iso_3166_1_numeric": "364",
    "currency": {
      "IRR": {
        "iso_4217_code": "IRR",
        "iso_4217_numeric": 364,
        "iso_4217_name": "Iranian rial",
        "iso_4217_minor_unit": 2
      }
    },
    "tld": [
      ".ir",
      "ایران."
    ],
    "alt_spellings": [
      "IR",
      "Islamic Republic of Iran",
      "Iran, Islamic Republic of",
      "Jomhuri-ye Eslāmi-ye Irān"
    ],
    "languages": {
      "fas": "Persian"
    },
    "translations": {
      "deu": {
        "official": "Islamische Republik Iran",
        "common": "Iran"
      },
      "fra": {
        "official": "République islamique d'Iran",
        "common": "Iran"
      },
      "hrv": {
        "official": "Islamska Republika Iran",
        "common": "Iran"
      },
      "jpn": {
        "official": "イラン·イスラム共和国",
        "common": "イラン・イスラム共和国"
      },
      "nld": {
        "official": "Islamitische Republiek Iran",
        "common": "Iran"
      },
      "por": {
        "official": "República Islâmica do Irã",
        "common": "Irão"
      },
      "rus": {
        "official": "Исламская Республика Иран",
        "common": "Иран"
      },
      "spa": {
        "official": "República Islámica de Irán",
        "common": "Iran"
      },
      "fin": {
        "official": "Iranin islamilainen tasavalta",
        "common": "Iran"
      }
    },
    "geo": {
      "continent": {
        "AS": "Asia"
      },
      "postal_code": true,
      "latitude": "32 00 N",
      "latitude_dec": "32.50077819824219",
      "longitude": "53 00 E",
      "longitude_dec": "54.2942008972168",
      "max_latitude": "39.7754",
      "max_longitude": "62",
      "min_latitude": "25.05",
      "min_longitude": "27.4455",
      "area": 1648195,
      "region": "Asia",
      "subregion": "Southern Asia",
      "world_region": "EMEA",
      "region_code": "142",
      "subregion_code": "034",
      "landlocked": false,
      "borders": [
        "AFG",
        "ARM",
        "AZE",
        "IRQ",
        "PAK",
        "TUR",
        "TKM"
      ],
      "independent": "Yes"
    },
    "dialling": {
      "calling_code": [
        "98"
      ],
      "national_prefix": "0",
      "national_number_lengths": [
        10
      ],
      "national_destination_code_lengths": [
        2
      ],
      "international_prefix": "00"
    },
    "extra": {
      "geonameid": 130758,
      "edgar": 0,
      "itu": "IRN",
      "marc": "ir",
      "wmo": "IR",
      "ds": "IR",
      "fifa": "IRN",
      "fips": "IR",
      "gaul": 117,
      "ioc": "IRI",
      "cowc": "IRN",
      "cown": 630,
      "fao": 102,
      "imf": 429,
      "ar5": "MAF",
      "address_format": null,
      "eu_member": null,
      "vat_rates": null
    },
    "population": {
      "count": 79615300,
      "worldPercentage": 1.07
    },
    "wikiLink": "/wiki/Iran"
  }
}
```

## Languages Data
The Languages data based on ISO 639-3 languages codes.

### Data Structure
- `full` - language full name
- `speak` (optional)
    - `isExist` - true if language speaker exist
    - `optional` - another speaker that speak the language
    - `speakerGenderRestriction` - Male when Female speaker does not exist

### Example: Azerbaijani
```json
{
  "aze": {
    "full": "Azerbaijani",
    "speak": {
      "isExist": false
    }
  }
}
```

### Example: Malay
```json
{
  "msa": {
    "full": "Malay",
    "speak": {
      "optional": "eng"
    }
  }
}
```

### Example: Albanian
```json
{
  "alb": {
    "full": "Albanian",
    "speak": {
      "speakerGenderRestriction": "Male"
    }
  }
}
```

## Anthems Data
The country keys is based on iso_3166_1_alpha2 (a2) countries codes.

### Data Structure
- `link` - full link to audio file 
- `source` - link source

### Example: United States
```json
{ 
  "US": {
    "link": "https://commons.wikimedia.org/wiki/File%3AStar Spangled Banner instrumental.ogg?embedplayer=yes",
    "source": "wikimedia"
  }
}
```

### Initial Data Source
The initial json data is part of [rinvex country](https://github.com/rinvex/country) repository.
