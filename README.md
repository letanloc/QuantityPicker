# Quantity Picker v1.0.2
[![Platform](http://img.shields.io/badge/platform-android-brightgreen.svg?style=flat)](http://developer.android.com/index.html) [![Language](http://img.shields.io/badge/language-java-orange.svg?style=flat)](http://www.oracle.com/technetwork/java/javase/downloads/index.html) [![License](http://img.shields.io/badge/license-apache2.0-lightgrey.svg?style=flat)](http://www.apache.org/licenses/LICENSE-2.0)

The android library that provides a simple and similar to NumberPicker that can be used in shopping cart as a quantity picker. It's very easy to use.
 . I hope that you will like it, and enjoys it. ^ ^
### Screenshots

<img src="screenshots/picker.png" width="25%" />

```Maven
####Maven
<dependency>
  <groupId>com.andanhm.quantitypicker</groupId>
  <artifactId>quantitypicker</artifactId>
  <version>1.0.2</version>
  <type>pom</type>
</dependency>
```

```Gradle
####Gradle
repositories {
    maven {
        url 'https://dl.bintray.com/andanhm3/maven'
    }
}

dependencies {
    compile 'com.andanhm.quantitypicker:quantitypicker:1.0.2'
}
```
If it doesn't work, please send me a email, andanhm3@gmail.com

####Or

Import the library, then add it to your `/settings.gradle` and `/app/build.gradle`
### License

It's very easy, just like this:
#### XML

add `xmlns:app="http://schemas.android.com/apk/res-auto"`

```xml
    <com.andanhm.quantitypicker.QuantityPicker
        xmlns:app="http://schemas.android.com/apk/res-auto/"
        android:id="@+id/quantityPicker"
        app:minQuantity="1"
        app:maxQuantity="5"
        app:textStyle="bold"
        app:quantityColor="@color/colorPrimary"
        app:buttonColor="@color/colorAccent"
        app:layout_width="wrap_content"
        app:layout_height="wrap_content"/>
```
### Attributes

|attribute name|attribute description|
|:-:|:-:|
|minQuantity|To set the minimum value of the quantity picker (default Min Quantity : 1 )|
|maxQuantity|To set the maximum value of the quantity picker (default Max Quantity : 10 )| 
|quantityColor|To set the text color of the quantity picker|
|buttonColor|To set the button color of the quantity picker|
|textSize|To set the text size of the quantity picker|
|textStyle|To set text style of the quantity picker (bold,italic,bold_italic,normal)|

#### Java

```java
        QuantityPicker quantityPicker = (QuantityPicker) findViewById(R.id.quantityPicker);

        //Returns the selected quantity
        quantityPicker.getQuantity();

        //Allows to set the minimum quantity
        quantityPicker.setMinQuantity(1);

        //Allows to set the maximum quantity
        quantityPicker.setMaxQuantity(10);

        //Enable/Disable quantity picker
        quantityPicker.setQuantityPicker(true);

        //Allows to set the text style quantity
        quantityPicker.setTextStyle(QuantityPicker.BOLD);

        //To set the quantity text color
        quantityPicker.setQuantityTextColor(R.color.colorPrimaryDark);

        //To set the quantity button color
        quantityPicker.setQuantityButtonColor(R.color.colorAccent);

        // Returns the quantity on quantity selection
        quantityPicker.setOnQuantityChangeListener(new QuantityPicker.OnQuantityChangeListener() {
            @Override
            public void onValueChanged(int quantity) {

            }
        });

```
Copyright 2015 Google, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements. See the NOTICE file distributed with this work for
additional information regarding copyright ownership. The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License. You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
License for the specific language governing permissions and limitations under
the License.
```
