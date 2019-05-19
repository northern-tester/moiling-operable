# Operability Hooks

## Focus on Snapshot and Action

Start in src/api/index.js

Add: 

import state from './state'

and

router.use('/state', state)

Add a folder to api called 'state', then a file called index.js

Populate that file with:

import {Router} from 'express'

const router = new Router();

router.get('/', function (req, res) {
  res.send("blobby")
});

export default router;

Expand to gather data:

import {Router} from 'express'
import {Speaker} from '../speaker'

const router = new Router();

router.get('/:action?', async function (req, res) {
  if (req.query.action === "speakers") {
    const count = await Speaker.count({}, function (err) {
    });
    const distinct = await Speaker.distinct('name', function (err) {
    });
    res.json({
      "numberOfSpeakers": count,
      "distinctSpeakers": distinct
    });
  } else {
    res.status(500).send("No parameter")
  }
});







