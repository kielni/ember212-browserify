# ember 2.13.2 and browserify issue

    ember init
    npm install --save-dev browserify d3
    ember g controller application

in app/controllers/application.js

    import d3 from 'npm:d3';

run `ember server`

in console:

    ember.debug.js:19818 Error: Could not find module `npm:d3` imported from `ember213/controllers/application`
        at missingModule (loader.js:232)
        at findModule (loader.js:243)
        at Module.findDeps (loader.js:173)
        at findModule (loader.js:247)
        at requireModule (loader.js:26)
        at Class._extractDefaultExport (index.js:392)
        at Class.resolveOther (index.js:108)
        at Class.superWrapper [as resolveOther] (ember.debug.js:42834)
        at Class.resolveController (ember.debug.js:7337)
        at Class.resolve (ember.debug.js:7190)
