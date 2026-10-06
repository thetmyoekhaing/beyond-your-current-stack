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

## Deeper: Investigation Is an Engineering Skill

Experienced developers are not people who never get stuck. They are often people who are better at turning “I'm stuck” into useful questions.

Ask: What exactly failed? What changed? Can I reproduce it? Is it local or external? What does the official documentation say? Has someone reported the same behavior? Can I reduce it to a tiny example?

### Prefer primary evidence

A useful investigation order is often official documentation → source code → issue tracker → pull requests/discussions → reputable technical articles → community posts. Community knowledge can be excellent, but primary sources help verify what the software actually promises.

### Make experiments tiny

If you are evaluating a queue, send one message. If you are evaluating a database feature, create one small database. If you are evaluating observability, trace one request. The experiment should answer one question.

That turns “learn technology X” into “can X solve this specific problem under these conditions?”
