# cordova-build-fail

To repro:
```
$ git clone https://github.com/brucejo75/cordova-build-fail
$ cd cordova-build-fail/app
$ meteor npm install
$ npm run build |& tee .buildlog
```

Errors out:
```
Plugin cordova-plugin-statusbar was not installed.
/home/brucejo/.meteor/packages/meteor-tool/.2.7.3.1xu2799.gx8e++os.linux.x86_64+web.browser+web.browser.legacy+web.cordova/mt-os.linux.x86_64/dev_bundle/lib/node_modules/meteor-promise/promise_server.js:218
      throw error;
      ^

Error: Some Cordova plugins installation failed: (cordova-plugin-statusbar).
    at CordovaProject.ensurePluginsWereInstalled (/tools/cordova/project.js:822:13)
    at CordovaProject.ensurePluginsWereInstalled (/tools/cordova/project.js:819:12)
    at /tools/cordova/project.js:781:14
    at Object.enterJob (/tools/utils/buildmessage.js:388:12)
    at CordovaProject.ensurePluginsAreSynchronized (/tools/cordova/project.js:639:18)
    at CordovaProject.prepareFromAppBundle (/tools/cordova/project.js:271:10)
    at /tools/cli/commands.js:1183:24
    at Object.enterJob (/tools/utils/buildmessage.js:388:12)
    at /tools/cli/commands.js:1171:20
    at Object.capture (/tools/utils/buildmessage.js:283:5)
    at Object.main.captureAndExit (/tools/cli/main.js:281:29)
    at buildCommand (/tools/cli/commands.js:1162:10)
    at /tools/cli/commands.js:949:25
    at Function.run (/home/brucejo/.meteor/packages/meteor-tool/.2.7.3.1xu2799.gx8e++os.linux.x86_64+web.browser+web.browser.legacy+web.cordova/mt-os.linux.x86_64/tools/tool-env/tools/tool-env/profile.ts:289:14)
    at /tools/cli/commands.js:947:18
    at /home/brucejo/.meteor/packages/meteor-tool/.2.7.3.1xu2799.gx8e++os.linux.x86_64+web.browser+web.browser.legacy+web.cordova/mt-os.linux.x86_64/dev_bundle/lib/node_modules/meteor-promise/fiber_pool.js:43:40
 => awaited here:
    at Promise.await (/home/brucejo/.meteor/packages/meteor-tool/.2.7.3.1xu2799.gx8e++os.linux.x86_64+web.browser+web.browser.legacy+web.cordova/mt-os.linux.x86_64/dev_bundle/lib/node_modules/meteor-promise/promise_server.js:60:12)
    at /tools/cli/main.js:1535:7
```
