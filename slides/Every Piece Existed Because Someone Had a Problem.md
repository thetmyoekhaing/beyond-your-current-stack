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

##

Technology တစ်ခုချင်းစီမှာ သူ့နောက်က problem တစ်ခုနဲ့ trade-off တချို့ ရှိတတ်ပါတယ်။ Queue တစ်ခုက background work ကို request ကနေ ခွဲပေးနိုင်ပေမယ့် retry, ordering, duplicate message, failure handling စတာတွေကို ထပ်စဉ်းစားရနိုင်ပါတယ်။ Cache က response မြန်စေနိုင်ပေမယ့် data နှစ်နေရာမှာ ရှိလာတဲ့အတွက် consistency ကို ထပ်စဉ်းစားရပါတယ်။ Database က data ကို တည်ငြိမ်စွာသိမ်းပေးနိုင်ပေမယ့် migration, index, backup, transaction စတာတွေကိုလည်း တာဝန်ယူရပါတယ်။

ဒါကြောင့် technology တစ်ခုကို လေ့လာတဲ့အခါ “သူက ဘာလုပ်နိုင်လဲ” တစ်ခုတည်း မမေးဘဲ “သူမရှိခင် ဘာက ခက်နေတာလဲ” လို့ မေးကြည့်တာ အရမ်းအသုံးဝင်ပါတယ်။ CDN ဆိုတာ global content delivery ကို လွယ်စေဖို့၊ load balancer ဆိုတာ traffic ခွဲပေးဖို့၊ CI ဆိုတာ code ကို repeatable ဖြစ်အောင် စစ်ပြီး deploy လုပ်ဖို့ ပေါ်လာတာမျိုးပါ။

ပြီးရင် တစ်ဖက်ပြန်ကြည့်ရပါမယ်။ “ဒီ tool ကို ထည့်လိုက်ရင် ဘာအသစ်တွေ ခက်လာမလဲ” ဆိုတာပါ။ Managed service တစ်ခုက server maintenance ကို လျှော့ပေးနိုင်ပေမယ့် provider-specific limitation တွေ ရှိလာနိုင်ပါတယ်။ Distributed system က scale နဲ့ reliability တချို့ကို ကောင်းစေနိုင်ပေမယ့် network failure နဲ့ consistency လို ပြဿနာအသစ်တွေကို ယူလာနိုင်ပါတယ်။

ဒါကြောင့် technology ကို ကောင်းတယ်၊ မကောင်းဘူးလို့ အလွယ်တကူ မဆုံးဖြတ်သင့်ပါဘူး။ ဒီ problem အတွက် ဒီ complexity ကို ထည့်ရတာ တန်ရဲ့လားဆိုတာပဲ အရေးကြီးပါတယ်။