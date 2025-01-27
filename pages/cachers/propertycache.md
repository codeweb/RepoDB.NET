---
layout: default
sidebar: cachers
title: "PropertyCache"
description: "A class that is being used to retrieve the cached properties of the class or data entity."
permalink: /cacher/propertycache
tags: [repodb, class, propertycache, orm, hybrid-orm, sqlserver, sqlite, mysql, postgresql]
parent: CACHERS
---

# PropertyCache

---

A hugely-used cacher class for the [ClassProperty](/class/classproperty). It provides a 2nd-layer caching for the library when it comes to the class properties extraction.

> Internally, this class is widely used within the library.

### Methods

Below are the methods available from this class.

- `Flush` - allows you to flush the caches.
- `Get` - returns the list of [ClassProperty](/class/classproperty) objects.

### Usability

You can simply call the `Get()` method of this class by passing the class type.

```csharp
var properties = PropertyCache.Get(typeof(Person));
// Use the 'properties' here
```

Or, via generic type.

```csharp
var properties = PropertyCache.Get<Person>();
// Use the 'properties' here
```

> Internally, it uses the [PropertyMapper](/mapper/propertymapper) and [ClassExpression](/class/classexpression) classes to extract and cache the list of [ClassProperty](/class/classproperty) objects.