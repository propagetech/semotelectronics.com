You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | About us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | Contact Us",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/68d309b9f7fd0db5144e39c51ce5e0cb.css",
    "context": {
      "path": "css/68d309b9f7fd0db5144e39c51ce5e0cb.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c363a15baf9b3719c1570c22b012b369.css",
    "context": {
      "path": "css/c363a15baf9b3719c1570c22b012b369.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "gridsmart-backup.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | Gridsmart",
      "first_heading": "GRIDSMART\u00ae"
    }
  },
  {
    "path": "imgs/1d3d475620052fa3be15728b013c2e6c.webp",
    "context": {
      "refs": [
        {
          "alt": "GridsmartsiteChennai",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30dcf3abffd22554c15c471a30217d4e.webp",
    "context": {
      "refs": [
        {
          "alt": "TIRTL Working Demo Indian -Traffic",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/318263f4458fc8718f2f57972d552b82.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3c64eea8720e510dba572618a730d5b4.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/614fd06c049abfdaed3befebbcdd3ec5.webp",
    "context": {
      "refs": [
        {
          "alt": "TIRTL Temporary Survey",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d3dae0632ed34f87a23c0ca5eaa44c2.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7ca4662b437cf96c000630e049f8c165.webp",
    "context": {
      "refs": [
        {
          "alt": "TIRTL Toll Audit Installation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/865d63c9a1bf74714e736c7105fcd3c0.webp",
    "context": {
      "refs": [
        {
          "alt": "Gridsmart site Mumbai",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc54b5208b1980e1ec784159f831eb31.webp",
    "context": {
      "refs": [
        {
          "alt": "TIRTL Solar Installation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cff214fb099aeb79ac4ae0757574ed03.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d18185e604e59a788bab86439e49f713.webp",
    "context": {
      "refs": [
        {
          "alt": "Gridsmart site Bangalore",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d8a3356272c2b33343f123cc4f396664.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ded37c10292d28a15bd469360edb4d46.webp",
    "context": {
      "refs": [
        {
          "alt": "TIRTLs are implemented as ATCC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea64ae09892c9058fa0d95869e22f144.webp",
    "context": {
      "refs": [
        {
          "alt": "Products",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb42062cb7c89be60675ae8d15206460.webp",
    "context": {
      "refs": [
        {
          "alt": "About us",
          "title": ""
        },
        {
          "alt": "Semot Electronics LLP",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eef7292ae0096da8a1f36c72608665e6.webp",
    "context": {
      "refs": [
        {
          "alt": "Services",
          "title": ""
        },
        {
          "alt": "SEMOT ELECTRONICS SERVICES INCLUDE SYSTEM INTEGRATION, OPERATION AND MAINTENANCE support.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | Home",
      "first_heading": "semot electronics llp"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/5bf52d48a7da4927bf805b6cf41943ca.js",
    "context": {
      "path": "js/5bf52d48a7da4927bf805b6cf41943ca.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "projects.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | Projects",
      "first_heading": "PROJECTS"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | Services",
      "first_heading": "SERVICES"
    }
  },
  {
    "path": "tirtl.html",
    "context": {
      "title": "SEMOT ELECTRONICS LLP | TIRTL",
      "first_heading": "TIRTL"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.