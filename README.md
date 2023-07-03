Throughout several months, we embarked on a software engineering school project that challenged us to design and develop an innovative application. Our task involved integrating three distinct APIs into a cohesive mobile app, resulting in the creation of the project we have extensively discussed.

This project served as a platform for us to apply our software engineering skills and demonstrate our proficiency in working with APIs. Over the course of its development, we meticulously crafted a user-friendly and feature-rich application that showcases the seamless integration of these APIs.

The primary objective was to leverage the functionalities provided by the APIs to enhance the overall user experience and provide valuable features to our app's target audience. Through careful planning, extensive research, and countless iterations, we successfully achieved this goal.

As a testament to our dedication and perseverance, the resulting app showcases a seamless fusion of technologies, offering a wide range of practical features and a polished user interface. We are excited to present the culmination of our efforts and share the outcome of this school project in the form of our remarkable application.

This is the case we chose: https://in2000.met.no/2023/5-opencase-hav 


Here are some screenshots from the application: 





Installation guide
     1. Clone the GitHub project / Unzip the project folder.
     2. Open the project in Android Studio.
     3. Navigate to README.md.
     4. Copy the three keys and paste them at the bottom of local.properties.
     5. Copy the dependencies and paste them into build.gradle (Module: App). You can overwrite other dependencies already present there.
     6. Click on Sync Now in the message that appears above the code box.
     7. Open the Device Manager, click on Create device, and select Pixel 2 with API level 28.
     8. Start the emulator, open Extended controls (three dots stacked on top of each other).
     9. Under Location, drag the map to Norway and click on a location along the coast. Click on SAVE POINT and then Set location.
     10. Start the app by clicking on the green arrow in the menu at the top.


add to local.properties:

    GOOGLE_MAPS_API_KEY = AIzaSyCtUtAv6RFDzClFOc8LbxK5B5cRybtb1KI
    MET_KEY = dc1732ae-a8a0-4dd5-8052-26094bfbca11
    GEO_KEY = "Ef8bkbpLK+TeaAk43qgYqw==mZBU9A3ckObEAYY7"
    SEAORLAND_KEY = "6e4ec9b570msh7ec67a9af607dbdp1fce72jsnddb99294423f"


gradle.build:

    dependencies {
        implementation "androidx.core:core-ktx:1.9.0"
        implementation "androidx.core:core:1.9.0"
        implementation 'androidx.lifecycle:lifecycle-runtime-ktx:2.5.1'
        implementation 'androidx.activity:activity-compose:1.6.1'
        // Need this or MapEffect throws exception.
        implementation "androidx.appcompat:appcompat:1.5.1"

        // Compose
        // From https://www.jetpackcomposeversion.com/
        implementation "androidx.compose.ui:ui:1.3.2"
        implementation "androidx.compose.material:material:1.3.1"

        // Google maps
        implementation 'com.google.android.gms:play-services-maps:18.1.0'
        implementation 'com.google.android.gms:play-services-location:21.0.1'
        // Google maps for compose
        implementation 'com.google.maps.android:maps-compose:2.8.0'

        // KTX for the Maps SDK for Android
        implementation 'com.google.maps.android:maps-ktx:3.2.1'
        // KTX for the Maps SDK for Android Utility Library
        implementation 'com.google.maps.android:maps-utils-ktx:3.2.1'

        // Hilt
        implementation "com.google.dagger:hilt-android:2.42"
        implementation 'junit:junit:4.12'
        implementation 'androidx.constraintlayout:constraintlayout:2.1.4'
        kapt "com.google.dagger:hilt-compiler:2.42"

        //Ikoner
        implementation "androidx.compose.material:material-icons-extended:$compose_version"
        implementation "androidx.compose.material:material-icons-core"

        //Navigasjon
        implementation "androidx.navigation:navigation-compose:2.4.0-alpha06"

        implementation 'androidx.core:core-ktx:1.7.0'
        implementation 'androidx.lifecycle:lifecycle-runtime-ktx:2.3.1'
        implementation 'androidx.activity:activity-compose:1.3.1'
        implementation "androidx.compose.ui:ui:$compose_version"
        implementation "androidx.compose.ui:ui-tooling-preview:$compose_version"
        implementation 'androidx.compose.material3:material3:1.0.0-alpha11'
        testImplementation 'junit:junit:4.13.2'
        androidTestImplementation 'androidx.test.ext:junit:1.1.5'
        androidTestImplementation 'androidx.test.espresso:espresso-core:3.5.1'
        androidTestImplementation "androidx.compose.ui:ui-test-junit4:$compose_version"
        debugImplementation "androidx.compose.ui:ui-tooling:$compose_version"
        debugImplementation "androidx.compose.ui:ui-test-manifest:$compose_version"

        implementation 'com.google.android.gms:play-services-maps:18.1.0'


        //imports for viewmodel
        implementation"androidx.lifecycle:lifecycle-viewmodel-compose:2.5.1"
        implementation"androidx.compose.runtime:runtime-livedata:$compose_version"

        implementation 'com.google.android.material:material:1.5.0'
        implementation "androidx.compose.material3:material3:1.1.0-alpha03" // Material 3

        implementation("org.jetbrains.kotlinx:kotlinx-coroutines-core:1.6.4")


        def ktor_version = "2.2.3"
        implementation"io.ktor:ktor-client-android:$ktor_version"
        implementation"io.ktor:ktor-client-content-negotiation:$ktor_version"
        implementation"io.ktor:ktor-serialization-gson:$ktor_version"
        implementation "io.ktor:ktor-serialization-kotlinx-json:$ktor_version"

        implementation "androidx.lifecycle:lifecycle-viewmodel-compose:2.5.1"

    }
