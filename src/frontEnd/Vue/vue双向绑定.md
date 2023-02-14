## vue2 双向绑定

vue2 的双向绑定一般是用过 v-model 使用的  
v-model 是 vue2 双向绑定的一个语法糖，具体是结合了： v-bind:value和 v-on:input 来实现的，  
+ v-bind:value实现了 data  --> UI 的单向绑定
+ v-on:input实现了  UI --> data 的单向绑定

两者结合，就形成了双向绑定

`v-bind:value`的具体实现是借助了 `Object.defineprototype` 函数，给数据的 getter和 setter属性，修改，监听数据修改的时机，进而去更新 UI

`v-on`是通过 `template`给 `Dom`添加监听事件， `Dom input`的值改变了，就回去更新 `data`