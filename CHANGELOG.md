### v0.4.0

* update `Caret.js` to `v0.0.2`
* `contenteditable` support !!
* change content of default item template `tpl`
* new rule to insert the `at` : will always remove the `at` from inputor but will add it back from `tpl` in default.
  so, if you are using your own `tpl` and want to show the `at` char, you have to do it yourself.
* add `insert_tpl` setting for `contenteditable`.
  it will insert `data-value` of li element that eval from `tpl` in default.
* new APIs for `contenteditable`: `getInsertedItemsWithIDs`, `getInsertedItems`, `getInsertedIDs`

### 2013-08-07 - v0.3.2

* bower
* remove `Caret.js` codes and add it as bower dependencies
* remove `display_flag` settings.
* add `start_with_space` settings, default `true`
* change `super_call` function to `call_default`

### 2013-04-28

* release new api `load`, `run`
* add `alias` setting for `load` data or as the view's id
* matching key with a space before it
* register key in settings `{at: "@", data: []}` instead of being a argument
* `max_len` setting for max length to search
* change the default matcher regrex rule: occur at start of line or after whitespace
* will not sort the datay without valid query string

### 2013-04-23

* group all data handlers as `Model` class.
* All callbacks's context would be current `Controller`

### 2013-04-05

* `data` setting will be used to load data either local or remote. If it's String as URL it will preload data from remote by launch a ajax request (every times At.js call `reg` to update settings)

* remove default `remote_filter` from callbacks list.
* add `get_data` and `save_data` function to contoller. They are used to get and save whole data for At.js
* `save_data` will invoke `data_refactor` everytime

* will filter local data which is set in `settings` first and if it get nothing then call `remote_filter` if it's exists in callbacks list that is set by user.

### 2013-04

* remove ability of changing common setting after inputor binded
* can fix list view after matched query in IE now.
* separated core function (get offset of inputor) as a jquery plugins.

### v0.2.0 - 2012-12

**No more testing in IEs browsers.**

#### Note
The name `atWho` was changed to `atwho`.

#### New features

* Customer data handlers(matcher, filter, sorter) and template renders(highlight, template eval) by a group of configurable callbacks.
* Support **AMD**

#### Removed features

* Filter by local data and remote (by ajax) data at the same time.
* Caching
* Mouse event

#### Changed settings

`-` mean removed option
`+` mean new added option
The one that start without `-` or `+` mean not change.

* `-` data: [],
* `+` data: null,

* `-` choose: "data-value",
* `+` search_key: "name",

* `-` callback: null,
* `+` callbacks: DEFAULT_CALLBACKS,

* `+` display_timeout: 300,

* `-` tpl: _DEFAULT_TPL
* `+` tpl: DEFAULT_TPL

* `-` cache: false

Not change settings

*     cache: true,
*     limit: 5,
*     display_flag: true,

### v0.1.7

同步 `jquery-atwho-rails` gem 的版本号
这会是 `v0.1` 的固定版本. 不再有新功能更新.

###v0.1.2 2012-3-23
* box showing above instead of bottom when it get close to the bottom of window
* coffeescript here is.
* every registered character able to have thire own options such as template(`tpl`)
* every inputor (textarea, input) able to have their own registered character and different behavior
  even the same character to other inputor

###v0.1.0
* 可以監聽多個字符
    multiple char listening.
* 顯示缺省列表.
    show default list.
