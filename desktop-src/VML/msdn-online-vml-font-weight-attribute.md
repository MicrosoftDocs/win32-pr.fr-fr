---
title: Attribut Font-Weight VML
description: Attribut Font-Weight VML
ms.assetid: d7b2b0c5-b5cf-4e7d-bbca-c554d12bf97e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14dd5edb3fed869390edeff514471359162ee39fd1d78796af3d2a260c96bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754640"
---
# <a name="vml-font-weight-attribute"></a>Attribut Font-Weight VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit l’épaisseur des lettres de la police. En lecture/écriture. **Chaîne**.

**S’applique à**

[TextPath](msdn-online-vml-textpath-element.md)

**Syntaxe de balise**

<v : *Element* style = "font-weight : *expression* " >

**Syntaxe du script**

*Element* . style. FontWeight = "*expression*"

*expression* = *Element*. style. FontWeight

**Remarques**

Les valeurs sont les mêmes que les attributs de style HTML standard. Ces valeurs comprennent :



| Valeur   | Description                                                                 |
|---------|-----------------------------------------------------------------------------|
| normal  | Normal. Par défaut.                                                            |
| gras    | Gras.                                                                       |
| bolder  | Plus lourd que la normale.                                                        |
| lighter | Plus clair que la normale.                                                        |
| 100     | Au moins aussi clair que le poids de 200.                                        |
| 200     | Au moins aussi gras que le poids de 100 et au moins aussi clair que le poids de 300. |
| 300     | Au moins aussi gras que le poids de 200 et au moins aussi clair que le poids de 400. |
| 400     | Normal.                                                                     |
| 500     | Au moins aussi gras que le poids de 400 et au moins aussi clair que le poids de 600. |
| 600     | Au moins aussi gras que le poids de 500 et au moins aussi clair que le poids de 700. |
| 700     | Gras.                                                                       |
| 800     | Au moins aussi gras que le poids de 700 et au moins aussi clair que le poids de 900. |
| 900     | Au moins aussi gras que le poids de 800.                                         |



 

*Attribut standard VML*

**Exemple**

L’épaisseur de la police est en gras.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal bold 36pt Arial"/>
   </v:line>
```



 

 