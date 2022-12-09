Open the command prompt on your computer.
Navigate to the directory where the keytool utility is located (usually in the "bin" folder of your Java installation directory).
Type the following command to generate a new keystore file:
keytool -genkey -alias [insert alias name] -keyalg RSA -keysize 2048 -keystore [insert keystore file name].jks

Enter the necessary information when prompted, such as your name, organization, and password for the keystore.

Once the keystore has been generated, you can use the following command to add a certificate to the keystore:

keytool -import -trustcacerts -alias [insert alias name] -file [insert certificate file name].crt -keystore [insert keystore file name].jks

Enter the password for the keystore when prompted.

To view the contents of the keystore, use the following command:

keytool -list -v -keystore [insert keystore file name].jks

Enter the password for the keystore when prompted. The keystore contents will be displayed in the command prompt.

To export a certificate from the keystore, use the following command:

keytool -export -alias [insert alias name] -file [insert certificate file name].crt -keystore [insert keystore file name].jks

Enter the password for the keystore when prompted. The certificate will be exported to the specified file.
