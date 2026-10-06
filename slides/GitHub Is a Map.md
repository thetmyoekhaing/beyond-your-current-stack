# GitHub Is a Map

GitHub ကို code သိမ်းတဲ့နေရာတစ်ခုတည်းလို မမြင်ဘဲ **software ecosystem ကို လေ့လာဖို့ map** တစ်ခုလို သုံးကြည့်နိုင်ပါတယ်။

## Repository တစ်ခုထဲမှာ ဘာတွေကြည့်မလဲ?

### README.md
Project က ဘာကြောင့်ရှိတာလဲ၊ ဘာလုပ်ပေးတာလဲဆိုတာ သိနိုင်ပါတယ်။

### /src
တကယ်တမ်း ဘယ်လို build လုပ်ထားလဲဆိုတာ ကြည့်နိုင်ပါတယ်။

### /docs
Project က ဘာတွေလုပ်နိုင်လဲ၊ ဘယ်လိုအသုံးပြုရမလဲဆိုတာ နားလည်နိုင်ပါတယ်။

### Issues
လက်ရှိဘာတွေ broken ဖြစ်နေလဲ၊ users/maintainers တွေ ဘာကို အရေးကြီးတယ်လို့ မြင်လဲ သိနိုင်ပါတယ်။

### Pull Requests
Code ပြောင်းတဲ့အခါ ဘာကြောင့် အဲဒီဆုံးဖြတ်ချက်ကို ချခဲ့လဲဆိုတာ ပိုမြင်နိုင်ပါတယ်။

### Releases
Project ဘယ်လို mature ဖြစ်လာလဲဆိုတာ ကြည့်နိုင်ပါတယ်။

## Slide မှာ အကြံပြုထားတဲ့ repo ၄ ခု

- `torvalds/linux` — အလွန်ကြီးမားတဲ့ system တစ်ခုကို ဘယ်လို navigate လုပ်နိုင်လဲ လေ့လာဖို့
- `pallets/flask` — အတော်လေးသေးတဲ့ codebase တစ်ခုကို အဆုံးထိ ဖတ်ကြည့်ဖို့
- `excalidraw/excalidraw` — real product တစ်ခုမှာ trade-off တွေ ဘယ်လိုပေါ်လာလဲ ကြည့်ဖို့
- `sindresorhus/awesome` — အသုံးဝင်တဲ့ lists တွေကို ဘယ်လို curate လုပ်လဲ ကြည့်ဖို့

## အဓိက shift

> “How do I build this?”
>
> ထက်
>
> “Who has already built this?”

လို့ အရင်မေးကြည့်ပါ။ ကိုယ့် problem ကို တစ်ယောက်ယောက်က ဖြေရှင်းပြီးသားဖြစ်နိုင်ပါတယ်။

##

GitHub ကို code သိမ်းတဲ့နေရာတစ်ခုလိုပဲ သုံးမယ်ဆိုရင် ရနိုင်တဲ့ information တော်တော်များများကို လွတ်သွားနိုင်ပါတယ်။ Repository တစ်ခုရဲ့ current code က အခုဘာရှိလဲဆိုတာ ပြပါတယ်။ Commit history, issue, pull request နဲ့ discussion တွေကတော့ ဘာကြောင့် ဒီလိုဖြစ်လာတာလဲဆိုတာ ပြပေးနိုင်ပါတယ်။

ထူးဆန်းနေတဲ့ abstraction တစ်ခုက production bug တစ်ခုကို ဖြေရှင်းဖို့ ထည့်ထားတာ ဖြစ်နိုင်ပါတယ်။ Code နှစ်နေရာမှာ တူနေတာက မကောင်းတဲ့ design မဟုတ်ဘဲ နှစ်ခုရဲ့ constraint မတူလို့ intentionally ခွဲထားတာလည်း ဖြစ်နိုင်ပါတယ်။ Compatibility code တစ်ခုက old users တွေအတွက် မဖျက်နိုင်သေးတာ ဖြစ်နိုင်ပါတယ်။

Repository အသစ်တစ်ခုကို ဖတ်မယ်ဆိုရင် README ကနေ စပြီး folder tree ကိုကြည့်၊ entry point တစ်ခုကိုရှာ၊ feature တစ်ခုကို အဆုံးထိလိုက်ကြည့်၊ tests ကိုဖတ်၊ ပြီးရင် issue နဲ့ pull request တွေကို ကြည့်လို့ရပါတယ်။ Repository တစ်ခုလုံးကို ခေါင်းထဲထည့်ဖို့ မလိုပါဘူး။ မေးခွန်းတစ်ခုနဲ့ ဝင်ပြီး အဖြေကို code ထဲမှာ လိုက်ရှာတာ ပိုလွယ်ပါတယ်။

Large repository တွေက scale, boundary, ownership နဲ့ collaboration ကို သင်ပေးပါတယ်။ Small repository တွေက implementation detail နဲ့ code path တစ်ခုလုံးကို နားလည်ဖို့ ကူညီပါတယ်။ နှစ်မျိုးလုံးက တန်ဖိုးရှိပါတယ်။ Repository တစ်ခုဟာ တခြား developer တွေ ချမှတ်ခဲ့တဲ့ engineering decision တွေကို code အနေနဲ့ ဖတ်နိုင်တဲ့ case study တစ်ခုလိုပါပဲ။