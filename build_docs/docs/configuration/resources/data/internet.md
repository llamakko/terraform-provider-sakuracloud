# ルータ(sakuracloud_internet)

---

### 設定例

```hcl
data sakuracloud_internet "router" {
  name_selector = ["foobar"]
}
```

### パラメーター

|パラメーター         |必須  |名称                |初期値     |設定値                    |補足                                          |
|-------------------|:---:|--------------------|:--------:|------------------------|----------------------------------------------|
| `name_selectors`  | -   | 検索条件(名称)      | -        | リスト(文字列)           | 複数指定した場合はAND条件  |
| `tag_selectors`   | -   | 検索条件(タグ)      | -        | リスト(文字列)           | 複数指定した場合はAND条件  |
| `filter`          | -   | 検索条件(その他)    | -        | オブジェクト             | APIにそのまま渡されます。検索条件を指定してもAPI側が対応していない場合があります。 |
| `zone`            | -   | ゾーン | - | `is1a`<br />`is1b`<br />`tk1a`<br />`tk1v` | - |


### 属性

|属性名                | 名称                    | 補足                                        |
|---------------------|------------------------|--------------------------------------------|
| `id`                | ルータID               | -                                          |
| `name`              | ルータ名           | - |
| `nw_mask_len`       | ネットワークマスク長  | - |
| `band_width`        | 帯域幅(Mbps単位)  | - |
| `enable_ipv6`       | IPv6有効化  | - |
| `icon_id`           | アイコンID         | - |
| `description`       | 説明  | - |
| `tags`              | タグ | - |
| `zone`              | ゾーン | - |
| `server_ids`        | サーバID              | 接続されているサーバのID(リスト)             |
| `switch_id`         | スイッチID              | (内部的に)接続されているスイッチID              |
| `nw_address`        | ネットワークアドレス      | ルータに割り当てられたグローバルIPのネットワークアドレス |
| `gateway`           | ゲートウェイ             | ルータに割り当てられたセグメントのゲートウェイIPアドレス |
| `min_ipaddress`     | 最小IPアドレス           | ルータに割り当てられたグローバルIPアドレスのうち、利用可能な先頭IPアドレス [注1](#ルータ-sakuracloud_internet_属性_注1) |
| `max_ipaddress`     | 最大IPアドレス           | ルータに割り当てられたグローバルIPアドレスのうち、利用可能な最後尾IPアドレス [注1](#ルータ-sakuracloud_internet_属性_注1) |
| `ipaddresses`       | IPアドレスリスト         | ルータに割り当てられたグローバルIPアドレスのうち、利用可能なIPアドレスのリスト [注1](#ルータ-sakuracloud_internet_属性_注1)|
| `ipv6_prefix`       | IPv6アドレスプレフィックス| -              |
| `ipv6_prefix_len`   | IPv6アドレスプレフィックス長 | -             |
| `ipv6_nw_address`   | IPv6ネットワークアドレス     | -             |
