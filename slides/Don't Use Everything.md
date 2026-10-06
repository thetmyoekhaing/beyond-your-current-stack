# Don't Use Everything

## Popularity Driven vs Problem Driven

Technology တစ်ခု popular ဖြစ်နေတယ်ဆိုတာနဲ့ ကိုယ့် project ထဲမှာ ထည့်သုံးရမယ်လို့ မဆိုလိုပါဘူး။

### Popularity driven
> “ဒီ technology က trend ဖြစ်နေတယ်။ သုံးသင့်တယ်။”

ဒီလိုစဉ်းစားရင် technology က problem ကို ဆုံးဖြတ်ပေးသွားနိုင်ပါတယ်။

### Problem driven
> “ကျွန်တော်တို့မှာ ဒီ problem ရှိတယ်။ ဘယ် solution တွေရှိလဲ၊ trade-off တွေက ဘာတွေလဲ?”

ဒီနည်းမှာ problem ကနေစပြီး toolbox ထဲက သင့်တော်တာကို ရွေးပါတယ်။

## Slide ထဲက example သုံးခု

### “We should move to Kubernetes.”
Service တစ်ခုတည်းရှိနေပြီး Kubernetes သုံးလိုက်ရင် application ထက် control plane နဲ့ operational complexity က ပိုကြီးလာနိုင်ပါတယ်။

### “We need real-time. Add Kafka.”
တစ်နေ့ event 50 ခုလောက်ပဲရှိနေသေးရင် Kafka က problem ထက်ပိုကြီးတဲ့ solution ဖြစ်နိုင်ပါတယ်။

### “The DB is slow. Add a cache.”
ဒီတစ်ခုကတော့ measurement ရှိပါတယ် — `800ms → 40ms`။ ဘာကြောင့် cache ထည့်တယ်ဆိုတာကို data နဲ့ ရှင်းပြနိုင်ပါတယ်။

## အဓိက takeaway

**Know the toolbox. Choose the right tool.**

Technology အသစ်ကို သိထားတာနဲ့ technology အသစ်တိုင်းကို သုံးရမယ်ဆိုတာ မတူပါဘူး။ Engineering judgment ဆိုတာလည်း ဒီလို trade-off တွေကို နားလည်ပြီး ဆုံးဖြတ်နိုင်ခြင်းပါ။

##

Technology ရွေးတဲ့အခါ “အကောင်းဆုံး tool” ဆိုတာ တစ်ခုတည်း မရှိပါဘူး။ Workload, team ရဲ့အတွေ့အကြုံ, ecosystem, operational cost, deployment environment, performance, reliability နဲ့ project ရဲ့သက်တမ်းပေါ်မူတည်ပြီး အဖြေက ပြောင်းနိုင်ပါတယ်။

Framework တစ်ခုက development ကို မြန်စေနိုင်ပါတယ်။ Managed database က server ထိန်းသိမ်းရတာကို လျှော့ပေးနိုင်ပါတယ်။ Container platform က deployment ကို စံချိန်တင်ပေးနိုင်ပါတယ်။ ဒါပေမယ့် abstraction အောက်မှာ ဘာဖြစ်နေတယ်ဆိုတာ မသိရင် failure ဖြစ်တဲ့အချိန် debug လုပ်ရခက်နိုင်ပါတယ်။ ဒါကြောင့် foundation ကို သိထားတာက tool အများကြီးသုံးတတ်တာထက် တစ်ခါတလေ ပိုအသုံးဝင်ပါတယ်။

Project အသစ်စတဲ့အချိန်မှာ ပြန်ပြောင်းရလွယ်တဲ့ decision တွေကို ရွေးတာကောင်းပါတယ်။ User နည်းနေသေးရင် simple database တစ်ခုနဲ့ စနိုင်ပါတယ်။ Background job နည်းနည်းပဲရှိရင် worker တစ်ခုနဲ့ စနိုင်ပါတယ်။ Deployment ကို server တစ်လုံးနဲ့ စလို့ရနိုင်ပါတယ်။ တကယ်လိုအပ်လာမှ specialized infrastructure ထည့်ပါ။

ဒါဟာ technology မသုံးချင်တာ မဟုတ်ပါဘူး။ Technology ရဲ့ cost ကို problem က တောင်းဆိုတဲ့အချိန်မှ ပေးချင်တာပါ။