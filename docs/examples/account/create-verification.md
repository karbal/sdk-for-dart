import 'package:appwrite/appwrite.dart';

// Init SDK
Client client = Client();
Account account = Account(client);

client
    .setProject('5df5acd0d48c2') // Your project ID
;

Future result = account.createVerification(
    url: 'https://example.com',
);

result
  .then((response) {
    print(response);
  }).catchError((error) {
    print(error);
  });