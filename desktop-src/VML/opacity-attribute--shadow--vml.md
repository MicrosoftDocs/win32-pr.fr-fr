---
title: Attribut Opacity (Shadow) (VML)
description: Attribut Opacity (Shadow) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43287a4bb6de9f2dd0d9d2b0af97d971314ab7e93ab2c4fae58b666ee1a94124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680619"
---
# <a name="opacity-attribute-shadowvml"></a>Attribut Opacity (Shadow) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine la transparence d’une ombre. En lecture/écriture. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : *Element* Opacity = " *expression* " >

**Syntaxe du script**

*Element* . Opacity = "*expression*"

*expression* = *Element*. Opacity

**Remarques**

La valeur par défaut est 1. La valeur 0 crée une ombre entièrement transparente.

*Attribut standard VML*

**Exemple**

La forme possède une ombre qui est transparente à 50%.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 