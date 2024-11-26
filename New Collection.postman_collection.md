{
	"info": {
		"_postman_id": "f5260558-7228-47ab-9a75-620e0048e433",
		"name": "New Collection",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "26490451",
		"_collection_link": "https://tha777.postman.co/workspace/API-Testing-Be-Talent-Tech~34b05c61-c969-4edd-9654-9ef29b3036b1/collection/26490451-f5260558-7228-47ab-9a75-620e0048e433?action=share&source=collection_link&creator=26490451"
	},
	"item": [
		{
			"name": "Autenticação",
			"item": [
				{
					"name": "Autenticação válida",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"\r",
									"pm.test(\"Status code is 200\", function () {\r",
									"    pm.response.to.have.status(200);\r",
									"});\r",
									"\r",
									""
								],
								"type": "text/javascript",
								"packages": {}
							}
						}
					],
					"request": {
						"auth": {
							"type": "bearer",
							"bearer": [
								{
									"key": "token",
									"value": "4ac3a64cd28caa8",
									"type": "string"
								}
							]
						},
						"method": "POST",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "{\r\n    \"username\" : \"admin\",\r\n    \"password\" : \"password123\"\r\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/auth",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"auth"
							]
						}
					},
					"response": []
				},
				{
					"name": "Autenticação inválida",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"pm.test(\"Status code is 200\", function () {\r",
									"    pm.response.to.have.status(200);\r",
									"});\r",
									""
								],
								"type": "text/javascript",
								"packages": {}
							}
						}
					],
					"request": {
						"auth": {
							"type": "bearer",
							"bearer": [
								{
									"key": "token",
									"value": "4ac3a64cd28caa8",
									"type": "string"
								}
							]
						},
						"method": "POST",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "{\r\n    \"username\" : \"admin\",\r\n    \"password\" : \"password12345\"\r\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/auth",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"auth"
							]
						}
					},
					"response": []
				}
			]
		},
		{
			"name": "Gestão de Reservas",
			"item": [
				{
					"name": "Criar Reserva",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"pm.test(\"Body matches string\", function () {\r",
									"    pm.expect(pm.response.text()).to.include(\"\");\r",
									"});\r",
									"\r",
									"pm.test(\"Status code is 200\", function () {\r",
									"    pm.response.to.have.status(200);\r",
									"});\r",
									"\r",
									"pm.globals.set(\"variable_key\", \"variable_value\");"
								],
								"type": "text/javascript",
								"packages": {}
							}
						}
					],
					"request": {
						"auth": {
							"type": "bearer",
							"bearer": [
								{
									"key": "token",
									"value": "4ac3a64cd28caa8",
									"type": "string"
								}
							]
						},
						"method": "POST",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "{\r\n    \"firstname\" : \"Jim\",\r\n    \"lastname\" : \"Brown\",\r\n    \"totalprice\" : 111,\r\n    \"depositpaid\" : true,\r\n    \"bookingdates\" : {\r\n        \"checkin\" : \"2018-01-01\",\r\n        \"checkout\" : \"2019-01-01\"\r\n    },\r\n    \"additionalneeds\" : \"Breakfast\"\r\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/booking",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"booking"
							]
						}
					},
					"response": []
				},
				{
					"name": "Listar Reservas",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"\r",
									"\r",
									"pm.test(\"Status code is 200\", function () {\r",
									"    pm.response.to.have.status(200);\r",
									"});"
								],
								"type": "text/javascript",
								"packages": {}
							}
						}
					],
					"protocolProfileBehavior": {
						"disableBodyPruning": true
					},
					"request": {
						"auth": {
							"type": "bearer",
							"bearer": [
								{
									"key": "token",
									"value": "4ac3a64cd28caa8",
									"type": "string"
								}
							]
						},
						"method": "GET",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "[\r\n  {\r\n    \"bookingid\": 1\r\n  },\r\n  {\r\n    \"bookingid\": 2\r\n  },\r\n  {\r\n    \"bookingid\": 3\r\n  },\r\n  {\r\n    \"bookingid\": 4\r\n  }\r\n]",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/booking/",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"booking",
								""
							]
						}
					},
					"response": []
				},
				{
					"name": "Buscar Reserva Específica",
					"protocolProfileBehavior": {
						"disableBodyPruning": true
					},
					"request": {
						"auth": {
							"type": "bearer",
							"bearer": [
								{
									"key": "token",
									"value": "4ac3a64cd28caa8",
									"type": "string"
								}
							]
						},
						"method": "GET",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "{\r\n    \"firstname\": \"Sally\",\r\n    \"lastname\": \"Brown\",\r\n    \"totalprice\": 111,\r\n    \"depositpaid\": true,\r\n    \"bookingdates\": {\r\n        \"checkin\": \"2013-02-23\",\r\n        \"checkout\": \"2014-10-23\"\r\n    },\r\n    \"additionalneeds\": \"Breakfast\"\r\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/booking/912",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"booking",
								"912"
							]
						}
					},
					"response": []
				},
				{
					"name": "Atualizar Reserva",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"pm.test(\"Status code is 200\", function () {\r",
									"    pm.response.to.have.status(200);\r",
									"});\r",
									"\r",
									"pm.test(\"Body matches string\", function () {\r",
									"    pm.expect(pm.response.text()).to.include(\"\");\r",
									"});"
								],
								"type": "text/javascript",
								"packages": {}
							}
						}
					],
					"request": {
						"auth": {
							"type": "basic",
							"basic": [
								{
									"key": "password",
									"value": "password123",
									"type": "string"
								},
								{
									"key": "username",
									"value": "admin",
									"type": "string"
								}
							]
						},
						"method": "PUT",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "{\r\n    \"firstname\": \"Mary\",\r\n    \"lastname\": \"Wilson\",\r\n    \"totalprice\": 890,\r\n    \"depositpaid\": false,\r\n    \"bookingdates\": {\r\n        \"checkin\": \"2017-05-06\",\r\n        \"checkout\": \"2024-09-08\"\r\n    }\r\n}",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/booking/4",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"booking",
								"4"
							]
						}
					},
					"response": []
				},
				{
					"name": "Deletar Reserva",
					"event": [
						{
							"listen": "test",
							"script": {
								"exec": [
									"pm.globals.set(\"variable_key\", \"variable_value\");\r",
									"\r",
									"pm.test(\"Response time is less than 200ms\", function () {\r",
									"  pm.expect(pm.response.responseTime).to.be.below(200);\r",
									"});\r",
									"\r",
									"\r",
									""
								],
								"type": "text/javascript",
								"packages": {}
							}
						}
					],
					"request": {
						"auth": {
							"type": "basic",
							"basic": [
								{
									"key": "password",
									"value": "password123",
									"type": "string"
								},
								{
									"key": "username",
									"value": "admin",
									"type": "string"
								}
							]
						},
						"method": "DELETE",
						"header": [],
						"body": {
							"mode": "raw",
							"raw": "",
							"options": {
								"raw": {
									"language": "json"
								}
							}
						},
						"url": {
							"raw": "https://restful-booker.herokuapp.com/booking/3",
							"protocol": "https",
							"host": [
								"restful-booker",
								"herokuapp",
								"com"
							],
							"path": [
								"booking",
								"3"
							]
						}
					},
					"response": []
				}
			]
		}
	],
	"variable": [
		{
			"key": "variable_key",
			"value": ""
		}
	]
}