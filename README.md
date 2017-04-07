# api documentation for  [rollbar (v0.6.5)](https://rollbar.com/docs/notifier/node_rollbar/)  [![npm package](https://img.shields.io/npm/v/npmdoc-rollbar.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-rollbar) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-rollbar.svg)](https://travis-ci.org/npmdoc/node-npmdoc-rollbar)
#### A standalone (Node.js) client for Rollbar

[![NPM](https://nodei.co/npm/rollbar.png?downloads=true)](https://www.npmjs.com/package/rollbar)

[![apidoc](https://npmdoc.github.io/node-npmdoc-rollbar/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-rollbar_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-rollbar/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-rollbar/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-rollbar/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rollbar, Inc.",
        "email": "support@rollbar.com"
    },
    "bugs": {
        "url": "https://github.com/rollbar/node_rollbar/issues"
    },
    "dependencies": {
        "async": "~1.2.1",
        "debug": "2.2.0",
        "decache": "^3.0.5",
        "json-stringify-safe": "~5.0.0",
        "lru-cache": "~2.2.1",
        "request-ip": "~1.2.3",
        "uuid": "~3.0.0"
    },
    "description": "A standalone (Node.js) client for Rollbar",
    "devDependencies": {
        "express": "*",
        "jade": "~0.27.7",
        "sinon": "1.16.1",
        "vows": "~0.7.0"
    },
    "directories": {},
    "dist": {
        "shasum": "e20352201fdab79b96e3c6a02d7f4a12c3dc2dfe",
        "tarball": "https://registry.npmjs.org/rollbar/-/rollbar-0.6.5.tgz"
    },
    "engines": {
        "node": ">= 0.6.0"
    },
    "gitHead": "cd5953564b59426bae9ad94848bcc2c7bca017a9",
    "homepage": "https://rollbar.com/docs/notifier/node_rollbar/",
    "keywords": [
        "rollbar",
        "exception",
        "uncaughtException",
        "error",
        "ratchetio",
        "ratchet"
    ],
    "license": "MIT",
    "main": "rollbar",
    "maintainers": [
        {
            "name": "brianr",
            "email": "brianrue@gmail.com"
        },
        {
            "name": "coryvirok",
            "email": "cory@ratchet.io"
        },
        {
            "name": "dampier",
            "email": "dampierface@gmail.com"
        },
        {
            "name": "jfarrimo",
            "email": "jay@rollbar.com"
        },
        {
            "name": "jondeandres",
            "email": "jon@rollbar.com"
        },
        {
            "name": "rokob",
            "email": "fabian.ledvina@gmail.com"
        }
    ],
    "name": "rollbar",
    "optionalDependencies": {
        "decache": "^3.0.5"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/rollbar/node_rollbar.git"
    },
    "scripts": {
        "test": "vows --spec test/*.js",
        "test-and-coverage": "istanbul cover -- vows --spec test/*.js"
    },
    "version": "0.6.5"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module rollbar](#apidoc.module.rollbar)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>Error (message, nested)](#apidoc.element.rollbar.Error)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>Error.super_ ()](#apidoc.element.rollbar.Error.super_)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>errorHandler (accessToken, options)](#apidoc.element.rollbar.errorHandler)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>handleError (err, req, callback)](#apidoc.element.rollbar.handleError)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>handleErrorWithPayloadData (err, payloadData, req, callback)](#apidoc.element.rollbar.handleErrorWithPayloadData)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>handleUncaughtExceptions (accessToken, options)](#apidoc.element.rollbar.handleUncaughtExceptions)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>handleUncaughtExceptionsAndRejections (accessToken, options)](#apidoc.element.rollbar.handleUncaughtExceptionsAndRejections)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>handleUnhandledRejections (accessToken, options)](#apidoc.element.rollbar.handleUnhandledRejections)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>init (accessToken, options)](#apidoc.element.rollbar.init)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>reportMessage (message, level, req, callback)](#apidoc.element.rollbar.reportMessage)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>reportMessageWithPayloadData (message, payloadData, req, callback)](#apidoc.element.rollbar.reportMessageWithPayloadData)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>wait (callback)](#apidoc.element.rollbar.wait)
1.  object <span class="apidocSignatureSpan">rollbar.</span>api
1.  object <span class="apidocSignatureSpan">rollbar.</span>deploy
1.  object <span class="apidocSignatureSpan">rollbar.</span>logger
1.  object <span class="apidocSignatureSpan">rollbar.</span>notifier
1.  object <span class="apidocSignatureSpan">rollbar.</span>parser
1.  object <span class="apidocSignatureSpan">rollbar.</span>parser.cache

#### [module rollbar.Error](#apidoc.module.rollbar.Error)
1.  [function <span class="apidocSignatureSpan">rollbar.</span>Error (message, nested)](#apidoc.element.rollbar.Error.Error)
1.  [function <span class="apidocSignatureSpan">rollbar.Error.</span>super_ ()](#apidoc.element.rollbar.Error.super_)

#### [module rollbar.Error.super_](#apidoc.module.rollbar.Error.super_)
1.  [function <span class="apidocSignatureSpan">rollbar.Error.</span>super_ ()](#apidoc.element.rollbar.Error.super_.super_)
1.  [function <span class="apidocSignatureSpan">rollbar.Error.super_.</span>captureStackTrace ()](#apidoc.element.rollbar.Error.super_.captureStackTrace)
1.  number <span class="apidocSignatureSpan">rollbar.Error.super_.</span>stackTraceLimit

#### [module rollbar.api](#apidoc.module.rollbar.api)
1.  [function <span class="apidocSignatureSpan">rollbar.api.</span>init (accessToken, options)](#apidoc.element.rollbar.api.init)
1.  [function <span class="apidocSignatureSpan">rollbar.api.</span>postItem (item, callback)](#apidoc.element.rollbar.api.postItem)
1.  object <span class="apidocSignatureSpan">rollbar.api.</span>accessToken
1.  string <span class="apidocSignatureSpan">rollbar.api.</span>VERSION
1.  string <span class="apidocSignatureSpan">rollbar.api.</span>endpoint

#### [module rollbar.deploy](#apidoc.module.rollbar.deploy)
1.  [function <span class="apidocSignatureSpan">rollbar.deploy.</span>createDeploy (accessToken, params, opts, callback)](#apidoc.element.rollbar.deploy.createDeploy)
1.  [function <span class="apidocSignatureSpan">rollbar.deploy.</span>getDeploy (accessToken, deployId, opts, callback)](#apidoc.element.rollbar.deploy.getDeploy)
1.  [function <span class="apidocSignatureSpan">rollbar.deploy.</span>listDeploys (accessToken, pageNum, opts, callback)](#apidoc.element.rollbar.deploy.listDeploys)

#### [module rollbar.logger](#apidoc.module.rollbar.logger)
1.  [function <span class="apidocSignatureSpan">rollbar.logger.</span>error ()](#apidoc.element.rollbar.logger.error)
1.  [function <span class="apidocSignatureSpan">rollbar.logger.</span>log ()](#apidoc.element.rollbar.logger.log)

#### [module rollbar.notifier](#apidoc.module.rollbar.notifier)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>_extractIp (req)](#apidoc.element.rollbar.notifier._extractIp)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>_levelGteMinimum (item)](#apidoc.element.rollbar.notifier._levelGteMinimum)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>_scrubRequestHeaders (headersToScrub, headers)](#apidoc.element.rollbar.notifier._scrubRequestHeaders)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>_scrubRequestParams (paramsToScrub, params)](#apidoc.element.rollbar.notifier._scrubRequestParams)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>handleError (err, req, callback)](#apidoc.element.rollbar.notifier.handleError)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>handleErrorWithPayloadData (err, payloadData, req, callback)](#apidoc.element.rollbar.notifier.handleErrorWithPayloadData)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>init (api, options)](#apidoc.element.rollbar.notifier.init)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>pendingItemsCount ()](#apidoc.element.rollbar.notifier.pendingItemsCount)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>reportMessage (message, level, req, callback)](#apidoc.element.rollbar.notifier.reportMessage)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>reportMessageWithPayloadData (message, payloadData, req, callback)](#apidoc.element.rollbar.notifier.reportMessageWithPayloadData)
1.  [function <span class="apidocSignatureSpan">rollbar.notifier.</span>wait (callback)](#apidoc.element.rollbar.notifier.wait)
1.  string <span class="apidocSignatureSpan">rollbar.notifier.</span>VERSION

#### [module rollbar.parser](#apidoc.module.rollbar.parser)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.</span>parseException (exc, callback)](#apidoc.element.rollbar.parser.parseException)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.</span>parseStack (stack, callback)](#apidoc.element.rollbar.parser.parseStack)
1.  object <span class="apidocSignatureSpan">rollbar.parser.</span>cache
1.  object <span class="apidocSignatureSpan">rollbar.parser.</span>pendingReads

#### [module rollbar.parser.cache](#apidoc.module.rollbar.parser.cache)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>del (key)](#apidoc.element.rollbar.parser.cache.del)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>dump ()](#apidoc.element.rollbar.parser.cache.dump)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>dumpLru ()](#apidoc.element.rollbar.parser.cache.dumpLru)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>forEach (fn, thisp)](#apidoc.element.rollbar.parser.cache.forEach)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>get (key)](#apidoc.element.rollbar.parser.cache.get)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>has (key)](#apidoc.element.rollbar.parser.cache.has)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>keys ()](#apidoc.element.rollbar.parser.cache.keys)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>lengthCalculator ()](#apidoc.element.rollbar.parser.cache.lengthCalculator)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>reset ()](#apidoc.element.rollbar.parser.cache.reset)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>set (key, value)](#apidoc.element.rollbar.parser.cache.set)
1.  [function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>values ()](#apidoc.element.rollbar.parser.cache.values)
1.  number <span class="apidocSignatureSpan">rollbar.parser.cache.</span>itemCount
1.  number <span class="apidocSignatureSpan">rollbar.parser.cache.</span>length
1.  number <span class="apidocSignatureSpan">rollbar.parser.cache.</span>max



# <a name="apidoc.module.rollbar"></a>[module rollbar](#apidoc.module.rollbar)

#### <a name="apidoc.element.rollbar.Error"></a>[function <span class="apidocSignatureSpan">rollbar.</span>Error (message, nested)](#apidoc.element.rollbar.Error)
- description and source-code
```javascript
function RollbarError(message, nested)
{
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);

  this.message = message;
  this.nested = nested;
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.Error.super_"></a>[function <span class="apidocSignatureSpan">rollbar.</span>Error.super_ ()](#apidoc.element.rollbar.Error.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.errorHandler"></a>[function <span class="apidocSignatureSpan">rollbar.</span>errorHandler (accessToken, options)](#apidoc.element.rollbar.errorHandler)
- description and source-code
```javascript
errorHandler = function (accessToken, options) {
<span class="apidocCodeCommentSpan">  /*
   * A middleware handler for connect and express.js apps. For a list
   * of supported options, see the init() docs above.
   *
   * All exceptions thrown from inside an express or connect get/post/etc... handler
   * will be sent to rollbar when this middleware is installed.
   */
</span>  exports.init(accessToken, options);
  return function (err, req, res, next) {
    var cb = function (rollbarErr) {
      if (rollbarErr) {
        logger.error('Error reporting to rollbar, ignoring: ' + rollbarErr);
      }
      return next(err, req, res);
    };

    if (!err) {
      return next(err, req, res);
    }

    if (err instanceof Error) {
      return notifier.handleError(err, req, cb);
    }

    return notifier.reportMessage('Error: ' + err, 'error', req, cb);
  };
}
```
- example usage
```shell
...
var app = express();

app.get('/', function(req, res) {
  // ...
});

// Use the rollbar error handler to send exceptions to your rollbar account
app.use(rollbar.errorHandler('POST_SERVER_ITEM_ACCESS_TOKEN'));

app.listen(6943);
'''

### Using Hapi

'''js
...
```

#### <a name="apidoc.element.rollbar.handleError"></a>[function <span class="apidocSignatureSpan">rollbar.</span>handleError (err, req, callback)](#apidoc.element.rollbar.handleError)
- description and source-code
```javascript
handleError = function (err, req, callback) {
  if (typeof req === 'function') {
    callback = req;
    req = null;
  }
  if (err instanceof Error) {
    return exports.handleErrorWithPayloadData(err, {}, req, callback);
  }

  var stringError;
  try {
    stringError = JSON.stringify(err);
  } catch (e) {
    stringError = stringify(err);
  } finally {
    return exports.reportMessage(stringError, 'error', req, callback);
  }
}
```
- example usage
```shell
...
server.on('request-error', function(request, error) {
// Note: before Hapi v8.0.0, this should be 'internalError' instead of 'request-error'
var cb = function(rollbarErr) {
  if (rollbarErr)
    console.error('Error reporting to rollbar, ignoring: '+rollbarErr);
};
if (error instanceof Error)
  return rollbar.handleError(error, request, cb);
rollbar.reportMessage('Error: '+error, 'error', request, cb);
});
// End Rollbar initialization code

server.route({
method: 'GET',
path:'/throw_error',
...
```

#### <a name="apidoc.element.rollbar.handleErrorWithPayloadData"></a>[function <span class="apidocSignatureSpan">rollbar.</span>handleErrorWithPayloadData (err, payloadData, req, callback)](#apidoc.element.rollbar.handleErrorWithPayloadData)
- description and source-code
```javascript
handleErrorWithPayloadData = function (err, payloadData, req, callback) {
  // Allow the user to call with an optional request and callback
  // e.g. handleErrorWithPayloadData(err, payloadData, req, callback)
  //   or handleErrorWithPayloadData(err, payloadData, callback)
  //   or handleErrorPayloadData(err, payloadData)
  if (typeof req === 'function') {
    callback = req;
    req = null;
  }

  if (!(err instanceof Error)) {
    if (typeof callback === 'function') {
      return callback(new Error('handleError was passed something other than an Error: ' + err));
    }
  }
  addItem({error: err, payload: payloadData, request: req}, callback);
}
```
- example usage
```shell
...
    }
  });

  // if you have a request and a callback, pass the callback last
  rollbar.handleError(e, request, callback);

  // to specify payload options - like extra data, or the level - use handleErrorWithPayloadData
  rollbar.handleErrorWithPayloadData(e, {level: "warning", custom: {someKey: "arbitrary value"}});

  // can also take request and callback, like handleError:
  rollbar.handleErrorWithPayloadData(e, {level: "info"}, request);
  rollbar.handleErrorWithPayloadData(e, {level: "info"}, callback);
  rollbar.handleErrorWithPayloadData(e, {level: "info"}, request, callback);
}
'''
...
```

#### <a name="apidoc.element.rollbar.handleUncaughtExceptions"></a>[function <span class="apidocSignatureSpan">rollbar.</span>handleUncaughtExceptions (accessToken, options)](#apidoc.element.rollbar.handleUncaughtExceptions)
- description and source-code
```javascript
handleUncaughtExceptions = function (accessToken, options) {
<span class="apidocCodeCommentSpan">  /*
   * Registers a handler for the process.uncaughtException event
   *
   * If options.exitOnUncaughtException is set to true, the notifier will
   * immediately send the uncaught exception + all queued items to rollbar,
   * then call process.exit(1).
   *
   * Note: The node.js authors advise against using these type of handlers.
   * More info: http://nodejs.org/api/process.html#process_event_uncaughtexception
   *
   */
</span>
  // Default to not exiting on uncaught exceptions unless options.exitOnUncaughtException is set.
  options = options || {};
  var exitOnUncaught = options.exitOnUncaughtException === undefined ?
        false : !!options.exitOnUncaughtException;
  delete options.exitOnUncaughtException;

  exports.init(accessToken, options);

  if (initialized) {
    process.on('uncaughtException', function (err) {
      logger.error('Handling uncaught exception.');
      logger.error(err);

      notifier.handleError(err, function (err) {
        if (err) {
          logger.error('Encountered an error while handling an uncaught exception.');
          logger.error(err);
        }

        if (exitOnUncaught) {
          process.exit(1);
        }
      });
    });
  } else {
    logger.error('Rollbar is not initialized. Uncaught exceptions will not be tracked.');
  }
}
```
- example usage
```shell
...
var options = {
  // Call process.exit(1) when an uncaught exception occurs but after reporting all
  // pending errors to Rollbar.
  //
  // Default: false
  exitOnUncaughtException: true
};
rollbar.handleUncaughtExceptions("POST_SERVER_ITEM_ACCESS_TOKEN", options);
'''

#### Unhandled rejections

Rollbar can also be registered as a handler for any unhandled Promise rejections in your Node process:

'''js
...
```

#### <a name="apidoc.element.rollbar.handleUncaughtExceptionsAndRejections"></a>[function <span class="apidocSignatureSpan">rollbar.</span>handleUncaughtExceptionsAndRejections (accessToken, options)](#apidoc.element.rollbar.handleUncaughtExceptionsAndRejections)
- description and source-code
```javascript
handleUncaughtExceptionsAndRejections = function (accessToken, options) {
  exports.handleUncaughtExceptions(accessToken, options);
  exports.handleUnhandledRejections(accessToken, options);
}
```
- example usage
```shell
...
'''js
rollbar.handleUnhandledRejections("POST_SERVER_ITEM_ACCESS_TOKEN");
'''

To simplify enabling both handlers, you can use the 'handleUncaughtExceptionsAndRejections' method.

'''js
rollbar.handleUncaughtExceptionsAndRejections("POST_SERVER_ITEM_ACCESS_TOKEN", options);
'''

### Caught exceptions

To report an exception that you have caught, use ['handleError'](https://github.com/rollbar/node_rollbar/blob/master/rollbar.js#
L152) or the full-powered ['handleErrorWithPayloadData'](https://github.com/rollbar/node_rollbar/blob/master/rollbar.js#L176):

'''js
...
```

#### <a name="apidoc.element.rollbar.handleUnhandledRejections"></a>[function <span class="apidocSignatureSpan">rollbar.</span>handleUnhandledRejections (accessToken, options)](#apidoc.element.rollbar.handleUnhandledRejections)
- description and source-code
```javascript
handleUnhandledRejections = function (accessToken, options) {
<span class="apidocCodeCommentSpan">  /*
   * Registers a handler for the process.unhandledRejection event.
   */
</span>
  options = options || {};

  exports.init(accessToken, options);

  if (initialized) {
    process.on('unhandledRejection', function (reason) {
      logger.error('Handling unhandled rejection.');
      logger.error(reason);

      notifier.handleError(reason, function (err) {
        if (err) {
          logger.error('Encountered an error while handling an unhandled rejection.');
          logger.error(err);
        }
      })
    });
  } else {
    logger.error('Rollbar is not initialized. Uncaught rejections will not be tracked.');
  }
}
```
- example usage
```shell
...
'''

#### Unhandled rejections

Rollbar can also be registered as a handler for any unhandled Promise rejections in your Node process:

'''js
rollbar.handleUnhandledRejections("POST_SERVER_ITEM_ACCESS_TOKEN");
'''

To simplify enabling both handlers, you can use the 'handleUncaughtExceptionsAndRejections' method.

'''js
rollbar.handleUncaughtExceptionsAndRejections("POST_SERVER_ITEM_ACCESS_TOKEN", options);
'''
...
```

#### <a name="apidoc.element.rollbar.init"></a>[function <span class="apidocSignatureSpan">rollbar.</span>init (accessToken, options)](#apidoc.element.rollbar.init)
- description and source-code
```javascript
init = function (accessToken, options) {
<span class="apidocCodeCommentSpan">  /*
   * Initialize the rollbar library.
   *
   * For more information on each option, see http://rollbar.com/docs/api_items/
   *
   * Supported options, (all optional):
   *
   *  host - Default: os.hostname() - the hostname of the server the node.js process is running on
   *  environment - Default: 'unspecified' - the environment the code is running in. e.g. 'staging'
   *  endpoint - Default: 'https://api.rollbar.com/api/1/' - the url to send items to
   *  root - the path to your code, (not including any trailing slash) which will be used to link
   *    source files on rollbar
   *  branch - the branch in your version control system for this code
   *  codeVersion - the version or revision of your code
   *  enabled - Default: true - determines if errors gets reported to Rollbar
   *
   */
</span>  if (!initialized) {
    options = options || {};
    if (!accessToken && options.enabled !== false) {
      logger.error('Missing access_token.');
      return;
    }

    options.environment = options.environment || process.env.NODE_ENV || 'unspecified';

    api.init(accessToken, options);
    notifier.init(api, options);
    initialized = true;
  }
}
```
- example usage
```shell
...
<!-- Sub:[TOC] -->

## Quick start

'''js
// include and initialize the rollbar library with your access token
var rollbar = require("rollbar");
rollbar.init("POST_SERVER_ITEM_ACCESS_TOKEN");

// record a generic message and send to rollbar
rollbar.reportMessage("Hello world!");

// more is required to automatically detect and report errors.
// keep reading for details.
'''
...
```

#### <a name="apidoc.element.rollbar.reportMessage"></a>[function <span class="apidocSignatureSpan">rollbar.</span>reportMessage (message, level, req, callback)](#apidoc.element.rollbar.reportMessage)
- description and source-code
```javascript
reportMessage = function (message, level, req, callback) {
  return exports.reportMessageWithPayloadData(message, {level: level}, req, callback);
}
```
- example usage
```shell
...

'''js
// include and initialize the rollbar library with your access token
var rollbar = require("rollbar");
rollbar.init("POST_SERVER_ITEM_ACCESS_TOKEN");

// record a generic message and send to rollbar
rollbar.reportMessage("Hello world!");

// more is required to automatically detect and report errors.
// keep reading for details.
'''

<!-- RemoveNextIfProject -->
Be sure to replace '''POST_SERVER_ITEM_ACCESS_TOKEN''' with your project's '''post_server_item''' access token, which you can find
 in the Rollbar.com interface.
...
```

#### <a name="apidoc.element.rollbar.reportMessageWithPayloadData"></a>[function <span class="apidocSignatureSpan">rollbar.</span>reportMessageWithPayloadData (message, payloadData, req, callback)](#apidoc.element.rollbar.reportMessageWithPayloadData)
- description and source-code
```javascript
reportMessageWithPayloadData = function (message, payloadData, req, callback) {
  if (SETTINGS.showReportedMessageTraces) {
    logger.log(message, new Error().stack);
  }
  addItem({message: message, payload: payloadData, request: req}, callback);
}
```
- example usage
```shell
...
// only the first param is required
// valid severity levels: "critical", "error", "warning", "info", "debug"
rollbar.reportMessage("Response time exceeded threshold of 1s", "warning", request, callback);

// reports a string message along with additional data conforming to the Rollbar API Schema
// documented here: https://rollbar.com/docs/api/items_post/
// only the first two params are required
rollbar.reportMessageWithPayloadData("Response time exceeded threshold of 1s", {
    level: "warning",
    custom: {
      threshold: 1,
      timeElapsed: 2.3
    }
  }, request, callback);
'''
...
```

#### <a name="apidoc.element.rollbar.wait"></a>[function <span class="apidocSignatureSpan">rollbar.</span>wait (callback)](#apidoc.element.rollbar.wait)
- description and source-code
```javascript
wait = function (callback) {
  if (exports.pendingItemsCount() === 0) {
    callback();
  } else {
    waitCallback = callback;
  }
}
```
- example usage
```shell
...
});
'''

## Waiting on pending items

There may be some cases where you need to do a hard 'process.exit(1)', but you also don't
want to lose any errors that may be in-flight to Rollbar at the time.  That is where the
'rollbar.wait(cb)' function comes into play.  It will execute the callback when there are
no pending items being sent to Rollbar.  It could execute immediately (if there are none
pending), or it could take a few seconds while the queue is flushed.

'''javascript
var rollbar = require('rollbar');
rollbar.init(rollbarToken);
rollbar.handleError('Test');
...
```



# <a name="apidoc.module.rollbar.Error"></a>[module rollbar.Error](#apidoc.module.rollbar.Error)

#### <a name="apidoc.element.rollbar.Error.Error"></a>[function <span class="apidocSignatureSpan">rollbar.</span>Error (message, nested)](#apidoc.element.rollbar.Error.Error)
- description and source-code
```javascript
function RollbarError(message, nested)
{
  Error.call(this);
  Error.captureStackTrace(this, this.constructor);

  this.message = message;
  this.nested = nested;
  this.name = this.constructor.name;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.Error.super_"></a>[function <span class="apidocSignatureSpan">rollbar.Error.</span>super_ ()](#apidoc.element.rollbar.Error.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rollbar.Error.super_"></a>[module rollbar.Error.super_](#apidoc.module.rollbar.Error.super_)

#### <a name="apidoc.element.rollbar.Error.super_.super_"></a>[function <span class="apidocSignatureSpan">rollbar.Error.</span>super_ ()](#apidoc.element.rollbar.Error.super_.super_)
- description and source-code
```javascript
function Error() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.Error.super_.captureStackTrace"></a>[function <span class="apidocSignatureSpan">rollbar.Error.super_.</span>captureStackTrace ()](#apidoc.element.rollbar.Error.super_.captureStackTrace)
- description and source-code
```javascript
function captureStackTrace() { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rollbar.api"></a>[module rollbar.api](#apidoc.module.rollbar.api)

#### <a name="apidoc.element.rollbar.api.init"></a>[function <span class="apidocSignatureSpan">rollbar.api.</span>init (accessToken, options)](#apidoc.element.rollbar.api.init)
- description and source-code
```javascript
init = function (accessToken, options) {
  var opt, portCheck;

  options = options || {};
  exports.accessToken = accessToken;
  exports.endpoint = options.endpoint || exports.endpoint;

  for (opt in options) {
    if (options.hasOwnProperty(opt)) {
      SETTINGS[opt] = options[opt];
    }
  }

  SETTINGS.endpointOpts = url.parse(exports.endpoint);
  SETTINGS.protocol = SETTINGS.endpointOpts.protocol.split(':')[0];
  SETTINGS.transport = {http: http, https: https}[SETTINGS.protocol];
  SETTINGS.proxy = options.proxy;

  portCheck = SETTINGS.endpointOpts.host.split(':');
  if (portCheck.length > 1) {
    SETTINGS.endpointOpts.host = portCheck[0];
    SETTINGS.port = parseInt(portCheck[1], 10);
  }
}
```
- example usage
```shell
...
<!-- Sub:[TOC] -->

## Quick start

'''js
// include and initialize the rollbar library with your access token
var rollbar = require("rollbar");
rollbar.init("POST_SERVER_ITEM_ACCESS_TOKEN");

// record a generic message and send to rollbar
rollbar.reportMessage("Hello world!");

// more is required to automatically detect and report errors.
// keep reading for details.
'''
...
```

#### <a name="apidoc.element.rollbar.api.postItem"></a>[function <span class="apidocSignatureSpan">rollbar.api.</span>postItem (item, callback)](#apidoc.element.rollbar.api.postItem)
- description and source-code
```javascript
postItem = function (item, callback) {
  return postApi('item/', buildPayload(item), callback);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rollbar.deploy"></a>[module rollbar.deploy](#apidoc.module.rollbar.deploy)

#### <a name="apidoc.element.rollbar.deploy.createDeploy"></a>[function <span class="apidocSignatureSpan">rollbar.deploy.</span>createDeploy (accessToken, params, opts, callback)](#apidoc.element.rollbar.deploy.createDeploy)
- description and source-code
```javascript
createDeploy = function (accessToken, params, opts, callback) {
  if (typeof callback != 'function')
    callback = function(){};

  var requestOpts = createRequestOpts('POST', 'deploy/', accessToken);

  var req = https.request(requestOpts, function(res) {
    handleResponse(res, callback);
  });

  var writeData = {};
  try {
    try {
      writeData = JSON.stringify(params);
    } catch (e) {
      writedata = stringify(params);
    }
  } catch (e) {
    logger.error('Could not safe-stringify data.  Giving up');
    return callback(e);
  }
  req.write(writeData);
  req.end();
}
```
- example usage
```shell
...

Please refer to [the Rollbar API Spec](https://rollbar.com/docs/api/deploys/) for implementation
details and deeper explanations of the options available.

'''javascript
var deploy = require('rollbar/deploy');

deploy.createDeploy('POST_SERVER_ITEM_ACCESS_TOKEN', {
    environment: 'production',
    revision: '1.2.3'
  });
'''

## Help / Support
...
```

#### <a name="apidoc.element.rollbar.deploy.getDeploy"></a>[function <span class="apidocSignatureSpan">rollbar.deploy.</span>getDeploy (accessToken, deployId, opts, callback)](#apidoc.element.rollbar.deploy.getDeploy)
- description and source-code
```javascript
getDeploy = function (accessToken, deployId, opts, callback) {
  if (typeof callback != 'function')
    callback = function(){};

  var params = [];
  params.push('access_token='+accessToken);
  var paramsStr = params.join('&');

  var requestOpts = createRequestOpts('GET', 'deploy/'+deployId+'/?'+paramsStr, accessToken);

  var req = https.request(requestOpts, function(res) {
    handleResponse(res, callback);
  });

  req.end();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.deploy.listDeploys"></a>[function <span class="apidocSignatureSpan">rollbar.deploy.</span>listDeploys (accessToken, pageNum, opts, callback)](#apidoc.element.rollbar.deploy.listDeploys)
- description and source-code
```javascript
listDeploys = function (accessToken, pageNum, opts, callback) {
  if (typeof pageNum != 'number' || pageNum < 1)
    pageNum = 1;

  if (typeof callback != 'function')
    callback = function(){};

  var params = [];
  params.push('page='+pageNum);
  params.push('access_token='+accessToken);
  var paramsStr = params.join('&');


  var requestOpts = createRequestOpts('GET', 'deploys?'+paramsStr, accessToken);

  var req = https.request(requestOpts, function(res) {
    handleResponse(res, callback);
  });

  req.end();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rollbar.logger"></a>[module rollbar.logger](#apidoc.module.rollbar.logger)

#### <a name="apidoc.element.rollbar.logger.error"></a>[function <span class="apidocSignatureSpan">rollbar.logger.</span>error ()](#apidoc.element.rollbar.logger.error)
- description and source-code
```javascript
function disabled() {
}
```
- example usage
```shell
...
// Begin Rollbar initialization code
var rollbar = require('rollbar');
rollbar.init('POST_SERVER_ITEM_ACCESS_TOKEN');
server.on('request-error', function(request, error) {
  // Note: before Hapi v8.0.0, this should be 'internalError' instead of 'request-error'
  var cb = function(rollbarErr) {
    if (rollbarErr)
      console.error('Error reporting to rollbar, ignoring: '+rollbarErr);
  };
  if (error instanceof Error)
    return rollbar.handleError(error, request, cb);
  rollbar.reportMessage('Error: '+error, 'error', request, cb);
});
// End Rollbar initialization code
...
```

#### <a name="apidoc.element.rollbar.logger.log"></a>[function <span class="apidocSignatureSpan">rollbar.logger.</span>log ()](#apidoc.element.rollbar.logger.log)
- description and source-code
```javascript
function disabled() {
}
```
- example usage
```shell
...
  handler: function (request, reply) {
    throw new Error('Example error manually thrown from route.');
  }
});
server.start(function(err) {
  if (err)
    throw err;
  console.log('Server running at:', server.info.uri);
});
'''

### Standalone

In your main application, require and initialize using your access_token::
...
```



# <a name="apidoc.module.rollbar.notifier"></a>[module rollbar.notifier](#apidoc.module.rollbar.notifier)

#### <a name="apidoc.element.rollbar.notifier._extractIp"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>_extractIp (req)](#apidoc.element.rollbar.notifier._extractIp)
- description and source-code
```javascript
_extractIp = function (req) {
  return extractIp(req);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.notifier._levelGteMinimum"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>_levelGteMinimum (item)](#apidoc.element.rollbar.notifier._levelGteMinimum)
- description and source-code
```javascript
_levelGteMinimum = function (item) {
  return levelGteMinimum(item);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.notifier._scrubRequestHeaders"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>_scrubRequestHeaders (headersToScrub, headers)](#apidoc.element.rollbar.notifier._scrubRequestHeaders)
- description and source-code
```javascript
_scrubRequestHeaders = function (headersToScrub, headers) {
  return scrubRequestHeaders(headers, headersToScrub ? {scrubHeaders: headersToScrub} : undefined);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.notifier._scrubRequestParams"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>_scrubRequestParams (paramsToScrub, params)](#apidoc.element.rollbar.notifier._scrubRequestParams)
- description and source-code
```javascript
_scrubRequestParams = function (paramsToScrub, params) {
  return scrubRequestParams(params, paramsToScrub ? {scrubFields: paramsToScrub} : undefined);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.notifier.handleError"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>handleError (err, req, callback)](#apidoc.element.rollbar.notifier.handleError)
- description and source-code
```javascript
handleError = function (err, req, callback) {
  if (typeof req === 'function') {
    callback = req;
    req = null;
  }
  if (err instanceof Error) {
    return exports.handleErrorWithPayloadData(err, {}, req, callback);
  }

  var stringError;
  try {
    stringError = JSON.stringify(err);
  } catch (e) {
    stringError = stringify(err);
  } finally {
    return exports.reportMessage(stringError, 'error', req, callback);
  }
}
```
- example usage
```shell
...
server.on('request-error', function(request, error) {
// Note: before Hapi v8.0.0, this should be 'internalError' instead of 'request-error'
var cb = function(rollbarErr) {
  if (rollbarErr)
    console.error('Error reporting to rollbar, ignoring: '+rollbarErr);
};
if (error instanceof Error)
  return rollbar.handleError(error, request, cb);
rollbar.reportMessage('Error: '+error, 'error', request, cb);
});
// End Rollbar initialization code

server.route({
method: 'GET',
path:'/throw_error',
...
```

#### <a name="apidoc.element.rollbar.notifier.handleErrorWithPayloadData"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>handleErrorWithPayloadData (err, payloadData, req, callback)](#apidoc.element.rollbar.notifier.handleErrorWithPayloadData)
- description and source-code
```javascript
handleErrorWithPayloadData = function (err, payloadData, req, callback) {
  // Allow the user to call with an optional request and callback
  // e.g. handleErrorWithPayloadData(err, payloadData, req, callback)
  //   or handleErrorWithPayloadData(err, payloadData, callback)
  //   or handleErrorPayloadData(err, payloadData)
  if (typeof req === 'function') {
    callback = req;
    req = null;
  }

  if (!(err instanceof Error)) {
    if (typeof callback === 'function') {
      return callback(new Error('handleError was passed something other than an Error: ' + err));
    }
  }
  addItem({error: err, payload: payloadData, request: req}, callback);
}
```
- example usage
```shell
...
    }
  });

  // if you have a request and a callback, pass the callback last
  rollbar.handleError(e, request, callback);

  // to specify payload options - like extra data, or the level - use handleErrorWithPayloadData
  rollbar.handleErrorWithPayloadData(e, {level: "warning", custom: {someKey: "arbitrary value"}});

  // can also take request and callback, like handleError:
  rollbar.handleErrorWithPayloadData(e, {level: "info"}, request);
  rollbar.handleErrorWithPayloadData(e, {level: "info"}, callback);
  rollbar.handleErrorWithPayloadData(e, {level: "info"}, request, callback);
}
'''
...
```

#### <a name="apidoc.element.rollbar.notifier.init"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>init (api, options)](#apidoc.element.rollbar.notifier.init)
- description and source-code
```javascript
init = function (api, options) {
  var opt;

  SETTINGS.accessToken = api.accessToken;

  apiClient = api;
  options = options || {};

  for (opt in options) {
    if (options.hasOwnProperty(opt)) {
      SETTINGS[opt] = options[opt];
    }
  }
  initialized = true;
}
```
- example usage
```shell
...
<!-- Sub:[TOC] -->

## Quick start

'''js
// include and initialize the rollbar library with your access token
var rollbar = require("rollbar");
rollbar.init("POST_SERVER_ITEM_ACCESS_TOKEN");

// record a generic message and send to rollbar
rollbar.reportMessage("Hello world!");

// more is required to automatically detect and report errors.
// keep reading for details.
'''
...
```

#### <a name="apidoc.element.rollbar.notifier.pendingItemsCount"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>pendingItemsCount ()](#apidoc.element.rollbar.notifier.pendingItemsCount)
- description and source-code
```javascript
pendingItemsCount = function () {
  return pendingItems.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.notifier.reportMessage"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>reportMessage (message, level, req, callback)](#apidoc.element.rollbar.notifier.reportMessage)
- description and source-code
```javascript
reportMessage = function (message, level, req, callback) {
  return exports.reportMessageWithPayloadData(message, {level: level}, req, callback);
}
```
- example usage
```shell
...

'''js
// include and initialize the rollbar library with your access token
var rollbar = require("rollbar");
rollbar.init("POST_SERVER_ITEM_ACCESS_TOKEN");

// record a generic message and send to rollbar
rollbar.reportMessage("Hello world!");

// more is required to automatically detect and report errors.
// keep reading for details.
'''

<!-- RemoveNextIfProject -->
Be sure to replace '''POST_SERVER_ITEM_ACCESS_TOKEN''' with your project's '''post_server_item''' access token, which you can find
 in the Rollbar.com interface.
...
```

#### <a name="apidoc.element.rollbar.notifier.reportMessageWithPayloadData"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>reportMessageWithPayloadData (message, payloadData, req, callback)](#apidoc.element.rollbar.notifier.reportMessageWithPayloadData)
- description and source-code
```javascript
reportMessageWithPayloadData = function (message, payloadData, req, callback) {
  if (SETTINGS.showReportedMessageTraces) {
    logger.log(message, new Error().stack);
  }
  addItem({message: message, payload: payloadData, request: req}, callback);
}
```
- example usage
```shell
...
// only the first param is required
// valid severity levels: "critical", "error", "warning", "info", "debug"
rollbar.reportMessage("Response time exceeded threshold of 1s", "warning", request, callback);

// reports a string message along with additional data conforming to the Rollbar API Schema
// documented here: https://rollbar.com/docs/api/items_post/
// only the first two params are required
rollbar.reportMessageWithPayloadData("Response time exceeded threshold of 1s", {
    level: "warning",
    custom: {
      threshold: 1,
      timeElapsed: 2.3
    }
  }, request, callback);
'''
...
```

#### <a name="apidoc.element.rollbar.notifier.wait"></a>[function <span class="apidocSignatureSpan">rollbar.notifier.</span>wait (callback)](#apidoc.element.rollbar.notifier.wait)
- description and source-code
```javascript
wait = function (callback) {
  if (exports.pendingItemsCount() === 0) {
    callback();
  } else {
    waitCallback = callback;
  }
}
```
- example usage
```shell
...
});
'''

## Waiting on pending items

There may be some cases where you need to do a hard 'process.exit(1)', but you also don't
want to lose any errors that may be in-flight to Rollbar at the time.  That is where the
'rollbar.wait(cb)' function comes into play.  It will execute the callback when there are
no pending items being sent to Rollbar.  It could execute immediately (if there are none
pending), or it could take a few seconds while the queue is flushed.

'''javascript
var rollbar = require('rollbar');
rollbar.init(rollbarToken);
rollbar.handleError('Test');
...
```



# <a name="apidoc.module.rollbar.parser"></a>[module rollbar.parser](#apidoc.module.rollbar.parser)

#### <a name="apidoc.element.rollbar.parser.parseException"></a>[function <span class="apidocSignatureSpan">rollbar.parser.</span>parseException (exc, callback)](#apidoc.element.rollbar.parser.parseException)
- description and source-code
```javascript
parseException = function (exc, callback) {
  var multipleErrs = getMultipleErrors(exc.errors);

  return exports.parseStack(exc.stack, function (err, stack) {
    var message, clss, ret, firstErr, jadeMatch, jadeData;

    if (err) {
      logger.error('could not parse exception, err: ' + err);
      return callback(err);
    }
    message = String(exc.message || '<no message>') ;
    clss = String(exc.name || '<unknown>');

    ret = {
      class: clss,
      message: message,
      frames: stack
    };

    if (multipleErrs && multipleErrs.length) {
      firstErr = multipleErrs[0];
      ret = {
        class: clss,
        message: String(firstErr.message || '<no message>'),
        frames: stack
      };
    }

    jadeMatch = message.match(jadeFramePattern);
    if (jadeMatch) {
      jadeData = parseJadeDebugFrame(message);
      ret.message = jadeData.message;
      ret.frames.push(jadeData.frame);
    }
    return callback(null, ret);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.parseStack"></a>[function <span class="apidocSignatureSpan">rollbar.parser.</span>parseStack (stack, callback)](#apidoc.element.rollbar.parser.parseStack)
- description and source-code
```javascript
parseStack = function (stack, callback) {
  var lines, _stack = stack;

  // Some JS frameworks (e.g. Meteor) might bury the stack property
  while (typeof _stack === 'object') {
    _stack = _stack && _stack.stack;
  }

  // grab all lines except the first
  lines = (_stack || '').split('\n').slice(1);

  // Parse out all of the frame and filename info
  async.map(lines, parseFrameLine, function (err, frames) {
    if (err) {
      return callback(err);
    }
    frames.reverse();
    async.filter(frames, function (frame, callback) { callback(!!frame); }, function (results) {
      gatherContexts(results, callback);
    });
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.rollbar.parser.cache"></a>[module rollbar.parser.cache](#apidoc.module.rollbar.parser.cache)

#### <a name="apidoc.element.rollbar.parser.cache.del"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>del (key)](#apidoc.element.rollbar.parser.cache.del)
- description and source-code
```javascript
del = function (key) {
  del(cache[key])
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.dump"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>dump ()](#apidoc.element.rollbar.parser.cache.dump)
- description and source-code
```javascript
dump = function () {
  return cache
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.dumpLru"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>dumpLru ()](#apidoc.element.rollbar.parser.cache.dumpLru)
- description and source-code
```javascript
dumpLru = function () {
  return lruList
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.forEach"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>forEach (fn, thisp)](#apidoc.element.rollbar.parser.cache.forEach)
- description and source-code
```javascript
forEach = function (fn, thisp) {
  thisp = thisp || this
  var i = 0;
  for (var k = mru - 1; k >= 0 && i < itemCount; k--) if (lruList[k]) {
    i++
    var hit = lruList[k]
    fn.call(thisp, hit.value, hit.key, this)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.get"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>get (key)](#apidoc.element.rollbar.parser.cache.get)
- description and source-code
```javascript
get = function (key) {
  if (!hOP(cache, key)) return
  var hit = cache[key]
  if (maxAge && (Date.now() - hit.now > maxAge)) {
    this.del(key)
    return allowStale ? hit.value : undefined
  }
  shiftLU(hit)
  hit.lu = mru ++
  lruList[hit.lu] = hit
  return hit.value
}
```
- example usage
```shell
...

'''js
var express = require('express');
var rollbar = require('rollbar');

var app = express();

app.get('/', function(req, res) {
  // ...
});

// Use the rollbar error handler to send exceptions to your rollbar account
app.use(rollbar.errorHandler('POST_SERVER_ITEM_ACCESS_TOKEN'));

app.listen(6943);
...
```

#### <a name="apidoc.element.rollbar.parser.cache.has"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>has (key)](#apidoc.element.rollbar.parser.cache.has)
- description and source-code
```javascript
has = function (key) {
  if (!hOP(cache, key)) return false
  var hit = cache[key]
  if (maxAge && (Date.now() - hit.now > maxAge)) {
    return false
  }
  return true
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.keys"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>keys ()](#apidoc.element.rollbar.parser.cache.keys)
- description and source-code
```javascript
keys = function () {
  var keys = new Array(itemCount)
  var i = 0
  for (var k = mru - 1; k >= 0 && i < itemCount; k--) if (lruList[k]) {
    var hit = lruList[k]
    keys[i++] = hit.key
  }
  return keys
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.lengthCalculator"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>lengthCalculator ()](#apidoc.element.rollbar.parser.cache.lengthCalculator)
- description and source-code
```javascript
function naiveLength() { return 1 }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.reset"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>reset ()](#apidoc.element.rollbar.parser.cache.reset)
- description and source-code
```javascript
reset = function () {
  if (dispose) {
    for (var k in cache) {
      dispose(k, cache[k].value)
    }
  }
  cache = {}
  lruList = {}
  lru = 0
  mru = 0
  length = 0
  itemCount = 0
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.set"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>set (key, value)](#apidoc.element.rollbar.parser.cache.set)
- description and source-code
```javascript
set = function (key, value) {
  if (hOP(cache, key)) {
    // dispose of the old one before overwriting
    if (dispose) dispose(key, cache[key].value)
    if (maxAge) cache[key].now = Date.now()
    cache[key].value = value
    this.get(key)
    return true
  }

  var len = lengthCalculator(value)
  var age = maxAge ? Date.now() : 0
  var hit = new Entry(key, value, mru++, len, age)

  // oversized objects fall out of cache automatically.
  if (hit.length > max) {
    if (dispose) dispose(key, value)
    return false
  }

  length += hit.length
  lruList[hit.lu] = cache[key] = hit
  itemCount ++

  if (length > max) trim()
  return true
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.rollbar.parser.cache.values"></a>[function <span class="apidocSignatureSpan">rollbar.parser.cache.</span>values ()](#apidoc.element.rollbar.parser.cache.values)
- description and source-code
```javascript
values = function () {
  var values = new Array(itemCount)
  var i = 0
  for (var k = mru - 1; k >= 0 && i < itemCount; k--) if (lruList[k]) {
    var hit = lruList[k]
    values[i++] = hit.value
  }
  return values
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
