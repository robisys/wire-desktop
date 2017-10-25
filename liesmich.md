# liesmich


    "name": "wire-desktop",
    "license": "LicenseRef-LICENSE",
    "private": true,
    "lint-staged": {
    "*.css": [
      "npm run lint:style",
      "git add"
 
 
  
# scripts 
    
    "preinstall": "cd electron && npm install",
    "install": "cd electron && npm run rebuild-native-modules",
    "postinstall": "cd electron && npm run rebuild-neon",
    "prestart": "npm run bundle:dev",
    "start": "electron electron --inspect --devtools --enable-logging",
    "edge": "npm run prestart && electron electron --inspect --devtools --enable-logging --env=https://wire-webapp-edge.zinfra.io",
    "staging": "npm run prestart && electron electron --inspect --devtools --enable-logging --env=https://wire-webapp-staging.zinfra.io",
    "prod": "npm run prestart && electron electron --inspect --devtools --enable-logging --env=https://app.wire.com",
    "localhost": "npm run prestart && electron electron --inspect --devtools --enable-logging --env=http://localhost:8888",
    "lint": "eslint electron",
    "lint:fix:style": "prettier --single-quote --print-width=120 --write '**/*.css'",
    "jest": "jest",
    
## test: 
    "test": "npm run lint && npm run jest && electron-mocha tests",
    "build:macos": "grunt macos-prod",
    "build:win": "grunt win-prod",
    "build:linux": "grunt linux-prod",
    "bundle:dev": "webpack",
    "bundle": "webpack --env.production"
 
 
 
    "repository": {
    "type": "git",
    "url": "https://github.com/wireapp/wire-desktop.git"
 
 
 
    "build": {
    "directories": {
      "buildResources": "resources",
      "app": "electron",
      "output": "wrap/dist"


  
    "devDependencies": {
    "babel-core": "6.26.0",
    "babel-jest": "21.2.0",
    "babel-loader": "7.1.2",
    "babel-plugin-transform-object-rest-spread": "6.26.0",
    "babel-preset-es2015": "6.24.1",
    "babel-preset-react": "6.24.1",
    "css-loader": "0.28.7",
    "electron-builder": "18.6.2",
    "electron-mocha": "4.0.3",
    "electron-packager": "9.1.0",
    "electron-winstaller": "2.5.2",
    "electron": "1.7.9",
    "eslint-plugin-react": "7.4.0",
    "eslint": "4.9.0",
    "grunt-contrib-clean": "1.1.0",
    "grunt-git": "1.0.7",
    "grunt-github-changes": "0.1.0",
    "grunt-gitinfo": "0.1.8",
    "grunt": "1.0.1",
    "husky": "0.14.3",
    "jest": "21.2.1",
    "lint-staged": "4.3.0",
    "load-grunt-tasks": "3.5.2",
    "prettier": "1.7.4",
    "style-loader": "0.19.0",


    "webpack": "3.8.1"
    "dependencies": {
    "debug": "3.1.0"

