# hanguel-jamo-analyzer

### [HenryJeong's Blog](http://jjeong.tistory.com)

*  HanguelJamoMorphTokenizer 사용법

```{.java}
public static void main(String args[]) {
    String query = "Nike 청바지";
    HanguelJamoMorphTokenizer tokenizer = new HanguelJamoMorphTokenizer();

    String chosung = tokenizer.tokenizer(query, HanguelJamoMorphTokenizer.JAMO.CHOSUNG);
    String jungsung = tokenizer.tokenizer(query, HanguelJamoMorphTokenizer.JAMO.JUNGSUNG);
    String jongsung = tokenizer.tokenizer(query, HanguelJamoMorphTokenizer.JAMO.JONGSUNG);

    System.out.println("원문 : [" + query + "]");
    System.out.println("초성 : [" + chosung + "]");
    System.out.println("중성 : [" + jungsung + "]");
    System.out.println("종성 : [" + jongsung + "]");
  }
```

* 실행 결과
```
원문 : [Nike 청바지]
초성 : [Nikeㅊㅂㅈ]
중성 : [Nikeㅓㅏㅣ]
종성 : [Nikeㅇ  ]
```