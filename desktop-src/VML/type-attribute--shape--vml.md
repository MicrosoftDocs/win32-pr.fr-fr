---
title: Attribut type (Shape) (VML)
description: Attribut type (Shape) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031398"
---
# <a name="type-attribute-shapevml"></a>Attribut type (Shape) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une référence à l’ID d’un élément [Typedeforme](msdn-online-vml-shapetype-element.md) . En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

``` syntax
<v:
          element 
          type=" expression ">
```

**Syntaxe du script**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Remarques**

Si l’attribut de **type** fait référence à l’ID d’un élément **Typedeforme** , les remplissages, les tracés et les traits de **Typedeforme** sont utilisés comme modèles pour créer la forme. Les valeurs dérivées de **Typedeforme** peuvent être remplacées par des valeurs de forme individuelle.

S’il est utilisé dans les balises, la valeur de chaîne doit commencer par un symbole de signe dièse ( \# ).

**Attribut standard VML**

**Exemple**

Une forme **Typedeforme** est créée avec « MyType » comme ID.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Ensuite, si vous créez une forme à l’aide des valeurs **Typedeforme** , la forme aura les attributs du « MyType » **Typedeforme**; autrement dit, « shape01 » aura un remplissage rouge avec un trait bleu.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



Vous pouvez remplacer les valeurs héritées, par exemple en remplaçant la couleur par le vert.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Exemple d’attribut de type](/previous-versions/bb264099(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 