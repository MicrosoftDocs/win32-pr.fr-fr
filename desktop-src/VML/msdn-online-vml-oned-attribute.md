---
title: Attribut OnEd de VML
description: Attribut OnEd de VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316290"
---
# <a name="vml-oned-attribute"></a>Attribut OnEd de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si les poignées supplémentaires d’une forme sont masquées. En lecture/écriture. **VgTriState**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :ONED = " *expression* " >

**Remarques**

Masque toutes les poignées de forme à l’exception des poignées supérieure gauche et inférieure droite ; autrement dit, les mêmes Handles utilisés pour un segment de ligne droite. La valeur par défaut est **False**.

*Attribut extensions Microsoft Office*

**Exemple**

Toutes les poignées, sauf les poignées supérieure gauche et inférieure droite de la forme, sont masquées.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 