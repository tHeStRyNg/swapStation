## SwapStation Interface

### Install
#### Use Node 16 as required
``` error detective-postcss@5.1.1: The engine "node" is incompatible with this module. Expected version "12.x || 14.x || 16.x". Got "20.12.0" ```

#### Install Node 16
``` nvm use 16 ``` # nvm install 16 and then nvm use 16

#### Yarn Install
``` yarn install ```

#### NPM Build
``` npm run build ```

#### NPM Start
``` npm run start ```

Few things to understand:

npm: run command is mandatory to execute user defined scripts.
yarn: run command is not mandatory to execute user defined scripts.

start command is not a user defined script name, so you may not need to specify run command to execute it.

So, all the below commands work similar!

npm start
npm run start
yarn start
yarn run start
If you have a user defined script named 'app':

npm app (Does not work!) XX
npm run app (Works!)
yarn app (Works!)
yarn run app (Works!)
Note: By default start runs node server.js in case not explicitly defined.

#### Troubleshooting Build Process
``` FATAL ERROR: Ineffective mark-compacts near heap limit Allocation failed - JavaScript heap out of memory ```

### Set value of max-space-size (in MB)
``` export NODE_OPTIONS="--max-old-space-size=8192" ```
### See the current value of max-old-space-size (in MB)
``` node -e 'console.log(v8.getHeapStatistics().heap_size_limit/(1024*1024))' ```