FROM python:3.10-slim-buster
# select a existing docker image fro docker hub
# which again depends on other images

WORKDIR /backend-flask
# defines your working directory in your container

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
# install needed python libs

COPY . .
#copy whole app directory to the image

ENV PORT=4567
ENV FLASK_ENV=development
ENV GITPOD_WORKSPACE_ID=krga-awsbootcampcrudd-u9rqfgo81x9
ENV GITPOD_WORKSPACE_CLUSTER_HOST=ws-eu87.gitpod.io
ENV FRONTEND_URL="https://3000-${GITPOD_WORKSPACE_ID}.${GITPOD_WORKSPACE_CLUSTER_HOST}"
ENV BACKEND_URL="https://4567-${GITPOD_WORKSPACE_ID}.${GITPOD_WORKSPACE_CLUSTER_HOST}"

EXPOSE ${PORT}
CMD ["python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]