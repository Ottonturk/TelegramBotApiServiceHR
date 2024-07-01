# TelegramBotApiServiceHR
Telegram bot for HR to allow you collect recruiters CV and save their data to google cloud

IF you want to build dockerhub image:
1. Open folder with the project and select with the reight button f the selector git bash on the "my_telegram_bot"

next actions do in the git bash:
2.docker login 
###login to docker/dockerhub app)

3. docker build -t PROJECT_ID/REPOSIORY_ID:tag .

##check in the docker app if it was built in the docker

4. docker push YOUR_PROJECT_ID/YOUR_REPOSIORY_ID:tag

or in the app select button:
push to dockerhub

5. Run the app in the docker with 8080:8080 port installed in the app. Check that it works

##next actions in the google cloud terminal (previously install google cloud cli):

gcloud auth login
gcloud config set project telegram-bot-hr --this is current project..


1. docker login
2.$ gcloud run deploy telegram-bot-hr --image gcr.io/PROJECT_ID/REPOSIORY_ID:tag --platform=managed --region=us-central1 --allow-unauthenticated --timeout=300

