# swagger-turismo.sj
{
  "openapi": "3.0.1",
  "info": {
    "title": "Turismo SJ - API",
    "version": "1.0.0"
  },
  "servers": [
    {
      "url": "https://virtserver.swaggerhub.com/TAMIGALLARDO12/turismo.sj.cfi.api/1.0.0",
      "description": "SwaggerHub API Auto Mocking"
    },
    {
      "url": "http://localhost:8888",
      "description": "Generated server url"
    }
  ],
  "paths": {
    "/user/{userId}": {
      "put": {
        "tags": [
          "user-controller"
        ],
        "operationId": "edit",
        "parameters": [
          {
            "name": "userId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "string",
              "format": "uuid"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/UserCreateRequest"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/UserResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/subcategory/{id}": {
      "get": {
        "tags": [
          "subcategory-controller"
        ],
        "operationId": "findById",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/SubCategoryDto"
                }
              }
            }
          }
        }
      },
      "put": {
        "tags": [
          "subcategory-controller"
        ],
        "operationId": "edit_1",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/SubcategoryCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/SubCategoryDto"
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "subcategory-controller"
        ],
        "operationId": "delete",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/SubCategoryDto"
                }
              }
            }
          }
        }
      }
    },
    "/service/entrepreneurship/{entrepreneurshipId}": {
      "put": {
        "tags": [
          "assistance-controller"
        ],
        "operationId": "edit_2",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "type": "array",
                "items": {
                  "$ref": "#/components/schemas/AssistanceEditDTO"
                }
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/AssistanceDto"
                  }
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "assistance-controller"
        ],
        "operationId": "delete_1",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "serviceIds",
            "in": "query",
            "required": true,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "boolean"
                }
              }
            }
          }
        }
      }
    },
    "/role/{roleId}": {
      "get": {
        "tags": [
          "role-controller"
        ],
        "operationId": "findById_1",
        "parameters": [
          {
            "name": "roleId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/RoleDto"
                }
              }
            }
          }
        }
      },
      "put": {
        "tags": [
          "role-controller"
        ],
        "operationId": "updateRole",
        "parameters": [
          {
            "name": "roleId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/RoleCreateDTO"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/RoleDto"
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "role-controller"
        ],
        "operationId": "delete_2",
        "parameters": [
          {
            "name": "roleId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/RoleDto"
                }
              }
            }
          }
        }
      }
    },
    "/entrepreneurship/{id}": {
      "get": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "findById_2",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      },
      "put": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "edit_4",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/EntrepreneurshipCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "delete_3",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      }
    },
    "/entrepreneurship/{id}/fullCreate": {
      "put": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "fullCreate",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "edit",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "boolean"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      }
    },
    "/entrepreneurship/{id}/enabledDisabled": {
      "put": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "enabledDisabled",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      }
    },
    "/entrepreneurship/{id}/approveReject": {
      "put": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "approveReject",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "stateId",
            "in": "query",
            "required": true,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          },
          {
            "name": "reason",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      }
    },
    "/document/{id}/approveReject": {
      "put": {
        "tags": [
          "document-controller"
        ],
        "operationId": "approveReject_1",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "reason",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "status",
            "in": "query",
            "required": true,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentDto"
                }
              }
            }
          }
        }
      }
    },
    "/document/type/{id}": {
      "get": {
        "tags": [
          "document-controller"
        ],
        "operationId": "findById_3",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentTypeResponseDto"
                }
              }
            }
          }
        }
      },
      "put": {
        "tags": [
          "document-controller"
        ],
        "operationId": "edit_5",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/DocumentTypeDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentTypeResponseDto"
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "document-controller"
        ],
        "operationId": "deleteType",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentTypeResponseDto"
                }
              }
            }
          }
        }
      }
    },
    "/category/{categoryId}": {
      "put": {
        "tags": [
          "category-controller"
        ],
        "operationId": "edit_6",
        "parameters": [
          {
            "name": "categoryId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/CategoryCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/CategoryDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{id}": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "findById_5",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      },
      "put": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "edit_7",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "stateId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/ActivityEventDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{id}/publishUnpublished": {
      "put": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "publishUnpublished",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "stateId",
            "in": "query",
            "required": true,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "reason",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{id}/approveReject": {
      "put": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "approveReject_2",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "stateId",
            "in": "query",
            "required": true,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "reason",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{id}/activate": {
      "put": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "activate",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "stateId",
            "in": "query",
            "required": true,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{activityEventId}/photosVideos": {
      "put": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "addPhotosVideo",
        "parameters": [
          {
            "name": "activityEventId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "create",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "boolean"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/ActivityEventPhotoVideoCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/user": {
      "get": {
        "tags": [
          "user-controller"
        ],
        "operationId": "getUserLogged",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/UserResponseDTO"
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "user-controller"
        ],
        "operationId": "createUser",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/UserCreateRequest"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/UserResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/subcategory": {
      "get": {
        "tags": [
          "subcategory-controller"
        ],
        "operationId": "findByAll_1",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 1
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "Desc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "categoryId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "enabled",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageSubCategoryDto"
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "subcategory-controller"
        ],
        "operationId": "createCategory",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/SubcategoryCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/SubCategoryDto"
                }
              }
            }
          }
        }
      }
    },
    "/service/{entrepreneurshipId}": {
      "post": {
        "tags": [
          "assistance-controller"
        ],
        "operationId": "create",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "type": "array",
                "items": {
                  "$ref": "#/components/schemas/AssistanceCreateDto"
                }
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      }
    },
    "/role": {
      "get": {
        "tags": [
          "role-controller"
        ],
        "operationId": "findByAll_2",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/RoleDto"
                  }
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "role-controller"
        ],
        "operationId": "createRole",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/RoleCreateDTO"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/RoleDto"
                }
              }
            }
          }
        }
      }
    },
    "/publico/register": {
      "post": {
        "tags": [
          "demo-rest"
        ],
        "operationId": "createUser_1",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/UserCreateRequest"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/UserResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/publico/authenticate": {
      "post": {
        "tags": [
          "demo-rest"
        ],
        "operationId": "authenticate",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/AuthenticationReq"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/TokenInfo"
                }
              }
            }
          }
        }
      }
    },
    "/landing/entrepreneurship": {
      "post": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getEntrepreneurship",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 10
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "ASC"
            }
          },
          {
            "name": "type",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/FiltersEntrepreneurshipDTO"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageResponseEntrepreneurshipDTO"
                }
              }
            }
          }
        }
      }
    },
    "/landing/activity-events": {
      "post": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getActivityEvent",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 10
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "ASC"
            }
          },
          {
            "name": "type",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "date",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "subcategoryName",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/FiltersActivityEventDTO"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/entrepreneurship": {
      "get": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "findByAll_5",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "Asc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "personalityIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "stateIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int32"
              }
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageEntrepreneurshipDto"
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "entrepreneurship-controller"
        ],
        "operationId": "create_1",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/EntrepreneurshipCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDto"
                }
              }
            }
          }
        }
      }
    },
    "/document": {
      "post": {
        "tags": [
          "document-controller"
        ],
        "operationId": "createDocument",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/DocumentCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentDto"
                }
              }
            }
          }
        }
      }
    },
    "/document/type": {
      "get": {
        "tags": [
          "document-controller"
        ],
        "operationId": "findByAll_6",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "asc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "statusIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "areaIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "categoryIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "subcategoryIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "personalityIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageDocumentTypeResponseDto"
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "document-controller"
        ],
        "operationId": "createType",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/DocumentTypeDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentTypeResponseDto"
                }
              }
            }
          }
        }
      }
    },
    "/category": {
      "get": {
        "tags": [
          "category-controller"
        ],
        "operationId": "findByAll_7",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 1
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "Desc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "areaId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "enabled",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageCategoryDto"
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "category-controller"
        ],
        "operationId": "createCategory_1",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/CategoryCreateDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/CategoryDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "findByAll_9",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "Asc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "areaIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "categoryIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "subcategoryIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "typeIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "statusIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "dayIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageActivityEventDto"
                }
              }
            }
          }
        }
      },
      "post": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "create_2",
        "requestBody": {
          "content": {
            "application/json": {
              "schema": {
                "$ref": "#/components/schemas/ActivityEventDto"
              }
            }
          },
          "required": true
        },
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/user/{userId}/disable": {
      "patch": {
        "tags": [
          "user-controller"
        ],
        "operationId": "disable",
        "parameters": [
          {
            "name": "userId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "string",
              "format": "uuid"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/UserResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{activityEventId}/featured": {
      "patch": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "updateFeatured",
        "parameters": [
          {
            "name": "activityEventId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    },
    "/user/{id}": {
      "get": {
        "tags": [
          "user-controller"
        ],
        "operationId": "getUser",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "string",
              "format": "uuid"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/UserResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/user/permissions": {
      "get": {
        "tags": [
          "user-controller"
        ],
        "operationId": "getPermissions",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object",
                  "additionalProperties": {
                    "type": "boolean"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/user/list": {
      "get": {
        "tags": [
          "user-controller"
        ],
        "operationId": "findByAll",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 1
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "Desc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "name"
            }
          },
          {
            "name": "sector",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "roleId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          },
          {
            "name": "search",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageUserResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/service/{entrepreneurshipId}/entrepreneurship": {
      "get": {
        "tags": [
          "assistance-controller"
        ],
        "operationId": "findByEntrepreneurship",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "asc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "areaIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "categoryIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "subcategoryIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageAssistanceDto"
                }
              }
            }
          }
        }
      }
    },
    "/province": {
      "get": {
        "tags": [
          "province-controller"
        ],
        "operationId": "findByAll_3",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ProvinceDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/province/{provinceId}/departments": {
      "get": {
        "tags": [
          "province-controller"
        ],
        "operationId": "findAllDepartmentByProvinceId",
        "parameters": [
          {
            "name": "provinceId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/DepartmentDTO"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/parameter/valley": {
      "get": {
        "tags": [
          "parameter-controller"
        ],
        "operationId": "findByAllValley",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ParameterDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/parameter/personality": {
      "get": {
        "tags": [
          "parameter-controller"
        ],
        "operationId": "findByAllPersonality",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ParameterDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/parameter/language": {
      "get": {
        "tags": [
          "parameter-controller"
        ],
        "operationId": "findByAllLanguage",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ParameterDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/parameter/TypeService": {
      "get": {
        "tags": [
          "parameter-controller"
        ],
        "operationId": "findByAllTypeService",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ParameterDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/language": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "findByAllLanguage_1",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ParameterDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/featured": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getActivityEventFeatured",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageActivityEventFeaturedDTO"
                }
              }
            }
          }
        }
      }
    },
    "/landing/entrepreneurship/{entrepreneurshipId}": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getEntrepreneurshipById",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/EntrepreneurshipDTO"
                }
              }
            }
          }
        }
      }
    },
    "/landing/department": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getDepartment",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/DepartmentDTO"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/department/{departmentId}/locations": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getLocations",
        "parameters": [
          {
            "name": "departmentId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/LocationDTO"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/category/{categoryId}/subcategorys": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getSubCategory",
        "parameters": [
          {
            "name": "categoryId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/SubCategoryDTO"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/area": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getArea",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/AreaDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/area/{areaId}/categorys": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getCategory",
        "parameters": [
          {
            "name": "areaId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/CategoryDTO"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/landing/activity-event/{activityEventId}": {
      "get": {
        "tags": [
          "landing-controller"
        ],
        "operationId": "getActivityEventById",
        "parameters": [
          {
            "name": "activityEventId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDTO"
                }
              }
            }
          }
        }
      }
    },
    "/document/{entrepreneurshipId}/subcategory": {
      "get": {
        "tags": [
          "document-controller"
        ],
        "operationId": "findAllDocumentSubcategory",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/DocumentSubcategoryDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/document/{entrepreneurshipId}/entrepreneurship": {
      "get": {
        "tags": [
          "document-controller"
        ],
        "operationId": "findAllDocument",
        "parameters": [
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/DocumentEntrepreneurshipDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/document/{entrepreneurshipId}/entrepreneurship/all-documents": {
      "get": {
        "tags": [
          "document-controller"
        ],
        "operationId": "findAllDocuments",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "asc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          },
          {
            "name": "entrepreneurshipId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          },
          {
            "name": "requirementIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "statusIds",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "array",
              "items": {
                "type": "integer",
                "format": "int64"
              }
            }
          },
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/PageDocumentResponseDTO"
                }
              }
            }
          }
        }
      }
    },
    "/configuration": {
      "get": {
        "tags": [
          "configuration-controller"
        ],
        "operationId": "findAll",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ConfigurationDto"
                }
              }
            }
          }
        }
      }
    },
    "/configuration/state": {
      "get": {
        "tags": [
          "configuration-controller"
        ],
        "operationId": "findAllByState",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/StateConfigurationDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/configuration/state/document": {
      "get": {
        "tags": [
          "configuration-controller"
        ],
        "operationId": "findAllByStateDocument",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/StateConfigurationDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/configuration/permissions/by-role": {
      "get": {
        "tags": [
          "configuration-controller"
        ],
        "operationId": "permissionsByRole",
        "parameters": [
          {
            "name": "pageNumber",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 0
            }
          },
          {
            "name": "pageSize",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int32",
              "default": 100
            }
          },
          {
            "name": "orderCriteria",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "Asc"
            }
          },
          {
            "name": "orderField",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string",
              "default": "id"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/category/{id}": {
      "get": {
        "tags": [
          "category-controller"
        ],
        "operationId": "findById_4",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/CategoryDto"
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "category-controller"
        ],
        "operationId": "delete_4",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/CategoryDto"
                }
              }
            }
          }
        }
      }
    },
    "/category/by-subcategories": {
      "get": {
        "tags": [
          "category-controller"
        ],
        "operationId": "findAllBySubcategory",
        "parameters": [
          {
            "name": "areaId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/CategoryDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/authority": {
      "get": {
        "tags": [
          "authority-controller"
        ],
        "operationId": "findAll_1",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/AuthorityDTO"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/area": {
      "get": {
        "tags": [
          "area-controller"
        ],
        "operationId": "findByAll_8",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/AreaDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/area/by-categories": {
      "get": {
        "tags": [
          "area-controller"
        ],
        "operationId": "findByAllByCategories",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/AreaDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/services/{serviceId}": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "activityEventByServiceId",
        "parameters": [
          {
            "name": "serviceId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "$ref": "#/components/schemas/ActivityEventDto"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/labels": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "labelsActivityEvent",
        "parameters": [
          {
            "name": "searchQuery",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "array",
                  "items": {
                    "type": "string"
                  }
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-type": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countByType",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-subcategory": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countBySubcategory",
        "parameters": [
          {
            "name": "categoryId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-status": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countByStatus",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-hours": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countByHours",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-days": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countByDays",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-category": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countByCategory",
        "parameters": [
          {
            "name": "areaId",
            "in": "query",
            "required": false,
            "style": "form",
            "explode": true,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/by-area": {
      "get": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "countByArea",
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "type": "object"
                }
              }
            }
          }
        }
      }
    },
    "/document/{id}": {
      "delete": {
        "tags": [
          "document-controller"
        ],
        "operationId": "deleteDocument",
        "parameters": [
          {
            "name": "id",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int32"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/DocumentDto"
                }
              }
            }
          }
        }
      }
    },
    "/activityEvent/{activityEventId}": {
      "delete": {
        "tags": [
          "activity-event-controller"
        ],
        "operationId": "delete_5",
        "parameters": [
          {
            "name": "activityEventId",
            "in": "path",
            "required": true,
            "style": "simple",
            "explode": false,
            "schema": {
              "type": "integer",
              "format": "int64"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "content": {
              "*/*": {
                "schema": {
                  "$ref": "#/components/schemas/ActivityEventDto"
                }
              }
            }
          }
        }
      }
    }
  },
  "components": {
    "schemas": {
      "FileBase64DTO": {
        "type": "object",
        "properties": {
          "name": {
            "type": "string"
          },
          "accessControlRule": {
            "type": "string"
          },
          "file": {
            "type": "string"
          }
        }
      },
      "UserCreateRequest": {
        "type": "object",
        "properties": {
          "email": {
            "type": "string"
          },
          "name": {
            "type": "string"
          },
          "surname": {
            "type": "string"
          },
          "password": {
            "type": "string"
          },
          "identityNumber": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "role_id": {
            "type": "integer",
            "format": "int32"
          },
          "location": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "privateSector": {
            "type": "boolean"
          },
          "initialRegistration": {
            "type": "boolean"
          },
          "province_id": {
            "type": "integer",
            "format": "int32"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/FileBase64DTO"
          }
        }
      },
      "Authority": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "authority": {
            "type": "string"
          },
          "displayName": {
            "type": "string"
          }
        }
      },
      "ContentDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "url": {
            "type": "string"
          },
          "kind": {
            "type": "string"
          }
        }
      },
      "Links": {
        "type": "object",
        "additionalProperties": {
          "$ref": "#/components/schemas/Link"
        }
      },
      "ProfileDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "identityNumber": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "location": {
            "type": "string"
          },
          "province": {
            "$ref": "#/components/schemas/ProvinceDto"
          },
          "privateSector": {
            "type": "boolean"
          },
          "sector": {
            "type": "string"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/ContentDTO"
          }
        }
      },
      "ProvinceDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          }
        }
      },
      "RoleDto": {
        "type": "object",
        "properties": {
          "role": {
            "type": "string"
          },
          "authorities": {
            "uniqueItems": true,
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/Authority"
            }
          },
          "id": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "UserResponseDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "string"
          },
          "name": {
            "type": "string"
          },
          "surname": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "emailVerified": {
            "type": "boolean"
          },
          "profile": {
            "$ref": "#/components/schemas/ProfileDto"
          },
          "role": {
            "$ref": "#/components/schemas/RoleDto"
          },
          "_links": {
            "$ref": "#/components/schemas/Links"
          }
        }
      },
      "SubcategoryCreateDto": {
        "type": "object",
        "properties": {
          "name": {
            "type": "string"
          },
          "categoryId": {
            "type": "integer",
            "format": "int64"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/FileBase64DTO"
          },
          "enabled": {
            "type": "boolean"
          }
        }
      },
      "AreaDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          }
        }
      },
      "CategoryDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "area": {
            "$ref": "#/components/schemas/AreaDto"
          },
          "enabled": {
            "type": "boolean"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/ContentDTO"
          },
          "histories": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/HistoryDto"
            }
          }
        }
      },
      "HistoryDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "action": {
            "type": "string"
          },
          "dateHour": {
            "type": "string"
          },
          "user": {
            "$ref": "#/components/schemas/UserResponseDTO"
          }
        }
      },
      "SubCategoryDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "category": {
            "$ref": "#/components/schemas/CategoryDto"
          },
          "enabled": {
            "type": "boolean"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/ContentDTO"
          },
          "histories": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/HistoryDto"
            }
          }
        }
      },
      "AssistanceEditDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "provinceId": {
            "type": "integer",
            "format": "int32"
          },
          "departmentId": {
            "type": "integer",
            "format": "int32"
          },
          "location": {
            "type": "string"
          },
          "gps": {
            "type": "string"
          },
          "contactName": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "webPage": {
            "type": "string"
          },
          "facebook": {
            "type": "string"
          },
          "instagram": {
            "type": "string"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/FileBase64DTO"
          }
        }
      },
      "AssistanceDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "area": {
            "$ref": "#/components/schemas/AreaDto"
          },
          "name": {
            "type": "string"
          },
          "category": {
            "$ref": "#/components/schemas/CategoryDto"
          },
          "subcategory": {
            "$ref": "#/components/schemas/SubCategoryDto"
          },
          "address": {
            "type": "string"
          },
          "department": {
            "$ref": "#/components/schemas/DepartmentDTO"
          },
          "gps": {
            "type": "string"
          },
          "contactName": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "webPage": {
            "type": "string"
          },
          "facebook": {
            "type": "string"
          },
          "instagram": {
            "type": "string"
          },
          "entrepreneurshipId": {
            "type": "integer",
            "format": "int32"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/ContentDTO"
          },
          "location": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "province": {
            "$ref": "#/components/schemas/ProvinceDto"
          }
        }
      },
      "DepartmentDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          }
        }
      },
      "RoleCreateDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int32"
          },
          "name": {
            "type": "string"
          },
          "permissionsIds": {
            "type": "array",
            "items": {
              "type": "integer",
              "format": "int64"
            }
          }
        }
      },
      "EntrepreneurshipCreateDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int32"
          },
          "personalityId": {
            "type": "integer",
            "format": "int32"
          },
          "name": {
            "type": "string"
          },
          "identityNumber": {
            "type": "string"
          },
          "privateSector": {
            "type": "boolean"
          },
          "description": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "provinceId": {
            "type": "integer",
            "format": "int32"
          },
          "departmentId": {
            "type": "integer",
            "format": "int32"
          },
          "location": {
            "type": "string"
          },
          "gps": {
            "type": "string"
          },
          "contactName": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "webPage": {
            "type": "string"
          },
          "userId": {
            "type": "string"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/FileBase64DTO"
          },
          "visible": {
            "type": "boolean"
          }
        }
      },
      "EntrepreneurshipDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "personality": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "name": {
            "type": "string"
          },
          "identityNumber": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "department": {
            "$ref": "#/components/schemas/DepartmentDTO"
          },
          "location": {
            "type": "string"
          },
          "gps": {
            "type": "string"
          },
          "contactName": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "webPage": {
            "type": "string"
          },
          "user": {
            "$ref": "#/components/schemas/UserResponseDTO"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/ContentDTO"
          },
          "privateSector": {
            "type": "boolean"
          },
          "rejectionReason": {
            "type": "string"
          },
          "visible": {
            "type": "boolean"
          },
          "services": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/AssistanceDto"
            }
          },
          "state": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "histories": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/HistoryDto"
            }
          },
          "countServices": {
            "type": "integer",
            "format": "int64"
          },
          "province": {
            "$ref": "#/components/schemas/ProvinceDto"
          }
        }
      },
      "ParameterDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          }
        }
      },
      "DocumentDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "state": {
            "$ref": "#/components/schemas/DocumentStateDto"
          },
          "rejectionReason": {
            "type": "string"
          },
          "entrepreneurship": {
            "$ref": "#/components/schemas/EntrepreneurshipDto"
          },
          "type": {
            "$ref": "#/components/schemas/DocumentTypeResponseDto"
          },
          "subCategory": {
            "$ref": "#/components/schemas/SubCategoryDto"
          },
          "file": {
            "$ref": "#/components/schemas/ContentDTO"
          }
        }
      },
      "DocumentStateDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int32"
          },
          "name": {
            "type": "string"
          }
        }
      },
      "DocumentTypeHistoryDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "action": {
            "type": "string"
          },
          "dateHour": {
            "type": "string"
          },
          "user": {
            "$ref": "#/components/schemas/UserResponseDTO"
          }
        }
      },
      "DocumentTypeResponseDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "subCategory": {
            "$ref": "#/components/schemas/SubCategoryDto"
          },
          "personality": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "name": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "enabled": {
            "type": "boolean"
          },
          "history": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DocumentTypeHistoryDto"
            }
          }
        }
      },
      "DocumentTypeDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "subCategoryId": {
            "type": "integer",
            "format": "int32"
          },
          "subcategoryName": {
            "type": "string"
          },
          "personalityId": {
            "type": "integer",
            "format": "int32"
          },
          "personalityName": {
            "type": "string"
          },
          "name": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "enabled": {
            "type": "boolean"
          }
        }
      },
      "CategoryCreateDto": {
        "type": "object",
        "properties": {
          "name": {
            "type": "string"
          },
          "areaId": {
            "type": "integer",
            "format": "int64"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/FileBase64DTO"
          },
          "enabled": {
            "type": "boolean"
          }
        }
      },
      "ActivityEventDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "type": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "service": {
            "$ref": "#/components/schemas/AssistanceDto"
          },
          "title": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "labels": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "department": {
            "$ref": "#/components/schemas/DepartmentDTO"
          },
          "location": {
            "type": "string"
          },
          "gps": {
            "type": "string"
          },
          "contactName": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "reservationLink": {
            "type": "string"
          },
          "sector": {
            "type": "string"
          },
          "startDate": {
            "type": "string"
          },
          "endDate": {
            "type": "string"
          },
          "dayHours": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DayHoursDto"
            }
          },
          "reservationTime": {
            "type": "string"
          },
          "difficulty": {
            "type": "string"
          },
          "minimumCapacity": {
            "type": "integer",
            "format": "int32"
          },
          "maximumCapacity": {
            "type": "integer",
            "format": "int32"
          },
          "language": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "minimumAge": {
            "type": "integer",
            "format": "int32"
          },
          "maximumAge": {
            "type": "integer",
            "format": "int32"
          },
          "freeEntrance": {
            "type": "boolean"
          },
          "entryWithCost": {
            "type": "boolean"
          },
          "freeRetirees": {
            "type": "boolean"
          },
          "freeKids": {
            "type": "boolean"
          },
          "motorDisability": {
            "type": "boolean"
          },
          "visualDisability": {
            "type": "boolean"
          },
          "auditoryDisability": {
            "type": "boolean"
          },
          "individualBathrooms": {
            "type": "boolean"
          },
          "mixedBathrooms": {
            "type": "boolean"
          },
          "handicapBathrooms": {
            "type": "boolean"
          },
          "ramp": {
            "type": "boolean"
          },
          "magneticRing": {
            "type": "boolean"
          },
          "brailleSystem": {
            "type": "boolean"
          },
          "wifi": {
            "type": "boolean"
          },
          "celiac": {
            "type": "boolean"
          },
          "vegans": {
            "type": "boolean"
          },
          "vegetarian": {
            "type": "boolean"
          },
          "petFriendly": {
            "type": "boolean"
          },
          "parkingLot": {
            "type": "boolean"
          },
          "otherServices": {
            "type": "string"
          },
          "featured": {
            "type": "boolean"
          },
          "allYear": {
            "type": "boolean"
          },
          "observations": {
            "type": "string"
          },
          "cancellationPolicies": {
            "type": "string"
          },
          "state": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "photos": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventPhotoViewDto"
            }
          },
          "videos": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventVideoDto"
            }
          },
          "histories": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/HistoryDto"
            }
          }
        }
      },
      "ActivityEventPhotoViewDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "photo": {
            "$ref": "#/components/schemas/ContentDTO"
          }
        }
      },
      "ActivityEventVideoDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "linkVideo": {
            "type": "string"
          }
        }
      },
      "DayHoursDto": {
        "type": "object",
        "properties": {
          "day": {
            "type": "integer",
            "format": "int32"
          },
          "startHour": {
            "type": "string"
          },
          "endHour": {
            "type": "string"
          },
          "startDate": {
            "type": "string"
          },
          "endDate": {
            "type": "string"
          }
        }
      },
      "ActivityEventPhotoDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "photo": {
            "$ref": "#/components/schemas/FileBase64DTO"
          }
        }
      },
      "ActivityEventPhotoVideoCreateDto": {
        "type": "object",
        "properties": {
          "photos": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventPhotoDto"
            }
          },
          "linkVideos": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventVideoDto"
            }
          }
        }
      },
      "AssistanceCreateDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "areaId": {
            "type": "integer",
            "format": "int32"
          },
          "categoryId": {
            "type": "integer",
            "format": "int32"
          },
          "subcategoryId": {
            "type": "integer",
            "format": "int32"
          },
          "description": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "provinceId": {
            "type": "integer",
            "format": "int32"
          },
          "departmentId": {
            "type": "integer",
            "format": "int32"
          },
          "location": {
            "type": "string"
          },
          "gps": {
            "type": "string"
          },
          "contactName": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "webPage": {
            "type": "string"
          },
          "facebook": {
            "type": "string"
          },
          "instagram": {
            "type": "string"
          },
          "profilePicture": {
            "$ref": "#/components/schemas/FileBase64DTO"
          }
        }
      },
      "AuthenticationReq": {
        "type": "object",
        "properties": {
          "user": {
            "type": "string",
            "writeOnly": true
          },
          "password": {
            "type": "string"
          },
          "usuario": {
            "type": "string"
          }
        }
      },
      "TokenInfo": {
        "type": "object",
        "properties": {
          "jwtToken": {
            "type": "string"
          }
        }
      },
      "FiltersEntrepreneurshipDTO": {
        "type": "object",
        "properties": {
          "area": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "category": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "subcategory": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "departments": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "locations": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "PageResponseEntrepreneurshipDTO": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ResponseEntrepreneurshipDTO"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "PageableObject": {
        "type": "object",
        "properties": {
          "offset": {
            "type": "integer",
            "format": "int64"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "pageNumber": {
            "type": "integer",
            "format": "int32"
          },
          "pageSize": {
            "type": "integer",
            "format": "int32"
          },
          "paged": {
            "type": "boolean"
          },
          "unpaged": {
            "type": "boolean"
          }
        }
      },
      "ResponseEntrepreneurshipDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "location": {
            "type": "string"
          },
          "department": {
            "type": "string"
          },
          "areaName": {
            "type": "string"
          },
          "subcategoryName": {
            "type": "string"
          },
          "categoryName": {
            "type": "string"
          },
          "photo": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "SortObject": {
        "type": "object",
        "properties": {
          "empty": {
            "type": "boolean"
          },
          "sorted": {
            "type": "boolean"
          },
          "unsorted": {
            "type": "boolean"
          }
        }
      },
      "FiltersActivityEventDTO": {
        "type": "object",
        "properties": {
          "area": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "category": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "subcategory": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "departments": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "locations": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "entrepreneurshipName": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "days": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "hours": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/LocalTime"
            }
          },
          "people": {
            "type": "integer",
            "format": "int64"
          },
          "duration": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "difficulty": {
            "type": "array",
            "items": {
              "type": "string"
            }
          },
          "languages": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "LocalTime": {
        "type": "object",
        "properties": {
          "hour": {
            "type": "integer",
            "format": "int32"
          },
          "minute": {
            "type": "integer",
            "format": "int32"
          },
          "second": {
            "type": "integer",
            "format": "int32"
          },
          "nano": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "DayHoursDTO": {
        "type": "object",
        "properties": {
          "day": {
            "type": "string"
          },
          "startHour": {
            "type": "string"
          },
          "endHour": {
            "type": "string"
          }
        }
      },
      "PageResponseDTO": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ResponseDTO"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "ResponseDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "location": {
            "type": "string"
          },
          "department": {
            "type": "string"
          },
          "startDate": {
            "type": "string"
          },
          "dayHours": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DayHoursDTO"
            }
          },
          "type": {
            "type": "integer",
            "format": "int64"
          },
          "featured": {
            "type": "boolean"
          },
          "difficulty": {
            "type": "string"
          },
          "areaName": {
            "type": "string"
          },
          "categoryName": {
            "type": "string"
          },
          "subcategoryName": {
            "type": "string"
          },
          "entrepreneurshipName": {
            "type": "string"
          },
          "language": {
            "type": "string"
          },
          "duration": {
            "type": "string"
          },
          "maximumCapacity": {
            "type": "integer",
            "format": "int64"
          },
          "photos": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "DocumentCreateDto": {
        "type": "object",
        "properties": {
          "entrepreneurshipId": {
            "type": "integer",
            "format": "int64"
          },
          "documentTypeId": {
            "type": "integer",
            "format": "int64"
          },
          "file": {
            "$ref": "#/components/schemas/FileBase64DTO"
          }
        }
      },
      "PageUserResponseDTO": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/UserResponseDTO"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "PageSubCategoryDto": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/SubCategoryDto"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "PageAssistanceDto": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/AssistanceDto"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "ActivityEventFeaturedDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "featured": {
            "type": "boolean"
          },
          "startDate": {
            "type": "string"
          },
          "endDate": {
            "type": "string"
          },
          "entrepreneurshipName": {
            "type": "string"
          },
          "photos": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "PageActivityEventFeaturedDTO": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventFeaturedDTO"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "ActivityEventsDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "subcategoryName": {
            "type": "string"
          },
          "type": {
            "type": "integer",
            "format": "int64"
          },
          "daysHours": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DayHoursDTO"
            }
          },
          "startDate": {
            "type": "string"
          },
          "endDate": {
            "type": "string"
          }
        }
      },
      "EntrepreneurshipDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "address": {
            "type": "string"
          },
          "location": {
            "type": "string"
          },
          "department": {
            "type": "string"
          },
          "province": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "email": {
            "type": "string"
          },
          "phone": {
            "type": "string"
          },
          "whatsApp": {
            "type": "string"
          },
          "webPage": {
            "type": "string"
          },
          "facebookLink": {
            "type": "string"
          },
          "instagramLink": {
            "type": "string"
          },
          "activityEvents": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventsDTO"
            }
          },
          "services": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ServicesDTO"
            }
          },
          "areaName": {
            "type": "string"
          },
          "categoryName": {
            "type": "string"
          },
          "subcategoryName": {
            "type": "string"
          },
          "photo": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "ServicesDTO": {
        "type": "object",
        "properties": {
          "categoryName": {
            "type": "string"
          },
          "name": {
            "type": "string"
          }
        }
      },
      "LocationDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "departmentId": {
            "type": "integer",
            "format": "int64"
          }
        }
      },
      "SubCategoryDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "subcategoryName": {
            "type": "string"
          },
          "categoryId": {
            "type": "integer",
            "format": "int64"
          }
        }
      },
      "CategoryDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "categoryName": {
            "type": "string"
          },
          "areaId": {
            "type": "integer",
            "format": "int64"
          }
        }
      },
      "ActivityEventDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "phoneNumber": {
            "type": "string"
          },
          "location": {
            "type": "string"
          },
          "department": {
            "type": "string"
          },
          "startDate": {
            "type": "string"
          },
          "endDate": {
            "type": "string"
          },
          "dayHours": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DayHoursDTO"
            }
          },
          "type": {
            "type": "integer",
            "format": "int64"
          },
          "featured": {
            "type": "boolean"
          },
          "difficulty": {
            "type": "string"
          },
          "areaName": {
            "type": "string"
          },
          "categoryName": {
            "type": "string"
          },
          "subcategoryName": {
            "type": "string"
          },
          "entrepreneurshipName": {
            "type": "string"
          },
          "language": {
            "type": "string"
          },
          "duration": {
            "type": "string"
          },
          "maximumCapacity": {
            "type": "integer",
            "format": "int64"
          },
          "reservationLink": {
            "type": "string"
          },
          "instagramLink": {
            "type": "string"
          },
          "photos": {
            "type": "array",
            "items": {
              "type": "string"
            }
          }
        }
      },
      "PageEntrepreneurshipDto": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/EntrepreneurshipDto"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "DocumentBasicDto": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "rejectionReason": {
            "type": "string"
          },
          "file": {
            "$ref": "#/components/schemas/ContentDTO"
          }
        }
      },
      "DocumentEntrepreneurshipDto": {
        "type": "object",
        "properties": {
          "type": {
            "$ref": "#/components/schemas/DocumentTypeResponseDto"
          },
          "document": {
            "$ref": "#/components/schemas/DocumentBasicDto"
          },
          "state": {
            "$ref": "#/components/schemas/DocumentStateDto"
          }
        }
      },
      "DocumentSubcategoryDto": {
        "type": "object",
        "properties": {
          "subcategoryId": {
            "type": "integer",
            "format": "int64"
          },
          "subcategoryName": {
            "type": "string"
          },
          "documents": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DocumentEntrepreneurshipDto"
            }
          }
        }
      },
      "DocumentResponseDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "description": {
            "type": "string"
          },
          "requirement": {
            "type": "string"
          },
          "document": {
            "$ref": "#/components/schemas/DocumentBasicDto"
          },
          "state": {
            "$ref": "#/components/schemas/DocumentStateDto"
          }
        }
      },
      "PageDocumentResponseDTO": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DocumentResponseDTO"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "PageDocumentTypeResponseDto": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DocumentTypeResponseDto"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "CategoryConfigurationDto": {
        "type": "object",
        "properties": {
          "area": {
            "$ref": "#/components/schemas/AreaDto"
          },
          "amountCategory": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "ConfigurationDto": {
        "type": "object",
        "properties": {
          "users": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/UserConfigurationDto"
            }
          },
          "categories": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/CategoryConfigurationDto"
            }
          },
          "subcategories": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/SubcategoryConfigurationDto"
            }
          },
          "documentTypes": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/DocumentTypeConfigurationDto"
            }
          }
        }
      },
      "DocumentTypeConfigurationDto": {
        "type": "object",
        "properties": {
          "subCategory": {
            "$ref": "#/components/schemas/SubCategoryDto"
          },
          "personality": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "amount": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "SubcategoryConfigurationDto": {
        "type": "object",
        "properties": {
          "category": {
            "$ref": "#/components/schemas/CategoryDto"
          },
          "amountSubcategory": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "UserConfigurationDto": {
        "type": "object",
        "properties": {
          "role": {
            "$ref": "#/components/schemas/RoleDto"
          },
          "amountUser": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "StateConfigurationDto": {
        "type": "object",
        "properties": {
          "state": {
            "$ref": "#/components/schemas/ParameterDto"
          },
          "amount": {
            "type": "integer",
            "format": "int32"
          }
        }
      },
      "PageCategoryDto": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/CategoryDto"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "AuthorityDTO": {
        "type": "object",
        "properties": {
          "id": {
            "type": "integer",
            "format": "int64"
          },
          "name": {
            "type": "string"
          },
          "displayName": {
            "type": "string"
          }
        }
      },
      "PageActivityEventDto": {
        "type": "object",
        "properties": {
          "totalPages": {
            "type": "integer",
            "format": "int32"
          },
          "totalElements": {
            "type": "integer",
            "format": "int64"
          },
          "first": {
            "type": "boolean"
          },
          "last": {
            "type": "boolean"
          },
          "size": {
            "type": "integer",
            "format": "int32"
          },
          "content": {
            "type": "array",
            "items": {
              "$ref": "#/components/schemas/ActivityEventDto"
            }
          },
          "number": {
            "type": "integer",
            "format": "int32"
          },
          "sort": {
            "$ref": "#/components/schemas/SortObject"
          },
          "numberOfElements": {
            "type": "integer",
            "format": "int32"
          },
          "pageable": {
            "$ref": "#/components/schemas/PageableObject"
          },
          "empty": {
            "type": "boolean"
          }
        }
      },
      "Link": {
        "type": "object",
        "properties": {
          "href": {
            "type": "string"
          },
          "hreflang": {
            "type": "string"
          },
          "title": {
            "type": "string"
          },
          "type": {
            "type": "string"
          },
          "deprecation": {
            "type": "string"
          },
          "profile": {
            "type": "string"
          },
          "name": {
            "type": "string"
          },
          "templated": {
            "type": "boolean"
          }
        }
      }
    }
  }
}
