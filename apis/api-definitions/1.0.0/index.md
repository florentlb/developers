---
layout: "apiDefinition_1.0.0"
api-definition:
  specVersion: "4.0.0"
  info:
    name: "API Designer"
    version: "1.0.0"
    description: "This is the documentation of Talend API Designer's management API.\n\n**Prerequisite:** To manipulate this API, your user account must at least have the `API Designer` role."
    contact: {}
  contract:
    baseUrls:
      "0b86912f-899b-48fe-b2f8-7a81201c5a20":
        url: "https://apid.eu.cloud.talend.com/api/v1"
        description: "This is your API mock endpoint. When called, it will simulate the behavior of your API."
    unsortedElementOrder:
    - "#/contract/resources/4657f830-8e59-421d-b637-5734219e36f0"
    - "#/contract/resources/8bb691ac-a0c7-4d91-9216-dcd38dfec6bd"
    - "#/contract/resources/cda8ea7a-bd5d-447c-bc59-c46faef09ed9"
    - "#/contract/resources/66b48367-9cbd-4f21-a1ec-c545a0d346c4"
    - "#/contract/resources/6471097b-dee8-43ba-8d87-398b980cbd76"
    - "#/contract/resources/bb3f6a12-00d6-4d48-b950-66677d581393"
    - "#/contract/types/809db309-c0a1-459c-adbb-8a733e8eb1cd"
    - "#/contract/types/2c541e7e-186f-4023-8aba-376c58df35ac"
    - "#/contract/types/84b94400-affe-40d4-ae28-ea153c632bc5"
    - "#/contract/types/70d1910c-ac81-4822-a24c-052cd4a19905"
    - "#/contract/types/46437223-bd0d-4a3f-8717-da2d32faa7e3"
    - "#/contract/types/96256aae-c421-463c-8b6a-9d4513a66f7a"
    - "#/contract/types/ae32245f-ef70-4295-834f-d08cb1050557"
    - "#/contract/types/7a27a8a9-79f5-42ed-8464-a37ff1fca2c9"
    - "#/contract/types/ad7c65ea-b44b-48b7-bcda-45e76bb3e1ec"
    - "#/contract/types/2273e7cf-8019-4b6e-8dbb-98f6a4c3b19f"
    - "#/contract/types/429606f0-03c6-4d1e-9451-151284591bc1"
    - "#/contract/types/83a71fc5-3368-4ea4-a6de-0d2ff212f38a"
    - "#/contract/types/695b03fe-7f60-4a0e-aac4-afb32b8b3e10"
    - "#/contract/types/3a7f05f1-ee1d-4091-aabb-28ea621beef0"
    - "#/contract/types/16a207d6-ffe9-4013-8f21-da00f3d20237"
    - "#/contract/types/6cb8812f-7cee-4508-a4ad-bb774b159047"
    - "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
    securitySchemes:
      "49b3914f-8999-4741-89cc-bde1c23f48df":
        name: "Personal Access Token"
        type: "custom"
        description: "This API is secured by a Personal Access Token. To generate one see the [Talend Cloud documentation](https://help.talend.com/reader/I48H6c~0i42r2CnSb9d3tw/62smZ0FMeL~wFkFI6Bck4Q)"
        describedBy:
          headers:
            "60556abd-6864-4256-b133-1c3844e8cf5e":
              name: "Authorization"
              type: "STRING"
    securedBy:
    - scheme: "#/contract/securitySchemes/49b3914f-8999-4741-89cc-bde1c23f48df"
    resources:
      "4657f830-8e59-421d-b637-5734219e36f0":
        path: "/api-definitions"
        operations:
          "93bb50b7-d411-4fb6-b4c2-7cc27129a077":
            name: "Search an API definition"
            method: "GET"
            description: " User with granted access can search in the API definitions using filters."
            queryParameters:
              ecfbfb2c-82c0-4e12-913c-dbe0027886ec:
                name: "lastUpdatedDateTo"
                type: "DATETIME"
                format: "RFC3339"
                description: "Filter projects by last updated date\n\nList all projects modified before `lastUpdatedDateTo` (inclusive)"
              d916a137-32c4-42b4-8535-5fc54321434f:
                name: "creationDateTo"
                type: "DATETIME"
                format: "RFC3339"
                description: "Filter projects by creation date\n\nList all projects created before `creationDateTo` (inclusive)"
              a446aad4-c8cc-45f5-aa96-fced029cefa0:
                name: "sortOrder"
                type: "STRING"
                description: "Change the sorting order of the search results"
                default: "asc"
                enum:
                - "asc"
                - "desc"
                examples:
                  "7fa859aa-0b93-4ec6-96b2-2b34e96f476b":
                    value: "asc"
              b10f2480-736d-4bde-9bf1-70a7f1371912:
                name: "creationDateFrom"
                type: "DATETIME"
                format: "RFC3339"
                description: "Filter projects by creation date\n\nList all projects created after `creationDateFrom` (inclusive)"
              a9c4ff3d-d201-4b10-8b6d-98615c2172e9:
                name: "sortBy"
                type: "STRING"
                description: "Change the sorting filter of the search results"
                default: "lastUpdatedDate"
                enum:
                - "creationDate"
                - "lastUpdatedDate"
                - "name"
                examples:
                  cb8d8911-392c-430a-abc6-0d96350e75ce:
                    value: "name"
              "126f0814-f17a-405a-abd0-e61454ac306e":
                name: "lastUpdatedDateFrom"
                type: "DATETIME"
                format: "RFC3339"
                description: "Filter projects by last updated date\n\nList all projects modified after `lastUpdatedDateFrom` (inclusive)."
              "51b5aa3e-207a-491a-81da-43716101612d":
                type: "#/components/queryParameters/91a65648-987a-4973-9d46-93fcac76d2e0"
              "0e906668-9937-496a-b1c4-df0f366af4bf":
                name: "limit"
                type: "INTEGER"
                format: "INT32"
                description: "Max number of expected responses"
                examples:
                  b04316d3-e335-49d1-bfd3-6355f288b9da:
                    value: 20
              e34a07c8-6b23-49bc-958a-93664f1d6dbf:
                name: "version"
                type: "STRING"
                description: "Filter your results with the version of the API Definition"
                examples:
                  "22acdc50-21c6-412c-963c-a5b65ebbe1fd":
                    value: "1.0.0"
            responses:
              d0bee3ee-5e68-43e2-a604-dde591368cbc:
                status: "200"
                description: "Status 200"
                bodies:
                  da6a4512-523f-40eb-bcda-c827dfd5e620:
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/809db309-c0a1-459c-adbb-8a733e8eb1cd"
                    examples:
                      "244b23b0-3f3d-4785-9158-75fcc18cecb8":
                        value: "[\n  {\n   \"apiId\":\"95d709ad-da33-467f-88ea-e3bb8a629c82\",\n   \"id\": \"99b0d27a-523a-44f6-82cb-24832df61bd0\",\n   \"version\": \"1.0.0\",\n   \"name\":\"Task API\",\n   \"description\":\"Task API description\",\n   \"creationDate\":\"2019-07-05T08:59:45.712Z\",\n   \"lastUpdatedDate\":\"2019-07-05T08:59:45.712Z\",\n   \"creatorId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n   \"lastUpdaterId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n   \"sharings\":{\n      \"users\":[\n         {\n            \"userId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n            \"level\":{\n               \"code\":\"OWNER\",\n               \"label\":\"Owner\",\n               \"order\":1\n            },\n            \"firstName\":\"Joe\",\n            \"lastName\":\"C\",\n            \"fullName\":\"Joe C\"\n         }\n      ],\n      \"groups\":[\n\n      ]\n   }\n}\n]"
                    mediaTypes:
                    - "application/json"
              fb5621f9-28e0-4dd8-9069-4e10896b7138:
                status: "400"
                reference: "#/components/responses/3c4620f4-957e-4a33-80a4-993f99928aca"
              "4a4c0152-2c5d-4023-9de3-3a07e3716c4b":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              "00918e48-79ed-42d1-8604-7cc7a468d91c":
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "1809f85a-838a-426b-afa8-647f70dbb5b1":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
          "14f4b125-7ed7-4672-99b4-d62e1d7ebd0d":
            name: "Create a new API definition"
            method: "POST"
            description: "Create a new API definition in API Designer that you will own"
            queryParameters:
              b79d0677-5062-421b-a54f-096423996818:
                name: "format"
                type: "STRING"
                description: "The API definition format desired or passed in the input"
                default: "OpenApi3"
                enum:
                - "OpenApi3"
                - "Swagger20"
                - "Swagger12"
                - "Raml10"
                - "Raml08"
                examples:
                  c35aab4d-c416-45f0-b7ff-6a522afb9c88:
                    value: "OpenApi3"
              "52700497-3912-48d6-9d1c-8b813327b218":
                type: "#/components/queryParameters/9cdb2e98-4bba-4736-a3c3-dac009d14ead"
              "6b4c9300-0170-4477-b30a-2d57655064ec":
                type: "#/components/queryParameters/c29e62bb-337f-4613-b7b1-bbc74adbad62"
            headers:
              "0413dfaa-cb0a-4708-aca6-5ba4dad23d27":
                type: "#/components/headers/cbc72033-2a4e-4503-a29d-7f5d015e9972"
            bodies:
              "1666bc71-e9b4-4639-a93a-97b3120fd0d1":
                type: "#/contract/types/2273e7cf-8019-4b6e-8dbb-98f6a4c3b19f"
                mediaTypes:
                - "application/json"
                - "application/x-yaml"
                - "application/zip"
            responses:
              "4777b8ac-a25a-4bdf-8d1e-8b8b2e14d24d":
                status: "201"
                description: "Status 201"
                headers:
                  e34420f1-c3c1-44fe-ad5d-7463d37cf3fd:
                    name: "Location"
                    type: "STRING"
                    description: "URL of the new API definition."
                    examples:
                      cabd7041-a2c2-4d44-b8be-f7ead03ec460:
                        value: "https://apid.eu.cloud.talend.com/api/v1/api-definitions/bfc2b4b3-78fa-4f96-a3a8-d372865f1139"
                bodies:
                  d17cd519-2083-40c7-aa3b-9a3218eb6a6b:
                    type: "#/contract/types/6cb8812f-7cee-4508-a4ad-bb774b159047"
                    mediaTypes:
                    - "application/json"
              d7235ad1-ca43-4b02-92cb-701296506e18:
                status: "400"
                reference: "#/components/responses/23ac0ed8-07b3-4b6f-953a-f2765bdfb5a8"
              "58e290e0-89e9-4e34-ba7d-73513c394499":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              fadade35-21f9-467b-8e7a-a064950c8b2e:
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              dbaacee2-b513-4def-ad82-93a4b0a8b476:
                status: "412"
                reference: "#/components/responses/81cdd681-2d83-4ba2-9f5e-8524937d1f11"
              ddd9a792-b7a3-468b-be87-b81aac3f48a2:
                status: "415"
                reference: "#/components/responses/96badfcb-8b34-441b-8571-39e8a48aefb6"
              dc8cfac5-e6d3-4512-8003-2dfb12a43a06:
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
      "8bb691ac-a0c7-4d91-9216-dcd38dfec6bd":
        path: "/api-definitions/{id}"
        pathVariables:
          fb2d0aef-0ced-4286-ad2f-a5f1bb7e1d11:
            type: "#/components/pathVariables/3f7ed797-105d-4dd7-bc0c-77504436b1a0"
        operations:
          bff9e98a-a95c-486e-a8a3-9caf5bd99fe2:
            name: "Fetch an API definition"
            method: "GET"
            description: "Fetch an API definition in a specific format using its ID"
            queryParameters:
              "38c16f54-abd9-4ca5-a391-67f6f165c83d":
                type: "#/components/queryParameters/52a8dc1c-e9cb-4c15-8bf2-53e547d93f83"
              "2dc8fc5e-35c1-4884-b1a6-d9f0c0f2f5cd":
                type: "#/components/queryParameters/a9f20be2-39f0-459b-b5f4-e8e54150fad8"
            headers:
              "8443e000-60d6-4370-a192-284f1b66b1a7":
                type: "#/components/headers/d6cb867f-acaa-4b4a-bfdf-6513cc1a0c41"
            responses:
              "76a43442-9c20-4d84-8441-674377182439":
                status: "200"
                description: "Status 200"
                headers:
                  "3c8f6dd9-e27c-4527-a6da-3d6479df7922":
                    name: "X-Audit-Location"
                    type: "STRING"
                    description: "Contains the URL that allows the user to fetch the report of the export.\n\nAppears only if the report is not empty."
                    examples:
                      "62b9cfcf-0e75-4141-8011-91885dd1eb34":
                        value: "http://api.eu.talend.com/v1/api-definition/a609483f-72a5-4937-a1be-243cb507fffb/audit"
                  "91e9863f-a802-46d0-97e9-5d1dfb0c9024":
                    name: "X-V2-ApiId"
                    type: "STRING"
                    description: "Reference of the `api_id` used in V2"
                  "61808796-a8ae-4532-9959-86c3eda302a2":
                    name: "X-V2-VersionId"
                    type: "STRING"
                    description: "Reference of the `version_id` used in V2"
                bodies:
                  "75e5fc15-0c98-4e6d-b0f2-ce158f2aa006":
                    type: "#/contract/types/2273e7cf-8019-4b6e-8dbb-98f6a4c3b19f"
                    mediaTypes:
                    - "application/json"
                    - "application/x-yaml"
              deddcd5f-81d8-47f3-a79a-c4bead04349d:
                status: "400"
                reference: "#/components/responses/3c4620f4-957e-4a33-80a4-993f99928aca"
              "91ddc550-8ef2-4961-8379-36558d11d0f2":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              f8b1adb0-f99b-4219-9699-9492fc958e2d:
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "121e9243-9d54-4106-b58b-e8ab4782f7b6":
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              c99bb66a-dbaa-4c9b-ad40-84c4f872c80e:
                status: "415"
                reference: "#/components/responses/96badfcb-8b34-441b-8571-39e8a48aefb6"
              "85fe42c2-7885-4b50-9e33-af5d9d3b58e2":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
          "6a69d591-f5d6-4b2e-8848-9676264c6ba7":
            name: "Replace an existing API definition"
            method: "PUT"
            description: "Replace an existing API definition by another definition\n\n*TBV: May be not available for API/version change (we propose an error message with a link to V2 instead)*"
            queryParameters:
              "570c5f46-1b82-4d5c-8feb-5ff66cc68941":
                name: "format"
                type: "STRING"
                description: "The API definition format desired or passed in the input"
                default: "OpenApi3"
                enum:
                - "OpenApi3"
                - "Swagger20"
                - "Swagger12"
                - "Raml10"
                - "Raml08"
              "3ce9a43c-1c4d-480a-b253-4f28666aef5a":
                type: "#/components/queryParameters/9cdb2e98-4bba-4736-a3c3-dac009d14ead"
              c0b1f099-c805-44d4-9ee1-abb6816ef216:
                type: "#/components/queryParameters/c29e62bb-337f-4613-b7b1-bbc74adbad62"
            headers:
              bc8b9481-a5ed-46c2-b18e-027f81c1062b:
                type: "#/components/headers/cbc72033-2a4e-4503-a29d-7f5d015e9972"
            bodies:
              "643e22f6-2333-4aed-acd8-f0b738e0cfd9":
                type: "#/contract/types/2273e7cf-8019-4b6e-8dbb-98f6a4c3b19f"
                mediaTypes:
                - "application/json"
                - "application/x-yaml"
            responses:
              ea354e58-44d0-4040-8647-93464afd0321:
                status: "200"
                description: "Acknowledgement, the replacement is complete"
                bodies:
                  ba4ee5e9-f501-4405-bfc4-84d8adfa0e4b:
                    type: "#/contract/types/6cb8812f-7cee-4508-a4ad-bb774b159047"
                    mediaTypes:
                    - "application/json"
              e93cb543-b6c0-44e2-b3b1-b9eb1dbb1d4c:
                status: "400"
                reference: "#/components/responses/423ced9c-f2f0-4837-9e41-008540bd03e1"
              a0b100ac-8e58-4022-a6be-e53818e200a0:
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              "900e5084-865a-43db-9e94-5f25ab4c25c8":
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              ad242cba-63d9-4998-955a-3bfaa2b6e82e:
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              "7d96f73f-53d5-41aa-b15f-001a190db6cd":
                status: "412"
                reference: "#/components/responses/81cdd681-2d83-4ba2-9f5e-8524937d1f11"
              "00a95e1d-1870-4848-8a9a-c8b0bc7d06c6":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
          "8e872735-4ca2-4580-9e91-e8fd10f34685":
            name: "Delete an API definition"
            method: "DELETE"
            description: "Delete an API definition using its ID\n\n*Note: This action is available only for the owner*"
            responses:
              "1fc42028-c164-4c41-94df-35beaac7bfd9":
                status: "204"
                description: "Acknowledgement, the deletion is complete"
              bf028ae1-3330-4bdd-a3fc-6f5a44952b94:
                status: "400"
                reference: "#/components/responses/12b47b66-8935-405a-a3d8-05032612178a"
              "4479c8a8-5595-4b0f-828f-7a6e527a4ad7":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              "1bccf7f3-10fb-4775-84fb-96f66300e87e":
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "9f39dff8-58ea-4d0a-a930-6d99b6c73e93":
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              afc2d5a2-8a4f-42e7-876d-0168b8cf1803:
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
      cda8ea7a-bd5d-447c-bc59-c46faef09ed9:
        path: "/api-definitions/{id}/sharings"
        pathVariables:
          "1a251b23-a4bc-4adc-84de-4059f16e0ee9":
            type: "#/components/pathVariables/3f7ed797-105d-4dd7-bc0c-77504436b1a0"
        operations:
          "69527c92-2a7d-4150-9260-dc9427b616de":
            name: "Get sharing configuration of an API definition"
            method: "GET"
            description: "Retrieve all the users and groups that have access to the API definition (along with their access level)"
            responses:
              "6c6c426f-2835-4b01-b9a5-cc72b4144bd8":
                status: "200"
                description: "Status 200"
                bodies:
                  "534fa3e3-3d72-41ae-8599-84987dc1b5da":
                    type: "#/contract/types/429606f0-03c6-4d1e-9451-151284591bc1"
                    mediaTypes:
                    - "application/json"
              "4ddfbdf1-1ad7-4566-84fc-db62126921ba":
                status: "400"
                reference: "#/components/responses/3881f958-a6d3-415d-aacb-1584d4ce3b51"
              "3da74db2-5d43-4fc4-9c34-8b52208b7985":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              "466ba062-7381-49f0-9574-b1310419b277":
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              fc42cae8-18d5-4a0a-b79c-2f039b12a929:
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              "04ea8018-4457-4f12-aace-676b0e597c3e":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
          "69581254-72b6-47cd-88ff-a9b37ee8cde4":
            name: "Update sharing configuration of an API definition"
            method: "PUT"
            description: "Set the users and groups that should be granted access to this API definition"
            bodies:
              d897cc45-3494-4835-bad8-31f583b448ee:
                type: "#/contract/types/429606f0-03c6-4d1e-9451-151284591bc1"
                mediaTypes:
                - "application/json"
            responses:
              "64e0e406-5888-4b4b-8c2f-6c746cb13f0b":
                status: "204"
                description: "Status 204"
              "53852141-d668-439e-b7da-998ee4242e76":
                status: "400"
                description: "- the payload doesn't contains required data"
                bodies:
                  "6642d1fc-31fa-46e6-a50d-6bd854384af8":
                    type: "OBJECT"
                    properties:
                      "045d1070-47e7-4c15-a9ce-3fb203e831ab":
                        name: "message"
                        type: "STRING"
                        required: true
                      "88d4bf7b-dd5a-461f-9a69-f74857d8f98f":
                        name: "status"
                        type: "STRING"
                        description: "**Value:** 400"
                        required: true
                    mediaTypes:
                    - "application/json"
              a42d86dc-2a2d-476d-be7c-928a1966c6ab:
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              cd61d29e-c1ed-472f-bdcb-29950b7b6296:
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "7f429cff-fafa-403f-81ab-69546d3a8445":
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              "5ea24dcb-6230-47c1-a9d1-0305fd1bf4ac":
                status: "422"
                description: "Status 422"
                bodies:
                  "21cab947-790b-46da-85c7-35d244230269":
                    type: "OBJECT"
                    properties:
                      "23cadda4-b2c3-4272-85db-7053798280c6":
                        name: "message"
                        type: "STRING"
                        required: true
                      "45e26b3d-ddcd-47a5-b671-8a749d5ce6ae":
                        name: "status"
                        type: "INTEGER"
                        format: "INT32"
                        required: true
                    examples:
                      "8a28ba5b-8e2c-4a60-ad0f-7e1134cb2d14":
                        value: "{\n  \"message\": \"string\",\n  \"status\": 422\n}"
                    mediaTypes:
                    - "*/*"
              "6e060063-d88a-4179-8f6b-65b4b492c643":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
      "66b48367-9cbd-4f21-a1ec-c545a0d346c4":
        path: "/api-definitions/{id}/metadata"
        pathVariables:
          "9bc32ec4-afd5-467c-80b3-839c92077b6b":
            type: "#/components/pathVariables/3f7ed797-105d-4dd7-bc0c-77504436b1a0"
        operations:
          cc6aa963-d9d7-428f-bfbf-6dff2e5851a6:
            name: "Fetch an API definition metadata"
            method: "GET"
            responses:
              "0417d823-70a1-4ef7-9208-e9cd16a82f50":
                status: "200"
                description: "Status 200"
                bodies:
                  "39e4915f-37b5-4bd5-b70d-6e14f57b993c":
                    type: "#/contract/types/809db309-c0a1-459c-adbb-8a733e8eb1cd"
                    mediaTypes:
                    - "application/json"
              "0114362b-e661-4800-8979-9c9de5056346":
                status: "400"
                reference: "#/components/responses/3881f958-a6d3-415d-aacb-1584d4ce3b51"
              "7c65cb5e-cd6a-4295-8de6-a9761773da3b":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              e9c84294-4ef4-4c3a-a205-2d3072cc5426:
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "26afbdad-8678-4da8-87ce-ab6aceeb6709":
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              d0c91a56-fff7-4a3d-9524-fda70ab43b50:
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
      "6471097b-dee8-43ba-8d87-398b980cbd76":
        path: "/api-definitions/sharings/eligibles"
        operations:
          cd7b9ff0-5380-4733-a050-cb843fd3cffb:
            name: "Get eligible users and groups"
            method: "GET"
            description: "Returns the users and groups that the user can share an API definition to"
            responses:
              "26792807-7e88-4390-8e13-6f23f57a9d44":
                status: "200"
                description: "Status 200"
                bodies:
                  "394de6e5-1600-458b-a14c-20540d3ea689":
                    type: "#/contract/types/16a207d6-ffe9-4013-8f21-da00f3d20237"
                    mediaTypes:
                    - "application/json"
              ee0ab626-89d3-491d-827e-3124dc6fce4c:
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              "1c395c7e-62a6-46b0-a5c9-864943d8a09c":
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "1cd5c314-88a5-4b87-ac48-1e2e951af703":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
      bb3f6a12-00d6-4d48-b950-66677d581393:
        path: "/api-definitions/{id}/audit"
        pathVariables:
          aac309a9-f97e-4020-9f1c-58e359813ef9:
            name: "id"
            type: "STRING"
            required: true
        operations:
          "9eac5dc8-24d7-4a51-9962-2ce05c1c6248":
            name: "Fetch the export audit of an API definition"
            method: "GET"
            queryParameters:
              "0360aac1-95c3-4067-affe-852c82350b9a":
                name: "format"
                type: "STRING"
                required: true
                enum:
                - "OpenApi3Aws"
                - "Swagger20Azure"
                examples:
                  "147bd9ef-f958-4c3a-a0e8-cbdc0bcc8f34":
                    value: "OpenApi3Aws"
            responses:
              "3b9a8594-1146-417a-a67e-7f3bc02bedca":
                status: "200"
                description: "Status 200"
                bodies:
                  "6130bbd4-fbec-465b-8457-6287b50f0ad5":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
                    examples:
                      "6d1ebc0b-59ab-4371-802e-7d816f517037":
                        value: "[\n  {\n   \"message\":\"The base URLs must be absolute. The server 'serverUrl' is ignored.\",\n   \"code\":\"OAS3_IMPORT_RELATIVE_PATH_SERVER\",\n   \"field\":\"Server 1\",\n   \"type\":\"warning\"\n}\n]"
                    mediaTypes:
                    - "application/json"
                  "04e57488-2ba4-40b8-8111-27ac44efb79f":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
                    mediaTypes:
                    - "application/x-yaml"
              "7fca184a-d80d-4c16-875f-318ba4961c6a":
                status: "400"
                reference: "#/components/responses/3c4620f4-957e-4a33-80a4-993f99928aca"
              "29068894-5d99-4161-beaf-bcfb99f2a801":
                status: "401"
                reference: "#/components/responses/cf1fea88-d209-44a9-a068-60682408eb1c"
              e53eb581-8a17-47fb-8180-66596082b676:
                status: "403"
                reference: "#/components/responses/19ab93ff-4dc8-49f3-bbf8-8496d5342c02"
              "53a0ba8f-7633-47ee-88d7-d2240e44ebb0":
                status: "404"
                reference: "#/components/responses/4385fdf0-582e-43e3-badb-343dc93d8696"
              e6786498-37e0-407e-beb1-ccdf8e4687a8:
                status: "415"
                reference: "#/components/responses/96badfcb-8b34-441b-8571-39e8a48aefb6"
              "80d6c44e-4a2b-40e3-a8fb-ad8aac65cbcb":
                status: "500"
                reference: "#/components/responses/e3ba95c4-7093-4b25-acb4-613ec73bb0c2"
    types:
      "809db309-c0a1-459c-adbb-8a733e8eb1cd":
        name: "ApiDefinitionMetadata"
        type: "OBJECT"
        description: "Summarized representation of an API definition"
        properties:
          f258103d-a498-4a5e-ae0a-c29a3e0ef26b:
            name: "id"
            type: "STRING"
            description: "API definition ID"
            required: true
            examples:
              d968dae4-6583-40f8-b49c-9f77f508c10b:
                value: "95d709ad-da33-467f-88ea-e3bb8a629c82"
          "3bd654ee-3935-4f04-b0da-d9efb9109eec":
            name: "name"
            type: "STRING"
            description: "API definition name"
            required: true
            examples:
              "76ef2513-0fed-4278-8703-4580aea3221d":
                value: "Task API"
          "8449cdeb-889b-458f-bc85-c9c167f8e45d":
            name: "apiId"
            type: "STRING"
            description: "API ID (for API Designer Management API v2)"
            required: true
          "210189ef-c078-4ea9-a7fd-f17a74f7b8e1":
            name: "version"
            type: "STRING"
            description: "The API definition version"
            required: true
          fa311022-2c61-428f-bf69-13a797987156:
            name: "description"
            type: "STRING"
            description: "API definition description"
            examples:
              ce3c088f-ae16-4fda-8aa6-de5f0774dd60:
                value: "Task API description"
          afa92f35-e076-4619-9938-26065ffa136c:
            name: "creatorId"
            type: "STRING"
            description: "User ID of the creator."
            required: true
            examples:
              "80251b3f-ac15-49fc-bdcb-2f34e905ea48":
                value: "db65aa86-2d8e-439b-a5aa-862d8e039bfd"
          da282c4e-a289-4e5f-b33a-8da9e60c4f61:
            name: "lastUpdaterId"
            type: "STRING"
            description: "User ID of the last updater."
            required: true
            examples:
              c4734de4-dc6e-4994-b735-be3bd91a277c:
                value: "db65aa86-2d8e-439b-a5aa-862d8e039bfd"
          "12a36e69-87d2-456e-be6c-a03575ac5197":
            name: "creationDate"
            type: "DATETIME"
            format: "RFC3339"
            required: true
          "7a66d951-0395-4f92-b696-b0c76a439f81":
            name: "lastUpdatedDate"
            type: "DATETIME"
            format: "RFC3339"
            required: true
          "96e76154-c3ed-4a26-9537-974553400511":
            name: "sharings"
            type: "#/contract/types/429606f0-03c6-4d1e-9451-151284591bc1"
            required: true
        examples:
          "277e6ec1-552f-41ff-a300-c17d071e170a":
            value: "{\n   \"apiId\":\"95d709ad-da33-467f-88ea-e3bb8a629c82\",\n   \"id\":\"95d709ad-da33-467f-88ea-e3bb8a629c82\",\n   \"name\":\"Task API\",\n   \"version\": \"1.0.0\",\n   \"apiId\": \"99b0d27a-523a-44f6-82cb-24832df61bd0\",\n   \"description\":\"Task API description\",\n   \"creationDate\":\"2019-07-05T08:59:45.712Z\",\n   \"lastUpdatedDate\":\"2019-07-05T08:59:45.712Z\",\n   \"creatorId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n   \"lastUpdaterId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n   \"sharings\":{\n      \"users\":[\n         {\n            \"userId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n            \"level\":{\n               \"code\":\"OWNER\",\n               \"label\":\"Owner\",\n               \"order\":1\n            },\n            \"firstName\":\"Joe\",\n            \"lastName\":\"C\",\n            \"fullName\":\"Joe C\"\n         }\n      ],\n      \"groups\":[\n\n      ]\n   }\n}"
      "2c541e7e-186f-4023-8aba-376c58df35ac":
        name: "OAS3.0"
        type: "OBJECT"
        description: "See specifications in order to find the entire description of the format.\n\n**Specifications:** [OpenAPI Specifications](https://github.com/OAI/OpenAPI-Specification)"
      "84b94400-affe-40d4-ae28-ea153c632bc5":
        name: "OAS-Swagger2.0"
        type: "OBJECT"
        description: "See specifications in order to find the entiere description of the format.\n\n**Specifications:**  [OAS/Swagger 2.0 specifications](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md)"
      "70d1910c-ac81-4822-a24c-052cd4a19905":
        name: "ApiPortalContent"
        type: "OBJECT"
        description: "Definition used by Talend Developer Portal"
        examples:
          "3dcf1eeb-7730-45c6-9f41-f20cf5dc0552":
            value: "---\nlayout: apiDefinition_1.0.0\napi-definition:\n    specVersion: \"4.0.0\"\n    info:\n      name: \"sample\"\n      version: \"1.0.0\"\n      description: \"No description\"\n      contact:\n        name: John Doe\n        url: http://example.com\n        email: john.doe@example.com\n    contract: {}\n---"
      "46437223-bd0d-4a3f-8717-da2d32faa7e3":
        name: "Swagger1.2"
        type: "OBJECT"
        description: "See specifications in order to find the entiere description of the format.\n\n**Specifications:**  [Swagger 1.2 specifications](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/1.2.md)"
      "96256aae-c421-463c-8b6a-9d4513a66f7a":
        name: "RAML1.0"
        type: "OBJECT"
        description: "See specifications in order to find the entiere description of the format.\n\n**Specifications:**  [RAML 1.0 Specifications](https://github.com/raml-org/raml-spec/blob/master/versions/raml-10/raml-10.md)"
      ae32245f-ef70-4295-834f-d08cb1050557:
        name: "RAML0.8"
        type: "OBJECT"
        description: "See specifications in order to find the entiere description of the format\n\n**Specifications:**  [RAML 0.8 Specifications](https://github.com/raml-org/raml-spec/blob/master/versions/raml-08/raml-08.md)"
      "7a27a8a9-79f5-42ed-8464-a37ff1fca2c9":
        name: "OAS-Swagger2.0-for-Azure"
        type: "OBJECT"
        description: "See Azure gateway documentation"
      ad7c65ea-b44b-48b7-bcda-45e76bb3e1ec:
        name: "OAS3.0-for-AWS"
        type: "OBJECT"
        description: "See AWS Gateway documentation"
      "2273e7cf-8019-4b6e-8dbb-98f6a4c3b19f":
        name: "One of all API definition formats"
        type: "ONEOF"
        oneOf:
        - "#/contract/types/84b94400-affe-40d4-ae28-ea153c632bc5"
        - "#/contract/types/2c541e7e-186f-4023-8aba-376c58df35ac"
        - "#/contract/types/ae32245f-ef70-4295-834f-d08cb1050557"
        - "#/contract/types/96256aae-c421-463c-8b6a-9d4513a66f7a"
        - "#/contract/types/46437223-bd0d-4a3f-8717-da2d32faa7e3"
        - "#/contract/types/ad7c65ea-b44b-48b7-bcda-45e76bb3e1ec"
        - "#/contract/types/7a27a8a9-79f5-42ed-8464-a37ff1fca2c9"
        - "#/contract/types/70d1910c-ac81-4822-a24c-052cd4a19905"
      "429606f0-03c6-4d1e-9451-151284591bc1":
        name: "SharingSet"
        type: "OBJECT"
        description: "A SharingSet is a representation of the users and groups that are allowed access to an API definition.\n\n**Important:** A list of users and a list of groups **must** be provided, even if it may be empty.\n\n**Data constraints:**\n- a SharingSet must contain a single owner (SharingLevel) and it must be a SharingUser (contained in `users` array)"
        properties:
          "26add705-2f8a-4ded-b6ec-01076a81c8b4":
            name: "users"
            type: "ARRAY"
            description: "Users that have access to the API. \n\nNB: Must contain a user (and only one) with owner sharing level."
            required: true
            items:
              type: "#/contract/types/3a7f05f1-ee1d-4091-aabb-28ea621beef0"
          f24827b9-22e7-4aa9-b5ab-bc72db9df5b5:
            name: "groups"
            type: "ARRAY"
            description: "Groups that have access to the API."
            required: true
            items:
              type: "#/contract/types/695b03fe-7f60-4a0e-aac4-afb32b8b3e10"
        examples:
          d481c75f-0823-418e-8294-4d3b6a3cc9d6:
            value: "{\n\t\"users\":\n\t    [\n\t        {\n                \"userId\": \"UUID-user2\",\n                \"lastName\": \"Doe\",\n                \"firstName\": \"John\",\n                \"level\": {\n                    \"code\": \"OWNER\",\n                    \"label\": \"Owner\",\n                    \"order\": 1\n                 }\n    \t\t}\n        ],\n\t\"groups\":\n        [\n            {\n                \"groupId\": \"UUID-group1\",\n                \"groupName\": \"Human resources\",\n                \"level\": {\n                    \"code\": \"WRITER\",\n                    \"label\": \"Editor\",\n                    \"order\": 2\n                }\n            }\n        ],\n    \"tenantSharing\": []\n}"
      "83a71fc5-3368-4ea4-a6de-0d2ff212f38a":
        name: "SharingLevel"
        type: "OBJECT"
        description: "Describes the permissions that a user or group possesses on an API definition."
        properties:
          fb2d92af-07d4-483b-b00f-e2e902aed396:
            name: "code"
            type: "STRING"
            required: true
            enum:
            - "WRITER"
            - "OWNER"
          "021651ff-1329-4197-81cb-dad8ceabc086":
            name: "label"
            type: "STRING"
            restrictions: "READ_ONLY"
            required: true
          fcdb4769-55df-4b7d-b77f-4fc6c4322e92:
            name: "order"
            type: "INTEGER"
            format: "INT32"
            restrictions: "READ_ONLY"
            required: true
        examples:
          "33fc4189-15f0-4b2a-8a50-9d2dec44e87a":
            value: "{\n  \"code\": \"WRITER\",\n  \"label\": \"Editor\",\n  \"order\": 2\n}"
      "695b03fe-7f60-4a0e-aac4-afb32b8b3e10":
        name: "SharingGroup"
        type: "OBJECT"
        description: "Describes a group of users."
        properties:
          "471624cd-4ae2-4f4b-b94c-988dae660249":
            name: "groupId"
            type: "STRING"
            required: true
          b23fcddf-9b43-4ebc-bc7a-7c0cedc9174f:
            name: "groupName"
            type: "STRING"
            restrictions: "READ_ONLY"
          "97df7ad8-c858-4df8-9f80-92fcd3b17dcb":
            name: "level"
            type: "#/contract/types/83a71fc5-3368-4ea4-a6de-0d2ff212f38a"
            required: true
        examples:
          "186fba46-b36e-4737-bf1d-2c29da6c247f":
            value: "{\n   \"groupId\":\"UUID-group1\",\n   \"groupName\":\"Human resources\",\n   \"level\":{\n      \"code\":\"WRITER\",\n      \"label\":\"Editor\",\n      \"order\":2\n   }\n}"
      "3a7f05f1-ee1d-4091-aabb-28ea621beef0":
        name: "SharingUser"
        type: "OBJECT"
        description: "Describe a user"
        properties:
          "2201c441-8303-4a77-9e1c-a30ffcf1561b":
            name: "userId"
            type: "STRING"
            required: true
          "78c5db6e-1347-4f1e-aa6b-cda72144a486":
            name: "lastName"
            type: "STRING"
            restrictions: "READ_ONLY"
            required: true
          "720a7275-f771-4f03-b411-3aaeebd75be2":
            name: "firstName"
            type: "STRING"
            restrictions: "READ_ONLY"
            required: true
          d4ce27b5-126d-46bc-85ca-6a97b8d54700:
            name: "level"
            type: "#/contract/types/83a71fc5-3368-4ea4-a6de-0d2ff212f38a"
            required: true
        examples:
          eefcef33-daf1-4c4c-a706-352ab698269b:
            value: "{\n   \"userId\":\"UUID-user2\",\n   \"lastName\":\"Doe\",\n   \"firstName\":\"John\",\n   \"level\":{\n      \"code\":\"OWNER\",\n      \"label\":\"Owner\",\n      \"order\":1\n   }\n}"
      "16a207d6-ffe9-4013-8f21-da00f3d20237":
        name: "SharingEligibles"
        type: "OBJECT"
        description: "The users and groups that you can share an API definition with"
        properties:
          a8cc9624-b25b-46a1-8b9e-48762c96f7a9:
            name: "users"
            type: "ARRAY"
            required: true
            items:
              type: "OBJECT"
              properties:
                ee385b55-c2f9-4399-9051-b52175b95196:
                  name: "userId"
                  type: "STRING"
                  required: true
                "915befe8-0185-49e6-83c1-59952645f81a":
                  name: "lastName"
                  type: "STRING"
                  required: true
                "19f3ee6c-1b6c-4593-bc8b-eee95a91b4c5":
                  name: "firstName"
                  type: "STRING"
                  required: true
              examples:
                "6419a941-60e6-4281-b8a7-46d5275856fc":
                  value: "{\n    \"userId\": \"UUID-user2\",\n    \"lastName\": \"Doe\",\n    \"firstName\": \"John\"\n}"
          dd4b52ce-b592-4947-98ea-2876bde2f87b:
            name: "groups"
            type: "ARRAY"
            required: true
            items:
              type: "OBJECT"
              properties:
                fd0dcb41-b0f3-4581-abee-2ec2d4f475ab:
                  name: "groupId"
                  type: "STRING"
                  required: true
                "0320266b-fe4c-4748-84b7-1b9e5df43282":
                  name: "groupName"
                  type: "STRING"
                  required: true
              examples:
                db3b9162-22d5-4ac7-9696-846ec03b6320:
                  value: " {\n    \"groupId\": \"UUID-group1\",\n    \"groupName\": \"Human resources\"\n}"
          ea1392af-94c1-4c34-b0b4-469bc765d2cb:
            name: "tenantSharing"
            type: "ARRAY"
            required: true
            items:
              type: "STRING"
        examples:
          "5736cec3-bea6-4fde-91de-f447722ec5a6":
            value: "{\n\t\"users\":\n\t    [\n\t        {\n                \"userId\": \"UUID-user2\",\n                \"lastName\": \"Doe\",\n                \"firstName\": \"John\"\n    \t\t},\n            {\n                \"userId\": \"UUID-user3\",\n                \"lastName\": \"Stane\",\n                \"firstName\": \"Bob\"\n            }\n        ],\n\t\"groups\":\n        [\n            {\n                \"groupId\": \"UUID-group1\",\n                \"groupName\": \"Human resources\"\n            },\n            {\n                \"groupId\": \"UUID-group2\",\n                \"groupName\": \"Sales\"\n            }\n        ],\n    \"tenantSharing\":[]        \n}"
      "6cb8812f-7cee-4508-a4ad-bb774b159047":
        name: "ApiDefinitionWriteResponse"
        type: "OBJECT"
        properties:
          "20017f4e-13b1-42bf-8922-82be28fffe57":
            name: "metadata"
            type: "#/contract/types/809db309-c0a1-459c-adbb-8a733e8eb1cd"
            required: true
          a28e07c3-847e-49fb-9294-c5f5b8101fd1:
            name: "validationMessages"
            type: "ARRAY"
            required: true
            items:
              type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
        examples:
          ad5af638-958e-48c9-96f4-ed0228efd361:
            value: "{\n   \"metadata\":{\n      \"id\":\"008ea8c1-75b5-409e-a930-2b0f49508e86\",\n      \"name\":\"Test\",\n      \"apiId\": \"99b0d27a-523a-44f6-82cb-24832df61bd0\",\n      \"version\": \"1.0.0\",\n      \"creationDate\":\"2019-07-05T10:20:08.576Z\",\n      \"lastUpdatedDate\":\"2019-07-05T10:20:08.576Z\",\n      \"sharings\":{\n         \"users\":[\n            {\n               \"userId\":\"db65aa86-2d8e-439b-a5aa-862d8e039bfd\",\n               \"level\":{\n                  \"code\":\"OWNER\",\n                  \"label\":\"Propriétaire\",\n                  \"order\":1\n               },\n               \"firstName\":\"Pierre\",\n               \"lastName\":\"C\",\n               \"fullName\":\"Pierre C\"\n            }\n         ],\n         \"groups\":[\n\n         ]\n      }\n   },\n   \"validationMessages\":[\n      {\n         \"message\":\"The base URLs must be absolute. The server 'serverUrl' is ignored.\",\n         \"code\":\"OAS3_IMPORT_RELATIVE_PATH_SERVER\",\n         \"field\":\"Server 1\",\n         \"type\":\"warning\"\n      }\n   ]\n}"
      "7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f":
        name: "ApiDefinitionMessage"
        type: "OBJECT"
        properties:
          "699eef3e-965e-4c33-8fa2-0749bf4e523d":
            name: "message"
            type: "STRING"
            required: true
          "53d7ed51-67c9-4189-b364-dc51fbd8e2e8":
            name: "type"
            type: "STRING"
            required: true
            enum:
            - "info"
            - "warning"
            - "error"
          a4fb7f42-021e-4091-9c78-25f2ac434156:
            name: "code"
            type: "STRING"
            required: true
          "4b715332-e2cd-47b9-a525-b1e85f1e11c5":
            name: "field"
            type: "STRING"
          b484a8ca-5678-46fb-8936-df9221325bd4:
            name: "location"
            type: "STRING"
        examples:
          dfedf60b-e3e2-4608-9df7-de23cd961736:
            value: "{\n   \"message\":\"The base URLs must be absolute. The server 'serverUrl' is ignored.\",\n   \"code\":\"OAS3_IMPORT_RELATIVE_PATH_SERVER\",\n   \"field\":\"Server 1\",\n   \"type\":\"warning\"\n}"
  components:
    pathVariables:
      "3f7ed797-105d-4dd7-bc0c-77504436b1a0":
        name: "id"
        componentName: "id"
        type: "STRING"
        description: "API definition ID\n\n**Format:** [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier)"
        required: true
        examples:
          be7cbd1d-3844-4016-b221-7eff074d7ccb:
            value: "a609483f-72a5-4937-a1be-243cb507fffb"
    queryParameters:
      a9f20be2-39f0-459b-b5f4-e8e54150fad8:
        name: "format"
        componentName: "format"
        type: "STRING"
        description: "The API definition output format"
        default: "OpenApi3"
        enum:
        - "OpenApi3"
        - "Swagger20"
        - "Swagger12"
        - "Raml10"
        - "Raml08"
        - "OpenApi3Aws"
        - "Swagger20Azure"
        - "ApiPortalContent"
        examples:
          "96cb5ffa-4c88-4240-9d96-f376d36dd735":
            value: "OpenApi3"
      "52a8dc1c-e9cb-4c15-8bf2-53e547d93f83":
        name: "talendExtensions"
        componentName: "talendExtensions"
        type: "BOOLEAN"
        description: "Export (or not) Talend Extensions inside the API definition"
        default: false
      "91a65648-987a-4973-9d46-93fcac76d2e0":
        name: "name"
        componentName: "name"
        type: "STRING"
        description: "Filter your results with the name of the API Definition\n\nThis filter allow to use a query language:\n- `*`: to replace 0 or more characters\n- `?`: to replace 1 characters\n- `\\`: use to escape a `*` or `?`\n\n**Examples:**\n - `a*a` -> return: all API definitions with a name that begins and ends with “a”\n - `*a` -> return: all API definitions with a name that ends with “a”\n - `a*` -> return: all API definitions with a name that begins with “a”\n - `a`-> return: all API definitions with the name equals to “a”\n - `a\\*` -> return: all API definitions with the name equals to “a*”"
        examples:
          dc5bf853-d860-424a-af5a-608eda880b1b:
            value: "my_name"
      c29e62bb-337f-4613-b7b1-bbc74adbad62:
        name: "failOnWarnings"
        componentName: "failOnWarnings"
        type: "BOOLEAN"
        description: "Stop the process at the first warning on model transformation"
        default: false
      "9cdb2e98-4bba-4736-a3c3-dac009d14ead":
        name: "mainFile"
        componentName: "mainFile"
        type: "STRING"
        description: "Name of the main API definition file when importing a multi-file definition (a ZIP file)"
        examples:
          cfa2018e-e596-4e43-a485-a40053483188:
            value: "file.json"
    headers:
      cbc72033-2a4e-4503-a29d-7f5d015e9972:
        name: "Content-Type"
        componentName: "Content-Type"
        type: "STRING"
        description: "The input format of the API contract"
        required: true
        enum:
        - "application/x-yaml"
        - "application/json"
        - "application/zip"
        examples:
          "6c6a7cd2-7852-4c3b-9676-e0cb0edb2174":
            value: "application/json"
      d6cb867f-acaa-4b4a-bfdf-6513cc1a0c41:
        name: "Accept"
        componentName: "Accept"
        type: "STRING"
        description: "The output format of the API contract\n\nThe data is not required and the default value depends on the API format itself for the following:\n\n- **OpenApi3** API definition format: application/json\n- **Swagger20** API definition format: application/json\n- **Swagger12** API definition format: application/zip\n- **Raml** API definition format: application/x-yaml"
        enum:
        - "application/x-yaml"
        - "application/json"
        - "application/zip"
        examples:
          "20c937c3-7c23-4aa4-860f-a0fee620d8e3":
            value: "application/json"
    responses:
      "3c4620f4-957e-4a33-80a4-993f99928aca":
        componentName: "400 - Generic"
        description: "- The API definition ID is malformed (see your resource path)\n- The format contained in the request body is invalid according to the *format* or *media type* parameters\n- The API definition contained in the request body is invalid according to the format specifications\n- The wanted output does not exist, the combination of format, data type and extensions is impossible"
        bodies:
          "45b35e93-9ae8-44a0-b14d-3b2006571147":
            type: "OBJECT"
            properties:
              "151e6ae7-df58-4bc8-84bb-72ec149a98d1":
                name: "message"
                type: "STRING"
                description: "Error message that explains the reason why the error occurs"
                required: true
              "9e2cf329-afb3-49f0-9d61-d4ca89d5aefe":
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** `400`"
                required: true
              "00df3311-5599-4a3c-8942-38cd29a16338":
                name: "validationMessages"
                type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
            examples:
              f0fe4c46-954f-4ee1-b3cd-51a7e4391260:
                value: "{\n\"status\": 400,\n\"message\": \"Bad request\"\n}"
            mediaTypes:
            - "application/json"
      "3881f958-a6d3-415d-aacb-1584d4ce3b51":
        componentName: "400 - API definition ID"
        description: "- The API definition ID is malformed (see your resource path)"
        bodies:
          "149d9ad1-e49a-4ef5-a678-fcfe1f0d7562":
            type: "OBJECT"
            properties:
              "9d8dc5cc-e51c-4f00-9d20-9b3c06fa5928":
                name: "message"
                type: "STRING"
                description: "Error message that explains the reason why the error occurs"
                required: true
              df057df8-be6e-4f15-b82f-2f9ac6872b6b:
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** `400`"
                required: true
            examples:
              "8678b04a-e36e-4b3e-a334-7e4033ec0faa":
                value: "{\n\"status\": 400,\n\"message\": \"Bad request\"\n}"
            mediaTypes:
            - "application/json"
      "12b47b66-8935-405a-a3d8-05032612178a":
        componentName: "400 - Invalid API delete"
        description: "- The API definition ID is malformed (see your resource path)\n- The API definition is the last version of this API, the API Designer Management API v2 must be used the delete the API (doc link)"
        bodies:
          e7b2dcb0-50cb-470e-9ecd-43d91b2f6f7e:
            type: "OBJECT"
            properties:
              "372c9a5b-9e9b-4b91-8209-322dd64f66bf":
                name: "message"
                type: "STRING"
                description: "Error message that explains the reason why the error occurs"
                required: true
              d70dc019-5c7c-4ab3-b6a4-424da0e613c5:
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** `400`"
                required: true
            examples:
              eaa67e23-c0a1-466a-ac29-4a89dc6946d0:
                value: "{\n\"status\": 400,\n\"message\": \"Bad request\"\n}"
            mediaTypes:
            - "application/json"
      "23ac0ed8-07b3-4b6f-953a-f2765bdfb5a8":
        componentName: "400 - Complete"
        description: "- The API definition ID is malformed (see your resource path)\n- The format contained in the request body is invalid according to the *format* or *media type* parameters\n- The API definition contained in the request body is invalid according to the format specifications\n- The wanted output does not exist, the combination of format, data type and extensions is impossible\n- The specified main file is not found"
        bodies:
          "5ee0067b-2325-4bba-a79d-44b40073e6a0":
            type: "OBJECT"
            properties:
              ad3f95cb-1bb6-432b-8c04-5a907ea68969:
                name: "message"
                type: "STRING"
                description: "Error message that explains the reason why the error occurs"
                required: true
              "53f9763c-a8d4-423a-86c2-19f6b2336083":
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** `400`"
                required: true
              b6026268-cb21-4b69-a99e-a7bc476ffa69:
                name: "validationMessages"
                type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
            examples:
              d0149cff-0849-4b49-a8d5-88f9cb2e1dc7:
                value: "{\n\"status\": 400,\n\"message\": \"Bad request\"\n}"
            mediaTypes:
            - "application/json"
      "423ced9c-f2f0-4837-9e41-008540bd03e1":
        componentName: "400 - Invalid API update"
        description: "- The API definition ID is malformed (see your resource path)\n- The format contained in the request body is invalid according to the *format* or *media type* parameters\n- The API definition contained in the request body is invalid according to the format specifications\n- Field `version` is mandatory\n- Field `title` is mandatory\n- Field `version` should contain less than 255 characters\n- The API definition contained in the request has a version that is already taken in other version of the API\n- The API must have only a single version to be able to update the name with API Management v1, please use the v2 API instead\n- The wanted output does not exist, the combination of format, data type and extensions is impossible\n- The specified main file is not found"
        bodies:
          "6a73174d-e5b0-482b-9efe-5f11c5a4a2f3":
            type: "OBJECT"
            properties:
              e15a1c31-21e6-4bba-9587-befaba677d3e:
                name: "message"
                type: "STRING"
                description: "Error message that explains the reason why the error occurs"
                required: true
              "3f672646-95e0-4848-a2ec-3b84b8dd4695":
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** `400`"
                required: true
              a02320b2-3e25-43cc-b50a-564833823271:
                name: "validationMessages"
                type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
            examples:
              "6f065118-71d4-4942-8c52-c3366e5672ac":
                value: "{\n\"status\": 400,\n\"message\": \"Bad request\"\n}"
            mediaTypes:
            - "application/json"
      cf1fea88-d209-44a9-a068-60682408eb1c:
        componentName: "401 - Generic"
        description: "- Authentication token is required"
        bodies:
          "534ee011-3a0f-4159-86c3-400e3e4eb013":
            type: "OBJECT"
            properties:
              "2545e0b1-e40b-4269-9017-893c04ef5643":
                name: "status"
                type: "STRING"
                examples:
                  "487201bc-139c-498d-8d8d-5ac4ec2e85f1":
                    value: "401"
            examples:
              "69f51c08-6a55-4fab-924b-fc9d5dabd370":
                value: "{\n\"status\": 401\n}"
            mediaTypes:
            - "application/json"
      "19ab93ff-4dc8-49f3-bbf8-8496d5342c02":
        componentName: "403 - Generic"
        description: "- User is not authorized to make this action (check user account roles)\n- User tries to access data that he does not have access to"
        bodies:
          "0c839f31-8ca9-41ec-a13b-4d35ae0bfd6c":
            type: "OBJECT"
            properties:
              "67d072d4-a84e-477a-b4ad-577675f4bd38":
                name: "message"
                type: "STRING"
                required: true
                examples:
                  "1cdab3f4-1b6b-48c3-b4a4-bb6c0a9cde47":
                    value: "Not authorized"
              c7f5407d-2fcd-4ad9-bb58-ed117d167911:
                name: "status"
                type: "STRING"
                description: "**Value:** 403"
                required: true
                examples:
                  "9094bec6-7b7b-42d6-b61e-038b43192c55":
                    value: "403"
            examples:
              b31eb27b-2525-4d0a-a147-5d45c5444af6:
                value: "{\n\"status\": 403,\n\"message\": \"Forbidden\"\n}"
            mediaTypes:
            - "application/json"
      "4385fdf0-582e-43e3-badb-343dc93d8696":
        componentName: "404 - Generic"
        description: "The API definition was not found"
        bodies:
          "8bbebb0d-d9b5-4394-9717-630dcb92a8dc":
            type: "OBJECT"
            properties:
              "0f71a59e-18ae-499d-9762-6f84e58824cb":
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** 404"
                required: true
            examples:
              "7dbd6cc8-4ced-408b-9e99-c548989839dd":
                value: "{\n\"status\": 404,\n\"message\": \"Not found\"\n}"
            mediaTypes:
            - "application/json"
      "96badfcb-8b34-441b-8571-39e8a48aefb6":
        componentName: "415 - Designer"
        description: "- if the media-type is not supported by the API format (see Content-Type description)\n- if the media-type is not supported (not present in the available list)"
        bodies:
          d3be19f1-74ba-40f5-94df-30c5b9d9d329:
            type: "OBJECT"
            properties:
              "8fd5b831-a616-4a42-bdfd-66e7c70410e0":
                name: "message"
                type: "STRING"
                required: true
              "0d6e6ad0-9a3c-46f1-9d94-50853fdf5d49":
                name: "status"
                type: "STRING"
                required: true
                default: "415"
            examples:
              a8af20cf-8e81-4d81-82d7-cccc63bbdea7:
                value: "{\n\"message\": \"Unsupported Media Type\",\n\"status\": 415\n}"
            mediaTypes:
            - "application/json"
      e3ba95c4-7093-4b25-acb4-613ec73bb0c2:
        componentName: "500 - General"
        description: "An unexpected error occurred while executing your action"
        bodies:
          "7233d321-6c16-4dde-a033-f5a8bfd22675":
            type: "OBJECT"
            properties:
              f42a1a56-dcf9-46e0-991b-22f981818e7b:
                name: "message"
                type: "STRING"
              "63a20e4a-3380-4044-9bf1-b85be54ad416":
                name: "status"
                type: "INTEGER"
                format: "INT32"
                description: "**Value:** `500`"
                required: true
            examples:
              d12a2e87-0f95-4cc2-89c8-68a3158a607c:
                value: "{\n\"message\": \"Server error\",\n\"status\": 500\n}"
            mediaTypes:
            - "application/json"
      "81cdd681-2d83-4ba2-9f5e-8524937d1f11":
        componentName: "412 - Fail on warnings"
        description: "412 - Fail on warnings"
        bodies:
          a61ff160-5811-4a1e-b40f-343d7970eb37:
            type: "OBJECT"
            properties:
              "0905f7d7-41b8-44cf-8632-71baf2f11e41":
                name: "message"
                type: "STRING"
              "823f7389-bf07-4bc9-8f4e-c2b948853c38":
                name: "status"
                type: "STRING"
                default: "412"
              daeec138-b64a-4b13-89ac-00bfe520d9cf:
                name: "validationMessages"
                type: "ARRAY"
                items:
                  type: "#/contract/types/7e6185b9-1e0c-4e1c-9da7-06f64b4ba14f"
            examples:
              bf31f8c5-afed-4fd5-b62f-f7d5550dd1f8:
                value: "{\n   \"validationMessages\":[\n      {\n         \"message\":\"The base URLs must be absolute. The server 'serverUrl' is ignored.\",\n         \"code\":\"OAS3_IMPORT_RELATIVE_PATH_SERVER\",\n         \"field\":\"Server 1\",\n         \"type\":\"warning\"\n      }\n   ],\n   \"message\":\"The import of the API definition generated 1 warning message(s)\",\n   \"status\":412\n}"
            mediaTypes:
            - "application/json"
---