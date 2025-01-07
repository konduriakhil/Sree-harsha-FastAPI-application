# Overwrite CMD Instruction
docker run --rm -d --name app1 --publish 8081:8080  sreeharshav/devsecopsb41:v6 --port 8080

<!-- docker run --rm -d --name fastapi1 \
-e AWS_ACCESS_KEY_ID=AKIA2QEFLENWNTLXQINZ \
-e AWS_SECRET_ACCESS_KEY=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 \
-e APP_NAME="FASTAPI_APP" -e HOSTNAME="TESTCON1" -e DEPLOYMENT_BRANCH="DEV" \
-p 9000:80 sreeharshav/devsecopsb42:v4 -->

<!-- docker run --rm -d --name fastapi1 \
-e AWS_ACCESS_KEY_ID=AKIA2QEFLENWA6Z4KDDT \
-e AWS_SECRET_ACCESS_KEY=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 \
-v /root:/rootdata \
-p 80:80 sreeharshav/multistage:v1 -->

#Build Arguments
docker build --build-arg T_VERSION="1.8.5"  -t sreeharshav/devsecopsb41:v2 -f Dockerfile.Dev .

con_name = os.getenv("HOSTNAME")
b_name = os.getenv("DEPLOYMENT_BRANCH")
app_name = os.getenv("APP_NAME")