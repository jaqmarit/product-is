Update forked repo
https://github.com/jaqmarit/product-is.git

Steps:
git fetch upstream
git checkout master
git merge upstream/master
git push origin master


To build:
#!/bin/sh
set -x
mvn clean install -DskipTests
#unzip -o modules/distribution/target/wso2is-5.7.0.zip wso2is-5.7.0/repository/components/plugins/org.wso2.carbon.user.core_4.4.35.jar
#cp  wso2is-5.7.0/repository/components/plugins/org.wso2.carbon.user.core_4.4.35.jar  /Users/jmarit/dev/git/owens-wso2is/wso2is/owens-wso2is-dist/target/wso2is-5.7.0/repository/components/plugins/

Copy built dist to Owens project:
#!/bin/sh
set -x
cp modules/distribution/target/wso2is-5.7.0.zip /Users/jmarit/dev/git/owens-wso2is/wso2is/owens-wso2is-dist/src/main/artifacts/
