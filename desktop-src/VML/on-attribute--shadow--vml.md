---
title: On, attribut (Shadow) (VML)
description: On, attribut (Shadow) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda4d33fbd22d2a7913f13ae8ad874ba3240944f06303f020888aeaafaee88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345850"
---
# <a name="on-attribute-shadowvml"></a>On, attribut (Shadow) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Détermine si une ombre sera affichée. En lecture/écriture. **VgTriState**.

**S’applique à**

[Shadow](msdn-online-vml-shadow-element.md)

**Syntaxe de balise**

<v : *Element* on = " *expression* " >

**Syntaxe du script**

*Element* . on = "*expression*"

*expression* = *élément*. on

**Remarques**

Si la **valeur est true**, l’ombre est affichée. La valeur par défaut est **False**.

*Attribut standard VML*

**Exemple**

L’ombre s’affiche.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 