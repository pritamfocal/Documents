## Integration

> **Note**:
-  UserExperior supports os versions from Android JellyBean (4.3) API Level 16 to Android 11 API Level 30!

### 1. Add FocalxAI SDK

1. Follow the below link to download
- [Download (SDK)](http://focalx.ai)

2. Unzip the file and drag the `FocalxAi.aar` file  to the “libs” folder in your android studio project.

### 2. Add FocalX dependency in build.gradle of your app

Note: If FocalX is already integrated in your project, just re-sync the project with Gradle.

```
  implementation(name:'FocalxAi', ext:'aar'){ transitive = true; }
```

### 3. Start FocalX SDK

1. In your app where ever you want to present damage detectiopn model, include:

       import com.focalxai.guide.FocalxActivity;

2. In your app where ever you want to present damage detectiopn model, include:

       import com.focalxai.guide.FocalxActivity;

3. Before showing FocalX.ai damage Guide, please create a token and supply it to our SDK as parameter

-   Please check the API documentation to create Token to supply to our SDK 

     [API Token generation](https://github.com/pritamfocal/Documents/blob/main/api-authentification.md)

- Use following code in your activity present guiding system

        Intent myIntent = new Intent(MainActivity.this, FocalxActivity.class);
        myIntent.putExtra("token","token for authentification which you got from your API");
        MainActivity.this.startActivity(myIntent);
