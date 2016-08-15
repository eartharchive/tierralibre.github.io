---
layout: post
title: Chip and Nodejs
subtitle: Installing node on Chip and enabling i2c with node.
---

There is a little linux computer called [Chip](https://getchip.com/pages/chip) which costs 9$. It comes with 4gb of disk, 512mb of RAM bluetooth, wifi and a bunch of gpio's.
I wanted to set nodejs with it in order to talk to the BME280 environment sensor, which provides temperature, humidity and pressure.
This post outlines the steps to quickly do it.

First we install node from [nodesource](https://github.com/tierralibre/distributions#debinstall) by typing the following on the Chip terminal. (There is documentation on how to get Chip connected via terminal on the Chip docs).

This posts assumes you are using Chip's debian image.

~~~
curl -sL https://deb.nodesource.com/setup_6.x | bash -
apt-get install -y nodejs
~~~

Now that we have node installed it's time to do some preparation in order to install the i2c npm package.
We need to have the basic tools to compile as the i2c package will try to re-compile.

~~~
sudo apt-get install -y build-essential g++ python-setuptools python2.7-dev
~~~

Now we can go ahead and install our i2c packages via npm.

~~~
npm install i2c
~~~

If it does not work there are some instructions on the i2c npm package which can be handy about loading the i2c-dev module etc ...

In the next post we will discuss using the BMO280 sensor as part of a environmental adquisition project.

I hope it helps!

Enjoy!
