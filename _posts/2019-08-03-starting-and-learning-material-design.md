---
title: Starting & Learning Material Design For Android Applications
last_modified_at: 2019-08-03
categories: 
     - Blog
tags: 
     - Google
     - Material
     - Material_Design
     - Android
---

As an Android Developer, using Google’s [Material Design](https://material.io/design/introduction/) official website is the most important thing for developing an Android App.

But the question is, **what exactly the Material Design is**?

From [here](https://material.io/design/introduction/):

> Material Design is a visual language that synthesizes the classic principles of good design with the innovation of technology and science.

This is actually the new Google’s language for Applications, Websites and etc. We're not trying to go so deep inside what that is but *to know how to use it on Android Applications*.

#### Using Material Design Guidelines on Android Apps

In another words, those (rules) are actually some useful and standard ways for developing an Android Application. You can use those rules and make standard applications by using Material Design Guidelines which is a really helpful way to design a very attractive and beautiful UI for your apps.

Let's get started with a few examples. Imagine you're trying to add some `CardView`s to your app and you might have added following codes which includes a `TextView` inside a `CardView`:

#### CardView

```xml 
<!-- A CardView that contains a TextView -->
<androidx.cardview.widget.CardView
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginLeft="@dimen/mtrl_card_spacing"
    android:layout_marginTop="@dimen/mtrl_card_spacing"
    android:layout_marginRight="@dimen/mtrl_card_spacing"
    android:minHeight="200dp">
    
  <TextView
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"
      android:text="@string/demo_card_text"/>
      
</androidx.cardview.widget.CardView>
```

It will be just a `CardView` and a `TextView` inside. But, that's not the exact point. If you check [this link](https://material.io/design/components/cards.html#anatomy), you'll see the anatomy of a `CardView` which mentioned about the place of the `TextView`:

<img src="http://s8.picofile.com/file/8368655184/mio_staging_mio_design_1563837804615_assets_1eZNTdj8h1J0BFkbl23LyzEwjjvMzY_uV_cards_elements_2b.png" alt="first_pic" width="500px" height="350px">

There are still other widgets in there which are; 


- three `TextButton`s 
- an `ImageView` 
- a `CircleImageView`

And etc which is a good example for a `CardView`. However, we're talking & looking for some rules, some standard ways from Google Material Design and if you see the below image, you'll understand what I've been talking about:

<img src="http://s8.picofile.com/file/8368656050/secondpic.png" alt="secondPic" width="500px" height="350px">

Here, there is a `Rich Media`, `Primary Text`, `Supporting Text` and `Actions` which we can use this format for our `CardView`s in future but, here comes the rules.

<img src="http://s9.picofile.com/file/8368656650/third_pic.png" alt="secondPic" width="500px" height="350px">

As you can see, the title `TextView` has `34dp` from `CardView`’s above (`margin-top = 34dp`). Also, the `CircleImageView`’s size is `40dp`. Simple, right?! :)

#### CardView’s Elevation Rules

After `CardView`’s `TextView` margins, we go through the `CardView`’s Elevation rules:

<img src="http://s8.picofile.com/file/8368657718/elevation.png" alt="secondPic" width="500px" height="350px">

As you can see, they already explained about some default behaviours on mobile. 

> On mobile, a card’s default `elevation` is `1dp`, with a raised `elevation` of `8dp`.

- You can also change the elevation value by [`card_view:cardElevation`](https://developer.android.com/reference/android/support/v7/widget/CardView.html#attr_CardView_cardElevation) attribute.

That's it for now. Please check and refresh this post later again.

<sup>This article will be updated in future.</sup>


**Resources:**

[Introduction](https://material.io/design/introduction/)

[Material Card](https://material.io/develop/android/components/material-card-view/)

[Cards](https://material.io/design/components/cards.html)

[Elevation](https://material.io/design/environment/elevation.html)





