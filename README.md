# IIS
## Практична робота №2-3
## Мета-навчитись будувати семантичну мережу
## Варіант №13
## Завдання: Побудувати семантичну мережу правил гри у шашки
Звіт

1. Спочатку за допомогою онлайн редактора файлів [json editor online](http://www.jsoneditoronline.org/?id=94fdd7a32e99cbce3c24d301637a0362) використовуючи як приклад онтологію структури [primat.org](http://primat.org/demo/webowl/index.html#ontovibe) було створено свій файл з розширенням
json.

2. Для створення онтології я використала 18 класів "classCount" : 18, а також 20 зв'язків "axiomCount" : 20. В файлі я прописала назви всіх касів, а потім описала кожний класс окремо, де вказувала назву класу, його суб-клас (якщо вони в нього є) "subClasses" 
тобто ті класи які входять в мій клас, а також супер-клас (якщо він існує): "superClasses" в якому вказувала номер класу який буде виходити з щойно створенного класу.
Наступним кроком було оголошення всіх зв'язків між класами: "id" : "property". Після чого описала кожний зв'язок окремо де вказувала спочатку клас з якого виходить зв'язок, а потім клас в який він входить.

В результаті ми маємо наступний код:

{
  "_comment" : "Created with OWL2VOWL (version 0.2.0), http://vowl.visualdataweb.org",
  "namespace" : [ ],
  "header" : {
    "languages" : [ "IRI-based" ],
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl"
  },
    "metrics" : {
    "classCount" : 18,
    "datatypeCount" : 0,
    "objectPropertyCount" : 0,
    "datatypePropertyCount" : 0,
    "propertyCount" : 0,
    "nodeCount" : 18,
    "axiomCount" : 20,
    "individualCount" : 0
  },
  "class" : [ {
    "id" : "class1",
    "type" : "owl:Class"
  }, {
    "id" : "class2",
    "type" : "owl:Class"
  }, {
    "id" : "class3",
    "type" : "owl:Class"
  }, {
    "id" : "class4",
    "type" : "owl:Class"
  }, {
    "id" : "class5",
    "type" : "owl:Class"
  }, {
    "id" : "class6",
    "type" : "owl:Class"
  }, {
    "id" : "class7",
    "type" : "owl:Class"
  }, {
    "id" : "class8",
    "type" : "owl:Class"
  }, {
    "id" : "class9",
    "type" : "owl:Class"
  }, {
    "id" : "class10",
    "type" : "owl:Class"
  }, {
    "id" : "class11",
    "type" : "owl:Class"
  }, {
    "id" : "class12",
    "type" : "owl:Class"
  }, {
    "id" : "class13",
    "type" : "owl:Class"
  }, {
    "id" : "class14",
    "type" : "owl:Class"
  }, {
    "id" : "class15",
    "type" : "owl:Class"
  }, {
    "id" : "class16",
    "type" : "owl:Class"
  }, {
    "id" : "class17",
    "type" : "owl:Class"
  }, {
    "id" : "class18",
    "type" : "owl:Class"
  } ],
  "classAttribute" : [ {
    "id" : "class1",
    "label" : {
      "IRI-based" : "Шашки"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#шашки",
    "superClasses" : [ "class2" ],
    "instances" : 0
  }, {
    "id" : "class2",
    "label" : {
      "IRI-based" : "колір"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#колір",
    "subClasses" : ["class1"],
    "superClasses" : [ "class2", "class3"],
    "instances" : 0
  }, {
    "id" : "class3",
    "label" : {
      "IRI-based" : "білий"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#білий",
    "subClasses" : ["class2"],
    "superClasses" : [ "class5" ],
    "instances" : 0
  }, {
    "id" : "class4",
    "label" : {
      "IRI-based" : "чорний"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#чорний",
    "subClasses" : [ "class2" ],
    "superClasses" : [ "class6" ],
    "instances" : 0
  }, {
    "id" : "class5",
    "label" : {
      "IRI-based" : "ходимо перші"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#ходимо_перші",
    "subClasses" : ["class3"],
    "superClasses" : [ "class7" ],
    "instances" : 0
  }, {
    "id" : "class6",
    "label" : {
      "IRI-based" : "чекаємо поки білі походять"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#чекаємо",
    "subClasses" : ["class4"],
    "superClasses" : [ "class7" ],
    "instances" : 0
  }, {
    "id" : "class7",
    "label" : {
      "IRI-based" : "обираємо будь-яку шашку перед якою є вільна клітина і попереду немає суперника"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#обираємо_будь-яку_шашку",
    "subClasses" : ["class5","class6"],
    "superClasses" : [ "class8" ],
    "instances" : 0
  }, {
    "id" : "class8",
    "label" : {
      "IRI-based" : "Перевірити чи може будь-яка шашка  когось побити"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#download",
    "subClasses" : [ "class7"],
    "superClasses" : [ "class9","class13" ],
    "instances" : 0
  }, {
    "id" : "class9",
    "label" : {
      "IRI-based" : "ні"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#news",
    "subClasses" : [  "class8" ],
    "superClasses" : [ "class10" ],
    "instances" : 0
  }, {
    "id" : "class10",
    "label" : {
      "IRI-based" : "Ходимо шашкою проникаючи на поле суперника уникаючи бою"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#ходимо_шашкою",
    "subClasses" : [  "class9" ],
    "superClasses" : [ "class11" ],
    "instances" : 0
  }, {
    "id" : "class11",
    "label" : {
      "IRI-based" : "Якщо немає ходів мінімально віддалятись від початкової лінії"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#якщо_немає_ходів",
    "subClasses" : [ "class10" ],
    "superClasses" : [ "class12" ],
    "instances" : 0
  }, {
    "id" : "class12",
    "label" : {
      "IRI-based" : "Закінчення ходу"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#закінчення_ходу",
    "subClasses" : [ "class11", "class12", "class18"],
    "instances" : 0
  }, {
    "id" : "class13",
    "label" : {
      "IRI-based" : "так"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#так",
    "subClasses" : [  "class8" ],
    "superClasses" : [ "class14" ],
    "instances" : 0
  }, {
    "id" : "class14",
    "label" : {
      "IRI-based" : "Б'ємо, адже правила не дозволяють пропуску такого ходу"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#б'ємо",
    "subClasses" : [  "class13" ],
    "superClasses" : [ "class15" ],
    "instances" : 0
  }, {
    "id" : "class15",
    "label" : {
      "IRI-based" : "Перевірити чи можна ще бити"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#перевірити",
    "subClasses" : [  "class14" ],
    "superClasses" : [ "class16","class17" ],
    "instances" : 0
  }, {
    "id" : "class16",
    "label" : {
      "IRI-based" : "Так"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#Так",
    "subClasses" : [  "class15" ],
    "superClasses" : [ "class18"],
    "instances" : 0
  }, {
    "id" : "class17",
    "label" : {
      "IRI-based" : "Ні"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#ні",
    "subClasses" : [  "class15" ],
    "superClasses" : [ "class12"],
    "instances" : 0
  }, {
    "id" : "class18",
    "label" : {
      "IRI-based" : "Б'ємо, адже правила не дозволяють пропускати хід"
    },
    "iri" : "http://primat.org/demo/webowl/data/ontovibe.owl#б'ємо",
    "subClasses" : [  "class16" ],
    "superClasses" : [ "class12"],
    "instances" : 0
  } ],
  "property" : [ {
    "id" : "property1",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property2",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property3",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property4",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property5",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property6",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property7",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property8",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property9",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property10",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property11",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property12",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property13",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property14",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property15",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property16",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property17",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property18",
    "type" : "rdfs:SubClassOf"
  }, {
    "id" : "property19",
    "type" : "rdfs:SubClassOf"
  } , {
    "id" : "property20",
    "type" : "rdfs:SubClassOf"
  }],
  "propertyAttribute" : [ {
    "id" : "property1",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class1",
    "range" : "class2"
  }, {
    "id" : "property2",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class2",
    "range" : "class3"
  }, {
    "id" : "property3",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class2",
    "range" : "class4"
  }, {
    "id" : "property4",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class4",
    "range" : "class6"
  }, {
    "id" : "property5",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class3",
    "range" : "class5"
  }, {
    "id" : "property6",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class5",
    "range" : "class7"
  }, {
    "id" : "property7",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class6",
    "range" : "class7"
  }, {
    "id" : "property8",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class7",
    "range" : "class8"
  }, {
    "id" : "property9",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class8",
    "range" : "class9"
  }, {
    "id" : "property10",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class9",
    "range" : "class10"
  }, {
    "id" : "property11",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class10",
    "range" : "class11"
  }, {
    "id" : "property12",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class11",
    "range" : "class12"
  }, {
    "id" : "property13",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class8",
    "range" : "class13"
  }, {
    "id" : "property14",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class13",
    "range" : "class14"
  } , {
    "id" : "property15",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class14",
    "range" : "class15"
  }, {
    "id" : "property16",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class15",
    "range" : "class16"
  }, {
    "id" : "property17",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class15",
    "range" : "class17"
  }, {
    "id" : "property18",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class17",
    "range" : "class12"
  }, {
    "id" : "property19",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class16",
    "range" : "class18"
  }, {
    "id" : "property20",
    "label" : {
      "IRI-based" : "Subclass Of"
    },
    "domain" : "class18",
    "range" : "class12"
  }]
}

3. Після цього зберегаємо цей файл і відкриваємо його в [онлайн програмі](http://primat.org/demo/webowl/index.html#file=ontovibe (1).json)
