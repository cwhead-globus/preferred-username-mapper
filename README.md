## About
This mapper is intended for use with Keycloak as a custom protocol mapper. It maps the `preferred_username` token claim to `username@<KC_HOSTNAME>` rather than the default `username`.

## Installation
1. Install the `.zip` file containing the source code:
     
    ```
    wget https://github.com/cwhead-globus/preferred-username-mapper/archive/refs/heads/main.zip
    unzip main.zip
    rm main.zip
    ```
2. Install Maven:
    ```
    sudo apt install maven
    ```
3. Build the `.jar` file associated with the source code:
    From inside the `preferred-username-mapper-main` directory created by unzipping `main.zip`, run the following command:
    ```
    mvn clean install
    ```
4. Move the `target/globus-keycloak-mapper-1.0.jar` file to Keycloak's `providers/` directory.
