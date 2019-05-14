# Operability Hooks

## Types

* Liveness
* Readiness
* Snapshot
* Action

## Focus on Snapshot and Action

### Snapshot

* Lets build a summary of mongo contents hook for our containers
* We could do this from within an existing endpoint, ask people what they want to expose...

### Action

* Lets build a restart hook for the app
* Must be behind a master token I imagine:

import { password as passwordAuth, master, token } from '../../services/passport'
import { Router } from 'express'
import { middleware as query } from 'querymen'
import { middleware as body } from 'bodymen'
import { password as passwordAuth, master, token } from '../../services/passport'
import { reset } from './controller'

router.post('/',
  // for the token master(),
  // no body - body({ email, password, name, picture, role }),
  reset)

