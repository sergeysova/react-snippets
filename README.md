# Snippets for sublime react

Install:

```bash
./installMac
```


## Props

Trigger: `defaultProps`<br/>
Tab switch: 2<br/>
Template: `1:children`, `2:''`<br/>
Result:<br/>

```js
static defaultProps = {
  children: ''
};
```

---

Trigger: `propTypes`<br/>
Tab switch: 2<br/>
Template: `1:children`, `2:any`<br/>
Result:<br/>

```js
static propTypes = {
  children: React.PropTypes.any
};
```

## Context

Trigger: `getChildContext`<br/>
Tab switch: 2<br/>
Template: `1:name`, `2:string`<br/>
Result:<br/>

```js
static childContextTypes = {
  name: React.PropTypes.string
};

getChildContext() {
  return {
    name: string
  };
}
```

---

Trigger: `contextTypes`<br/>
Tab switch: 2<br/>
Template: `1:name`, `2:string`<br/>
Result:<br/>

```js
static contextTypes = {
  name: React.PropTypes.string
};
```

## Imports

Trigger: `imports`<br/>
Tab switch: 2<br/>
Template: `1:Directory`, `2:Component`<br/>
Result:<br/>

```js
import DirectoryComponent from 'Directory/Component/DirectoryComponent';
```

## Component

Trigger: `rComponent`<br/>
Tab switch: 1<br/>
Template: `1:ComponentName`<br/>
Result: <br/>

```js

import React, { Component } from 'react';


export default class ComponentName extends Component {

  /**
   * Render component ComponentName
   */
  render() {
    return (
      <div>
        
      </div>
    );
  }
}

```

---

Trigger: `rComponentStyled` (`rcs`)<br/>
Tab switch: 1<br/>
Template: `1:ComponentName`<br/>
Result:<br/>

```js

import CN from 'classnames';
import css from './ComponentName.styl';
import React, { Component } from 'react';


export default class ComponentName extends Component {

  /**
   * Render component ComponentName
   */
  render() {
    return (
      <div className={CN(css.ComponentName)}>
        
      </div>
    );
  }
}

```

---

Trigger: `rBranch` (`rba`)<br/>
Tab switch: 3<br/>
Template: `1:ComponentName`, `2:baobab_branch`, `3:array`<br/>
Result:<br/>

```js
import React, { Component } from 'react';


@SubscribedTo('baobab_branch')
export default class ComponentName extends Component {

  static propTypes = {
    baobab_branch: React.PropTypes.array.isRequired
  };

  /**
   * Render component ComponentName
   */
  render() {
    return (
      <div>
        
      </div>
    );
  }
}

```

---

Trigger: `rBranchStyled` (`rbs`)<br/>
Tab switch: 3<br/>
Template: `1:ComponentName`, `2:baobab_branch`, `3:array`<br/>
Result:<br/>

```js

import CN from 'classnames';
import css from './ComponentName.styl';
import React, { Component } from 'react';


@SubscribedTo('baobab_branch')
export default class ComponentName extends Component {

  static propTypes = {
    baobab_branch: React.PropTypes.array.isRequired
  }

  /**
   * Render component ComponentName
   */
  render() {
    return (
      <div className={CN(css.ComponentName)}>
        
      </div>
    );
  }
}

```

## Actions

Trigger: `rAction` (`rac`)<br/>
Tab switch: 4<br/>
Template: `1:getAccount`, `2:userID`, `3:get`, `4:account/${userID}`<br/>
Result:<br/>

```js

/**
 * !<Need description for getAccount>!
 *
 * @returns {Promise}       Thenable/Catcheable
 */
export function getAccount(userID) {
  return get(`/account/${userID}`)
    .then((response) => {
      
      return response;
    });
}

```
