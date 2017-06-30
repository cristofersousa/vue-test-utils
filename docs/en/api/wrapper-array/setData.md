# setData(data)

Sets Vue instance data and forces update of every wrapper in wrapper array.

Can only be called on a wrapper array of Vue component wrappers.

### Arguments

data (`Object`): Data properties and corresponding value to set

### Example

```js
import { mount } from 'vue-test-utils'
import { expect } from 'chai'
import Foo from './Foo.vue'
import Bar from './Bar.vue'

const wrapper = mount(Foo)
const barArray = wrapper.findAll(Bar)
barArray.setData({ foo: 'bar' })
expect(barArray.at(0).vm.foo).to.equal('bar')
```