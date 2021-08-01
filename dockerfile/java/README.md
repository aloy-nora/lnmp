# 先打包（后端项目）
docker run -it --rm -v "$PWD":/usr/src/mymaven -v "$HOME/.m2":/root/.m2 -w /usr/src/mymaven masseffect/maven:3.8.1-jdk-11-korant mvn clean package  
# 前端项目打包
docker run -it --rm --name nodejs-env -v "$PWD":/usr/src/app -w /usr/src/app node:14 sh -c "npm install && npm run build"
