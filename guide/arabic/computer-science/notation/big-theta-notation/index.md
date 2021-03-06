---
title: Big Theta Notation
localeTitle: كبير ثيتا التدوين
---
## كبير ثيتا التدوين

تخبرنا أوميغا الكبيرة بالحد الأدنى لوقت تشغيل إحدى الدالات ، وتخبرنا Big O بالحد الأعلى. في كثير من الأحيان ، تكون مختلفة ولا يمكننا تقديم ضمان على وقت التشغيل - سوف تختلف بين الحدود والمدخلات. لكن ماذا يحدث عندما يكونان متشابهين؟ ثم يمكننا أن نمنح **ثيتا** (Θ) ملزمة - سوف تعمل وظيفتنا في ذلك الوقت ، بغض النظر عن المدخلات التي نقدمها. بشكل عام ، نرغب دائمًا في منح ثيتا مقيدًا إذا كان ذلك ممكنًا نظرًا لأنه أكثر الحدود دقة ودقة. إذا لم نتمكن من إعطاء ثيتا ملزمة ، فإن أفضل شيء ثاني هو أقصى حد ممكن.

لنأخذ على سبيل المثال وظيفة تبحث عن مصفوفة للقيمة 0:

```python
def containsZero(arr): #assume normal array of length n with no edge cases
  for num x in arr:
    if x == 0:
       return true
  return false
``` 

1.  ما هي أفضل حالة؟ حسنًا ، إذا كانت الصفيف الذي نوفره له 0 كقيمة أولى ، فسيستغرق ذلك وقتًا ثابتًا: Ω (1)
2.  ما هي أسوأ حالة؟ إذا كان المصفوفة لا تحتوي على 0 ، فسنقوم بتكرارها من خلال المصفوفة بأكملها: O (n)

لقد أعطيناها أوميغا و O ملزمة ، فماذا عن ثيتا؟ لا يمكننا اعطائها واحدة! اعتمادا على صفيف نعطيه ، سيكون وقت التشغيل في مكان ما بين الثابت والخطية.

دعونا نغير كودنا قليلا.

```python
def printNums(arr): #assume normal array of length n with no edge cases
  for num x in arr:
    print(x)
``` 

يمكنك التفكير في أفضل حالة وأسوأ حالة ؟؟ لا استطيع بصرف النظر عن المجموعة التي نوفرها ، يجب علينا التكرار من خلال كل قيمة في الصفيف. وبالتالي فإن الدالة ستستغرق وقتًا قصيرًا (Ω (n)) ، لكننا نعرف أيضًا أنها لن تستغرق أكثر من وقت n (O (n)). ماذا يعني هذا؟ سوف تأخذ **وظيفتنا بالضبط** وقت n: Θ (n).

إذا كانت الحدود مربكة ، فكر في الأمر على هذا النحو. لدينا 2 أرقام ، س و ص. يتم إعطاؤنا ذلك x <= y و y <= x. إذا كانت x أقل من أو تساوي y ، و y أقل من أو تساوي x ، فإن x يجب أن تساوي y!

إذا كنت على دراية بالقوائم المرتبطة ، فاختبر نفسك وفكر في أوقات التشغيل لكل واحدة من هذه الوظائف!

1.  احصل على
2.  إزالة
3.  إضافة

تصبح الأمور أكثر إثارة عندما تفكر في قائمة مرتبطة بشكل مزدوج!

#### معلومات اكثر:

https://www.khanacademy.org/computing/computer-science/algorithms/asymptotic-notation/a/big-big-theta-notation https://stackoverflow.com/questions/10376740/what-exactly-does-big-٪D3٪A8-notation-represent https://www.geeksforgeeks.org/analysis-of-algorithms-set-3asymptotic-notations/