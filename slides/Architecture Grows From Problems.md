# Architecture Grows From Problems

Architecture က အစကတည်းက box တွေအများကြီးဆွဲပြီး တည်ဆောက်ရတာမဟုတ်ပါဘူး။ Application ကြီးလာတာနဲ့အမျှ **ပြဿနာတွေက architecture အသစ်တွေကို တောင်းဆိုလာတာ** ဖြစ်ပါတယ်။

## Phase 01 — One service. One database. It works.

အစမှာ application တစ်ခုနဲ့ database တစ်ခုလောက်နဲ့ပဲ အလုပ်လုပ်နိုင်ပါတယ်။ ဒီအချိန်မှာ cache, queue, worker, Kubernetes စတာတွေ မရှိလည်း ရပါတယ်။

“simple” ဖြစ်နေတာဟာ မကောင်းတာမဟုတ်ပါဘူး။ ပြဿနာမရှိသေးရင် ရိုးရှင်းတဲ့ architecture က အားသာချက်ဖြစ်နိုင်ပါတယ်။

## Phase 02 — Reads are slow. p95 is 800ms.

Database ကို request တိုင်း ထပ်ခါထပ်ခါ မေးနေရပြီး latency တက်လာရင် cache ထည့်ဖို့ အကြောင်းပြချက်ရှိလာပါတယ်။

`Database latency → Cache`

800ms ကနေ 40ms လောက်အထိ ကျသွားတယ်ဆိုရင် cache ထည့်ရတဲ့အကြောင်းရင်းကို တိုင်းတာချက်နဲ့ ရှင်းပြနိုင်ပါတယ်။

## Phase 03 — Emails block the request. Users wait.

Email ပို့တာလို background မှာလုပ်လို့ရတဲ့ အလုပ်တစ်ခုကြောင့် user request က စောင့်နေရတယ်ဆိုရင် queue နဲ့ worker ခွဲထုတ်နိုင်ပါတယ်။

`Heavy background tasks → Queue → Worker`

User ကို ချက်ချင်း response ပြန်ပေးပြီး slow work ကို နောက်ကွယ်မှာ ဆက်လုပ်စေနိုင်ပါတယ်။

## အဓိက takeaway

**Complexity should have a reason.**

Architecture ထဲကို box တစ်ခု ထပ်ထည့်တိုင်း “ဘာကြောင့်?” ဆိုတဲ့ sentence တစ်ကြောင်း ရှိသင့်ပါတယ်။ Problem မရှိဘဲ complexity ထည့်တာက engineering sophistication မဟုတ်ပါဘူး။

##

Architecture discussions should start with constraints rather than diagrams: latency, traffic volume, reliability, data size, deployment frequency, team size, security, cost, and failure tolerance.

The same application can reasonably have different architectures at different scales because its constraints are different.

### Avoid scale theatre

Designing for an imaginary future is a common source of unnecessary complexity. A team with ten users does not automatically need ten services, Kubernetes, multiple replicas, queues, and caches.

The better approach is to design for the problem you actually have while leaving sensible paths for growth.

### Measure before you add

“It's slow” is not enough. Where is it slow? Is the bottleneck CPU, database I/O, network latency, serialization, an external API, or lock contention? Measurements such as p95 latency, throughput, error rate, resource utilization, and queue depth turn architecture arguments into engineering arguments.

**Architecture should be explainable in terms of requirements and evidence.**
