###
#
##

CLIENT_ID =
CLIENT_SECRET =

build:
	./gradlew build
# build

bootRun:
	./gradlew bootRun
# bootRun

request: token
	curl -s localhost:8081 -H "Authorization: Bearer $$(cat token.tmp)"
# request

token:
	curl -s http://localhost:8080/oauth/token -d scope=read -d grant_type=password -d username=user -d password=password -u $(CLIENT_ID):$(CLIENT_SECRET) > token.tmp
# token

auth:
	echo "Make sure to set the client id and secret in the application.properties!!"
	java -jar .tmp/auth-server.jar
# auth

# Makefile
