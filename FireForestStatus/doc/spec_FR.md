Entité : FireForestStatus  
=========================









<details><summary><strong>full yaml details</strong></summary>    

FireForestStatus:    
  description: 'This entity describes the possible presence of smoke and/or fire in a forest.'    
  properties:    
    address:    
      description: 'The mailing address'    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        areaServed:    
          description: 'Property. The geographic area where a service or offered item is provided. Model:''https://schema.org/areaServed'''    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, Spain. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, Spain. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
      type: Property    
      x-ngsi:    
        model: https://schema.org/address    
    alternateName:    
      description: 'An alternative name for this item'    
      type: Property    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    description:    
      description: 'A description of this item'    
      type: Property    
    fireDetected:    
      description: 'Presence of a fire detected by cameras.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Boolean    
    fireDetectedConfidence:    
      description: 'Confidence in fire detection by cameras.'    
      maximum: 1    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    fireForestDailyRiskIndex:    
      description: 'Daily risk of fire. '    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    fireRiskIndex:    
      description: 'Risk of fire index.'    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    'fireWeatherIndex ':    
      description: 'Risk of fire based on weather conditions.'    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    id:    
      anyOf: &fireforeststatus_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Unique identifier of the entity'    
      type: Property    
    litterCoverage:    
      description: 'Percentage of surface with debris'    
      maximum: 1    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number.    
    location:    
      $id: https://geojson.org/schema/Geometry.json    
      $schema: "http://json-schema.org/draft-07/schema#"    
      oneOf:    
        - properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Point'    
          type: object    
        - properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON LineString'    
          type: object    
        - properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON Polygon'    
          type: object    
        - properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPoint'    
          type: object    
        - properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiLineString'    
          type: object    
        - properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: 'GeoJSON MultiPolygon'    
          type: object    
      title: 'GeoJSON Geometry'    
    name:    
      description: 'The name of this item.'    
      type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *fireforeststatus_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: Property    
    relativeHumidity:    
      description: 'Relative Humidity a number between 0 and 1 representing the range of 0% to 100%'    
      maximum: 1    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    seeAlso:    
      description: 'list of uri pointing to additional resources about the item'    
      oneOf:    
        - items:    
            - format: uri    
              type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      type: Property    
    smokeDetected:    
      description: 'Presence of smoke detected by cameras.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Boolean    
    smokeDetectedConfidence:    
      description: 'Confidence in smoke detection by cameras.'    
      maximum: 1    
      minimum: 0    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    soilTemperature:    
      description: 'The observed soil temperature in Celsius degrees'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Number    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: Property    
  required: []    
  type: object    
```  
</details>    





    "id": "FireForestStatus-South-1",  
    "dateObserved": "2021-02-24T00:00:00Z",  
    "location": {  
      "type": "Point",  
      "coordinates": [42.206302, -7.887465]  
    },  
    "name": "Ourense Forest - South",  
    "description": "Status of the Ourense Forest (south)",  
    "refDevice": {  
        "type": "Relationship",  
        "object": ["ground-humidity-sensor:1"]  
    },  
    "smokeDetected": false,  
    "smokeDetectedConfidence": 0.9,  
    "fireDetected": false,  
    "fireDetectedConfidence": 0.8,  
    "fireRiskIndex": 0.1,  
    "litterCoverage": 0.6,  
    "relativeHumidity": 0.70,  
    "soilTemperature": 25  
  }  
```  




  "id": "urn:ngsi-ld:FireForestStatus:id:JPEX:39548913",  
  "dateCreated": {  
    "type": "DateTime",  
    "value": "2011-04-09T04:07:43Z"  
  },  
  "dateModified": {  
    "type": "DateTime",  
    "value": "2011-04-09T04:07:43Z"  
  },  
  "source": {  
    "type": "Text",  
    "value": ""  
  },  
  "name": {  
    "type": "Text",  
    "value": "Ourense Forest - South"  
  },  
  "alternateName": {  
    "type": "Text",  
    "value": "Ourense Forest - South"  
  },  
  "description": {  
    "type": "Text",  
    "value": "Status of the Ourense Forest (south)"  
  },  
  "dataProvider": {  
    "type": "Text",  
    "value": ""  
  },  
  "owner": {  
    "type": "Array",  
    "value": [  
      "FireForestStatus.IPCZ.25073160",  
      "FireForestStatus.FPRB.78814414"  
    ]  
  },  
  "seeAlso": {  
    "type": "Array",  
    "value": [  
      "FireForestStatus.XZGT.71938385",  
      "FireForestStatus.GBWU:95431484"  
    ]  
  },  
  "location": {  
    "type": "geo:json",  
    "value": {  
      "type": "Point",  
      "coordinates": [  
        42.206302,  
        -7.887465  
      ]  
    }  
  },  
  "address": {  
    "type": "StructuredValue",  
    "value": {  
      "streetAddress": "",  
      "addressLocality": "Ourense",  
      "addressRegion": "Galicia",  
      "addressCountry": "ES",  
      "postalCode": "",  
      "postOfficeBoxNumber": "",  
      "areaServed": ""  
    }  
  },  
  "areaServed": {  
    "type": "Text",  
    "value": ""  
  },  
  "smokeDetected": {  
    "type": "Boolean",  
    "value": false  
  },  
  "smokeDetectedConfidence": {  
    "type": "Number",  
    "value": 0.9  
  },  
  "fireDetected": {  
    "type": "Boolean",  
    "value": false  
  },  
  "fireDetectedConfidence": {  
    "type": "Number",  
    "value": 0.8  
  },  
  "fireRiskIndex": {  
    "type": "Number",  
    "value": 0.1  
  },  
  "fireWeatherIndex ": {  
    "type": "Number",  
    "value": 0  
  },  
  "fireForestDailyRiskIndex": {  
    "type": "Number",  
    "value": 1  
  },  
  "litterCoverage": {  
    "type": "Number",  
    "value": 0.6  
  },  
  "relativeHumidity": {  
    "type": "Number",  
    "value": 0.7  
  },  
  "soilTemperature": {  
    "type": "Number",  
    "value": 25  
  }  
}  
```  




  "@context": [  
    "https://smartdatamodels.org/context.jsonld",  
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld"  
  ],  
  "id": "urn:ngsi-ld:FireForestStatus:FireForestStatus-South-1",  
  "type": "FireForestStatus",  
  "dateObserved": "2021-02-24T00:00:00Z",  
  "location": {  
    "type": "Point",  
    "coordinates": [  
      42.206302,  
      -7.887465  
    ]  
  },  
  "name": "Ourense Forest - South",  
  "description": "Status of the Ourense Forest (south)",  
  "refDevice": [  
    "urn:ngsi-ld:Device:ground-humidity-sensor-1"  
  ],  
  "smokeDetected": false,  
  "smokeDetectedConfidence": 0.9,  
  "fireDetected": false,  
  "fireDetectedConfidence": 0.8,  
  "fireRiskIndex": 0.1,  
  "litterCoverage": 0.6,  
  "relativeHumidity": 0.70,  
  "soilTemperature": 25  
}  
```  




  "id": "urn:ngsi-ld:FireForestStatus:id:JPEX:39548913",  
  "dateCreated": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2011-04-09T04:07:43Z"  
    }  
  },  
  "dateModified": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2011-04-09T04:07:43Z"  
    }  
  },  
  "source": {  
    "type": "Property",  
    "value": ""  
  },  
  "name": {  
    "type": "Property",  
    "value": "Ourense Forest - South"  
  },  
  "alternateName": {  
    "type": "Property",  
    "value": "Ourense Forest - South"  
  },  
  "description": {  
    "type": "Property",  
    "value": "Status of the Ourense Forest (south)"  
  },  
  "dataProvider": {  
    "type": "Property",  
    "value": ""  
  },  
  "owner": {  
    "type": "Property",  
    "value": [  
      "urn:ngsi-ld:FireForestStatus:items:IPCZ:25073160",  
      "urn:ngsi-ld:FireForestStatus:items:FPRB:78814414"  
    ]  
  },  
  "seeAlso": {  
    "type": "Property",  
    "value": [  
      "urn:ngsi-ld:FireForestStatus:items:XZGT:71938385",  
      "urn:ngsi-ld:FireForestStatus:items:GBWU:95431484"  
    ]  
  },  
  "location": {  
    "type": "Property",  
    "value": {  
      "type": "Point",  
      "coordinates": [  
        42.206302,  
      -7.887465  
      ]  
    }  
  },  
  "address": {  
    "type": "Property",  
    "value": {  
      "streetAddress": "",  
      "addressLocality": "Ourense",  
      "addressRegion": "Galicia",  
      "addressCountry": "ES",  
      "postalCode": "",  
      "postOfficeBoxNumber": "",  
      "areaServed": ""  
    }  
  },  
  "areaServed": {  
    "type": "Property",  
    "value": ""  
  },  
  "smokeDetected": {  
    "type": "Property",  
    "value": false  
  },  
  "smokeDetectedConfidence": {  
    "type": "Property",  
    "value": 0.9  
  },  
  "fireDetected": {  
    "type": "Property",  
    "value": false  
  },  
  "fireDetectedConfidence": {  
    "type": "Property",  
    "value": 0.8  
  },  
  "fireRiskIndex": {  
    "type": "Property",  
    "value": 0.1  
  },  
  "fireWeatherIndex ": {  
    "type": "Property",  
    "value": 864.6  
  },  
  "fireForestDailyRiskIndex": {  
    "type": "Property",  
    "value": 864.6  
  },  
  "litterCoverage": {  
    "type": "Property",  
    "value": 0.6  
  },  
  "relativeHumidity": {  
    "type": "Property",  
    "value": 0.7  
  },  
  "soilTemperature": {  
    "type": "Property",  
    "value": 25  
  }  
}  
```  