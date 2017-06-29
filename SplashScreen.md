# [Android Templates](https://github.com/gotoark/AndroidTemplates/blob/master/READ.md) - :boom: Splash Screen :boom:

### ToDo: :clipboard:

 * Create Splash Screen Drawable
 * Define a Custom Splash Screen theme
 * Add the theme to the activity in  Manifest
 * Create Splash Activity
 * Have a Cup of Cofee :coffee:


### 1. Add Splash Screen Drawable

```
<layer-list xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:drawable="@color/colorSplashScreen" />
    <item>
        <bitmap
            android:gravity="center"
            android:src="@mipmap/ic_launcher"/>
    </item>
</layer-list>
```
### 2. Define a Custom Splash Screen theme 

```
<resources>
    <!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <!-- Customize your theme here. -->
    </style>

    <style name="SplashTheme" parent="Theme.AppCompat.NoActionBar">
        <item name="android:windowBackground">@drawable/background_splash</item>
    </style>
</resources>
```

### 3. Add the theme to the activity in  Manifest 

```
<activity android:name=".screens.SplashScreen" android:theme="@style/SplashTheme">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
```

### 4 .Create Splash Activity 

```
public class SplashScreen extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);

        Intent intent=new Intent(this, Home.class);
        startActivity(intent);
        finish();
    }
}
```

### Final Result : :point_down:
      
 ![Splash Screen](/gifs/SplashScreen.gif?raw=true "Splash Screens the Right Way")     
      


### Reference :pray:
- [Splash Screens the Right Way](https://goo.gl/bvKH6o) by [Chris Stewart](https://www.bignerdranch.com/about/the-team/chris-stewart/) :person_with_blond_hair:

Made with :muscle: [Markdown Editor](https://jbt.github.io/markdown-editor/#bVNBbtswELzzFVs4gO3GltpremqTpgkQA0WTnoICoUVSpC1yBXJlJyn69y4pw84hgAnJ5HBmd2Y1gdkPRzfDenndyR1GreawknGrcB/gu3KEUYhvMrkGhqTN0IHRkoaooXOJLoSAj3BJsTu/hxouveInISS500BWg3GdPkGsM3QCHv4xvLGISR8vynQqASPcPKzuMsdVlC3IoEBF7EEWbnCBb1kdy+0OpQJHGXydDxsMpAMlkHyeqfk0lLp+/7qDhPCCAzQyQLIZkQmTEOJ26iEgtIgKJME+OnKhZQLfM2mdcZ2OQPqZFpmlxYJhCfSabMYycUy6M5UQd4jbBZeb/fpQ/DKI+bGWcXy8CvGV28pdTFMh4cqV/gAX55/Z4aenp43cydRE15M4m5khNOQwzOZ/BcDZbKrcbjqvLPluNr0F6VmMt6rp/Iv4x4vvC/FgXQL+PWKAMfA/M0vUp4u6bh3ZYV016OvNmmp/8H6pS/zz3GKnCbisbcA9OAO3U45p/Slus6NUSt7n8rld8ZPTSTmNVazgCnFdMsvyj7krGFlHdRb3UTGmiPcRN7qhVGfcQb2eL8BE9LC3rrEiZ+dC6l2U2YIsw4anRdEozll+ewGXo/Kc/QjjTIhBjfS5xMlkAvc0GJNHWmUOL7e6EI0D/Xi0wNG7Nr05f/s+52jjaXZ7GRMPQ2G85JZWLsY3necufdmqgqZ6vJwblHtdWkkvXP/z0rrWdryIax1NKYzH7WqTjpwJDe15lr0MTjapwtiWvfqIrnU4SI30cDzJc8ufBw7UD1QmENYdNttU5DZpqbTpJOl3HVEybLGVrj7hRpX21fV9pkYDSpI82s1zY3ixIn+MSfwH) and :kissing_heart: [GitHub Emoji](https://gist.github.com/rxaviers/7360908) :raised_hands:
