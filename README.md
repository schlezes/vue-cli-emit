# vue-cli-emit

Using Vue $emit to send-up A.vue component props for App.vue parent access

This is a very simple example for $emit working with the App.vue parent.

With a click event on the A.vue component, the parent App.vue methods has access to the A.vue properties and in this case expands the width property by 1.25 times.

The App.vue parent has access to the B.vue properties as well, and in this case updates the backgroundColor with the $event.target.style.backgroundColor.

Here is the HTML render shown with a screenshot.

![image](https://user-images.githubusercontent.com/89032071/169089984-56f8fb57-27a3-4a0e-b04d-2d87564d638e.png)

and the App.vue parent screenshot.

![image](https://user-images.githubusercontent.com/89032071/169091768-04fd77e1-d410-47cc-9b42-651323cc516c.png)

The A.vue component "emits" with a v-on:click="chg($emit, $event.target.value)

![image](https://user-images.githubusercontent.com/89032071/168941338-acc5e495-b1ec-4281-bcb5-b191ccc98fd8.png)

On the parent detecting a change in A.vue component, the v-on:chg="log" is invoked in the App.vue parent.

![image](https://user-images.githubusercontent.com/89032071/168941468-149883d5-1497-421d-aeaf-880d84d68ad9.png)

Now, there is access to A.vue properties from the App.vue parent by way of the methods log() function.

I have console.logged the several A.vue properties attached to the A.vue component.

The key to success is by way of the chg() $emit, $event.target that is passed upward from the child A.vue and made available in the methods: log() function in the parent App.vue.

There is a 2nd component, B.vue component, that just serves as a placeholder.  The App.vue parent changes the backgroundColor of this component with the $event.target.style.backgroundColor of the A.vue component.

With the B.vue component, a click event will also expand the width by 1.25 times and reset the backgroundColor to orange.


