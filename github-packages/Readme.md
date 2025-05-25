export GH_USERNAME='BlackMamba2707'
export GH_TOKEN=''
export GH_IMAGE_NAME='hello-world'
export GH_VER='1.0.0'
export TAG_NAME='ghcr.io/blackmamba2707/$GH_IMAGE_NAME:$GH_VER'
echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-world:latest $TAG_NAME

docker push $TAG_NAME