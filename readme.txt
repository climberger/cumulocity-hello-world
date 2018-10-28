
https://cumulocity.com/guides/microservice-sdk/java/#introduction

Local deployen:

application anlegen: 
POST {URL}/application/applications
"Authorization": "{AUTHORIZATION}"
"Content-Type": "application/vnd.com.nsn.cumulocity.application+json"
"Accept: application/vnd.com.nsn.cumulocity.application+json"

Die response enthält die application id


bootstrap user abfragen:
GET {URL}/application/applications/{APPLICATION_ID}/bootstrapUser
"Authorization": {AUTHORIZATION}
"Content-Type": application/vnd.com.nsn.cumulocity.user+json

die response enthält die tenant daten die als environment variablen zum starten des docker containers gesetzt werden müssen


Wenn über docker local deployed, dann: http://localhost:8080/hello?who=me

