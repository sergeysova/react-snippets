# Snippets for sublime react

Install:

```bash
./installMac
```


## Props

Trigger: `defaultProps`<br/>
Tab switch: 2<br/>
Template: `children`, `''`<br/>
Result:<br/>

```js
static defaultProps = {
  children: ''
};
```

---

Trigger: `propTypes`<br/>
Tab switch: 2<br/>
Template: `children`, `any`<br/>
Result:<br/>

```js
static propTypes = {
  children: React.PropTypes.any
};
```

## Imports

Trigger: `imports`<br/>
Tab switch: 2<br/>
Template: `Directory`, `Component`<br/>
Result:<br/>

```js
import DirectoryComponent from 'Directory/Component/DirectoryComponent';
```

## Component

Trigger: `rComponent`<br/>
Tab switch: 1<br/>
Template: `ComponentName`<br/>
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
Template: `ComponentName`<br/>
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
Template: `ComponentName`, `baobab_branch`, `array`<br/>
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
Template: `ComponentName`, `baobab_branch`, `array`<br/>
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
Template: `getAccount`, `userID`, `get`, `account/${userID}`<br/>
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
