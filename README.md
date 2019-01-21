### basket.js
---
https://github.com/addyosmani/basket.js

```
npm install & bower install
grunt release
```

```js
basket.require({ url: 'jquery.js' });

basket.require(
  { url: 'jquery.js' },
  { url: 'underscore.js' },
  { url: 'backbone.js' }
);

basket.require(
  { url: 'require.js' },
  { url: 'require.config.js', skipCache: true },
  { url: 'lib.js' }
);

basket
  .require({ url: 'jquery.js' })
  .then(function(){
    basket.require({ url: 'jquery-ui.js' });
  });
  
basket
  .require({ url: 'missing.js' })
  .then(function(){
    // Success
  }, function(error){
    console.log(error);
  });
  
basket.require({ url: 'jquery-2.0.0.min.js', key: 'jquery' });

basket.require({ url: 'jquery.min.js', expire: 2 })

basket.require({ url: 'jquery.min.js', execute: false });

basket.require({ url: 'jquery.min.js' });
basket.require({ url: 'jquery.min.js', unique: 123 });

var req
var ttl;
basket.require({ url: 'jquery.min.js', key: 'jquery' });
req = basket.get('jquery');
ttl = req.expire = req.stamp;

basket
  .remove('jquery.js')
  .remove('modernizr');
  
basket.clear();
basket.clear(true);

basket.isValidItem = funciton(source, obj){
  return myVerificationFunction(source, obj);
};



```

```
```

