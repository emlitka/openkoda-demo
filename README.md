## Run Demo App

### Option 1: Import .zip package to your clean Openkoda Core instance

1. Log in to Openkoda dashboard as an Admin.
2. Go to Configuration -> Import/Export (`/html/components`).
3. Choose the downloaded `.zip` file and Import it.
4. After a successful import, the application will take a short time to restart.
5. Log in to Dashboard again. All of the demo app components should be already visible there.

### Option 2. Unpack the .zip and run the Demo App from IDE

1. Unpack the downloaded .zip.
2. Create an empty database named `openkoda_components` in Postgres.\
   Alternatively adjust the settings in `src/main/resources/application-components.properties`.
3. Enter the unpacked contents folder and open a command line to run initialization of the App\
   `mvn spring-boot:run -Dspring-boot.run.profiles=openkoda,components,drop_and_init_database`
4. Run the App\
   `mvn spring-boot:run -Dspring-boot.run.profiles=openkoda,components`