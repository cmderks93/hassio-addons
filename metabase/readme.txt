docker build -t sanderdw/ha-metabase-aarch64:0.0.2 . --build-arg BUILD_FROM=homeassistant/aarch64-base-debian
docker login --username=sanderdw
docker push sanderdw/ha-metabase-aarch64:0.0.2

cd /github_workspace/hassio-addons/metabase
docker build -t sanderdw/ha-metabase-amd64:0.0.2 . --build-arg BUILD_FROM=homeassistant/amd64-base-debian
docker push sanderdw/ha-metabase-amd64:0.0.2