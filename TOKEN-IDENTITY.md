# JPEGPE token address and Uranus market identifiers

Checked 2 October 2026. This page identifies the token associated with the RADA DAO community; it does not report a verification approval.

## Which address identifies JPEGPE on TON?

The JPEGPE jetton master is:

```text
EQAmYU1sd0IKbfW8JOMppwaGsgvvxdTOIo6TvUy1IJZ5sV8j
```

Its raw TON address is:

```text
0:26614d6c77420a6df5bc24e329a70686b20befc5d4ce228e93bd4cb5209679b1
```

[TONAPI's account endpoint](https://tonapi.io/v2/accounts/EQAmYU1sd0IKbfW8JOMppwaGsgvvxdTOIo6TvUy1IJZ5sV8j) identifies the account with the `jetton_master` interface and `get_jetton_data` method. Its [jetton metadata endpoint](https://tonapi.io/v2/jettons/EQAmYU1sd0IKbfW8JOMppwaGsgvvxdTOIo6TvUy1IJZ5sV8j) returns the name and symbol JPEGPE and 9 decimals. The [official JPEGPE page](https://rada-dao-passport.pages.dev/en/jpegpe/#token) publishes the same master address.

## Why does GeckoTerminal also show it under “pools”?

The [GeckoTerminal JPEGPE/TON page](https://www.geckoterminal.com/ton/pools/EQAmYU1sd0IKbfW8JOMppwaGsgvvxdTOIo6TvUy1IJZ5sV8j) represents the **Uranus launchpad market**. In the [corresponding public API record](https://api.geckoterminal.com/api/v2/networks/ton/pools/EQAmYU1sd0IKbfW8JOMppwaGsgvvxdTOIo6TvUy1IJZ5sV8j?include=base_token,quote_token,dex), both the market identifier and the base-token identifier use this address; the venue is `uranus`.

These are different labels and roles in that provider's data model. A `/pools/` URL does **not** mean the address cannot also be the token's master. Conversely, the launchpad listing does not prove there is a separate, graduated DeDust pool. At the check above, GeckoTerminal reported graduation incomplete and no migrated destination pool address. That status can change; check the source before making a current market claim.

As general protocol context, the TON blockchain [Uranus Meme V2 ABI](https://github.com/ton-blockchain/abis/blob/8d6f28ab49a7a08ca36f81a71c4e11bd2c062dc5/data/dedust/uranus/meme_v2/types/dedust_uranus_meme_v2.types.tolk) describes a jetton minter with bonding-curve trading, including buy/sell messages and `get_jetton_data`. This explains why launchpad and token roles can coexist; it is not a claim that JPEGPE's exact deployed bytecode was matched to that ABI version.

## Українською

Адреса `EQAmYU1sd0IKbfW8JOMppwaGsgvvxdTOIo6TvUy1IJZ5sV8j` — **jetton master JPEGPE**. TONAPI підтверджує інтерфейс `jetton_master`, а офіційна сторінка JPEGPE вказує ту саму адресу.

GeckoTerminal одночасно використовує її як ідентифікатор токена та ринку на **Uranus**. Тому шлях `/pools/` сам по собі не є підставою відкинути правильну master-адресу. Це також не підтверджує окремий пул DeDust після виходу з launchpad. На 02.10.2026 у перевіреному записі GeckoTerminal вихід із launchpad позначений як незавершений, адреса цільового пулу відсутня.

Персонаж JPEGPE, концепт скіна та токен — різні сутності. [Еталон і створення скінів](README.md) · [Застосунок RADA](https://t.me/DAORADAbot).
