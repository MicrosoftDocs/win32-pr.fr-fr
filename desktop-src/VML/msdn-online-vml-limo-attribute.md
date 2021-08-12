---
title: Limo VML (attribut)
description: Limo VML (attribut)
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598309"
---
# <a name="vml-limo-attribute"></a>Limo VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit un point d’étirement sur le tracé. En lecture/écriture. **Vector2d**.

**S’applique à**

[Chemin d’accès](msdn-online-vml-path-element.md)

**Syntaxe de balise**

<v : *Element* Limo = " *expression* " >

**Syntaxe du script**

*Element* . Limo = "*expression*"

*expression* = *élément*. Limo

**Remarques**

La valeur par défaut est « 0 0 ». Les étirements Limo sont des points sur le bord d’une forme qui définissent où et comment une forme peut être étirée par un utilisateur dans un éditeur graphique.

*Attribut standard VML*

**Exemple**

Un point d’étirement de Limo est défini à mi-chemin le long de la ligne horizontale.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 