---
title: Attribut rempli VML
description: Attribut rempli VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7053263f989dbbef163e04ca19e28afa882d20347b103c97cf2db3be4b8d25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346603"
---
# <a name="vml-filled-attribute"></a>Attribut rempli VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si le tracé fermé est rempli. En lecture/écriture. **VgTriState**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* rempli = " *expression* " >

**Syntaxe du script**

*Element* . refilled = "*expression*"

*expression* = *élément*. rempli

**Remarques**

La valeur est dupliquée à partir de l’attribut **on** de l’élément [Fill](msdn-online-vml-fill-element.md) .

*Attribut standard VML*

**Exemple**

Le tracé de la forme est rempli.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemple d’attribut rempli](/previous-versions/bb229669(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 