# vue-cli-emit

Using Vue $emit to send-up A.vue component props for App.vue parent access

I have a very simple example for $emit working with the App.vue parent.

Here is the HTML render shown with a screen shot.

![image](https://user-images.githubusercontent.com/89032071/168940675-b8888c83-670e-4c5e-abe3-f85c26a9c388.png)

and the App.vue screenshot.

![image](https://user-images.githubusercontent.com/89032071/168940818-d4032a06-e46f-405f-970a-839e4897a219.png)

The A.vue component "emits" with a v-on:click="chg($emit, $event.arget.value)

![image](https://user-images.githubusercontent.com/89032071/168941338-acc5e495-b1ec-4281-bcb5-b191ccc98fd8.png)

On the parent detecting a change in A.vue component, the v-on:chg="log" is invoked in the App.vue parent.

![image](https://user-images.githubusercontent.com/89032071/168941468-149883d5-1497-421d-aeaf-880d84d68ad9.png)

Now, there is access to A.vue properties from the App.vue parent by way of the methods log() function.

I have console.logged the several A.vue properties attached to the A.vue component.

The key to success is by way of the chg() $emit, $event.target that is passed upward from the child A.vue and made available in the methods: log() function in the parent App.vue.

There is a 2nd component, B.vue component that just serves as a placeholder.  No $emits on this component.
