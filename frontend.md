# Vue

### №1. This relative module was not found

I ran `npm run serve` and vue throw error: `This relative module was not found * ./components/v-catalog in ./node_modules/cache-loader/dist/cjs.js`.

#### I try to:
- reinstall vue
- force audit fix
- clean cache
- create vue 2.x ver. project
- update dependecies
- delete dependecies
- update name in vue file-importer
- delete `node_modules`
- delete `"use stricts" in `cjs.js` 

#### What confuses me:
- All files are exists
- Empty vue project creates with high vulnerabilities, I think that means critical errors
- After deleting `HelloWorld.vue` generates new same error
- Message says about cache in `/node_modules/` *I know that compiler need to show when it crash and I shouldn't give this much attention*

#### What helps.
I had a typo in import line
```javascript
import vCatalog from './components/v-catalog'
```
All files has been in one folder **components** *(including importer-file and imported)* and I should to write:
```javascript
import vCatalog from './v-catalog'
```
