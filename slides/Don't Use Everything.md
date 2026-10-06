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

Technology choices depend on workload, team knowledge, ecosystem maturity, operational cost, deployment environment, performance, reliability, and maintenance horizon. A technically excellent tool can still be the wrong choice for a particular team.

Every abstraction has a cost. A framework can make common cases easy while hiding behavior you may need to understand during debugging. A managed service removes infrastructure work while potentially adding provider-specific constraints.

### Prefer reversible decisions early

Young projects benefit from decisions that are easy to change. A simple database, basic worker, or single-machine deployment can be a perfectly good starting point. As evidence accumulates, specialized infrastructure can be introduced.

This is not anti-technology. It is **pro-evidence**. Use powerful tools when the problem gives you a reason to pay their cost.
