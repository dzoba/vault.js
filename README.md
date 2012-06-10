storage.js
===============

wrapper for localStorage, sessionStorage and document.cookie that sets and gets true values

#### Demo
http://jimmybyrum.github.com/storage.js/

#### Usage
##### set and get
```
Storage.Session.set("foo", "bar");
Storage.Session.get("foo");
// returns "bar"

Storage.Local.set("my_array", [1,2,3,4]);
Storage.Local.get("my_array");
// [1,2,3,4]

Storage.Session.set("my_object", {
  foo: "bar",
  an_array: [1,2,3],
  year: 2012
});
Storage.Session.get("my_object");
// {
//   foo: "bar",
//   an_array: [1,2,3],
//   year: 2012
// }


Storage.Local.set("age", 33);
Storage.Local.get("age");
// returns the number 33
```

##### remove
removes an item
```
Storage.Session.remove("my_object");
Storage.Local.remove("my_array");
```

##### clear
clears all items
```
Storage.Session.clear();
Storage.Local.clear();
```

##### list
lists all items in Storage in the console
```
Storage.Session.list();
Storage.Local.list();
```

##### isSupported
returns a boolean to indicate if local and session storage are supported
```
Storage.Session.isSupported();
Storage.Local.isSupported();
```

#### TODO
- handle storage limit errors
- add support to request more storage
- handle storage events
