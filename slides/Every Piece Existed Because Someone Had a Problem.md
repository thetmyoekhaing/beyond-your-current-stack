# Every Piece Existed Because Someone Had a Problem

ဒီ slide မှာ software architecture ထဲက component တစ်ခုချင်းစီကို technology name အနေနဲ့မကြည့်ဘဲ **ဖြေရှင်းပေးတဲ့ problem** နဲ့တွဲကြည့်ထားပါတယ်။

| Piece | ဘာအတွက်လဲ | ဥပမာ |
|---|---|---|
| Interface | User မြင်ပြီး interact လုပ်တဲ့နေရာ | React, SwiftUI, Figma |
| API | System တွေ တစ်ခုနဲ့တစ်ခု စကားပြောဖို့ | REST, gRPC, GraphQL |
| Load Balancer | Traffic ကို ခွဲပေးဖို့ | Nginx, Envoy |
| CDN | User နဲ့နီးတဲ့နေရာကနေ content ပေးဖို့ | Cloudflare, Fastly |
| Database | Data ရဲ့ အဓိကအမှန်တရားကို သိမ်းဖို့ | Postgres, SQLite |
| Cache | ထပ်ခါထပ်ခါ မမေးဘဲ မြန်မြန်ပြန်ပေးဖို့ | Redis, in-process |
| Message Queue | Slow work ကို request နဲ့ ခွဲထုတ်ဖို့ | SQS, Kafka, NATS |
| Worker | Background မှာ အလုပ်လုပ်စေဖို့ | Celery, Temporal |
| Object Store | File တွေကို row မဟုတ်ဘဲ သိမ်းဖို့ | S3, R2 |
| CI / CD | Code ကို ယုံကြည်စိတ်ချစွာ ship လုပ်ဖို့ | GitHub Actions |
| Monitoring | System ပျက်တာ/ပြဿနာဖြစ်တာ သိဖို့ | OpenTelemetry, Grafana |
| Auth | Request လုပ်တဲ့သူ ဘယ်သူလဲ သိဖို့ | OAuth, OIDC |

Technology name ကိုပဲ မှတ်မယ်ဆိုရင် “Kafka ဆိုတာဘာလဲ?” လို့ အမြဲပြန်စရပါမယ်။ Problem ကို အရင်မြင်ထားရင် “ဒီ workload ကို asynchronous လုပ်ဖို့ queue လိုနိုင်တယ်” ဆိုပြီး technology တွေကို ပြန်ရှာနိုင်ပါတယ်။

Tool တစ်ခုကို တွေ့တိုင်း မေးလို့ရတဲ့မေးခွန်းတွေက —
- ဘာ problem ကို ဖြေရှင်းပေးတာလဲ?
- ဘယ်အချိန်မှာ တကယ်လိုအပ်တာလဲ?
- အခြားနည်းလမ်းတွေက ဘာတွေလဲ?
- ဒီ tool ထည့်လိုက်ရင် complexity ဘယ်လောက်တိုးသွားမလဲ?

Slide ထဲက **“two you almost never need on day one”** ဆိုတာကလည်း အစကတည်းက architecture ထဲကို tool အများကြီး ထည့်ဖို့မလိုဘူးဆိုတဲ့ point ကို ထောက်ပြတာပါ။

## Deeper: Tools Encode Trade-offs

A technology is usually a bundle of decisions. A queue can give you asynchronous processing while introducing retries, ordering, duplicate delivery, or dead-letter handling. A cache can reduce latency while creating another consistency problem. A database gives durable state while introducing migrations, indexes, backups, transactions, and operational work.

So learn both the capability and the cost.

A useful question is: **What became difficult before this tool existed?** A CDN makes global content delivery easier. A load balancer makes traffic distribution easier. CI makes repeatable validation and delivery easier.

Then ask the opposite: **What does this tool make harder?** Every abstraction moves complexity rather than deleting it. A managed service may remove server maintenance but add provider-specific constraints. A distributed system may improve availability while introducing network failure and consistency concerns.

The real engineering question is not “Is this technology good?” It is “For this problem, is the complexity this technology introduces worth the problem it removes?”
