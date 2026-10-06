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

Architecture ကို စဉ်းစားတဲ့အခါ diagram ကို အရင်မဆွဲဘဲ constraint ကို အရင်ကြည့်တာ ပိုမှန်ပါတယ်။ Latency ဘယ်လောက်လိုလဲ၊ traffic ဘယ်လောက်ရှိလဲ၊ reliability ဘယ်လောက်လိုလဲ၊ data ဘယ်လောက်ကြီးလဲ၊ team က ဘယ်လောက်ရှိလဲ၊ security နဲ့ cost requirement ဘယ်လိုရှိလဲဆိုတာတွေက architecture ကို သတ်မှတ်ပေးပါတယ်။

Application တစ်ခုတည်းတောင် user ၁၀ ယောက်ရှိတဲ့အချိန်နဲ့ user သန်းချီလာတဲ့အချိန် architecture မတူနိုင်ပါတယ်။ ဒါဟာ အစက architecture မကောင်းလို့ မဟုတ်ဘဲ problem ရဲ့ constraint ပြောင်းသွားလို့ပါ။

တစ်ခါတလေ future ကိုကြိုတွေးပြီး system ကို အရမ်းကြီးဆောက်မိတတ်ပါတယ်။ User မရှိသေးခင် service ၁၀ ခုခွဲတာ၊ Kubernetes ထည့်တာ၊ queue တွေ၊ cache တွေ၊ replica တွေ အများကြီးထားတာက impressive လို့ ထင်ရနိုင်ပေမယ့် operational cost ကိုပါ တိုးစေပါတယ်။

“System က slow ဖြစ်နေတယ်” ဆိုတာလည်း architecture ပြောင်းဖို့ လုံလောက်တဲ့ evidence မဟုတ်သေးပါဘူး။ ဘယ်နေရာမှာ slow ဖြစ်တာလဲ၊ database လား၊ network လား၊ CPU လား၊ external API လားဆိုတာ တိုင်းရပါမယ်။ p95 latency, throughput, error rate, resource usage, queue depth လို metric တွေက “ထင်တယ်” ဆိုတာကို “တိုင်းထားတယ်” ဖြစ်အောင် ပြောင်းပေးနိုင်ပါတယ်။

Architecture ထဲမှာ component တစ်ခု ထပ်ထည့်တိုင်း “ဘာကြောင့်?” ဆိုတဲ့အဖြေ ရှိသင့်ပါတယ်။ Problem နဲ့ evidence မရှိဘဲ complexity တိုးတာက engineering maturity မဟုတ်ပါဘူး။