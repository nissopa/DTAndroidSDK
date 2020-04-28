# Getting Started

Add the module's import in your app's gradle file:

``` gradle
implementation "com.discover-tech.sdk:core:[VERSION_NUMBER]"
```

On your main activity in the `onCreate` method add:

``` java

// Optional 
DTTracker.userDataProvider = new DTUserDataProvider() {
    @Override
            public String getUserName() {
                return "John Snow";
            }

            @Override
            public String getUserEmail() {
                return "exa@test.com";
            }

            @Override
            public Location getLocation() {
                Location loc = new Location()
                loc.setLong({SOME_LONGITUDE});
                loc.setLat({SOME_LATITUDE});
                loc.setLocationType({GPS or CELL});
                return new Location()
            }
};
```

On your main activity in the `onResume()` method add:

``` java

DTTracker.launchApp({APP_ID})
```

