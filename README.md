# api documentation for  [model (v6.0.1)](https://github.com/geddy/model)  [![npm package](https://img.shields.io/npm/v/npmdoc-model.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-model) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-model.svg)](https://travis-ci.org/npmdoc/node-npmdoc-model)
#### Datastore-agnostic ORM in JavaScript

[![NPM](https://nodei.co/npm/model.png?downloads=true)](https://www.npmjs.com/package/model)

[![apidoc](https://npmdoc.github.io/node-npmdoc-model/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-model_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-model/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-model/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-model/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matthew Eernisse",
        "email": "mde@fleegix.org",
        "url": "http://fleegix.org"
    },
    "bugs": {
        "url": "https://github.com/geddy/model/issues"
    },
    "dependencies": {
        "utilities": "1.0.x"
    },
    "description": "Datastore-agnostic ORM in JavaScript",
    "devDependencies": {
        "jake": "8.0.x",
        "level": "0.17.x",
        "mongodb": "1.x",
        "mysql": "2.0.x",
        "pg": "2.5.x",
        "sqlite3": "2.1.x"
    },
    "directories": {},
    "dist": {
        "shasum": "db70e97ba5d452d06b79e8789358c0ba45292f2e",
        "tarball": "https://registry.npmjs.org/model/-/model-6.0.1.tgz"
    },
    "engines": {
        "node": "*"
    },
    "homepage": "https://github.com/geddy/model",
    "keywords": [
        "model",
        "orm",
        "relation",
        "data",
        "mapper",
        "validation",
        "postgresql",
        "postgres",
        "mysql",
        "riak",
        "mongo",
        "mongodb",
        "leveldb",
        "sqlite"
    ],
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "mde",
            "email": "mde@fleegix.org"
        }
    ],
    "name": "model",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/geddy/model.git"
    },
    "scripts": {
        "test": "jake test --trace"
    },
    "version": "6.0.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module model](#apidoc.module.model)
1.  [function <span class="apidocSignatureSpan">model.</span>Migration (name, adapter)](#apidoc.element.model.Migration)
1.  [function <span class="apidocSignatureSpan">model.</span>ModelBase ()](#apidoc.element.model.ModelBase)
1.  [function <span class="apidocSignatureSpan">model.</span>ModelDefinitionBase (name)](#apidoc.element.model.ModelDefinitionBase)
1.  [function <span class="apidocSignatureSpan">model.</span>ModelDescription (name)](#apidoc.element.model.ModelDescription)
1.  [function <span class="apidocSignatureSpan">model.</span>PropertyDescription (name, datatype, o)](#apidoc.element.model.PropertyDescription)
1.  [function <span class="apidocSignatureSpan">model.</span>ValidationDescription (type, reference, opts)](#apidoc.element.model.ValidationDescription)
1.  [function <span class="apidocSignatureSpan">model.</span>clearDefinitions (defs)](#apidoc.element.model.clearDefinitions)
1.  [function <span class="apidocSignatureSpan">model.</span>createAdapter (name, config)](#apidoc.element.model.createAdapter)
1.  [function <span class="apidocSignatureSpan">model.</span>createForeignKeys ()](#apidoc.element.model.createForeignKeys)
1.  [function <span class="apidocSignatureSpan">model.</span>createItem (name, p, o)](#apidoc.element.model.createItem)
1.  [function <span class="apidocSignatureSpan">model.</span>getAdapterForModel (modelName)](#apidoc.element.model.getAdapterForModel)
1.  [function <span class="apidocSignatureSpan">model.</span>getAdapterInfo (name)](#apidoc.element.model.getAdapterInfo)
1.  [function <span class="apidocSignatureSpan">model.</span>getAssociation (main, assn)](#apidoc.element.model.getAssociation)
1.  [function <span class="apidocSignatureSpan">model.</span>getAssociationType (main, assn)](#apidoc.element.model.getAssociationType)
1.  [function <span class="apidocSignatureSpan">model.</span>getModelByName (name)](#apidoc.element.model.getModelByName)
1.  [function <span class="apidocSignatureSpan">model.</span>log ()](#apidoc.element.model.log)
1.  [function <span class="apidocSignatureSpan">model.</span>register (name, ModelDefinition)](#apidoc.element.model.register)
1.  [function <span class="apidocSignatureSpan">model.</span>registerDefinition (name, ModelDefinition)](#apidoc.element.model.registerDefinition)
1.  [function <span class="apidocSignatureSpan">model.</span>registerDefinitions (defs)](#apidoc.element.model.registerDefinitions)
1.  [function <span class="apidocSignatureSpan">model.</span>setDefaultAdapter (name, config)](#apidoc.element.model.setDefaultAdapter)
1.  [function <span class="apidocSignatureSpan">model.</span>setLocalRequireError (msg)](#apidoc.element.model.setLocalRequireError)
1.  [function <span class="apidocSignatureSpan">model.</span>updateItem (item, params, opts)](#apidoc.element.model.updateItem)
1.  [function <span class="apidocSignatureSpan">model.</span>validateAndUpdateFromParams (item, passedParams, opts)](#apidoc.element.model.validateAndUpdateFromParams)
1.  [function <span class="apidocSignatureSpan">model.</span>validateProperty (prop, params, opts)](#apidoc.element.model.validateProperty)
1.  object <span class="apidocSignatureSpan">model.</span>Migration.prototype
1.  object <span class="apidocSignatureSpan">model.</span>adapters
1.  object <span class="apidocSignatureSpan">model.</span>config
1.  object <span class="apidocSignatureSpan">model.</span>datatypes
1.  object <span class="apidocSignatureSpan">model.</span>defaultAdapter
1.  object <span class="apidocSignatureSpan">model.</span>descriptionRegistry
1.  object <span class="apidocSignatureSpan">model.</span>formatters
1.  object <span class="apidocSignatureSpan">model.</span>validators

#### [module model.Migration](#apidoc.module.model.Migration)
1.  [function <span class="apidocSignatureSpan">model.</span>Migration (name, adapter)](#apidoc.element.model.Migration.Migration)
1.  [function <span class="apidocSignatureSpan">model.Migration.</span>setDefaultAdapter (adapter)](#apidoc.element.model.Migration.setDefaultAdapter)

#### [module model.Migration.prototype](#apidoc.module.model.Migration.prototype)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>addColumn ()](#apidoc.element.model.Migration.prototype.addColumn)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>addIndex (table, column, options, cb)](#apidoc.element.model.Migration.prototype.addIndex)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>changeColumn (table, column, datatype, options, cb)](#apidoc.element.model.Migration.prototype.changeColumn)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>createTable ()](#apidoc.element.model.Migration.prototype.createTable)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>down (next)](#apidoc.element.model.Migration.prototype.down)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>dropTable (name, cb)](#apidoc.element.model.Migration.prototype.dropTable)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>removeColumn (table, column, cb)](#apidoc.element.model.Migration.prototype.removeColumn)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>removeIndex (table, column, cb)](#apidoc.element.model.Migration.prototype.removeIndex)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>renameColumn (table, column, newColumn, cb)](#apidoc.element.model.Migration.prototype.renameColumn)
1.  [function <span class="apidocSignatureSpan">model.Migration.prototype.</span>up (next)](#apidoc.element.model.Migration.prototype.up)

#### [module model.ModelBase](#apidoc.module.model.ModelBase)
1.  [function <span class="apidocSignatureSpan">model.</span>ModelBase ()](#apidoc.element.model.ModelBase.ModelBase)
1.  [function <span class="apidocSignatureSpan">model.ModelBase.</span>super_ ()](#apidoc.element.model.ModelBase.super_)

#### [module model.formatters](#apidoc.module.model.formatters)
1.  [function <span class="apidocSignatureSpan">model.formatters.</span>date (val)](#apidoc.element.model.formatters.date)
1.  [function <span class="apidocSignatureSpan">model.formatters.</span>time (val)](#apidoc.element.model.formatters.time)

#### [module model.validators](#apidoc.module.model.validators)
1.  [function <span class="apidocSignatureSpan">model.validators.</span>absent (name, val, params, rule, locale)](#apidoc.element.model.validators.absent)
1.  [function <span class="apidocSignatureSpan">model.validators.</span>confirmed (name, val, params, rule, locale)](#apidoc.element.model.validators.confirmed)
1.  [function <span class="apidocSignatureSpan">model.validators.</span>format (name, val, params, rule, locale)](#apidoc.element.model.validators.format)
1.  [function <span class="apidocSignatureSpan">model.validators.</span>length (name, val, params, rule, locale)](#apidoc.element.model.validators.length)
1.  [function <span class="apidocSignatureSpan">model.validators.</span>present (name, val, params, rule, locale)](#apidoc.element.model.validators.present)
1.  [function <span class="apidocSignatureSpan">model.validators.</span>withFunction (name, val, params, rule, locale)](#apidoc.element.model.validators.withFunction)



# <a name="apidoc.module.model"></a>[module model](#apidoc.module.model)

#### <a name="apidoc.element.model.Migration"></a>[function <span class="apidocSignatureSpan">model.</span>Migration (name, adapter)](#apidoc.element.model.Migration)
- description and source-code
```javascript
Migration = function (name, adapter) {
  this.name = name;
  this.adapter = adapter || defaultAdapter;
  this.generator = this.adapter.generator;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.ModelBase"></a>[function <span class="apidocSignatureSpan">model.</span>ModelBase ()](#apidoc.element.model.ModelBase)
- description and source-code
```javascript
ModelBase = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.ModelDefinitionBase"></a>[function <span class="apidocSignatureSpan">model.</span>ModelDefinitionBase (name)](#apidoc.element.model.ModelDefinitionBase)
- description and source-code
```javascript
ModelDefinitionBase = function (name) {
  var self = this
    , reg = model.descriptionRegistry
    , _createValidator = function (p) {
        return function () {
          var args = Array.prototype.slice.call(arguments);
          args.unshift(p);
          return self.validates.apply(self, args);
        };
      };

  this.name = name;

  this.setAdapter = function (name, config) {
    var adapter = adapters.create(name, config);
    this.adapter = adapter;
  };

  this.property = function (name, datatype, options) {
    var opts = options || {};

    // Don't allow users to define properties with the same
    // name as magical system properties
    if (!opts.isSystem && _systemProperties[name]) {
      throw new Error('You cannot define the property "' + name +
          '" on a model, as it\'s a reserved system-property name.');
    }

    reg[this.name].properties[name] =
      new model.PropertyDescription(name, datatype, opts);
  };

  this.defineProperties = function (obj) {
    var type
      , options
      , property;

    for (var name in obj) {
      property = obj[name];

      if (typeof property === 'string') {
        type = property;
        options = {};
      }
      else {
        type = property.type;
        options = property;
      }

      this.property(name, type, options);
    }
  }

  // (condition, name, [reference], [opts])
  this.validates = function () {
    var args = Array.prototype.slice.call(arguments)
      , arg
      , condition = args.shift()
      , name = args.shift()
      , reference
      , opts = {};
    while ((arg = args.pop())) {
      // Regex for validatesFormat or function for validatesWithFunction
      // or string param name for validatesConfirmed
      if (arg instanceof RegExp || typeof arg == 'function' ||
          typeof arg == 'string') {
        reference = arg;
      }
      else {
        opts = utils.mixin(opts, arg);
      }
    }

    // Old API allows passing simple number to validatesLength
    if (!isNaN(opts)) {
      opts = {is: opts};
    }

    // Default to 'create' and 'update' only for scenarios
    opts.on = opts.on || ['create', 'update'];

    if (typeof reg[this.name].properties[name] === 'undefined') {
      throw new Error('Validation cannot be added for "' + name +
                      '": property does not exist on the ' + this.name +
                      ' model.');
    }

    reg[this.name].properties[name].validations[condition] =
        new model.ValidationDescription(condition, reference, opts);
  };

  // For each of the validators, create a validatesFooBar from
  // validates('fooBar' ...
  for (var p in model.validators) {
    this['validates' + utils.string.capitalize(p)] = _createValidator(p);
  }

  // Add the base model properties -- these should not be handled by user input
  if (model.config.useTimestamps) {
    this.property('createdAt', 'datetime', {isSystem: true});
    this.property('updatedAt', 'datetime', {isSystem: true});
  }

  ['hasMany', 'hasOne', 'belongsTo'].forEach(function (assnKey) {
    self[assnKey] = function (name, options) {
      var opts = options || {}
        , assn = reg[self.name].associations[assnKey] || {}
        , assnName = name
        , modelName = opts.model || name;

      // Normalize inflection; we don't care which they use
      assnName = utils.string.getInflection(assnName, 'constructor', 'singular');
      modelName = utils.string.getInflection(modelName, 'constructor', 'singular');

      assn[assnName] = {
        name: assnName
      , model: modelName
      , through: opts.through
      , type: assnKey
      };

      reg[self.name].associations[assnKey] = assn;

      // Set up foreign keys
      var createForeignKey = function (assnName) {
        return function () {
          var ownerModelName
            , ownedModelName
            , idKey
            , datatype
            , def;

          if (assnKey == 'belongsTo') {
            ownerModelName = modelName;
            ownedModelName = self.name;
            idKey = modelName;
          }
          else {
            ownerModelName ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.ModelDescription"></a>[function <span class="apidocSignatureSpan">model.</span>ModelDescription (name)](#apidoc.element.model.ModelDescription)
- description and source-code
```javascript
ModelDescription = function (name) {
  this.name = name;
  this.properties = {};
  this.associations = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.PropertyDescription"></a>[function <span class="apidocSignatureSpan">model.</span>PropertyDescription (name, datatype, o)](#apidoc.element.model.PropertyDescription)
- description and source-code
```javascript
PropertyDescription = function (name, datatype, o) {
  var opts = o || {}
    , validations = {}
    , validationOpts = utils.mixin({}, opts);

  delete validationOpts.required;
  delete validationOpts.length;
  delete validationOpts.format;

  this.name = name;
  this.datatype = datatype;
  this.options = opts;

  // Creates results similar to 'this.validates', above in ModelDefinitionBase
  // Would be great to remove the duplication of logic
  for (var p in opts) {
    if (opts.required || opts.length) {
      validations.present =
          new model.ValidationDescription('present', null, validationOpts);
    }
    if (opts.length) {
      if (typeof opts.length == 'object') {
      // {min: 1, max: 2} or {is: 3}
      validations.length =
          new model.ValidationDescription('length', null,
              utils.mixin(opts.length, validationOpts));
      }
      // 1 or '1'
      else {
      validations.length =
          new model.ValidationDescription('length', null,
              utils.mixin({is: opts.length}, validationOpts));
      }
    }
    if (opts.format) {
      validations.format =
          new model.ValidationDescription('length', opts.format,
              validationOpts);
    }
  }
  this.validations = validations;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.ValidationDescription"></a>[function <span class="apidocSignatureSpan">model.</span>ValidationDescription (type, reference, opts)](#apidoc.element.model.ValidationDescription)
- description and source-code
```javascript
ValidationDescription = function (type, reference, opts) {
  this.type = type;
  this.reference = reference;
  this.opts = opts || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.clearDefinitions"></a>[function <span class="apidocSignatureSpan">model.</span>clearDefinitions (defs)](#apidoc.element.model.clearDefinitions)
- description and source-code
```javascript
clearDefinitions = function (defs) {
  var self = this;
  defs.forEach(function (m) {
    // Prefer 'name', accept older 'ctorName'
    var name = m.name || m.ctorName;
    // Registration may have happened in the model definition file
    // if using the old templates. Don't re-register
    delete self[name];
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.createAdapter"></a>[function <span class="apidocSignatureSpan">model.</span>createAdapter (name, config)](#apidoc.element.model.createAdapter)
- description and source-code
```javascript
createAdapter = function (name, config) {
  return adapters.create(name, config);
}
```
- example usage
```shell
...
- SQLite: 'npm install sqlite3 --save'
- MongoDB: 'npm install mongodb --save'
- LevelDB: 'npm install level --save'

The in-memory, filesystem, and Riak adapters work out of the box and don't need any
additional libraries.

#### model.createAdapter(_name_, _config_)

Use 'model.createAdapter(name, config)' to initialize an adapter and connect to the database.

_NOTE:_ The 'config' parameter for each adapter depends on the module used. As an example,
postgres uses 'database' for the database name whereas MongoDB uses 'dbName'. Model doesn't
try to standardize the config for each adapter. Instead it just passes the config you give it
in 'createAdapter' to the NPM module. To check the config setup for your adapter go to the
...
```

#### <a name="apidoc.element.model.createForeignKeys"></a>[function <span class="apidocSignatureSpan">model.</span>createForeignKeys ()](#apidoc.element.model.createForeignKeys)
- description and source-code
```javascript
createForeignKeys = function () {
  var creator;
  while((creator = _foreignKeyCreators.pop())) {
    creator();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.createItem"></a>[function <span class="apidocSignatureSpan">model.</span>createItem (name, p, o)](#apidoc.element.model.createItem)
- description and source-code
```javascript
createItem = function (name, p, o) {
  var params = p || {}
    , opts = o || {}
    , item = new model[name](params);

  // Default to the 'create' scenario
  opts.scenario = opts.scenario || 'create'

  model[name].emit('beforeCreate', p, o);

  this.validateAndUpdateFromParams(item, params, opts);

  if (this.config.useTimestamps && !item.createdAt) {
    item.createdAt = new Date();
  }

  if (typeof item.afterCreate === 'function') {
    item.afterCreate();
  }
  model[name].emit('create', item);
  return item;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.getAdapterForModel"></a>[function <span class="apidocSignatureSpan">model.</span>getAdapterForModel (modelName)](#apidoc.element.model.getAdapterForModel)
- description and source-code
```javascript
getAdapterForModel = function (modelName) {
  var ctor = this[modelName]
    , adapter = (ctor && ctor.adapter) || this.defaultAdapter;
  if (!adapter) {
    throw new Error('No adapter found for ' + modelName +
        '. Please define one with 'setAdapter', or define a default' +
        ' adapter with 'model.setDefaultAdapter'.');
  }
  return adapter;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.getAdapterInfo"></a>[function <span class="apidocSignatureSpan">model.</span>getAdapterInfo (name)](#apidoc.element.model.getAdapterInfo)
- description and source-code
```javascript
getAdapterInfo = function (name) {
  return adapters.getAdapterInfo(name);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.getAssociation"></a>[function <span class="apidocSignatureSpan">model.</span>getAssociation (main, assn)](#apidoc.element.model.getAssociation)
- description and source-code
```javascript
getAssociation = function (main, assn) {
  var mainName = utils.string.getInflection(main, 'constructor', 'singular')
    , assnName = utils.string.getInflection(assn, 'constructor', 'singular')
    , assn
    , assnItem;
  assn = this.descriptionRegistry[mainName].associations;
  for (var p in assn) {
    assnItem = assn[p][assnName];
    if (assnItem) {
      return assnItem;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.getAssociationType"></a>[function <span class="apidocSignatureSpan">model.</span>getAssociationType (main, assn)](#apidoc.element.model.getAssociationType)
- description and source-code
```javascript
getAssociationType = function (main, assn) {
  var mainName = utils.string.getInflection(main, 'constructor', 'singular')
    , assnName = utils.string.getInflection(assn, 'constructor', 'singular')
    , assn
    , assnItem;
  assn = this.descriptionRegistry[mainName].associations;
  for (var p in assn) {
    assnItem = assn[p][assnName];
    if (assnItem) {
      return p;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.getModelByName"></a>[function <span class="apidocSignatureSpan">model.</span>getModelByName (name)](#apidoc.element.model.getModelByName)
- description and source-code
```javascript
getModelByName = function (name) {
  return this[name];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.log"></a>[function <span class="apidocSignatureSpan">model.</span>log ()](#apidoc.element.model.log)
- description and source-code
```javascript
log = function () {}
```
- example usage
```shell
...
  // Update the model's name property
  model.name = "New name!";

  // Once we're done updating properties we can call save on the model.
  // Save will send the current model data to the DB you specified
  model.save(function (err, updatedModel) {
    if (err) throw new Error('Could not save the model');
    console.log("The model was updated!");
  });
});

'''

## Defining models
...
```

#### <a name="apidoc.element.model.register"></a>[function <span class="apidocSignatureSpan">model.</span>register (name, ModelDefinition)](#apidoc.element.model.register)
- description and source-code
```javascript
register = function (name, ModelDefinition) {
  return this.registerDefinition(name, ModelDefinition);
}
```
- example usage
```shell
...
    enabled: { type: 'boolean' },
    archived: { type: 'boolean' },
  });
};

// This registers the model with the model package so
// things like associations can work
Foo = model.register('Foo', Foo);

// Now we export Foo to create a reusable model module
module.exports = Foo;
'''

You can then use it like the following example:
...
```

#### <a name="apidoc.element.model.registerDefinition"></a>[function <span class="apidocSignatureSpan">model.</span>registerDefinition (name, ModelDefinition)](#apidoc.element.model.registerDefinition)
- description and source-code
```javascript
registerDefinition = function (name, ModelDefinition) {
  var origProto = ModelDefinition.prototype
    , defined
    , ModelCtor;

  // Create the place to store the metadata about the model structure
  // to use to do validations, etc. when constructing
  model.descriptionRegistry[name] = new model.ModelDescription(name);
  // Execute all the definition methods to create that metadata
  ModelDefinition.prototype = new model.ModelDefinitionBase(name);
  defined = new ModelDefinition();

  // Create the constructor function to use when calling static
  // ModelCtor.create. Gives them the proper instanceof value,
  // and .valid, etc. instance-methods.
  ModelCtor = _createModelItemConstructor(defined);

  // Mix in the static methods like .create and .load
  utils.mixin(ModelCtor, _createStaticMethodsMixin(name));
  // Mix on the statics on the definition 'ctor' onto the
  // instantiated ModelDefinition instance
  utils.mixin(defined, ModelDefinition);
  // Mix ModelDefinition instance properties as static properties
  // for the model item 'ctor'
  utils.mixin(ModelCtor, defined);
  // Same with EventEmitter methods
  utils.enhance(ModelCtor, new EventEmitter());

  // Mix any functions defined directly in the model-item definition
  // 'constructor' into the original prototype, and set it as the prototype of the
  // actual constructor
  utils.mixin(origProto, defined);

  ModelCtor.prototype = new model.ModelBase();
  // Preserve any inherited shit from the definition proto
  utils.enhance(ModelCtor.prototype, origProto);

  model[name] = ModelCtor;

  return ModelCtor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.registerDefinitions"></a>[function <span class="apidocSignatureSpan">model.</span>registerDefinitions (defs)](#apidoc.element.model.registerDefinitions)
- description and source-code
```javascript
registerDefinitions = function (defs) {
  var self = this;
  defs.forEach(function (m) {
    // Prefer 'name', accept older 'ctorName'
    var name = m.name || m.ctorName;
    // Registration may have happened in the model definition file
    // if using the old templates. Don't re-register
    if (!self[name]) {
      self.registerDefinition(name, m.ctor);
    }
  });
  this.createForeignKeys();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.setDefaultAdapter"></a>[function <span class="apidocSignatureSpan">model.</span>setDefaultAdapter (name, config)](#apidoc.element.model.setDefaultAdapter)
- description and source-code
```javascript
setDefaultAdapter = function (name, config) {
  var adapter = adapters.create(name, config);
  this.defaultAdapter = adapter;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.setLocalRequireError"></a>[function <span class="apidocSignatureSpan">model.</span>setLocalRequireError (msg)](#apidoc.element.model.setLocalRequireError)
- description and source-code
```javascript
setLocalRequireError = function (msg) {
  this.localRequireError = msg;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.updateItem"></a>[function <span class="apidocSignatureSpan">model.</span>updateItem (item, params, opts)](#apidoc.element.model.updateItem)
- description and source-code
```javascript
updateItem = function (item, params, opts) {
  var data = {}
    , name = item.type
    , opts = opts || {};

  // Default to the 'update' scenario
  opts.scenario = opts.scenario || 'update'

  model[name].emit('beforeUpdateProperties', item, params, opts);
  item.emit('beforeUpdateProperties');

  utils.mixin(data, item);
  utils.mixin(data, params);
  this.validateAndUpdateFromParams(item, data, opts);

  if (typeof item.afterUpdateProperties === 'function') {
    item.afterUpdateProperties();
  }

  model[name].emit('updateProperties', item);
  item.emit('updateProperties');

  return item;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validateAndUpdateFromParams"></a>[function <span class="apidocSignatureSpan">model.</span>validateAndUpdateFromParams (item, passedParams, opts)](#apidoc.element.model.validateAndUpdateFromParams)
- description and source-code
```javascript
validateAndUpdateFromParams = function (item, passedParams, opts) {
  var params
    , name = item.type
    , type = model.descriptionRegistry[name]
    , properties = type.properties
    , validated = null
    , errs = null
    , camelizedKey
    , skip = opts.skip
    , scenario = opts.scenario
    , skipKeys = {}
    , val;

  if (typeof item.beforeValidate === 'function') {
    item.beforeValidate(passedParams);
  }
  item.emit('beforeValidate')
  model[name].emit('beforeValidate', item, passedParams);

  // May be revalidating, clear errors
  delete item.errors;

  // Convert snake_case names in params to camelCase
  if (this.config.forceCamel) {
    params = {};
    for (var p in passedParams) {
      // Allow leading underscores in the keys for pseudo-privates
      camelizedKey = utils.string.camelize(p, {leadingUnderscore: true});
      params[camelizedKey] = passedParams[p];
    }
  }
  else {
    params = passedParams;
  }

  // User-input should never contain these -- but we still want
  // to validate them to make sure the format didn't get fucked up
  if (typeof item.createdAt != 'undefined') {
    params.createdAt = item.createdAt;
  }
  if (typeof item.updatedAt != 'undefined') {
    params.updatedAt = item.updatedAt;
  }

  if (skip) {
    for (var i in skip) {
      skipKeys[skip[i]] = true;
    }
  }

  for (var p in properties) {
    if (skipKeys[p]) {
      continue;
    }

    validated = this.validateProperty(properties[p], params, {scenario: scenario});
    // If there are any failed validations, the errs param
    // contains an Object literal keyed by field name, and the
    // error message for the first failed validation for that
    // property
    // Use raw, invalid value on the instance
    if (validated.err) {
      errs = errs || {};
      errs[p] = validated.err;
      item[p] = params[p];
    }
    // Otherwise add the type-coerced, valid value to the return item
    else {
      item[p] = validated.val;
    }
  }

  // Should never have been incuded in user input, so safe to
  // rm these from the params
  delete params.createdAt;
  delete params.updatedAt;

  if (errs) {
    item.errors = errs;
  }

  if (typeof item.afterValidate === 'function') {
    item.afterValidate();
  }

  item.emit('validate')
  model[name].emit('validate', item);

  return item;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validateProperty"></a>[function <span class="apidocSignatureSpan">model.</span>validateProperty (prop, params, opts)](#apidoc.element.model.validateProperty)
- description and source-code
```javascript
validateProperty = function (prop, params, opts) {

  var options = opts || {}
    , name = prop.name
    , val = params[name]
    , datatypeName = prop.datatype.toLowerCase()
    , datatypeValidator = this.datatypes[datatypeName].validate
    , result
    , scenario = opts.scenario
    , locale = options.locale || utils.i18n.getDefaultLocale();

  // Validate for the base datatype only if there actually is a value --
  // e.g., undefined will fail the validation for Number, even if the
  // field is optional
  if (!utils.isEmpty(val)) {
    // 'Any' datatype
    if (prop.datatype == '*') {
      result = {
        val: val
      };
    }
    // Specific datatype -- perform validation/type-coercion
    else {
      result = datatypeValidator(name, val, locale);
      if (result.err) {
        return {
          err: result.err,
          val: null
        };
      }
    }
    // Value may have been modified in the datatype check -- e.g.,
    // 'false' changed to false, '8.0' changed to 8, '2112' changed to
    // 2112, etc.
    val = result.val;
  }

  // Now go through all the base validations for this property
  var validations = prop.validations
    , validator
    , err
    , rule;

  for (var p in validations) {
    validator = model.validators[p]
    rule = utils.mixin({}, validations[p], {scenario: opts.scenario});

    if (typeof validator != 'function') {
      throw new Error(p + ' is not a valid validator');
    }

    err = validator(name, val, params, rule, locale);
    // If there's an error for a validation, don't bother
    // trying to continue with more validations -- just return
    // this first error message
    if (err) {
      return {
        err: err,
        val: null
      };
    }
  }

  // If there weren't any errors, return the value for this property
  // and no error
  return {
    err: null,
    val: val
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.model.Migration"></a>[module model.Migration](#apidoc.module.model.Migration)

#### <a name="apidoc.element.model.Migration.Migration"></a>[function <span class="apidocSignatureSpan">model.</span>Migration (name, adapter)](#apidoc.element.model.Migration.Migration)
- description and source-code
```javascript
Migration = function (name, adapter) {
  this.name = name;
  this.adapter = adapter || defaultAdapter;
  this.generator = this.adapter.generator;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.setDefaultAdapter"></a>[function <span class="apidocSignatureSpan">model.Migration.</span>setDefaultAdapter (adapter)](#apidoc.element.model.Migration.setDefaultAdapter)
- description and source-code
```javascript
setDefaultAdapter = function (adapter) {
  defaultAdapter = adapter;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.model.Migration.prototype"></a>[module model.Migration.prototype](#apidoc.module.model.Migration.prototype)

#### <a name="apidoc.element.model.Migration.prototype.addColumn"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>addColumn ()](#apidoc.element.model.Migration.prototype.addColumn)
- description and source-code
```javascript
addColumn = function () {
  var args = Array.prototype.slice.call(arguments)
    , sql = ''
    , table = args.shift()
    , column = args.shift()
    , datatype = args.shift()
    , cb = args.pop()
    , opts = args.pop() || {} // Optional

  sql = this.generator.alterTableStatement(table, {
    operation: 'add'
  , property: {
      name: column
    , datatype: datatype
    }
  });
  this.adapter.exec(sql, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.addIndex"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>addIndex (table, column, options, cb)](#apidoc.element.model.Migration.prototype.addIndex)
- description and source-code
```javascript
addIndex = function (table, column, options, cb) {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.changeColumn"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>changeColumn (table, column, datatype, options, cb)](#apidoc.element.model.Migration.prototype.changeColumn)
- description and source-code
```javascript
changeColumn = function (table, column, datatype, options, cb) {
  var args = Array.prototype.slice.call(arguments)
    , sql = ''
    , table = args.shift()
    , column = args.shift()
    , datatype = args.shift()
    , cb = args.pop()
    , opts = args.pop() || {} // Optional

  sql = this.generator.alterTableStatement(table, {
    operation: 'alter'
  , property: {
      name: column
    , datatype: datatype
    }
  });
  this.adapter.exec(sql, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.createTable"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>createTable ()](#apidoc.element.model.Migration.prototype.createTable)
- description and source-code
```javascript
createTable = function () {
  // FIXME: Shouldn't have to late-require 'model' here
  // Why is order of loading a problem here?
  var model = require('../index')
    , args = Array.prototype.slice.call(arguments)
    , arg
    , sql = ''
    , name = args.shift()
    , opts = {}
    , definition = function () {}
    , cb = args.pop()
    , col = new Columnator();

  // Optional opts/callback or callback/opts
  while ((arg = args.pop())) {
    if (typeof arg == 'function') {
      definition = arg;
    }
    else {
      opts = arg;
    }
  }

  definition(col);

  if (model.config.useTimestamps) {
    col.cols.createdAt = {
      name: 'createdAt'
    , datatype: 'datetime'
    };
    col.cols.updatedAt = {
      name: 'updatedAt'
    , datatype: 'datetime'
    };
  }

  sql = this.generator.createTableStatement(name, col.cols);
  this.adapter.exec(sql, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.down"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>down (next)](#apidoc.element.model.Migration.prototype.down)
- description and source-code
```javascript
down = function (next) {
  next();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.dropTable"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>dropTable (name, cb)](#apidoc.element.model.Migration.prototype.dropTable)
- description and source-code
```javascript
dropTable = function (name, cb) {
  var sql = this.generator.dropTableStatement(name);
  this.adapter.exec(sql, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.removeColumn"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>removeColumn (table, column, cb)](#apidoc.element.model.Migration.prototype.removeColumn)
- description and source-code
```javascript
removeColumn = function (table, column, cb) {
  var sql = this.generator.alterTableStatement(table, {
    operation: 'drop'
  , property: {
      name: column
    }
  });
  this.adapter.exec(sql, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.removeIndex"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>removeIndex (table, column, cb)](#apidoc.element.model.Migration.prototype.removeIndex)
- description and source-code
```javascript
removeIndex = function (table, column, cb) {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.renameColumn"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>renameColumn (table, column, newColumn, cb)](#apidoc.element.model.Migration.prototype.renameColumn)
- description and source-code
```javascript
renameColumn = function (table, column, newColumn, cb) {
  var sql = this.generator.alterTableStatement(table, {
    operation: 'rename'
  , property: {
      name: column
    , newName: newColumn
    }
  });
  this.adapter.exec(sql, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.Migration.prototype.up"></a>[function <span class="apidocSignatureSpan">model.Migration.prototype.</span>up (next)](#apidoc.element.model.Migration.prototype.up)
- description and source-code
```javascript
up = function (next) {
  next();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.model.ModelBase"></a>[module model.ModelBase](#apidoc.module.model.ModelBase)

#### <a name="apidoc.element.model.ModelBase.ModelBase"></a>[function <span class="apidocSignatureSpan">model.</span>ModelBase ()](#apidoc.element.model.ModelBase.ModelBase)
- description and source-code
```javascript
ModelBase = function () {}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.ModelBase.super_"></a>[function <span class="apidocSignatureSpan">model.ModelBase.</span>super_ ()](#apidoc.element.model.ModelBase.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.model.formatters"></a>[module model.formatters](#apidoc.module.model.formatters)

#### <a name="apidoc.element.model.formatters.date"></a>[function <span class="apidocSignatureSpan">model.formatters.</span>date (val)](#apidoc.element.model.formatters.date)
- description and source-code
```javascript
date = function (val) {
  return geddy.date.strftime(val, geddy.config.dateFormat);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.formatters.time"></a>[function <span class="apidocSignatureSpan">model.formatters.</span>time (val)](#apidoc.element.model.formatters.time)
- description and source-code
```javascript
time = function (val) {
  return geddy.date.strftime(val, geddy.config.timeFormat);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.model.validators"></a>[module model.validators](#apidoc.module.model.validators)

#### <a name="apidoc.element.model.validators.absent"></a>[function <span class="apidocSignatureSpan">model.validators.</span>absent (name, val, params, rule, locale)](#apidoc.element.model.validators.absent)
- description and source-code
```javascript
absent = function (name, val, params, rule, locale) {
  var validScenarios = rule.opts && rule.opts.on
    , scenario = rule.scenario
    , shouldValidate = false;

  // By default, we should validate on all scenarios
  if (!validScenarios) {
    shouldValidate = true;
  }

  // If the user specified scenarios
  if (!shouldValidate) {
    // Accept strings too
    if (! validScenarios instanceof Array) {
      validScenarios = [validScenarios];
    }

    // Normalize the input
    for(var i=0, ii=validScenarios.length; i < ii; i++) {
      validScenarios[i] = validScenarios[i].toLowerCase();
    }

    // Scenario might be undefined here, but don't hide the error as
    // we should always validate with a scenario in mind lest something
    // unexpected happen.
    shouldValidate = validScenarios.indexOf(scenario.toLowerCase()) >= 0;
  }

  if (shouldValidate) {
    return baseValidator(name, val, params, rule, locale);
  }
  else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validators.confirmed"></a>[function <span class="apidocSignatureSpan">model.validators.</span>confirmed (name, val, params, rule, locale)](#apidoc.element.model.validators.confirmed)
- description and source-code
```javascript
confirmed = function (name, val, params, rule, locale) {
  var validScenarios = rule.opts && rule.opts.on
    , scenario = rule.scenario
    , shouldValidate = false;

  // By default, we should validate on all scenarios
  if (!validScenarios) {
    shouldValidate = true;
  }

  // If the user specified scenarios
  if (!shouldValidate) {
    // Accept strings too
    if (! validScenarios instanceof Array) {
      validScenarios = [validScenarios];
    }

    // Normalize the input
    for(var i=0, ii=validScenarios.length; i < ii; i++) {
      validScenarios[i] = validScenarios[i].toLowerCase();
    }

    // Scenario might be undefined here, but don't hide the error as
    // we should always validate with a scenario in mind lest something
    // unexpected happen.
    shouldValidate = validScenarios.indexOf(scenario.toLowerCase()) >= 0;
  }

  if (shouldValidate) {
    return baseValidator(name, val, params, rule, locale);
  }
  else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validators.format"></a>[function <span class="apidocSignatureSpan">model.validators.</span>format (name, val, params, rule, locale)](#apidoc.element.model.validators.format)
- description and source-code
```javascript
format = function (name, val, params, rule, locale) {
  var validScenarios = rule.opts && rule.opts.on
    , scenario = rule.scenario
    , shouldValidate = false;

  // By default, we should validate on all scenarios
  if (!validScenarios) {
    shouldValidate = true;
  }

  // If the user specified scenarios
  if (!shouldValidate) {
    // Accept strings too
    if (! validScenarios instanceof Array) {
      validScenarios = [validScenarios];
    }

    // Normalize the input
    for(var i=0, ii=validScenarios.length; i < ii; i++) {
      validScenarios[i] = validScenarios[i].toLowerCase();
    }

    // Scenario might be undefined here, but don't hide the error as
    // we should always validate with a scenario in mind lest something
    // unexpected happen.
    shouldValidate = validScenarios.indexOf(scenario.toLowerCase()) >= 0;
  }

  if (shouldValidate) {
    return baseValidator(name, val, params, rule, locale);
  }
  else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validators.length"></a>[function <span class="apidocSignatureSpan">model.validators.</span>length (name, val, params, rule, locale)](#apidoc.element.model.validators.length)
- description and source-code
```javascript
length = function (name, val, params, rule, locale) {
  var validScenarios = rule.opts && rule.opts.on
    , scenario = rule.scenario
    , shouldValidate = false;

  // By default, we should validate on all scenarios
  if (!validScenarios) {
    shouldValidate = true;
  }

  // If the user specified scenarios
  if (!shouldValidate) {
    // Accept strings too
    if (! validScenarios instanceof Array) {
      validScenarios = [validScenarios];
    }

    // Normalize the input
    for(var i=0, ii=validScenarios.length; i < ii; i++) {
      validScenarios[i] = validScenarios[i].toLowerCase();
    }

    // Scenario might be undefined here, but don't hide the error as
    // we should always validate with a scenario in mind lest something
    // unexpected happen.
    shouldValidate = validScenarios.indexOf(scenario.toLowerCase()) >= 0;
  }

  if (shouldValidate) {
    return baseValidator(name, val, params, rule, locale);
  }
  else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validators.present"></a>[function <span class="apidocSignatureSpan">model.validators.</span>present (name, val, params, rule, locale)](#apidoc.element.model.validators.present)
- description and source-code
```javascript
present = function (name, val, params, rule, locale) {
  var validScenarios = rule.opts && rule.opts.on
    , scenario = rule.scenario
    , shouldValidate = false;

  // By default, we should validate on all scenarios
  if (!validScenarios) {
    shouldValidate = true;
  }

  // If the user specified scenarios
  if (!shouldValidate) {
    // Accept strings too
    if (! validScenarios instanceof Array) {
      validScenarios = [validScenarios];
    }

    // Normalize the input
    for(var i=0, ii=validScenarios.length; i < ii; i++) {
      validScenarios[i] = validScenarios[i].toLowerCase();
    }

    // Scenario might be undefined here, but don't hide the error as
    // we should always validate with a scenario in mind lest something
    // unexpected happen.
    shouldValidate = validScenarios.indexOf(scenario.toLowerCase()) >= 0;
  }

  if (shouldValidate) {
    return baseValidator(name, val, params, rule, locale);
  }
  else {
    return null;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.model.validators.withFunction"></a>[function <span class="apidocSignatureSpan">model.validators.</span>withFunction (name, val, params, rule, locale)](#apidoc.element.model.validators.withFunction)
- description and source-code
```javascript
withFunction = function (name, val, params, rule, locale) {
  var validScenarios = rule.opts && rule.opts.on
    , scenario = rule.scenario
    , shouldValidate = false;

  // By default, we should validate on all scenarios
  if (!validScenarios) {
    shouldValidate = true;
  }

  // If the user specified scenarios
  if (!shouldValidate) {
    // Accept strings too
    if (! validScenarios instanceof Array) {
      validScenarios = [validScenarios];
    }

    // Normalize the input
    for(var i=0, ii=validScenarios.length; i < ii; i++) {
      validScenarios[i] = validScenarios[i].toLowerCase();
    }

    // Scenario might be undefined here, but don't hide the error as
    // we should always validate with a scenario in mind lest something
    // unexpected happen.
    shouldValidate = validScenarios.indexOf(scenario.toLowerCase()) >= 0;
  }

  if (shouldValidate) {
    return baseValidator(name, val, params, rule, locale);
  }
  else {
    return null;
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
