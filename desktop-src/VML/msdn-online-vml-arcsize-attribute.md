---
title: Attribut VML de VML
description: Attribut VML de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512326"
---
# <a name="vml-arcsize-attribute"></a>Attribut VML de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit la quantité d’arrondi pour un rectangle arrondi. En lecture/écriture. [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**S’applique à**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Syntaxe de balise**

<v : *élément* d’arcs = « *expression* » >

**Syntaxe du script**

*Element* . arcs = "*expression*"

*expression* = *Element*. arcs

**Remarques**

Définit les angles arrondis d’un rectangle à coins arrondis sous la forme d’un pourcentage de la plus petite dimension de la longueur et de la largeur d’un rectangle. 0% aurait des angles carrés et 100% formerait des angles circulaires. Un carré avec une valeur d' **interpolation** de 1,0 est un cercle. La valeur par défaut est 0,2 (20%).

*Attribut standard VML*

**Exemple**

Le rectangle arrondi est dessiné avec des angles étroits et arrondis.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 