---
description: 'Lors de la création d’une instance avec des objets incorporés, effectuez les tâches suivantes :'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Création d’objets incorporés
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464169"
---
# <a name="creating-embedded-objects"></a>Création d’objets incorporés

Lors de la création d’une instance avec des objets incorporés, effectuez les tâches suivantes :

-   Vous devez déclarer un objet incorporé comme fortement typé ou faiblement typé.

    Un objet fortement typé pointe vers un objet d’une classe spécifique et utilise le nom de la classe. Un objet faiblement typé pointe vers un objet d’une classe non spécifiée et utilise le mot clé **Object** . Les deux objets sont mappés au type de **VT \_ inconnu** .

-   Vous pouvez utiliser **null** pour la valeur par défaut des objets et chemins d’accès incorporés dans les initialisations et les déclarations.
-   Lors de l’incorporation d’un chemin d’accès à un objet, ne placez pas d’espace blanc entre les éléments du chemin d’accès incorporé. Par exemple, le chemin d’accès à l’objet « Class1Index = 3 ; » ne contient pas d’espace entre le nom de la propriété « Class1index » et la valeur assignée, qui est « 3 ».

La déclaration de classe suivante montre comment déclarer des objets incorporés fortement typés et faiblement typés.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

Les exemples suivants décrivent comment déclarer des objets incorporés dans une déclaration de classe.

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

L’exemple suivant décrit l’initialisation d’une propriété qui est un objet fortement typé et une autre propriété qui est un tableau d’objets faiblement typés.

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



