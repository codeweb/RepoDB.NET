---
layout: default
sidebar: cachers
title: "IdentityCache"
description: "A class that is being used to retrieve the cached identity field of the class or data entity."
permalink: /cacher/identitycache
tags: [repodb, class, identitycache, orm, hybrid-orm, sqlserver, sqlite, mysql, postgresql]
parent: CACHERS
---

# IdentityCache

---

A cacher class for the class identity property. Underneath, it uses the [IdentityMapper](/mapper/identitymapper) class to extract the results and caching it for future use.

### Methods

Below are the methods available from this class.

- `Flush` - allows you to flush the caches.
- `Get` - returns the list of [Field](/class/field) objects.

### Usability

You can simply call the `Get()` method of this class by passing the class type.

```csharp
var identity = IdentityCache.Get(typeof(Person));
// Use the 'identity' here
```

Or, via generic type.

```csharp
var identity = IdentityCache.Get<Person>();
// Use the 'identity' here
```

> Internally, it uses the [IdentityMapper](/mapper/identitymapper) and [PropertyCache](/cacher/propertycache) classes to extract the list of [ClassProperty](/class/classproperty) and filter the result using the given [IsIdentity()](/class/classproperty#isidentity) method.