# Cymbal Group API

To use the Cymbal Group API, you need an API key. The key is a credential
that gives you access to the API.

## Why you need an API key

The Cymbal Group API uses an API key to authenticate your requests and ensure
optimal performance. You can't fetch data from the API without a key.

## Get an API key

To get an API key, follow these steps:

1.  Log into the main console.
2.  If you don't have an API key, create one.
3.  Make sure you have the correct account type (Developer or Administrator).
4.  Copy the generated alphanumeric string. This is your API key.

For more information about authentication, see [Authentication](link-to-auth-docs).

## Save the API key

After you create your API key, save it in the `config.json` file for the
Cymbal Group SDK. This file is located in your home directory.

Add the key to the `Key-Settings` section of the `config.json` file:

```
API_KEY = Y0UR_SUPER_L0NG_AND_C0MPL1CAT3D_K3Y
```

**Note:** Don't include quotation marks around the key value in the
configuration file.
