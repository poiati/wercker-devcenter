name: ubuntu12.04-webessentials
version: 0.0.1
inherits: wercker/ubuntu12.04-chef10.18.2
type : main
os : ubuntu@12.04
packages :
  - ruby@2.0.0
description : Base box with most popular libraries for the web installed
script : sudo chef-solo -c $WERCKER_SOURCE_DIR/solo.rb -j $WERCKER_SOURCE_DIR/solo.json -l debug
