# myPage

## Steps to deploy web app in firebase hosting

## Helpful Links
- https://firebase.google.com/docs/hosting/quickstart
- https://firebase.google.com/support/guides/app-links-universal-links

1. Install Firebase CLI
2. Initialize the project -> `firebase init hosting`
3. Deploy -> `firebase deploy --only hosting`

## Deeplinking - Android

1. add the file `asseslinks.json` under `/.well-known`
2. add the following to `firebase.json`
´´´ 
 "headers": [
    {
      "source": "/.well-known/assetlinks.json",
      "headers": [
        {
          "key": "Content-Type",
          "value": "application/json"
        }
      ]
    }
  ]

´´´


## Deeplinking - iOS

1. add the file `apple-app-site-association` under `/.well-known`
2. add the following to `firebase.json`
´´´ 
 "headers": [
    {
      "source": "/.well-known/apple-app-site-association",
      "headers": [
        {
          "key": "Content-Type",
          "value": "application/json"
        }
      ]
    }
  ]

´´´