### Starting via Docker

To start application via Docker, you have to follow these steps:
1. Clone the repository:
```
  $ git clone --recurse-submodules https://github.com/quizhorniw/ecommerce
```
2. Go to `ecommerce` directory:
```
  $ cd ecommerce
```
3. Create `.env` file with following variables:
```
SYMMETRIC_KEY_ID=some-value
AAD_CONTEXT=some-value
YC_ENDPOINT=some-value
OAUTH_TOKEN=some-value
JWT_KEY_ID=some-value
```
where
- `SYMMETRIC_KEY_ID` is ID of the symmetric key which you should create on [Yandex Cloud](https://console.yandex.cloud) platform
- `AAD_CONTEXT` (Additional Authenticated Data) is additional data passed to the input of the encrypt and decrypt operations. Can be anything
- `YC_ENDPOINT` is endpoint to Yandex Cloud API. Usually it is `api.cloud.yandex.net:443`
- `OAUTH_TOKEN` is your Yandex OAuth token. Read more about it [here](https://yandex.cloud/en/docs/iam/concepts/authorization/oauth-token)
- `JWT_KEY_ID` is ID used to store and access encrypted secret key through database. Can be anything
4. Run Docker-Compose:
```
  $ docker-compose up
```
