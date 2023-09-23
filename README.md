# Sjøvett - Enhancing Safety and Experience at Sea

Welcome to the Sjøvett application, developed to improve user safety and experience while at sea. This mobile app encompasses various functionalities, all aimed at empowering boat users with valuable tools and information. The application consists of six distinct pages, each serving a specific purpose:

- Mann-over-bord (Man Overboard): This feature leverages wave and weather information to provide an estimated search area in a man overboard situation. By analyzing these factors, it helps determine the most likely location where a person fell overboard, optimizing search and rescue efforts."
- Stormvarsel (Storm Warning): Stay informed about weather conditions with this feature, which offers real-time storm warnings and forecasts to ensure safe navigation.
- Reiseplanlegger (Trip Planner): Plan your trips efficiently using this tool, allowing you to map out your route and calculate estimated time of arrival.
- Sjøvettregler (Sea Safety Rules): Access a comprehensive collection of sea safety rules and guidelines to ensure responsible and safe behavior at sea.
- Livredning (Lifesaving): This feature equips users with essential lifesaving techniques and instructions to respond effectively to critical situations.
- Sjømerker (Sea Marks): Gain knowledge about various sea marks and navigational aids through this informative resource.


## About the Project
Throughout several months, we embarked on a software engineering school project that challenged us to design and develop an innovative application. Our task involved integrating three distinct APIs into a cohesive mobile app, resulting in the creation of this project.

This project served as a platform for us to apply our software engineering skills and demonstrate our proficiency in working with APIs, as well as Android Studio. Over the course of its development, we crafted a user-friendly and feature-rich application that showcases the integration of these APIs.

The primary objective was to leverage the functionalities provided by the APIs to enhance the overall user experience and provide valuable features to boat users. Through careful planning, extensive research, and countless iterations, we successfully achieved this goal.

As a testament to our dedication and perseverance, the resulting app showcases a seamless fusion of technologies, offering a wide range of practical features and a polished user interface. We are excited to present the culmination of our efforts and share the outcome of this school project in the form of our remarkable application.

To gain a better understanding of our project, we chose the following case as the basis for our application: https://in2000.met.no/2023/5-opencase-hav. 

## Screenshots
Here are some screenshots from the Sjøvett application:

#### Navigation Drawer
<img width="250" alt="image" src="https://github.com/alekshoi/Sjovett/assets/93198257/f9f9b008-8190-4fe1-9a6c-48445df97fe6">

#### Man Overboard
<img width="250" alt="image" src="https://github.com/alekshoi/Sjovett/assets/93198257/1204ce2b-f896-4337-a57c-e6e340ea1046">

#### Storm Warning
<img width="250" alt="image" src="https://github.com/alekshoi/Sjovett/assets/93198257/4ee72f8e-2dd9-44dc-9c9a-8192f39d8513">

#### Trip Planner
<img width="250" alt="image" src="https://github.com/alekshoi/Sjovett/assets/93198257/f0811b9f-eb88-46d8-8e98-6d78e5a5e871">


## Getting Started
To explore the full functionality of Sjøvett and experience its valuable features, please refer to installation guide.

We appreciate your interest in our project and hope that Sjøvett enhances your safety and enjoyment during your sea adventures. If you have any questions or feedback, please feel free to reach out to us.


### Installation guide
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
You need to generate API-keys for the following values:

- `GOOGLE_MAPS_API_KEY` =
- `MET_KEY` =
- `GEO_KEY` =
- `SEAORLAND_KEY` =


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
