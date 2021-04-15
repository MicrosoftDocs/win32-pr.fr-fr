---
title: MiterLimit VML (attribut)
description: MiterLimit VML (attribut)
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463302"
---
# <a name="vml-miterlimit-attribute"></a>MiterLimit VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le lissage de l’articulation mitre. En lecture/écriture. **VgNumber**.

**S’applique à**

[Stroke](msdn-online-vml-stroke-element.md)

**Syntaxe de balise**

<v : *Element* MiterLimit = " *expression* " >

**Syntaxe du script**

*Element* . MiterLimit = "*expression*"

*expression* = *élément*. MiterLimit

**Remarques**

Distance maximale entre le point interne et le point externe d’une jointure. Ce nombre est un multiple de l’épaisseur de la ligne.

La valeur par défaut est 8.

*Attribut standard VML*

**Exemple**

Les jointures sur la polyligne sont mitres avec une limite de 10, c’est-à-dire 5 fois 2 points.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 