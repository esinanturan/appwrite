import 'package:appwrite/appwrite.dart';

Client client = Client()
    .setEndpoint('https://<REGION>.cloud.appwrite.io/v1') // Your API Endpoint
    .setSession('') // The user session to authenticate with
    .setKey('') // 
    .setJWT('<YOUR_JWT>'); // Your secret JSON Web Token

Databases databases = Databases(client);

Document result = await databases.createDocument(
    databaseId: '<DATABASE_ID>',
    collectionId: '<COLLECTION_ID>',
    documentId: '<DOCUMENT_ID>',
    data: {},
    permissions: ["read("any")"], // optional
);
