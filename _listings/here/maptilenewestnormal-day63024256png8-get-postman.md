{
  "info": {
    "name": "HERE Map Tile API Multiple Base64 Encoded Map Tiles",
    "_postman_id": "119c041c-4a82-4642-907c-c8e1a79a3166",
    "description": "*Request multiple base64 encoded map tiles*\n\nA square consisting of multiple base64 encoded tiles is requested by adding the parameters `output=base64` and `range=NxN` to the request URL. The `column` and `row` in the path of the URL, defining the top left-hand corner of the tile group must be divisible by the value of the `range` parameter.\n  \n  Click on the response to decode the tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates the size of the array of tiles returned. Valid values are `2x2`, `3x3` or `4x4`\n\n Valid values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Terrain",
      "item": [
        {
          "id": "ac9aacc6-2556-4e58-9202-3d2211948949",
          "name": "TerrainDay76645256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/terrain.day/7/66/45/256/png8?app_code=%7B%7D&app_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a terrain map tile*\n\nTerrain map tile are available by passing `terrain.day` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b428426c-5213-4f8d-a812-87047fd8f976"
            }
          ]
        }
      ]
    },
    {
      "name": "Multiple",
      "item": [
        {
          "id": "dce32dde-697f-4d55-a45e-4b38dca718da",
          "name": "MaptileNewestNormalDay63024256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/6/30/24/256/png8?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D&range=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request multiple base64 encoded map tiles*\n\nA square consisting of multiple base64 encoded tiles is requested by adding the parameters `output=base64` and `range=NxN` to the request URL. The `column` and `row` in the path of the URL, defining the top left-hand corner of the tile group must be divisible by the value of the `range` parameter.\n  \n  Click on the response to decode the tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates the size of the array of tiles returned. Valid values are `2x2`, `3x3` or `4x4`\n\n Valid values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7155d0ed-f678-4b5a-934f-828d5d0a70f9"
            }
          ]
        }
      ]
    },
    {
      "name": "Color-reduced",
      "item": [
        {
          "id": "3b166009-4a80-4eef-916c-6f291800fe71",
          "name": "MaptileNewestNormalDayTransit1220741409256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day.transit/12/2074/1409/256/png8?app_code=%7B%7D&app_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a color-reduced map tile with public transport*\n\nColor-reduced street map tiles with full-color transit overlays are requested by passing `normal.day.transit` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11fe7755-6f99-4976-b821-714b279de5f0"
            }
          ]
        },
        {
          "id": "02966d6f-3412-48ad-ae65-14e7d0910b0b",
          "name": "MaptileNewestNormalDayGrey11525761256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day.grey/11/525/761/256/png8?app_code=%7B%7D&app_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a greyed out street map tile*\n\nMaps using a reduced color palette can be requested by passing `normal.day.grey` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e355786-5a41-4ebf-85ca-74273e6577ca"
            }
          ]
        }
      ]
    },
    {
      "name": "Hybrid",
      "item": [
        {
          "id": "116632f5-6bea-4835-9f36-2a5f8adaf945",
          "name": "HybridDay485256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/hybrid.day/4/8/5/256/png8?app_code=%7B%7D&app_id=%7B%7D&lg=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a hybrid map tile - satellite imagery with labels*\n\nHybrid map tile are available by passing `hybrid.day` in the path of the request URL. The map tiles will display using the default language of the server unless the `lg` query parameter is used to change the map tile language. Consult the  Map Tile API Reference for a full list of available languages.\n\n\n\n* **lg**  `enum`\n \\- Alters the language of the labels displayed on the map. Three letter MARC code, for example `rus` for Russian language.\n\n Valid values are : `ara` - Arabic, `chi` - Chinese, `cht` - Chinese (Trad), `dut` - Dutch, `eng` - English, `fre` - French, `ger` - German, `gle` - Gaelic, `gre` - Greek, `heb` - Hebrew, `hin` - Hindi, `ind` - Indonesian, `ita` - Italian, `per` - Persian, `pol` - Polish, `por` - Portuguese, `rus` - Russian, `sin` - Sinhalese, `spa` - Spanish, `tha` - Thai, `tur` - Turkish, `ukr` - Ukranian, `urd` - Urdu, `vie` - Vietnamese, `wel` - Welsh\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "94ab8ce0-8372-435f-86c3-b8d0bd8a1300"
            }
          ]
        }
      ]
    },
    {
      "name": "Truck",
      "item": [
        {
          "id": "2aaa08cc-e945-4e44-82c4-ca7b815879e0",
          "name": "TrucktileNewestNormalDay1221991342256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/trucktile/newest/normal.day/12/2199/1342/256/png8?app_code=%7B%7D&app_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a street map tile showing restrictions for heavy vehicles*\n\nTo obtain a map tile displaying route restrictions for trucks, use the `trucktile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a7106191-fb78-4e5d-9b51-60353b479a9e"
            }
          ]
        }
      ]
    },
    {
      "name": "Toll",
      "item": [
        {
          "id": "05b6fe7e-bb38-4918-b48e-4708756890af",
          "name": "MaptileNewestNormalDay9255170256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/9/255/170/256/png8?app_code=%7B%7D&app_id=%7B%7D&congestion=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a street map tile highlighting congestion and environmental toll zones*\n\nTo highlight such toll zones, add the `congestion` parameter to the request URL.\n\n\n\n* **congestion**  `null`\n \\- Flag to indicate if congestion zones are to be shown on the map.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d4acb6f3-64e5-490c-8c27-b068d37623c8"
            }
          ]
        }
      ]
    },
    {
      "name": "Satellite",
      "item": [
        {
          "id": "da43c74e-d941-4335-8cec-a09ad12b09e9",
          "name": "SatelliteDay51512256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/satellite.day/5/15/12/256/png8?app_code=%7B%7D&app_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a satellite map tile*\n\nSatellite map tiles do not display labels and are available by passing `satellite.day` in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4e18be15-5335-44d6-8585-525fd982af57"
            }
          ]
        }
      ]
    },
    {
      "name": "Fleet",
      "item": [
        {
          "id": "a48d32f9-3b5c-43ac-963b-28e99113a93f",
          "name": "MaptileNewestNormalDay1340932723256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/13/4093/2723/256/png8?app_code=%7B%7D&app_id=%7B%7D&style=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a street map tile using the fleet vehicle color scheme*\n\nFleet color scheme map tiles are available by passing `style=fleet` as a parameter of the request URL.\n\n\n\n* **style**  `enum`\n \\- If present, selects the style to use to render the tile.\n\n Valid values are : `default`, `alps`, `fleet`, `wings`, `dreamworks`, `flame`, `mini`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11945b49-1b3c-4dac-a445-01bdf95f44ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Base64",
      "item": [
        {
          "id": "2f46da29-b4f0-403c-ae67-253b2d839fe8",
          "name": "MaptileNewestNormalDay11525761256Png8Get4",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/maptile/newest/normal.day/11/525/761/256/png8?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a base64 encoded map tile*\n\nBase64 encoded tiles are requested by adding the parameter `output=base64` to the request URL.\n  \n  Click on the response to decode the tile returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return the tile as base64 encoded text.\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dbcab8ba-71d3-4dfd-84d0-6d11320eea1a"
            }
          ]
        }
      ]
    },
    {
      "name": "Map",
      "item": [
        {
          "id": "d8c55138-fe59-4b48-8d01-eafc77672da6",
          "name": "InfoGet",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/info?app_code=%7B%7D&app_id=%7B%7D&output=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request information about the types of map tiles available on a server*\n\nTo make a request for metadata information, use the `info` parameter in the path of the request URL.\n\n\n\n* **output**  `enum`\n \\- Indicates whether to return the information in XML format, JSON format or as an XML schema (XSD) of the API metadata\n\n Valid values are : `json`, `xml`, `xsd`\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "17e93e79-3abd-4103-97e7-9a0320ddb710"
            }
          ]
        }
      ]
    },
    {
      "name": "Transparent",
      "item": [
        {
          "id": "abdf140c-e506-4e53-9085-f8ccb809ff07",
          "name": "TruckonlytileNewestNormalDay1221991342256Png8Get",
          "request": {
            "url": "http://1.aerial.maps.cit.api.here.com/maptile/2.1/maptile/newest/truckonlytile/newest/normal.day/12/2199/1342/256/png8?app_code=%7B%7D&app_id=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "*Request a transparent tile showing restrictions for heavy vehicles only*\n\nTo obtain a transparent map tile displaying route restrictions for trucks, use the `truckonlytile` parameter in the path of the request URL.\n\n\n\n* **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d725f51-73aa-4c7a-b10f-38f71dcec198"
            }
          ]
        }
      ]
    }
  ]
}