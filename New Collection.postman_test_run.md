{
	"id": "6ff79a93-ca91-4e5a-afbd-da67a91c7bb4",
	"name": "New Collection",
	"timestamp": "2024-11-26T17:50:22.560Z",
	"collection_id": "26490451-f5260558-7228-47ab-9a75-620e0048e433",
	"folder_id": 0,
	"environment_id": "0",
	"totalPass": 6,
	"delay": 0,
	"persist": true,
	"status": "finished",
	"startedAt": "2024-11-26T17:50:20.669Z",
	"totalFail": 0,
	"results": [
		{
			"id": "e53c4daf-1076-4a69-b5c9-5ca18784bbfb",
			"name": "Autenticação válida",
			"url": "https://restful-booker.herokuapp.com/auth",
			"time": 169,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Status code is 200": true
			},
			"testPassFailCounts": {
				"Status code is 200": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				169
			],
			"allTests": [
				{
					"Status code is 200": true
				}
			]
		},
		{
			"id": "aca74fb8-e40f-41d8-9cac-d4f6ed5f55d9",
			"name": "Autenticação inválida",
			"url": "https://restful-booker.herokuapp.com/auth",
			"time": 165,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Status code is 200": true
			},
			"testPassFailCounts": {
				"Status code is 200": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				165
			],
			"allTests": [
				{
					"Status code is 200": true
				}
			]
		},
		{
			"id": "193cafdc-82bf-4893-b9a3-12dec78b7dfd",
			"name": "Criar Reserva",
			"url": "https://restful-booker.herokuapp.com/booking",
			"time": 160,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Body matches string": true,
				"Status code is 200": true
			},
			"testPassFailCounts": {
				"Body matches string": {
					"pass": 1,
					"fail": 0
				},
				"Status code is 200": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				160
			],
			"allTests": [
				{
					"Body matches string": true,
					"Status code is 200": true
				}
			]
		},
		{
			"id": "470ce88f-b050-4115-a1bb-7a6d14d6a09f",
			"name": "Listar Reservas",
			"url": "https://restful-booker.herokuapp.com/booking/",
			"time": 170,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Status code is 200": true
			},
			"testPassFailCounts": {
				"Status code is 200": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				170
			],
			"allTests": [
				{
					"Status code is 200": true
				}
			]
		},
		{
			"id": "9391c7be-868f-4f93-b3d4-6b03c53e461e",
			"name": "Buscar Reserva Específica",
			"url": "https://restful-booker.herokuapp.com/booking/912",
			"time": 157,
			"responseCode": {
				"code": 404,
				"name": "Not Found"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				157
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "045f040c-5d03-485e-a31f-bf3607220bf0",
			"name": "Atualizar Reserva",
			"url": "https://restful-booker.herokuapp.com/booking/912",
			"time": 164,
			"responseCode": {
				"code": 405,
				"name": "Method Not Allowed"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				164
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "3b492f34-d26e-46d4-bc19-99f6c59cb51f",
			"name": "Deletar Reserva",
			"url": "https://restful-booker.herokuapp.com/booking/3",
			"time": 162,
			"responseCode": {
				"code": 201,
				"name": "Created"
			},
			"tests": {
				"Response time is less than 200ms": true
			},
			"testPassFailCounts": {
				"Response time is less than 200ms": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				162
			],
			"allTests": [
				{
					"Response time is less than 200ms": true
				}
			]
		}
	],
	"count": 1,
	"totalTime": 1147,
	"collection": {
		"requests": [
			{
				"id": "e53c4daf-1076-4a69-b5c9-5ca18784bbfb",
				"method": "POST"
			},
			{
				"id": "aca74fb8-e40f-41d8-9cac-d4f6ed5f55d9",
				"method": "POST"
			},
			{
				"id": "193cafdc-82bf-4893-b9a3-12dec78b7dfd",
				"method": "POST"
			},
			{
				"id": "470ce88f-b050-4115-a1bb-7a6d14d6a09f",
				"method": "GET"
			},
			{
				"id": "9391c7be-868f-4f93-b3d4-6b03c53e461e",
				"method": "GET"
			},
			{
				"id": "045f040c-5d03-485e-a31f-bf3607220bf0",
				"method": "PUT"
			},
			{
				"id": "3b492f34-d26e-46d4-bc19-99f6c59cb51f",
				"method": "DELETE"
			}
		]
	}
}