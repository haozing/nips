# NIPs

NIPs stand for **Nostr Implementation Possibilities**. They exist to document what may be implemented by [Nostr](https://github.com/fiatjaf/nostr)-compatible _relay_ and _client_ software.

NIP 代表Nostr Implementation Possibilities。它们的存在是为了记录Nostr兼容的中继和客户端软件可以实现什么。
- [NIP-01: Basic protocol flow description](01.md)

  基本协议流程描述
- [NIP-02: Contact List and Petnames](02.md)

    联系人列表和昵称
- [NIP-03: OpenTimestamps Attestations for Events](03.md)

    事件的 OpenTimestamps 证明
- [NIP-04: Encrypted Direct Message](04.md)

    加密私信
- [NIP-05: Mapping Nostr keys to DNS-based internet identifiers](05.md)

    将 Nostr 密钥映射到基于 DNS 的互联网标识符
- [NIP-06: Basic key derivation from mnemonic seed phrase](06.md)

    助记种子短语的基本密钥推导
- [NIP-07: `window.nostr` capability for web browsers](07.md)

    window.nostr网络浏览器的能力
- [NIP-08: Handling Mentions](08.md)

    处理提及
- [NIP-09: Event Deletion](09.md)

    事件删除
- [NIP-10: Conventions for clients' use of `e` and `p` tags in text events](10.md)

    客户端在文本事件中使用`e`和`p`标签的约定
- [NIP-11: Relay Information Document](11.md)

    中继信息文档
- [NIP-12: Generic Tag Queries](12.md)

    通用标签查询
- [NIP-13: Proof of Work](13.md)

    工作量证明
- [NIP-14: Subject tag in text events.](14.md)

    文本事件中的主题标签
- [NIP-15: End of Stored Events Notice](15.md)

    存储事件的结束通知
- [NIP-16: Event Treatment](16.md)

    事件处理
- [NIP-19: bech32-encoded entities](19.md)

    bech32编码实体
- [NIP-20: Command Results](20.md)

    命令结果
- [NIP-21: `nostr:` URL scheme](21.md)

    `nostr:` URL 方案
- [NIP-22: Event `created_at` Limits](22.md)

    事件`created_at`限制
- [NIP-23: Long-form Content](23.md)

    长形式内容
- [NIP-25: Reactions](25.md)

    反应
- [NIP-26: Delegated Event Signing](26.md)

    委托事件签名
- [NIP-28: Public Chat](28.md)

    公共聊天
- [NIP-33: Parameterized Replaceable Events](33.md)

    参数化可替换事件
- [NIP-36: Sensitive Content](36.md)

    敏感内容
- [NIP-40: Expiration Timestamp](40.md)

    过期时间戳
- [NIP-42: Authentication of clients to relays](42.md)

    客户端向中继的身份验证
- [NIP-46: Nostr Connect](46.md)

    Nostr 连接
- [NIP-50: Keywords filter](50.md)

    关键字过滤
- [NIP-51: Lists](51.md)

    列表
- [NIP-56: Reporting](56.md)

    报告
- [NIP-57: Lightning Zaps](57.md)

    闪电 Zap
- [NIP-58: Badges](58.md)

    徽章
- [NIP-65: Relay List Metadata](65.md)

    中继列表元数据
- [NIP-78: Application-specific data](78.md)

    应用程序特定数据

## Event Kinds

活动种类

| kind          | description                      | NIP         |
| ------------- | -------------------------------- | ----------- |
| 0             | Metadata   元数据                 | [1](01.md)  |
| 1             | Short Text Note  简短的文字说明    | [1](01.md)  |
| 2             | Recommend Relay 推荐接力                 | [1](01.md)  |
| 3             | Contacts     联系人                    | [2](02.md)  |
| 4             | Encrypted Direct Messages  加密的直接消息      | [4](04.md)  |
| 5             | Event Deletion    事件删除               | [9](09.md)  |
| 7             | Reaction           反应              | [25](25.md) |
| 8             | Badge Award        徽章奖              | [58](58.md) |
| 40            | Channel Creation   频道创建              | [28](28.md) |
| 41            | Channel Metadata   渠道元数据              | [28](28.md) |
| 42            | Channel Message    频道留言              | [28](28.md) |
| 43            | Channel Hide Message   频道隐藏消息          | [28](28.md) |
| 44            | Channel Mute User   通道静音用户             | [28](28.md) |
| 1984          | Reporting    报告                    | [56](56.md) |
| 9734          | Zap Request      Zap 请求                | [57](57.md) |
| 9735          | Zap        电击                      | [57](57.md) |
| 10000         | Mute List    静音列表                    | [51](51.md) |
| 10001         | Pin List          	引脚列表               | [51](51.md) |
| 10002         | Relay List Metadata  中继列表元数据            | [65](65.md) |
| 22242         | Client Authentication   客户端认证         | [42](42.md) |
| 24133         | Nostr Connect     Nostr连接               | [46](46.md) |
| 30000         | Categorized People List  分类人物列表        | [51](51.md) |
| 30001         | Categorized Bookmark List  分类书签列表      | [51](51.md) |
| 30008         | Profile Badges           个人资料徽章        | [58](58.md) |
| 30009         | Badge Definition    徽章定义             | [58](58.md) |
| 30023         | Long-form Content      长篇内容          | [23](23.md) |
| 30078         | Application-specific Data  特定于应用程序的数据      | [78](78.md) |
| 1000-9999     | Regular Events   定期活动                | [16](16.md) |
| 10000-19999   | Replaceable Events   可替换事件            | [16](16.md) |
| 20000-29999   | Ephemeral Events    短暂的事件             | [16](16.md) |
| 30000-39999   | Parameterized Replaceable Events参数化可替换事件 | [33](33.md) |

## Message types消息类型

### Client to Relay客户端到中继
| type  | description                                         | NIP         |
|-------|-----------------------------------------------------|-------------|
| EVENT事件 | used to publish events  用于发布事件                            | [1](01.md)  |
| REQ 请求  | used to request events and subscribe to new updates用于请求事件和订阅新的更新 | [1](01.md)  |
| CLOSE 关闭| used to stop previous subscriptions  用于停止以前的订阅               | [1](01.md)  |
| AUTH 授权 | used to send authentication events     用于发送认证事件             | [42](42.md) |

### Relay to Client中继到客户端
| type   | description                                             | NIP         |
|--------|---------------------------------------------------------|-------------|
| EVENT事件  | used to send events requested to clients  用于向客户端发送请求的事件              | [1](01.md)  |
| NOTICE注意 | used to send human-readable messages to clients   用于向客户端发送人类可读的消息      | [1](01.md)  |
| EOSE EOSE  | used to notify clients all stored events have been sent用于通知客户端所有存储的事件已发送 | [15](15.md) |
| OK  好的   | used to notify clients if an EVENT was successful  用于通知客户事件是否成功     | [20](20.md) |
| AUTH 授权  | used to send authentication challenges	用于发送身份验证挑战                  | [42](42.md) |

Please update these lists when proposing NIPs introducing new event kinds.

请在提议引入新事件类型的 NIP 时更新这些列表。

When experimenting with kinds, keep in mind the classification introduced by [NIP-16](16.md).

在尝试种类时，请记住NIP-16引入的分类。
## Standardized Tags标准化标签

| name       | value                   | other parameters  | NIP                      |
| ---------- | ----------------------- | ----------------- | ------------------------ |
| e          | event id (hex)  事件 ID（十六进制）        | relay URL, marker | [1](01.md), [10](10.md)  |
| p          | pubkey (hex)      公钥（十六进制）      | relay URL         | [1](01.md)               |
| a          | coordinates to an event 事件的坐标| relay URL         | [33](33.md), [23](23.md) |
| r          | a reference (URL, etc) 参考（URL 等） |                   | [12](12.md)              |
| t          | hashtag   井号              |                   | [12](12.md)              |
| g          | geohash  地理散列               |                   | [12](12.md)              |
| nonce      | random   随机的               |                   | [13](13.md)              |
| subject    | subject    主题             |                   | [14](14.md)              |
| d          | identifier    标识符          |                   | [33](33.md)              |
| expiration | unix timestamp (string) unix 时间戳（字符串）|                   | [40](40.md)              |

## Criteria for acceptance of NIPs接受 NIP 的标准

1. They should be implemented in at least two clients and one relay -- when applicable.

    它们应该在至少两个客户端和一个中继中实现——如果适用的话。
2. They should make sense.

    它们应该有意义。
3. They should be optional and backwards-compatible: care must be taken such that clients and relays that choose to not implement them do not stop working when interacting with the ones that choose to.

    它们应该是可选的和向后兼容的：必须小心，以便选择不实现它们的客户端和中继在与选择的客户端和中继交互时不会停止工作。
4. There should be no more than one way of doing the same thing.

    不应该有超过一种方法来做同一件事。
5. Other rules will be made up when necessary.

    其他规则将在必要时制定。

## License

All NIPs are public domain.

所有 NIP 都是公共领域。
