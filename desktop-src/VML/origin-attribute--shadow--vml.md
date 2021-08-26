---
title: Origin, attribut (Shadow) (VML)
description: Origin, attribut (Shadow) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1776b0d8a857a3247543eae13d280d023585229d27c04a576420003ea53920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959179"
---
# <a name="origin-attribute-shadowvml"></a>Origin, attribut (Shadow) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le centre de l’ombre. En lecture/écriture. **VgVector2D**.

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : *élément* Origin = " *expression* " >

**Syntaxe du script**

*Element* . Origin = "*expression*"

*expression* = *élément*. Origin

**Remarques**

Paire de valeurs fractionnaires de la forme, comprise entre 50% et-50%. La valeur par défaut est 0,0.

*Attribut standard VML*

**Exemple**

L’ombre a une origine dont la valeur est inférieure à 20% et à 20% à droite de l’origine de la forme.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 