{% case page.lang %}
  {% when "python" %}
  {% else %}
![My helpful screenshot](/assets/firefox-console-729.png)
{% endcase %}
बात 1919 की है जब श्रीनिवास रामानुजन लंदन में थे। जी. एच. हार्डी उनसे मिलने एक टैक्सी से गये जिसका नंबर 1729 था। बातचीत में उन्होंने रामानुजन से कहा कि यह संख्या बड़ी साधारण सी है, कहीं किसी बुरे वक्त की ओर तो इशारा नहीं करती। "नहीं", रामानुजन बोले, "यह तो बड़ी मजेदार संख्या है; यह सबसे छोटी संख्या है जिसे दो संख्याओं के घनों को जोड़कर दो अलग-अलग तरीकों से बनाया जा सकता है।"

आइये, हम भी कंप्यूटर जी के साथ जावास्क्रिप्ट में बात करते-करते ऐसी ही मजेदार संख्याएं ढूंढें।

<details markdown="1">
<summary>कंप्यूटर जी पर फायरफॉक्स ब्राउज़र खोलें, Ctrl Shift K एक साथ दबाएं, और गणित का कोई सवाल टाईप करें। कंप्यूटर जी आपके सवाल का हल निकाल कर आपको देंगे। यह काम एक साधारण कैलकुलेटर पर भी हो जाएगा। या शायद आप अपने मन में ही इसे हल कर लें।</summary>

{% case page.lang %}
  {% when "python" %}
```python
>>> 9 * 9 * 9
729
```
  {% else %}
```javascript
>> 9 * 9 * 9;
729
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>1. 1 का 0 से भाग देकर देखें क्या आता है? </summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> 1/0
```
  {% else %}
```javascript
>> 1/0;
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>
कंप्यूटर जी को आप और भी बहुत से काम बता सकते हैं। आप कंप्यूटर जी को कह सकते हैं कि दिये गये नाम की एक जगह बनाएं और वहां हल को संभाल कर रख लें।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> cube9 = 729
```
  {% else %}
```javascript
>> let cube9 = 729;
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>
जिससे जरूरत पड़ने पर आप हल याद करने के बजाय उसका नाम उपयोग कर सकें।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> cube9
729
```
  {% else %}
```javascript
>> cube9;
729
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>
किसी नये हल को नये नाम की जगह बना कर वहां रख सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> cube10 = 1000
>>> cube10
1000
```
  {% else %}
```javascript
>> let cube10 = 1000;
>> cube10;
1000
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>
और बाद में उन हलों को लिखने के बजाय उनके नामों से ही नये सवालों का हल निकाल सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> cube9 + cube10
1729
```
  {% else %}
```javascript
>> cube9 + cube10;
1729
```
{% endcase %}
</details>
<br />
किसी संख्या को खुद से तीन बार गुणा करने से उस संख्या का घन निकलता है, जैसे 10 का घन 1000 है। यदि हमें किसी नयी संख्या जैसे कि 12 का घन निकालना हो तो फिर 12 * 12 * 12 लिखना होगा। क्या ऐसा हो सकता है कि हम कंप्यूटर जी को सवाल का हल निकालने का तरीका ही याद करा दें? 

<details markdown="1">
<summary>
कंप्यूटर जी के साथ हम अपना काम और भी कम कर सकते हैं। हम उन्हें कह सकते हैं कि दिये गये नाम की एक जगह बनाएं जहां हल निकालने के तरीके को ही संभाल कर रख लें>
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> def cube(n): 
...     return n * n * n
```
  {% else %}
```javascript
>> let cube = function (n) {
    return n * n * n;
}
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>
ऐसा करने से हमने एक function बना दिया है। अब वह काम करने के लिये बस उस काम का नाम ही काफी है, क्योंकि हमने कंप्यूटर जी को उस नाम का काम ही याद करा दिया है। अब हमारे पास कुछ वैसी ही मशीन बन गई है जिसमें जो सिक्का डालेंगे उसी के अनुसार वो आपका काम करेगी। अब हम अन्य सवालों का हल करा सकते हैं जिनमें वही तरीका काम आता है। 
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> cube(9)
729
>>> cube(10)
1000
>>> cube(9) + cube(10)
1729
>>> cube(8) + cube(11)
1842
```
  {% else %}
```javascript
>> cube(9);
729
>> cube(10);
1000
>> cube(9) + cube(10);
1729
>> cube(8) + cube(11);
1842
```
{% endcase %}
</details>
<br />
<details markdown="1">
<summary>
क्या और कोई संख्याऐं हैं जिन्हें cube(?) + cube(?) करने पर 1729 आता हो? कुछ अलग-अलग संख्याओं के साथ आज़माएं यदि 1729 आ जाये।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> cube(7) + cube(12)
```
  {% else %}
```javascript
>> cube(7) + cube(12)
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
 sumCubes नाम की एक जगह बनाएं जो दी गई दो संख्याओं को खुद से तीन बार गुणा करके जोड़ कर बताए।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
def sumCubes (a, b):
...    ?
>>> sumCubes(2, 3) 
35
```
  {% else %}
```javascript
let sumCubes = function(a, b) {
?
}
>> sumCubes(2, 3) 
35
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
यदि हमें कंप्यूटर जी से कुछ ढूंढने का काम कराना हो तो कंप्यूटर जी के पास यह पता करने का तरीका होना चाहिये कि वह चीज़ उन्हें मिल गई। कंप्यूटर जी के पास ऐसा तरीका है बस आपको उन्हें बताना होगा जांच क्या करनी है।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> if cube(12) + cube(1) == 1729: 
...     print('sum of 12 cubed and 1 cubed is 1729')
```
  {% else %}
```javascript
>> if (cube(12) + cube(1) == 1729) {
    console.log('sum of 12 cubed and 1 cubed is 1729');
} 
```
{% endcase %}
</details><br/>
<details markdown="1">
<summary>
और जांच के सफल या असफल होने पर अलग-अलग काम कर सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> if cube(13) + cube(0) != 1729:
...     print('13 cubed is not 1729')
... else:
...     print('13 cubed is 1729')
```
  {% else %}
```javascript
if (cube(13) + cube(0) != 1729) {
    console.log('13 cubed is not 1729');
} else {
    console.log('13 cubed is 1729');
}
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
 checkSumOfCubes नाम की एक जगह बनाएं जो दी गई दो संख्याओं के खुद से गुणा कर जोड़ कर देखे कि 1729 आता है या नहीं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> def checkSumOfCubes(a, b):
...     if cube(a) + cube(b) == 1729:
...         return ?
...     else:
...         return ?
>>> checkSumOfCubes(1, 11)
true
>>> checkSumOfCubes(2, 10)
false
```
  {% else %}
```javascript
>> let checkSumOfCubes = function(a, b) {
>> if (cube(a) + cube(b) == 1729) {
        return ?;
    } else {
        return ?;
    }
}
>> checkSumOfCubes(1, 11)
true
>> checkSumOfCubes(2, 10)
false
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
किसी काम को बार-बार कराने के लिये हम उस काम को बार-बार लिख सकते हैं। 
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> print('जय हो!')
जय हो!
>>> print('जय हो!')
जय हो!
>>> print('जय हो!')
जय हो!
```
  {% else %}
```javascript
>> console.log('जय हो!');
जय हो!
>> console.log('जय हो!');
जय हो!
>> console.log('जय हो!');
जय हो!
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
या कंप्यूटर जी को बता सकते हैं कि इस एक काम को हमेशा करते रहें।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> while (true):
...     print('जय हो!')
```
  {% else %}
```javascript
>> while (true) {
    console.log('जय हो!');
}
```
{% endcase %}
</details>
<br/>

पर कंप्यूटर जी अगर हमेशा एक ही काम करते रहे तो हम उनसे और कोई काम नहीं करा पायेंगे। हो सकता है कि उन्हें रोकना भी मुश्किल हो जाए।

<details markdown="1">
<summary>
 इसको चला कर देखें क्या होता है।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> n = 0

>>> n = n+1
>>> print(n)

>>> n = n+1
>>> print(n)

...
```
  {% else %}
```javascript
>> let n = 0;

>> n = n+1;
>> console.log(n);

>> n = n+1;
>> console.log(n)

...
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary> पिछले सवाल में जो काम बार-बार हो रहा है उसे while से कैसे कराएंगे
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> n = 0
>>> while (true):
...    ?
```
  {% else %}
```javascript
>> let n = 0;
>> while (true) {
    ?
}
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
 इस सवाल में जो काम बार-बार हो रहा है उसे while से कैसे कराएंगे।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> n = 0
>>> product = 1

>>> n = n+1
>>> product = product * 10
>>> print(n)

>>> n = n+1
>>> product = product * 10
>>> print(n)
```
  {% else %}
```javascript
>> let n = 0;
>> let product = 1;

>> n = n+1;
>> product = product * 10;
>> console.log(n);

>> n = n+1;
>> product = product * 10
>> console.log(n)
```
{% endcase %}
</details>
<br/>



<details markdown="1">
<summary>
किसी काम को हमेशा करते रहने कि बजाय हम कंप्यूटर जी को हम बता सकते हैं कि काम को दोहराने से पहले जांच कर लें कि काम को आगे करना भी है या नहीं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> n = 0
>>> while n < 10:
...    print(n)
...    n = n+1
```
  {% else %}
```javascript
>> let n = 0;
>> while (n < 10) {
    console.log(n);
    n = n+1;
}
```
{% endcase %}
</details>
<br/>



यदि हमें किसी संख्या को खुद से ही 100 बार गुणा करना हो तो कैसे करेंगे? 



<details markdown="1">
<summary>
यदि हमें एक जैसा काम कई चीज़ों पर दोहराना हो तो उन सबको नए नाम देने होंगे। इससे अच्छा होगा कि हम उन चीज़ों की एक सूची बना कर कंप्यूटर जी को उसे संभाल कर रखने के लिये कहें।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> greetings = ['सलाम', 'नमस्ते', 'हैलो']
>>> fib = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
```
  {% else %}
```javascript
>> let greetings = ['सलाम', 'नमस्ते', 'हैलो'];
>> let fib = [1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89];
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
अब हम कंप्यूटर जो को सूची की पहली चीज़ पर कुछ करने के लिये कह सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> print(names[0])
सलाम
```
  {% else %}
```javascript
>> console.log(names[0]);
सलाम
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
सूची की दूसरी चीज़ पर कुछ करने के लिये कह सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> print(names[1])
सलाम
```
  {% else %}
```javascript
>> console.log(names[1]);
सलाम
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
सूची में कितनी चीज़ें हैं पता कर सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> print(len(names))
3
```
  {% else %}
```javascript
>> console.log(names.length);
3
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
सूची की आखरी चीज़ पर कुछ करने के लिये कह सकते हं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
print(names[len(names) - 1])
हैलो
```
  {% else %}
```javascript
console.log(names[names.length-1]);
हैलो
```
{% endcase %}
</details>
<br/>


यदि हमें 1 से 100 तक की संख्याओं की सूची बनानी हो तो कैसे बनाएंगे?
<details markdown="1">
<summary>
numbersUpto नाम की एक जगह बनाएं जो 1 से लेकर दी गई संख्या तक की संख्याओं की एक सूची बना कर दे।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> define numbersUpto(start, end):
...     numbers = []
...     while start <= end: 
...         ?
>>> print(numbersUpto(10))
```
  {% else %}
```javascript
>> let numbersUpto = function(start, end) {
    let numbers = [];
    while (start <= end) {
        ?
    }   
}
>> console.log(numbersUpto(10));
```
{% endcase %}
</details>
<br/>



<details markdown="1">
<summary>
हम सूची में नई चीज जोड़ सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> greetings.push('सत् श्री अकाल')
>>> greetings.push('सत् श्री अकाल')
>>> print(len(greetings));
5
>>> print(greetings[3]);
सत् श्री अकाल
>>> print(greetings[4]);
सत् श्री अकाल
```
  {% else %}
```javascript
>> greetings.push('सत् स्री अकाल');
>> greetings.push('सत् श्री अकाल');
>> console.log(greetings.length);
5
>> console.log(greetings[3]);
सत् श्री अकाल
>> console.log(greetings[4]);
सत् श्री अकाल
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
या सूची की सारी चीज़ों पर कुछ करने के लिये कह सकते हैं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> for item in greetings:
...     print(item)
```
  {% else %}
```javascript
>> greetings.forEach(function(item, index, array) {
    console.log(item, index);
});
```
{% endcase %}
</details>
<br/>


<details markdown="1">
<summary>
 इसको चला कर देखें क्या आता है
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> for item1 in greetings:
...     for item2 in greetings:
...         print(item1, item2)
```
  {% else %}
```javascript
>> greetings.forEach(function(item1, index1, array1) {
    greetings.forEach(function(item2, index2, array2) {
        console.log(item1, item2);
    });
});
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
पिछले सवाल में कुछ लाईनें आती हैं जिनकी शायद हमें जरूरत ना हो, यदि हमें उनको हटाना हो तो क्या कर सकते हं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> for item1 in greetings:
...     for item2 in greetings:
...         if ?:
...             print(item1, item2)
```
  {% else %}
```javascript
>> greetings.forEach(function(item1, index1, array1) {
    greetings.forEach(function(item2, index2, array2) {
        if (?) {
            console.log(item1, item2);
        }
    });
});
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
हम सूची में पता लगा सकते हैं कि कोई चीज़ कहां पर है।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> print(greetings.index('सलाम'))
0
```
  {% else %}
```javascript
>> console.log(greetings.indexOf('सलाम'));
0
>> console.log(greetings.indexOf('अलविदा'));
-1
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
1 से 11 तक की संख्याओं को खुद से तीन बार गुणा करके एक सूची बनाएं।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> listOfNos = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]
>>> listOfCubes = []
>>> for item in listOfNos:
...     listOfCubes.append(?)
```
  {% else %}
```javascript
>>  let listOfNos = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11];
>>  let listOfCubes = [];
>>  listOfNos.forEach(function(item, index, array) {
        listOfCubes.push(?);
    });
```
{% endcase %}
</details>
<br/>
<details markdown="1">
<summary>
getListOfCubes नाम की एक जगह बनाएं जो दी गई संख्या तक की सारी संख्याओं के घनों की एक सूची बना कर दे
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>> def getListOfCubes(n):
...    ?
>> list = getListOfCubes(11)
>> print(list[len(list) - 1]);
1729
```
  {% else %}
```javascript
>> let getListOfCubes = function(n) {
    ?
}
>> let list = getListOfCubes(11);
>> console.log(list[list.length-1]);
1729
```
{% endcase %}
</details>
<br/>


<details markdown="1">
<summary>
यह एक function है जो हमें 9999 तक की सभी ऐसी संख्याएं बता देता है जो 2 संख्याओं के घनों से बनती हैं। 
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> def taxiNos():
...     list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 
...             12, 13, 14, 15, 16, 17, 18, 19, 20, 21];
...     nos = [];
...     for item1 in list:
...         for item2 in list:
...             sum = item1 * item1 * item1 + item2 * item2 * item2
...             // यदि sum चार अंकों तक का ही है और अभी तक नहीं मिला है
...             if sum <= 9999 && nos.indexOf(sum) == -1: 
...                 nos.append(sum)
...     return nos
```
  {% else %}
```javascript
>> let taxiNos = function() {
    let list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 
            12, 13, 14, 15, 16, 17, 18, 19, 20, 21];
    let nos = [];
    list.forEach(function(item1, index1, array1) {
        list.forEach(function(item2, index2, array2) {
            let sum = item1 * item1 * item1 + item2 * item2 * item2;
            // यदि sum चार अंकों तक का ही है और अभी तक नहीं मिला है
            if (sum <= 9999 && nos.indexOf(sum) == -1) {
                nos.push(sum);
            }
        });
    });
    return nos;
}
```
{% endcase %}
</details>
<br/>

<details markdown="1">
<summary>
Taxicab(n) नाम का एक function बनाएं जो वो सबसे छोटी संख्या बताए जो n अलग-अलग तरीकों से 2 संख्याओं के घनों को जोड़कर बनती है।
</summary>
{% case page.lang %}
  {% when "python" %}
```python
>>> def Taxicab(n):
...     ?
>> Taxicab(2)
1729
```
  {% else %}
```javascript
>> let Taxicab = function(n) {
       ?
}
>> Taxicab(2)
1729
```
{% endcase %}
</details>
<br/>

श्रीनिवास रामानुजन ऐसे सवाल बिना कंप्यूटर जी के, अपने मन में ही हल कर लेते थे। अच्छा है हमारे साथ कंप्यूटर जी हैं।

<details markdown="1">
<summary>
और जानने के लिये आप नीचे दी गयी या अन्य ऐसी वेबसाईट देख सकते हैं।
</summary>
* स्ट्रक्चर एंड इंटरप्रेटेशन ऑफ कंप्यूटर प्रोग्राम्स - <https://mitpress.mit.edu/sites/default/files/sicp/full-text/book/book.html>
* जावास्क्रिप्ट एम डी एन - <https://developer.mozilla.org/en-US/docs/Web/JavaScript>
* Taxicab number - <https://en.wikipedia.org/wiki/Taxicab_number>
* खान एकेडमी फ्री ऑनलाईन कोर्स, पाठ और अभ्यास - <https://www.khanacademy.org>
* LeetCode - दुनिया का अग्रणी ऑनलाईन प्रोग्रामिंग सीखने का प्लैटफॉर्म - <https://www.leetcode.com>
</details>
