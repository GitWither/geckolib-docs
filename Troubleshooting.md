# Troubleshooting
Occasionally you may run into issues with GeckoLib. Before submitting an issue, please read through this page first.

* **Animation isn't playing** - Check the console for logs, make sure GeckoLib is able to find the path to your animation file and the animation name's you are specifying are *exactly* what they are in the json file. Additionally, make sure you actually registered your AnimationController to your AnimationControllerCollection. Put a breakpoint in your AnimationPredicate and make sure it's actually being run. Read more about this [here.](https://github.com/bernie-g/geckolib/wiki/Animation-Controllers)

* **Animation only plays once** - Make sure that you set your animation to loop in blockbench. You can always use the overload of `AnimationBuilder#setAnimation()` that takes a loop parameter. This will override the loop value set in blockbench. Additionally, you can also set `AnimatedEntityModel#loopByDefault = true`, which will make every animation loop by default.

* **Animations take too long/too short to transition** - Make sure your transition length is in ticks. You can change this value in the `AnimationController` constructor or by setting the field directly.

If you still have problems, feel free to make an issue on github.