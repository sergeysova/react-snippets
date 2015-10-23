# Snippets for sublime react

Install:

```bash
./installMac
```


## Props

Trigger: `defaultProps`
Tab switch: 2
Template: `children`, `''`
Result:

```js
static defaultProps = {
  children: ''
};
```

---

Trigger: 'propTypes'
Tab switch: 2
Template: `children`, `any`
Result:

```js
static propTypes = {
  children: React.PropTypes.any
};
```

## Imports

Trigger: `imports`
Tab switch: 2
Template: `Directory`, `Component`
Result:

```js
import DirectoryComponent from 'Directory/Component/DirectoryComponent';
```

## Component

Trigger: `rComponent`
Tab switch: 1
Template: `ComponentName`
Result: 

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

Trigger: `rComponentStyled` (`rcs`)
Tab switch: 1
Template: `ComponentName`
Result:

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

Trigger: `rBranch` (`rba`)
Tab switch: 3
Template: `ComponentName`, `baobab_branch`, `array`
Result:

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

Trigger: `rBranchStyled` (`rbs`)
Tab switch: 3
Template: `ComponentName`, `baobab_branch`, `array`
Result:

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

Trigger: `rAction` (`rac`)
Tab switch: 4
Template: `getAccount`, `userID`, `get`, `account/${userID}`
Result:

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
