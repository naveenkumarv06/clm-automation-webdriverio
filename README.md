# install wdio
 - `npm init wdio .`

 # package.json
 - check `type`: `module`

 # tsconfig.json
 - check `"module":"ESNext"`
 - check `"resolveJsonModule": true`
 - add `"esModuleInterop": true`
 - change `"strict": false`

 # wdio.conf.ts
 - check `project: './tsconfig.json'`
 - add specs: [
        // ToDo: define location for spec files here
        `${process.cwd()}/test/features/**/*.feature`
    ]
 - add  `cucumberOpts: {
        // <string[]> (file/dir) require files before executing features
        require: ['./test/features/step-definitions/*.ts'], }`