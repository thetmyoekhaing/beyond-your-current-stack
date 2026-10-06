# When You Don't Know, Go Looking

မသိတာကို မသိဘူးလို့ ဝန်ခံနိုင်တာက အရေးကြီးပါတယ်။ ဒါပေမယ့် အဲဒီနေရာမှာ ရပ်မနေဘဲ **စုံစမ်းတဲ့ process** တစ်ခု ရှိထားဖို့ ပိုအရေးကြီးပါတယ်။

## 01 — Problem
Problem ကို sentence တစ်ကြောင်းတည်းနဲ့ ရေးပါ။

ဥပမာ — “ဒီ background task ကြောင့် user request က နှေးနေတယ်။”

## 02 — Explore
ကိုယ်သုံးနေတဲ့ language နဲ့ problem ကို တွဲပြီးရှာပါ။

`<lang> <problem>`

ဒီအဆင့်မှာ tool တစ်ခုတည်းကို ရှာတာထက် solution space ကို အရင်ကြည့်တာက ပိုကောင်းပါတယ်။

## 03 — Compare
Repository တွေကို ကြည့်တဲ့အခါ slide မှာပြောထားတဲ့ အခြေခံ signal သုံးခုက —
- Stars
- Last commit date
- Open issue count

ဒါတွေက quality ကို အပြည့်အဝမဆုံးဖြတ်ပေးနိုင်ပေမယ့် project ရဲ့ activity နဲ့ adoption ကို အကြမ်းဖျင်းမြင်နိုင်စေပါတယ်။

## 04 — Choose
Hype နဲ့ blog post တွေထက် documentation ကို ဖတ်ပါ။ Tool က ကိုယ့် problem နဲ့ တကယ်ကိုက်မကိုက်ကို docs က ပိုရှင်းပြပေးနိုင်ပါတယ်။

## 05 — Learn
Source code အကုန်မဖတ်ပါနဲ့။ File တစ်ဖိုင်လောက်ကို ရွေးပြီး “ဒါဘယ်လိုအလုပ်လုပ်တာလဲ?” ဆိုတာ စူးစမ်းကြည့်ပါ။

## 06 — Build
အကြီးကြီး project မစပါနဲ့။ အလုပ်လုပ်တာကို သက်သေပြနိုင်မယ့် **smallest thing that runs** ကို အရင်တည်ဆောက်ပါ။

## အဓိကမေးခွန်းများ
- Has someone already solved this?
- What tools exist for this?
- What are the alternatives?
- Why do people actually use this?

ဒီလို investigation တစ်ခုက တစ်ခါတလေ ၁၀ မိနစ်ပဲ ကြာနိုင်ပါတယ်။ မစုံစမ်းဘဲ ကိုယ်တိုင် တစ်ပတ်လောက် မှားပြီး build လုပ်တာထက် အများကြီးသက်သာပါတယ်။

##

Developer ကောင်းတစ်ယောက်ဆိုတာ ဘယ်တော့မှ မပိတ်မိတဲ့သူမဟုတ်ပါဘူး။ မသိတဲ့အချိန်မှာ “ဘယ်လိုရှာရမလဲ” သိတဲ့သူပါ။

ပြဿနာတစ်ခုတက်လာရင် answer တစ်ခုတည်းကို တန်းရှာမယ့်အစား မေးခွန်းသေးသေးလေးတွေ ခွဲကြည့်လို့ရပါတယ်။ ဘာက fail ဖြစ်တာလဲ။ ဘာပြောင်းသွားတာလဲ။ ပြန် reproduce လုပ်လို့ရလား။ Local problem လား၊ external dependency လား။ Official documentation က ဘာပြောထားလဲ။ အခြားသူတွေ ဒီလိုပြဿနာ ကြုံဖူးလား။ Minimal example တစ်ခုနဲ့ ခွဲစမ်းလို့ရလား။

Search လုပ်တဲ့အခါ primary source ကို အရင်ကြည့်တာကောင်းပါတယ်။ Official documentation, source code, issue tracker, pull request နဲ့ discussion တွေက software က တကယ်ဘာလုပ်ဖို့ ရည်ရွယ်ထားလဲဆိုတာ နားလည်ဖို့ ပိုကောင်းပါတယ်။ Blog နဲ့ community post တွေကလည်း အသုံးဝင်ပါတယ်၊ ဒါပေမယ့် အဖြေကို verify ပြန်လုပ်သင့်ပါတယ်။

Experiment လုပ်ရင်လည်း သေးသေးလေးလုပ်ပါ။ Queue ကို လေ့လာချင်ရင် message တစ်ခု ပို့ကြည့်ပါ။ Database feature တစ်ခုကို စမ်းချင်ရင် database သေးသေးတစ်ခုနဲ့ စမ်းပါ။ Observability ကို နားလည်ချင်ရင် request တစ်ခုကို trace လုပ်ကြည့်ပါ။

“Technology X ကို သင်မယ်” ဆိုတာထက် “ဒီ problem ကို X က ဒီအခြေအနေမှာ ဖြေရှင်းပေးနိုင်လား” ဆိုတဲ့မေးခွန်းက ပိုအသုံးဝင်ပါတယ်။