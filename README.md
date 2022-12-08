# Test Router

## Clone this repo
```sh
git clone git@github.com:dantenetwork/ink-test-router.git
cd ./ink-test-router
```

## Pull router docker image

```sh
sudo docker pull registry.us-west-1.aliyuncs.com/cherima/dante
```

## Create a router account

Use [polkadot.js](https://polkadot.js.org/apps/#/explorer).

Connect the substrate rpc, mentioned in [Ink! Test Guide](https://github.com/dantenetwork/protocol-stack-for-ink/blob/feature-sqos/test/README.md#test-environment).

![img](./assets/4.jpg)
<p align="center">Fig 1. create account</p>

Create an account as `Raw seed` and save the seed for configuration.

![img](./assets/1.jpg)
![img](./assets/2.jpg)
<p align="center">Fig 2. create account, choose Raw seed</p>

You can use one of those accounts, as shown in Fig.3, to transfer token to you router account.

![img](./assets/3.jpg)
<p align="center">Fig 3. transfer token</p>


## Configuration

```sh
$ cd config
$ mv .secret.example .secret
```

Modify the contents of `.secret`, as shown following.

```json
{
    "POLKADOTTEST": "YOU RAW SEED"
}
```

For `default.json`, keep `networks.POLKADOTTEST.nodeAddress` and `networks.POLKADOTTEST.crossChainContractAddress` consistent with mentioned in [Ink! Test Guide](https://github.com/dantenetwork/protocol-stack-for-ink/blob/feature-sqos/test/README.md#test-environment).

## Remember to contact us before run the docker as the Testnet is not fully open to the public at this stage  

* discord: `xeeeyu#4107`

## Run docker

```sh
$ sudo docker compose up
## show logs
$ sudo docker logs -f my_router
```

