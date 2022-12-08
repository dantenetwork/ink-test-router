# Test Router

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

You can use one of those accounts, as shown in Fig.2, to transfer token to you router account.

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

## Run docker

```sh
$ sudo docker compose up
## show logs
$ sudo docker logs -f my_router
```

