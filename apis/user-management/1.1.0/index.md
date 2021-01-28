---
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.0.0"
  info:
    name: "User Management"
    version: "1.1.0"
    description: "Service which exposes public API for customer operations facilitation"
    license:
      name: "Apache License Version 2.0"
      url: "https://github.com/Talend/tdf-platform-services#license"
    contact:
      name: "TPSVC Team"
  contract:
    baseUrls:
      b4ab7df5-9d6f-4e4b-8089-62c3da25e0da:
        url: "https://g40oosh.us.api-mocks.com"
        description: "Endpoint du mock de votre API. Lorsqu'il est appelé, il simule le comportement de votre API."
      "3f16576b-5928-4cc4-afc0-2be95963c22d":
        url: "http://public-api.arch.dev.datapwn.com/"
    sections:
      "0829a416-f710-453f-90a5-da0c7df3b274":
        name: "Group"
        elementOrder:
        - "#/contract/texts/3ad53cb2-1b9b-4ab7-8783-5efc04cefe96"
        - "#/contract/resources/8369001f-3031-4044-b506-1ef3601ab74f"
    unsortedElementOrder:
    - "#/contract/resources/cec28c98-bffa-4c63-bf3d-7bdfc249989e"
    - "#/contract/resources/28ac2802-4bd3-4650-a3c7-845718f22ee6"
    - "#/contract/resources/b5483e94-2d99-4ce6-aef9-c56a166c527e"
    - "#/contract/resources/ac2e27f2-10a4-4ea2-a2c9-b98737ac4ba2"
    - "#/contract/resources/316119ee-a717-4a60-be97-7a6eb18ee937"
    - "#/contract/resources/0258eb8f-edcd-4ce5-b0a9-f4ffb686492e"
    - "#/contract/resources/cf0e601b-8575-4a80-ab16-3ac0462dd3ec"
    - "#/contract/resources/5eccb011-7441-48d0-9c9d-4763eaaf759a"
    - "#/contract/resources/b2f42a31-fae8-4ce3-8a4a-5dc12fd28aef"
    - "#/contract/resources/99165c96-477c-47ec-bac2-931c6d7a7d4c"
    - "#/contract/resources/a0528585-1f87-43b4-9837-6d849c6482f7"
    - "#/contract/resources/dc742afa-5c7d-427f-ae88-5e50dc0d1be3"
    - "#/contract/resources/8932edd0-8651-49f5-9cb7-16485075aa60"
    - "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
    - "#/contract/types/e2151fc3-e92c-4b55-96bc-3c91b462260c"
    - "#/contract/types/98c8d3d5-a5c8-4ce8-bb5e-ca2d8de07d74"
    - "#/contract/types/1b3dc8b8-adc4-45c0-bd50-3b0fc8e00277"
    - "#/contract/types/d9b6997f-f06d-4c13-83b9-8117b18d6bc4"
    - "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
    - "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
    securitySchemes:
      "4efc51e7-8da5-4731-8194-350067ec54b8":
        name: "Bearer"
        type: "custom"
        describedBy:
          headers:
            e2c7fbe3-23a1-4642-8c23-1826785d2cfd:
              name: "Authorization"
              type: "STRING"
    resources:
      "8369001f-3031-4044-b506-1ef3601ab74f":
        path: "/v1/management/groups"
        section: "#/contract/sections/0829a416-f710-453f-90a5-da0c7df3b274"
        operations:
          "4c2e9b9a-bfbc-4f68-9edf-4ecaf467a080":
            name: "Retrieve filtered list of groups (updated)"
            method: "GET"
            operationId: "retrieveGroups"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              "3ff5d91e-4e0a-4866-90f7-035890fbed87":
                name: "nameFilter"
                type: "STRING"
                description: "nameFilter"
              "9ba6e587-92e4-454a-9d00-d077263bd27e":
                name: "page"
                type: "INTEGER"
                format: "INT32"
                default: 1
                examples:
                  ad680462-6f81-4633-8093-234ba695f758:
                    value: 1
              b304b667-3b93-45f8-b9c1-331d8002232e:
                name: "size"
                type: "INTEGER"
                format: "INT32"
                description: "This is a size"
                default: 50
                examples:
                  abd6c498-8561-4faf-a272-1a2a0814a143:
                    value: 50
            responses:
              ef0b62c2-de34-4349-9dec-0197540549ab:
                status: "200"
                description: "Groups successfully retrieved"
                headers:
                  acbf928a-26f4-47f9-a006-6d0c590b787f:
                    name: "page-first"
                    type: "BOOLEAN"
                  db3ff66e-00ee-4d25-a395-11c84e50a4ac:
                    name: "page-last"
                    type: "BOOLEAN"
                  f5365824-1192-499a-b658-2ba0d63cb876:
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  ab946fc3-33af-4df4-98e0-0d44bb3792ac:
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "0f8c0801-ae8c-4f83-acb0-e22054e3acf4":
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  b16f6e87-c949-4394-aea9-de8d379c50e5:
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  "43081a11-74bf-400f-8b2b-62febcf91c47":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              "32651604-21ee-4620-a428-7728a4a8b408":
                status: "400"
                description: "Invalid request URI"
              "1317637d-12d1-4266-ad25-0cc9e5302d72":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              "7e03add3-3334-45a6-a94e-d2701be1b6d3":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "1f850c3d-4c75-42c9-a39a-0bf392442ec8":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "58605d08-5c68-47dc-89a5-94ee76f8b178":
                status: "500"
                description: "Internal server error"
          b3cff4c9-e7ef-4cca-bbe2-5bebad79039b:
            name: "Register a new group"
            method: "POST"
            operationId: "registerANewGroup"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              "88b6a3dc-1544-4408-8f10-25354c12aab8":
                type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                mediaTypes:
                - "application/json"
            responses:
              "2cde95aa-7b77-43da-9331-8c5920bf3c01":
                status: "200"
                description: "OK"
                bodies:
                  ae156c0a-7b5b-4ab7-a9e1-d82c8fe1b55b:
                    type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              "0bf94e96-09e5-4461-9346-64d7da49c47c":
                status: "201"
                description: "New group successfully registered"
                headers:
                  b7c3bd0b-51f0-4618-9eef-f8756e561717:
                    name: "Location"
                    type: "STRING"
                bodies:
                  "2d068039-c1bf-4877-b6f0-536dde954d58":
                    type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              d8802e31-ff07-4c0c-bb34-f610b2f14d67:
                status: "400"
                description: "Invalid request body. The message will vary depending on the cause. E.g. at least one user in the list provided cannot be found"
              "471c0276-512d-47e9-b0ed-11ce7515deeb":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              b1c55a3e-e76b-47a3-b2d5-530590bef66c:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              b7b9367b-b867-4c89-89d9-716f68649048:
                status: "409"
                description: "Group with the same name already exists"
              "6fc2a65b-2de7-4529-9f11-6a536ebd28db":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "76d80da5-0af2-4cd1-a656-b8efd91dd5d5":
                status: "500"
                description: "Internal server error"
      cec28c98-bffa-4c63-bf3d-7bdfc249989e:
        path: "/v1/management/groups/{id}"
        pathVariables:
          "65cf9e04-dd90-49dd-bbdc-44eddd5e22fa":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          d5875f72-f2d7-415d-bf24-62f5af4970e6:
            name: "Retrieve group details"
            method: "GET"
            operationId: "retrieveGroup"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "8931dbe6-ff7c-4c17-a155-5f35a63e1a4b":
                status: "200"
                description: "Group successfully retrieved"
                headers:
                  "1d04972c-a013-45ac-8399-06c28b5c0b4d":
                    name: "page-first"
                    type: "BOOLEAN"
                  "50cb1fb1-a6fe-4262-a904-ca95356bc253":
                    name: "page-last"
                    type: "BOOLEAN"
                  "4253a8af-5aea-4c17-908c-097fc828df3a":
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  "11dd8863-3cdb-4e1d-893f-8728b9cdd403":
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  cd3e8d02-dcff-4b9c-b2fc-e3b65f594581:
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  a10b7a64-e45b-4719-be27-f78c8e530101:
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  "09c8c16b-499f-4c9f-a73f-73849026f7d1":
                    type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              e13b677b-8f86-4ebc-b14d-0cd092a31b2b:
                status: "400"
                description: "Invalid request URI"
              "22e35033-a8c3-439e-8829-6ece126f0f44":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              "4f9ee879-07b2-4e44-9ccd-a4b7238eb936":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "620ceab8-83cd-4b4b-b689-73bab60452f8":
                status: "404"
                description: "Group not found."
              f8f35711-624b-4571-ac4a-d3c85e7aea48:
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "1a664d5d-15f2-4ecf-b238-214482d6fe60":
                status: "500"
                description: "Internal server error"
          "13cd8610-4a56-4e40-91eb-aa028a479698":
            name: "Delete an existing group"
            method: "DELETE"
            operationId: "deleteGroup"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              def7fb72-1f75-4808-a233-0826e5777f1d:
                status: "200"
                description: "OK"
                bodies:
                  a26c6982-d7d0-48f4-9e9a-100dce1b9a0b:
                    type: "OBJECT"
                    mediaTypes:
                    - "application/json"
              "30842362-3a11-47ca-913b-71257f20a756":
                status: "204"
                description: "Group successfully deleted."
                bodies:
                  a7283fbe-7c37-4630-a3b9-981abbb3d0ab:
                    type: "OBJECT"
                    mediaTypes:
                    - "application/json"
              "32ca8abb-9076-471f-ad51-39b6faefc569":
                status: "400"
                description: "Invalid request URI"
              "1bdf81cb-f7cb-4572-90d4-5e78b604ef8b":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "9df66143-caa9-41a6-b395-1aca72834b5f":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "42d0bd84-d23b-4096-8c86-1e720b8f6010":
                status: "500"
                description: "Internal server error"
          "3e5eeca1-c17b-439c-ba26-664256cc23a8":
            name: "Rename an existing group"
            method: "PATCH"
            operationId: "renameGroup"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              "83bde11f-37ad-42cc-8524-1a296ed55e4f":
                type: "#/contract/types/d9b6997f-f06d-4c13-83b9-8117b18d6bc4"
                mediaTypes:
                - "application/json"
            responses:
              "7939e440-f83c-471f-9670-f98ea43fd26a":
                status: "200"
                description: "Group successfully renamed."
                bodies:
                  ccfd7a3f-e62e-4438-891a-b436adb091db:
                    type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              "56426bf6-9499-4211-8649-7b61579dd0e3":
                status: "400"
                description: "Invalid payload"
              "7f1d4677-dc70-4dcc-884d-23f98c9816ad":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              c151f8bc-5775-43e0-9480-f2514d75bdaa:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              c2db221a-387d-48ee-a5e6-0adaff962ea8:
                status: "404"
                description: "The group cannot be found"
              "16ce4ee4-711b-4e11-ad59-47179d8e6d3b":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers"
              "9814ea0f-5ff5-486e-a90b-4abff0f41535":
                status: "500"
                description: "Internal server error"
      "28ac2802-4bd3-4650-a3c7-845718f22ee6":
        path: "/v1/management/groups/{id}/users"
        pathVariables:
          "01dfa849-23a6-4a3e-a349-be1fe62132ff":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          "3661fac0-687c-4ec1-9a9f-1cde5d3cd937":
            name: "Retrieve users associated with a group"
            method: "GET"
            operationId: "retrieveGroupUsers"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              c049797d-13d6-4ca1-8cb3-ff87b7ed72ca:
                name: "page"
                type: "INTEGER"
                format: "INT32"
              "844999b5-f03a-4239-bbfd-c92cf8a8644c":
                name: "size"
                type: "INTEGER"
                format: "INT32"
            responses:
              "9eee55de-d736-423d-94f0-e190d03439d4":
                status: "200"
                description: "Users retrieved successfully for given group"
                headers:
                  "02feb1f8-5391-414a-91b2-a8201969aeb7":
                    name: "page-first"
                    type: "BOOLEAN"
                  "787e713a-a766-4773-a7e5-f63f71faaa96":
                    name: "page-last"
                    type: "BOOLEAN"
                  "0656f6b9-9215-4b24-b5b4-7e572d86818a":
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  "3fbcb2b0-164a-4ac0-9c7d-bea81e06af9f":
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  a1300d87-9350-4195-a46d-52bb22e01fae:
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "74d38135-2193-40d5-a1b1-e72c901aab9d":
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  f202852a-c99a-49ca-ad22-b231750e9536:
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "3e0d5c23-9989-4d25-b46f-33588e894066":
                status: "400"
                description: "Invalid request URI"
              eadced01-73a6-495f-b890-18c143cb7c26:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              fed2a17f-8b55-48f6-a910-1aedb8fa3c4c:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "28548aff-1263-444d-aa7f-2da4283cc3c8":
                status: "404"
                description: "Group not found"
              "6809a390-54be-4d49-ad4b-e12c1bdb93e6":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "3ac20cf8-ecd5-4225-8ff8-279bbf4eb43c":
                status: "500"
                description: "Internal server error"
          bc2d6d6b-f968-453a-b3e8-de034b9509e0:
            name: "Assign users to a group if not already in it"
            method: "POST"
            operationId: "assignUsersToAGroup"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              "55e94954-7cbd-4d35-9aef-b9673bc223f8":
                type: "ARRAY"
                items:
                  type: "STRING"
                mediaTypes:
                - "application/json"
            responses:
              "5cd65b28-0865-4b9b-84ad-2f68551f5799":
                status: "200"
                description: "Users successfully assigned to the group"
                bodies:
                  "0d65bb9a-719b-4790-92ae-521fbb28c1d0":
                    type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              e40325b0-9516-4d02-82e6-9c47e7f30d14:
                status: "400"
                description: "Invalid request or payload, e.g. at least one user in the list provided does not exist"
              "860fc6cc-2ab1-465c-9c39-13f45077c7be":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              "2f3519d6-e30d-4b7d-8b89-da5de27f555e":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "9e42d7e8-ee7d-4175-9913-63365b9e8fd1":
                status: "404"
                description: "The group cannot be found"
              "14def9dc-86fd-43f9-9043-b23d228b7f9e":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "8e7d5fb3-3984-4538-88a2-823bb050a3a3":
                status: "500"
                description: "Internal server error"
      b5483e94-2d99-4ce6-aef9-c56a166c527e:
        path: "/v1/management/groups/{id}/users/{userId}"
        pathVariables:
          "08a9ca7d-553c-4b5f-94c8-5fcfebf702e0":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
          cfb28692-23fa-48fc-a43d-b40a448ea546:
            name: "userId"
            type: "STRING"
            description: "userId"
            required: true
        operations:
          "5d63a9f6-338a-46df-8b60-06cdebb79048":
            name: "Remove a user from a group"
            method: "DELETE"
            operationId: "removeUser"
            tags:
            - "Group Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "4631bf09-c16a-443e-9d2d-c17d24fc3c8b":
                status: "200"
                description: "OK"
                bodies:
                  "1962f18b-6fd7-44a9-b65e-2d71b9482356":
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              "0ae32bf1-73b4-4b4e-a3e7-d2cecb702148":
                status: "204"
                description: "User successfully removed"
                bodies:
                  cc0d8db1-a0b5-411c-8668-46e9b76e9ddc:
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              "04bbbf03-c3ad-4ade-9397-bf3eea35d6a6":
                status: "400"
                description: "Invalid request URI"
              b8b7f828-9b81-42f8-b5be-13437e33cab9:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              af210dd9-bd19-4a37-bade-5b1adb9df91d:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "900b1d3e-bed6-4626-a052-7f2f24c555b0":
                status: "404"
                description: "Group is not found"
              adb2e151-d144-4403-bedc-bd952d25abe0:
                status: "500"
                description: "Internal server error"
      ac2e27f2-10a4-4ea2-a2c9-b98737ac4ba2:
        path: "/v1/management/roles"
        operations:
          "1152bf19-daee-4655-8e90-0625d95c9a2f":
            name: "Retrieve filtered list of roles"
            method: "GET"
            operationId: "retrieveRoles"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              ad4bd862-cd98-4264-8727-714229e39bc7:
                name: "nameFilter"
                type: "STRING"
                description: "nameFilter"
              "6d9a972f-fb77-4c9a-aa03-e8fc985995bb":
                name: "page"
                type: "INTEGER"
                format: "INT32"
                default: 1
                examples:
                  "30b38e69-9c39-428a-8b20-17105868c4a5":
                    value: 1
              e3234ec5-21a1-411f-91f4-c6857e54e3bf:
                name: "size"
                type: "INTEGER"
                format: "INT32"
                default: 50
                examples:
                  "8e5bc332-393f-419c-9c42-3723aee12b6e":
                    value: 50
            responses:
              "864ee946-9bf9-407f-901d-2bf8ffd6325d":
                status: "200"
                description: "Roles successfully retrieved"
                headers:
                  "8ecafe27-776e-4c79-a962-e02401faf2d8":
                    name: "page-first"
                    type: "BOOLEAN"
                  cf5a0de8-ae76-4b60-9c6e-1751e947672b:
                    name: "page-last"
                    type: "BOOLEAN"
                  "969123b4-2420-47f3-852b-69a5c1c03d65":
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  "7e0ff004-b985-45f6-8e11-f6f49e71a026":
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "3e0607aa-e908-460b-9866-740bd3f12721":
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  c919f3fc-4e9a-4265-873e-06f92a2fe85a:
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  a56f7da8-fda2-473c-ad1f-c18d1c920387:
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              "733d8a52-c515-4eb8-9024-840ba77f7e39":
                status: "400"
                description: "Invalid request URI"
              "276b4d2f-3684-4572-af17-ea9879c6bf26":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              "073ceac7-45cf-485e-9c0e-b8c1c65aeb86":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "61a25760-079a-4f62-8009-7dbfd48df658":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "24579e69-09bc-4229-8fe9-ab02e4d15301":
                status: "500"
                description: "Internal server error"
          "6c3e88e5-0a21-4bda-bafe-cc0a3c70a0ee":
            name: "Register a new role"
            method: "POST"
            operationId: "registerANewRole"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              "9bd5d78d-2fdd-4185-8a0d-ca2439a47dda":
                type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                mediaTypes:
                - "application/json"
            responses:
              "0ca6d454-2000-48b4-9062-2fe56ea5ea37":
                status: "200"
                description: "OK"
                bodies:
                  f213f7e0-c4a7-460d-a45b-dc8067812454:
                    type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              "4b4327a3-5346-462a-9f49-8070c1758c51":
                status: "201"
                description: "Role successfully registered"
                headers:
                  a1246479-066d-43d3-a17a-e3298b278c1a:
                    name: "Location"
                    type: "STRING"
                bodies:
                  "0af82879-f2c7-4fed-b31a-5d1713469753":
                    type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              "24379fbb-203b-49e9-ad59-6207af5b6a15":
                status: "400"
                description: "Invalid request body. The message will vary depending on the cause. E.g. at least one permission in the list provided cannot be found"
              "8712f233-511f-4880-a638-14e75724c0bc":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              b4ad6b71-394f-408a-a65e-78c8f5e1e985:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "83b3c2e9-3d9e-4ea1-9d71-3980ae906ebf":
                status: "409"
                description: "A role with the same name is already defined"
              "2dcbb20e-5c60-4002-a5de-d76e6cde3ca7":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              a5a061c5-138a-4923-b927-43af30d3f375:
                status: "500"
                description: "Internal server error"
      "316119ee-a717-4a60-be97-7a6eb18ee937":
        path: "/v1/management/roles/{id}"
        pathVariables:
          "06e0375e-0bef-424d-ab2c-9e00aa854999":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          "49738165-4ddb-4b9d-858e-6ece86488471":
            name: "Get a role by id"
            method: "GET"
            operationId: "getRoleById"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "96ce6196-6b04-447f-98d6-59620b38b203":
                status: "200"
                description: "Role successfully found"
                bodies:
                  "319d417c-6715-4143-b5c4-bec3bb1c4c11":
                    type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              "0d896b0b-6633-4c05-9a9b-6de4599703ac":
                status: "400"
                description: "Invalid request URI"
              aaab1653-1b36-440e-8be7-373923d66906:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              c0e6ba9e-19c8-436a-a22d-90dc73186177:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              f03d4a0a-17f1-43b6-9645-58948c7472bc:
                status: "404"
                description: "Role is not found"
              "90270fda-cc80-43b8-a579-92dbe5574553":
                status: "500"
                description: "Internal server error"
          a8f0a0c6-94f6-432c-9026-2d3ceffdc276:
            name: "Update a role"
            method: "PUT"
            operationId: "updateRole"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              d8b839d6-2e31-4cc1-9575-76d1f94e5d93:
                type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                mediaTypes:
                - "application/json"
            responses:
              "3ffb1a5c-7a8d-43ec-840c-7df3cf664b56":
                status: "200"
                description: "OK"
                bodies:
                  "57e26a1b-3a62-43bd-bdbd-0a3458e4b098":
                    type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              "3ba7b8fa-9fc8-4611-847d-2d7f3dc0ccd3":
                status: "204"
                description: "Role successfully updated"
                bodies:
                  c2cbe6c3-98de-4312-92ca-af276386251f:
                    type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              "2709046f-f3e6-4958-b256-991f2a699a74":
                status: "400"
                description: "Invalid request URI"
              dc165fbb-d69c-48d2-a739-98d7568036a3:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              b3e9f569-1915-4e52-b4f9-49ac0309529e:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              f165b46c-db77-49bb-a247-b7571ae05505:
                status: "404"
                description: "Role is not found"
              "5ce2807c-0ed4-4da1-a098-0eefe4eb8b95":
                status: "500"
                description: "Internal server error"
          "7f0f8461-f4e8-43fe-9547-3bc088e88ffe":
            name: "Delete an existing role"
            method: "DELETE"
            operationId: "assignUser"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "34865163-6213-402c-aff3-74881e4e06e6":
                status: "200"
                description: "OK"
                bodies:
                  "20f36f11-a920-47a4-9a48-83ccd967f310":
                    type: "OBJECT"
                    mediaTypes:
                    - "application/json"
              fa2a138b-77d4-4c1d-af4b-09de5c5bd6ea:
                status: "204"
                description: "Role successfully deleted."
                bodies:
                  "57791109-a8a3-4cff-886e-57e016aff5a2":
                    type: "OBJECT"
                    mediaTypes:
                    - "application/json"
              "458ae72a-52c1-4173-8137-7b8466b1712a":
                status: "400"
                description: "Invalid request URI"
              d3fc6e74-b170-4d59-9453-5dee0af60f8f:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "52f2ac17-c54e-40d3-9627-843f3c8b1997":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "305e044d-e8d2-4b93-9ac6-f5e4f9ef1751":
                status: "500"
                description: "Internal server error"
      "0258eb8f-edcd-4ce5-b0a9-f4ffb686492e":
        path: "/v1/management/roles/{id}/users"
        pathVariables:
          "12744951-7faf-452a-8acc-0e581f50e0ba":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          "5c6bb74b-7c62-4bf6-87e8-17bd87c80cad":
            name: "Retrieve users associated with a role"
            method: "GET"
            operationId: "retrieveUsers"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              "09c5f284-f49a-4ce4-a382-fda6c7a0cfd9":
                name: "page"
                type: "INTEGER"
                format: "INT32"
                default: 1
                examples:
                  "577f7231-d022-4591-a954-a05d21eff42e":
                    value: 1
              "1cf9e383-987e-4834-beed-22e9dc760646":
                name: "size"
                type: "INTEGER"
                format: "INT32"
                default: 50
                examples:
                  bb238883-e68d-4bb9-8307-caa81e53c2c7:
                    value: 50
            responses:
              "5bf5e56b-6dd3-4c4a-9ab8-333cc9b87351":
                status: "200"
                description: "Role users successfully retrieved"
                headers:
                  "3b39d83d-216c-4e52-8eb7-a73408303a94":
                    name: "page-first"
                    type: "BOOLEAN"
                  "0fbcd357-647d-4d56-bb5a-afe366e2335d":
                    name: "page-last"
                    type: "BOOLEAN"
                  "489d31fb-e938-4fc6-b260-5f861ba5d3e1":
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  "09f2fc4a-2dc5-451c-bdc9-e2f116d36321":
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  d1ea359e-1a7b-4c35-8d52-fe4b3a82f35b:
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "407f08c1-f14e-44f7-a9b5-3f9c3f49a412":
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  "710ca16c-82dd-4f3c-8dd3-f433ce053f50":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "8974c31b-e691-41d9-9886-1fbef8ad0455":
                status: "400"
                description: "Invalid request"
              "38ed15b8-f05c-4d02-ba74-66043a746666":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              "4d0bca56-bddc-4da5-be9b-3df5e368a478":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "8d8e8401-75a3-41eb-8902-991b16630c62":
                status: "404"
                description: "Role not found"
              e336bc4e-e71e-4aa9-b1c3-3fe9c4beab12:
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "762811e5-5dd5-4753-836c-82c41fc311f1":
                status: "500"
                description: "Internal server error"
          "929f0059-fd2b-4f7a-873e-2e2519a872d3":
            name: "Assign role to the users"
            method: "POST"
            operationId: "assignRoleToUsers"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              "6f32e4df-868d-46e7-9f87-083f421e91d5":
                type: "ARRAY"
                items:
                  type: "STRING"
                mediaTypes:
                - "application/json"
            responses:
              "7bbdcea8-ae5e-4f31-b45f-b4fce709ecda":
                status: "204"
                description: "Users successfully updated"
              "8cba03fd-bbc6-4d0a-9c48-ce37143d3190":
                status: "400"
                description: "Invalid request body, e.g. at least one user can not be found"
              "0c18c8a1-d77f-436f-9307-473b7fad07fa":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect"
              "89318294-691a-4296-9a8e-949b69ad2266":
                status: "402"
                description: "Action cannot be performed because it would bring your account above the limit authorized by your plan."
              "3349f4cc-c570-41af-8d5a-9cb7db36dbb8":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              d6769ab5-c29a-4bc6-afff-139dbf9dca00:
                status: "404"
                description: "Role not found"
              "8bc262cc-5e77-45bb-98cd-9cf1c7ab1d1d":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "4a037a33-97b2-4b74-90af-0cf95959c285":
                status: "500"
                description: "Internal server error"
      cf0e601b-8575-4a80-ab16-3ac0462dd3ec:
        path: "/v1/management/roles/{id}/users/{userId}"
        pathVariables:
          a7d27168-3e8f-4753-8088-bd0f93047a93:
            name: "id"
            type: "STRING"
            description: "id"
            required: true
          d60a219f-acd4-4077-9dd0-cde50143db32:
            name: "userId"
            type: "STRING"
            description: "userId"
            required: true
        operations:
          "7fd96d66-6e59-415e-94f4-4a0559dac26c":
            name: "Remove a role from a user"
            method: "DELETE"
            operationId: "removeRole"
            tags:
            - "Role Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              ae1fb6e9-3ea6-400f-a77b-817c1301a4aa:
                status: "200"
                description: "OK"
                bodies:
                  "715bc47f-09eb-49b4-ad8e-6c0375b6bfb9":
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              a30a691d-600b-4220-9205-ff92123a4201:
                status: "204"
                description: "Role successfully removed"
                bodies:
                  "058c375f-49f8-4734-be4c-dcd135ad3291":
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              "14004dfd-f7bb-4305-b7c7-e746377a5586":
                status: "400"
                description: "Invalid request URI"
              "2f04991c-97e4-42d1-80a9-72b078c0cad2":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "2e348aea-e1ce-42bd-b961-c26714571c3c":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "0de95628-8fe9-4ae7-8afa-f29694720190":
                status: "404"
                description: "Role is not found"
              "59c3c822-109f-492d-8798-0e0ddf7feadd":
                status: "500"
                description: "Internal server error"
      "5eccb011-7441-48d0-9c9d-4763eaaf759a":
        path: "/v1/management/users"
        operations:
          "75360246-159f-4206-a6dc-42600f219869":
            name: "Retrieve users"
            method: "GET"
            operationId: "retrieveUsers_1"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              "272502c2-8cc9-4606-8335-33cf26124c83":
                name: "page"
                type: "INTEGER"
                format: "INT32"
                default: 1
                examples:
                  d82f1de5-4926-480f-b231-88cdc5489e07:
                    value: 1
              "943751b7-5743-4933-b487-685a8e288377":
                name: "size"
                type: "INTEGER"
                format: "INT32"
                default: 50
                examples:
                  "61d4fd4b-1e0d-4719-a5cc-756e92ce2714":
                    value: 50
            responses:
              "24f58b14-220d-4185-af2f-1ddf8dda493d":
                status: "200"
                description: "The list of users retrieved in the requested range."
                headers:
                  "3cbb46f7-e6e0-4b77-8661-fd41aeb2438c":
                    name: "page-first"
                    type: "BOOLEAN"
                  "54e2e3ce-0855-48fb-baa4-6b0bdff3319f":
                    name: "page-last"
                    type: "BOOLEAN"
                  "09ef5e6c-d25e-48a0-929e-12d3f283a0b0":
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  "8405a649-1fbe-4a1f-82af-a398dc6d8a0b":
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "25d42203-e2b3-498a-821b-cbfb25852420":
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "4fb03986-3c0d-46a1-af44-0f5ffa98c4a2":
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  "1329cb5d-e7bb-4399-9124-555428f45012":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "11ba2ec7-3fcc-4961-924d-33d6029967a9":
                status: "400"
                description: "Invalid request body. The message will vary depending on the cause."
              "0a9087d7-f056-4760-aa6a-c9dd09522860":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              df4aee4d-23be-47ef-8d56-970cf3d6d727:
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              fc13c0f4-eac5-47bf-b576-4c38c95192b8:
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "071e5a20-3880-4c93-bf92-3cb4a363eeb3":
                status: "500"
                description: "Internal server error"
          c32ad67f-f7f7-4401-a2d4-e811d95cd953:
            name: "Create a new user"
            method: "POST"
            operationId: "createANewUser"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              "0bdf640e-891b-40bb-83c6-6715102feea6":
                name: "invite"
                type: "BOOLEAN"
                description: "invite"
                default: true
            bodies:
              "6ca64b4c-bfba-4c3b-ace3-9cf6a5c844d7":
                type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                mediaTypes:
                - "application/json"
            responses:
              fa9dd963-e75d-4ab5-8b52-e3d4b25c5836:
                status: "200"
                description: "OK"
                bodies:
                  "7b8ef681-dd85-4852-9ccb-baf399ce3393":
                    type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "5e811c98-b774-4a18-b407-8f4ad4a0bbaa":
                status: "201"
                description: "User successfully created."
                bodies:
                  "8f5455ae-275b-4062-9e57-34985fcf96ef":
                    type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "75111c56-899f-43d1-82fc-9794b03f08d2":
                status: "400"
                description: "Invalid request body. The message will vary depending on the cause."
              "78ebdc54-5836-49c3-8184-84b5d6cdb019":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "309cd76b-53f1-4752-b154-2295268e5297":
                status: "402"
                description: "Action cannot be performed because it would bring your account above the limit authorized by your plan."
              "2ef9b6fc-4010-4201-8874-031b8638a473":
                status: "409"
                description: "Provides more information about why the creation ended up in conflict"
              d2ba1788-1401-478c-b31c-99782a61946b:
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "118ed6d4-ec70-4f7a-bfd1-4f09971a2e14":
                status: "500"
                description: "Internal server error"
      b2f42a31-fae8-4ce3-8a4a-5dc12fd28aef:
        path: "/v1/management/users/{id}"
        pathVariables:
          "985e03b2-1004-46fd-a53c-f57ed660178f":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          "3357f56d-5968-4b30-9489-bf2c91a01786":
            name: "Retrieve user details"
            method: "GET"
            operationId: "retrieveUserDetails"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "93c079af-bd2e-4127-a611-b4efd40df953":
                status: "200"
                description: "User successfully retrieved."
                bodies:
                  "5f557d3e-6b51-4724-b180-b6356b766868":
                    type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "152a0b87-d476-47f1-9868-63f5a1fa7f70":
                status: "400"
                description: "Invalid request URI. The message will vary depending on the cause."
              dc22e572-cf94-4f13-bfae-6ad33713dd13:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "873eedf6-02c4-49f4-a034-f7b03c26d894":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              abf914c7-e1a8-44e4-85ae-81eb7cfed27c:
                status: "404"
                description: "User not found."
              "0f18167b-a6c9-468c-a48b-afe1dfad4856":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              "8f70fb6c-acae-4ec2-a8a5-69ed05fbfb70":
                status: "500"
                description: "Internal server error"
          "086f5507-b966-47db-8391-71c72531fbc6":
            name: "Update an existing user"
            method: "PUT"
            operationId: "updateUser"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              efdf7c70-e7c0-464a-8740-277c45a04219:
                type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                mediaTypes:
                - "application/json"
            responses:
              e2cf8a07-18db-40dd-8e0b-821dfa406176:
                status: "200"
                description: "User successfully updated."
                bodies:
                  b73318a3-1a29-4520-8584-dd6dacd57f7f:
                    type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "03ec4461-facb-4c6e-b2a1-2e97634f6a95":
                status: "400"
                description: "Invalid request URI or body."
              "5a530cc2-394d-47b0-816c-f464b7513354":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              ca3f4abc-12b7-4a59-9623-443c88863e4c:
                status: "402"
                description: "Action cannot be performed because it would bring your account above the limit authorized by your plan."
              "1ebf02b7-1383-4031-a183-5188c4de680d":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "89dd9454-80f6-4e4a-bab4-2de65766192b":
                status: "404"
                description: "User not found."
              "71b1e514-531e-4c53-9ef2-713f6abd3adf":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              ae1dab5d-9be3-4e97-831e-9da6e0601b13:
                status: "500"
                description: "Internal server error"
          d346a6ad-0cb4-424e-8208-0d5307dc49a8:
            name: "Delete an existing user"
            method: "DELETE"
            operationId: "assignUser_1"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "8fa21fd0-6164-4e55-a402-6803028c8ef9":
                status: "200"
                description: "OK"
                bodies:
                  a21fcc92-194d-4ac9-919f-5cd3d34c4124:
                    type: "OBJECT"
                    mediaTypes:
                    - "application/json"
              "273872c6-4d97-4cc8-99d4-fdf825fbf500":
                status: "204"
                description: "User successfully deleted."
                bodies:
                  "8e272eb1-bdb9-441b-b74f-595dc0304ca0":
                    type: "OBJECT"
                    mediaTypes:
                    - "application/json"
              "07d647c0-6379-479c-b0a1-b1e1b80f430f":
                status: "400"
                description: "Invalid request URI"
              fe3fd029-e60c-4b26-8dcd-dcc3fdece414:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "45606980-db63-4b59-b9c8-925a7ba3b816":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              e7ce4938-4bd4-493e-92a7-467baea50f36:
                status: "500"
                description: "Internal server error"
      "99165c96-477c-47ec-bac2-931c6d7a7d4c":
        path: "/v1/management/users/{id}/groups"
        pathVariables:
          "317a70a2-66c8-4ba0-bf55-e933cebdbe5a":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          aec93c36-cefc-45e6-b383-137c045c16d9:
            name: "List user groups"
            method: "GET"
            operationId: "listUserGroups"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              "079b2b0d-6793-4662-8b88-ae42098d6c9a":
                name: "nameFilter"
                type: "STRING"
                description: "nameFilter"
              "45b680e7-f524-48c9-b90b-5abfce95b5f3":
                name: "page"
                type: "INTEGER"
                format: "INT32"
                default: 1
                examples:
                  "0d10cc7c-2f9b-44d1-a528-4f071c7ef18e":
                    value: 1
              "326af1a5-79e4-4699-a315-d06720a9c867":
                name: "size"
                type: "INTEGER"
                format: "INT32"
                default: 50
                examples:
                  "680d71cc-e858-4569-bca2-cd55a4b0604f":
                    value: 50
            responses:
              "3ceaa81c-0119-49fd-ade6-95331b51cfb8":
                status: "200"
                description: "The list of user groups retrieved in the requested range."
                headers:
                  cee82941-2f70-4441-aa36-58cc5bdd6b8e:
                    name: "page-first"
                    type: "BOOLEAN"
                  "98205d2a-eb0e-4a91-9e88-33512595c96c":
                    name: "page-last"
                    type: "BOOLEAN"
                  "800ec8a0-03d7-426d-9df8-4e863e5697ce":
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  b7e5797e-7d56-4ec9-9499-d4c810e14b35:
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  d03fd31e-911a-46fe-9721-70a2e3e75071:
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "9abc1a50-6f05-4bfa-a17b-a5d6d2bb2c0a":
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  "581b2c5f-e601-4860-a49c-d5aafdbe54b8":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
                    mediaTypes:
                    - "application/json"
              d35245d0-6e9e-496f-9f35-8c1059575d08:
                status: "400"
                description: "Invalid request URI. The message will vary depending on the cause."
              "980a08e3-e4e2-428d-bbb5-ce96e8c0d36c":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "340d7641-4573-45b7-8620-03e18cc82372":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              bdecd90b-3350-4afa-af6d-4f860b304359:
                status: "404"
                description: "User not found."
              afc448f8-0070-4d08-a20a-0f2b3238f29f:
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              d8203f80-3f97-4111-b386-b7d41ebb1f44:
                status: "500"
                description: "Internal server error"
          "8d32a92a-d71f-4836-9d4e-2f1af90b944b":
            name: "Add the user to the specified groups"
            method: "POST"
            operationId: "addUserToGroups"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              f0dc6566-4c77-4383-bdc3-c71b0c330e3c:
                type: "ARRAY"
                items:
                  type: "STRING"
                mediaTypes:
                - "application/json"
            responses:
              "780da30a-1f2d-4378-b299-f9b3d8c3a95e":
                status: "200"
                description: "User successfully added to groups."
                bodies:
                  "0cb6dfcb-c09c-4eae-878e-069dfa3bd011":
                    type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              fcd575a0-78d9-4a08-a68a-a13c33bf9b6b:
                status: "400"
                description: "The data provided are not correct. This can happen if one group in the list do not exist."
              "8d7433e7-205d-494d-8fd7-8505fdd3d956":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "4f1b7623-daee-46d5-9d8e-4175c088811c":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "9f77c9ce-2ebf-4d8a-abde-ec9f69c40cfd":
                status: "404"
                description: "User not found."
              "30c465f3-f8f7-4119-9744-fac57bd1e0d9":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              e947c8bb-d6a4-4d61-a977-c96184ec3082:
                status: "500"
                description: "Internal server error"
      a0528585-1f87-43b4-9837-6d849c6482f7:
        path: "/v1/management/users/{id}/groups/{groupId}"
        pathVariables:
          "8a74b0b9-3b18-4aa2-992b-36b508263924":
            name: "groupId"
            type: "STRING"
            description: "groupId"
            required: true
          "04dd91cb-8204-4ba1-a005-cfe85dc0efed":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          "1c53fd59-17f5-4e9a-9726-8c78995c3c3f":
            name: "Remove a user from a group"
            method: "DELETE"
            operationId: "removeUserFromGroup"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              e67fefcd-0dc3-4200-b6b2-de343a1cba61:
                status: "200"
                description: "OK"
                bodies:
                  d8ddf6aa-01b7-4fa2-99e6-548baad94e6a:
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              "2d87c4fc-ad4d-4367-9170-a0a8130d0391":
                status: "204"
                description: "User successfully removed"
                bodies:
                  f82fa630-77e0-4cf1-bda3-f3af6b4a860d:
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              b7a42765-9187-4f1c-81df-22023aad0a6b:
                status: "400"
                description: "Invalid request URI"
              e6eab873-f58c-48bc-97ef-41fc5239dbb0:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "661afeed-6364-4d85-8212-9067b46ceba2":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              e310ca93-c702-4b9d-916e-fec6ac6c078d:
                status: "404"
                description: "User is not found"
              "353500f5-8d2a-46fe-ac33-7fe9f382f045":
                status: "500"
                description: "Internal server error"
      dc742afa-5c7d-427f-ae88-5e50dc0d1be3:
        path: "/v1/management/users/{id}/roles"
        pathVariables:
          "2203a521-d864-4774-8591-881ea9bbd90b":
            name: "id"
            type: "STRING"
            description: "id"
            required: true
        operations:
          ad942568-5771-45a3-8fbf-e37c7719d4b8:
            name: "List user roles"
            method: "GET"
            operationId: "listUserRoles"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            queryParameters:
              "264adc53-b514-4bf1-aecc-6a3282148576":
                name: "page"
                type: "INTEGER"
                format: "INT32"
                default: 1
                examples:
                  "0a284bc4-f276-4ebf-bf93-7112d0f7cad6":
                    value: 1
              eeabeadc-c9d5-45f8-8417-b83a3509a749:
                name: "size"
                type: "INTEGER"
                format: "INT32"
                default: 50
                examples:
                  f6629349-cedc-46f2-8a3b-d106565e9da7:
                    value: 50
            responses:
              c02c7633-3fff-4068-8921-eceb29a9f6bc:
                status: "200"
                description: "The list of user roles retrieved in the requested range."
                headers:
                  e587f5a7-c7b1-4fe8-a91b-1319c91c9cf0:
                    name: "page-first"
                    type: "BOOLEAN"
                  "002192d2-5888-43a1-ab4e-826bee391734":
                    name: "page-last"
                    type: "BOOLEAN"
                  fd9c6c35-f23d-4d1d-bc2a-51c8aaadb42b:
                    name: "page-number"
                    type: "INTEGER"
                    format: "INT32"
                  "97b7b978-45af-4b08-b875-9c0a1f5aa299":
                    name: "page-total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  e615d983-98fa-45b2-b03b-93b2ebd568f9:
                    name: "total-elements"
                    type: "INTEGER"
                    format: "INT32"
                  "6d449613-d420-4766-980c-3e630e4e0ab7":
                    name: "total-pages"
                    type: "INTEGER"
                    format: "INT32"
                bodies:
                  "5ca592d9-23d7-4ad3-9be4-44bc737bc6c3":
                    type: "ARRAY"
                    items:
                      type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
                    mediaTypes:
                    - "application/json"
              d5bed675-1fd3-4c41-8de5-4d429932d97c:
                status: "400"
                description: "Invalid request URI. The message will vary depending on the cause."
              "9181e012-45eb-43cb-87cc-1ae32652d96d":
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "7406930c-8b8a-45a8-8030-f1ac3948e8f0":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "3417c3ea-f426-46b2-8ac2-b90325eb887f":
                status: "404"
                description: "User not found."
              "990123cf-ed76-4df7-8bd7-da3507d685fc":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              b5344398-edf6-45fd-a4bd-fe76f706f61f:
                status: "500"
                description: "Internal server error"
          "4b24601f-820d-404e-989d-fb9d2332c125":
            name: "Assign new roles based on their unique identifiers to requested user"
            method: "POST"
            operationId: "assignRoles"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            bodies:
              "053c5fcd-e1f5-451c-9e0e-aae42367152e":
                type: "ARRAY"
                items:
                  type: "STRING"
                mediaTypes:
                - "application/json"
            responses:
              e1a466b7-e332-46a1-bc63-32ee8bcd78f4:
                status: "200"
                description: "Roles successfully associated with user."
                bodies:
                  d88b3812-98b3-4e77-8eb9-7d65c42088a7:
                    type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
                    mediaTypes:
                    - "application/json"
              "0a9aef7e-9ce5-472d-929b-7704f4abe794":
                status: "400"
                description: "Invalid request body. The message will vary depending on the cause. E.g. at least one role in the list provided cannot be found"
              e9522221-42ce-4eb5-835a-8a1e857e3e04:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              c0ef7c60-6457-484b-9671-277994833d90:
                status: "402"
                description: "Action cannot be performed because it would bring your account above the limit authorized by your plan."
              "35a94fca-de86-4207-9ac1-6a7d2be0ac2b":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "4b4f5a0a-0c62-4949-a9ff-f9085ecfe7a3":
                status: "404"
                description: "User not found."
              "6839b92c-87d6-4938-8e0c-006fac362536":
                status: "429"
                description: "Too many requests. Check the X-RateLimit-Limit, X-RateLimit-Remaining and X-RateLimit-Reset headers."
              c2a7b9cb-49b7-46cc-9dcd-af586de3c540:
                status: "500"
                description: "Internal server error"
      "8932edd0-8651-49f5-9cb7-16485075aa60":
        path: "/v1/management/users/{id}/roles/{roleId}"
        pathVariables:
          a3f1721a-cd69-4b2a-918a-fc33070dba33:
            name: "id"
            type: "STRING"
            description: "id"
            required: true
          "3b86db2e-cd67-4df6-b8ca-327ebf76c648":
            name: "roleId"
            type: "STRING"
            description: "roleId"
            required: true
        operations:
          db56d18b-0cc5-431c-9431-7afed6b181af:
            name: "Remove a role from a user"
            method: "DELETE"
            operationId: "removeRole_1"
            tags:
            - "User Management"
            securedBy:
            - scheme: "#/contract/securitySchemes/4efc51e7-8da5-4731-8194-350067ec54b8"
            responses:
              "244a808f-be5a-44a1-9625-4842ba715144":
                status: "200"
                description: "OK"
                bodies:
                  "4d3ec82d-b238-4698-a6e8-aa55710195d7":
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              b75d9a4f-e058-4cbb-ad9d-36af5e0497b7:
                status: "204"
                description: "Role successfully removed"
                bodies:
                  c4b59b48-acd5-4cfb-ae61-44836bf01504:
                    type: "OBJECT"
                    mediaTypes:
                    - "*/*"
              afa7185e-ad54-4c6e-9ad0-475e758e785b:
                status: "400"
                description: "Invalid request URI"
              fda15f37-854a-4014-954c-c8caa619b7e6:
                status: "401"
                description: "Indicates that the system failed to authenticate the user. Either the Authorization header was forgotten or the provided token is incorrect."
              "7af66f7a-9c12-4205-8365-05272c6d4507":
                status: "403"
                description: "The system failed to authorize the user. It indicates that the provided token is recognized but does not have the rights to perform the action. In that case, a security administrator must be contacted to be granted the proper rights."
              "66e64d45-af2f-4cb3-8a9b-b0db5718422a":
                status: "404"
                description: "User is not found"
              b93e737d-77e4-40af-8404-f17d104a5415:
                status: "500"
                description: "Internal server error"
    types:
      d654335b-3ced-41d8-9d8d-95708fd70820:
        name: "Group"
        type: "OBJECT"
        properties:
          a99c6b55-2295-4287-9f39-ac3d82b5e5bc:
            name: "name"
            type: "STRING"
          "90683a53-25fc-4163-b8c6-5dd83580d68c":
            name: "userIds"
            type: "ARRAY"
            items:
              type: "STRING"
      e2151fc3-e92c-4b55-96bc-3c91b462260c:
        name: "Page«Group»"
        type: "OBJECT"
        properties:
          "8c11c64f-af23-4d49-9679-fb6e32fa25e3":
            name: "content"
            type: "ARRAY"
            items:
              type: "#/contract/types/d654335b-3ced-41d8-9d8d-95708fd70820"
          "7debf4fd-69d9-48d3-8eec-a9c31d67bd9a":
            name: "currentSize"
            type: "INTEGER"
            format: "INT32"
          a41488c9-3a68-47fe-bc88-63cfcdd8f4fa:
            name: "empty"
            type: "BOOLEAN"
          f841ec6a-cc78-46bb-8a11-e8d19d10c8a0:
            name: "first"
            type: "BOOLEAN"
          "7581cb98-cddf-45ae-9d9a-ef8a8b71c5a2":
            name: "last"
            type: "INTEGER"
            format: "INT32"
          "3aa32869-1977-42a2-a013-6e0c055d4d84":
            name: "number"
            type: "INTEGER"
            format: "INT32"
          "9248a761-3009-450d-ad44-f6449cb9a048":
            name: "requestedSize"
            type: "INTEGER"
            format: "INT32"
          ca021607-c7f3-4ba3-8031-9ba929318e10:
            name: "totalResults"
            type: "INTEGER"
            format: "INT32"
      "98c8d3d5-a5c8-4ce8-bb5e-ca2d8de07d74":
        name: "Page«Role»"
        type: "OBJECT"
        properties:
          "2737a957-8c2c-48ef-be63-ae96bd8d49cf":
            name: "content"
            type: "ARRAY"
            items:
              type: "#/contract/types/4a317cd6-5a59-4bc7-9ea1-f7047adb35c7"
          "05639ba7-323c-467e-8b6f-49f603a633b9":
            name: "currentSize"
            type: "INTEGER"
            format: "INT32"
          "29e5df91-1231-4c00-a872-27fe9637937e":
            name: "empty"
            type: "BOOLEAN"
          "4d4b9e57-2c77-4b70-83a3-36119fc64fc4":
            name: "first"
            type: "BOOLEAN"
          b5eff68f-965b-4285-9512-6df67b319c83:
            name: "last"
            type: "INTEGER"
            format: "INT32"
          af2b5954-6793-49f4-bb24-402dcfea0b8d:
            name: "number"
            type: "INTEGER"
            format: "INT32"
          "32301f57-b6af-4fa3-bec2-ed02a59de8c6":
            name: "requestedSize"
            type: "INTEGER"
            format: "INT32"
          "7d5696bf-f1e6-4aec-af42-3310b9eb2316":
            name: "totalResults"
            type: "INTEGER"
            format: "INT32"
      "1b3dc8b8-adc4-45c0-bd50-3b0fc8e00277":
        name: "Page«User»"
        type: "OBJECT"
        properties:
          "103c0744-79a6-4926-b3ff-9b050f758b92":
            name: "content"
            type: "ARRAY"
            items:
              type: "#/contract/types/c5124c9a-7367-4a46-8548-e4bec578a316"
          cd228b05-e82f-4b51-9e55-a6607d9f78d5:
            name: "currentSize"
            type: "INTEGER"
            format: "INT32"
          "23fd31e2-51b9-44c0-916e-4db6852ff9b4":
            name: "empty"
            type: "BOOLEAN"
          "0ae9f64f-de88-4015-95a0-7f6379a4b945":
            name: "first"
            type: "BOOLEAN"
          d684bec4-ff56-4dfd-aa74-96e501a07e34:
            name: "last"
            type: "INTEGER"
            format: "INT32"
          d1ce807e-7118-4d3f-b985-8da5781872a9:
            name: "number"
            type: "INTEGER"
            format: "INT32"
          ee4decef-c870-4e34-83b0-1444497b591e:
            name: "requestedSize"
            type: "INTEGER"
            format: "INT32"
          "0a5f7cf6-c4b9-46bd-a92e-8c8c3c0cfd1d":
            name: "totalResults"
            type: "INTEGER"
            format: "INT32"
      d9b6997f-f06d-4c13-83b9-8117b18d6bc4:
        name: "RenameGroupRequest"
        type: "OBJECT"
        properties:
          "69015d1c-9567-4bb7-8bde-bfa7b9eb7a80":
            name: "name"
            type: "STRING"
      "4a317cd6-5a59-4bc7-9ea1-f7047adb35c7":
        name: "Role"
        type: "OBJECT"
        properties:
          "64800f1c-873b-4165-b633-b9a9cab95db7":
            name: "name"
            type: "STRING"
          b92eafde-4367-4937-a6aa-83c98f284b82:
            name: "permissions"
            type: "ARRAY"
            items:
              type: "STRING"
      c5124c9a-7367-4a46-8548-e4bec578a316:
        name: "User"
        type: "OBJECT"
        properties:
          "5b9c4211-143b-4d49-a7f3-58ea6a0802e4":
            name: "active"
            type: "BOOLEAN"
          "2da93437-3e6b-4851-9b84-7d0a3fe31de0":
            name: "email"
            type: "STRING"
          "1c8e64c8-abdc-4281-b8af-8817e41f8978":
            name: "firstName"
            type: "STRING"
          "0d470f38-1835-4d31-ac5d-7fa7621a3f4a":
            name: "lastName"
            type: "STRING"
          bab49eb0-8491-41c5-982e-fadaaa366053:
            name: "login"
            type: "STRING"
          "6ef283dc-0650-402d-b383-3c95e8f16ae8":
            name: "password"
            type: "STRING"
          "232b2b3d-16de-49e7-a61d-77e0d4a45dfd":
            name: "phone"
            type: "STRING"
          b7343be7-369a-4970-862a-b2497c985747:
            name: "preferredLanguage"
            type: "STRING"
            enum:
            - "EN"
            - "FR"
            - "JA"
            - "UNSUPPORTED"
          "58ecb0b7-bf32-42da-9a6b-3f878b497e4f":
            name: "roleIds"
            type: "ARRAY"
            items:
              type: "STRING"
          d1f7d2a7-993e-4d9c-a3fa-17592342ed09:
            name: "timezone"
            type: "STRING"
          "575cb15d-fef8-4f91-b6a8-f717496f750f":
            name: "title"
            type: "STRING"
    texts:
      "3ad53cb2-1b9b-4ab7-8783-5efc04cefe96":
        title: "Groups"
        content: "What is a group ? Well let's see"
        section: "#/contract/sections/0829a416-f710-453f-90a5-da0c7df3b274"
  components: {}
---