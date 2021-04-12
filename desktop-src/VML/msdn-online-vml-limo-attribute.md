---
title: Limo VML (attribut)
description: Limo VML (attribut)
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a364aebfc2384ac9e19c9dc5f2f0ae52f09228a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382019"
---
# <a name="vml-limo-attribute"></a>Limo VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

 