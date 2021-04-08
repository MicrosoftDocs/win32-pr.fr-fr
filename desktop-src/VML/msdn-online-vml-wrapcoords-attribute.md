---
title: WrapCoords VML (attribut)
description: WrapCoords VML (attribut)
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727964"
---
# <a name="vml-wrapcoords-attribute"></a>WrapCoords VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit le polygone englobant qui entoure une forme. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :wrapcoords = " *expression* " >

**Remarques**

Décrit une liste de x et ycoordinates délimitée par des virgules ; autrement dit, « x1, y1, x2, Y2, x3, Y3,... » Cela est utilisé lorsque le texte est fortement enveloppé autour d’une forme. La valeur par défaut est **null** (une chaîne vide) jusqu’à ce que l’attribut **mso-Wrap-mode** soit défini sur **Elevé** ou **sur**.

*Attribut extensions Microsoft Office*

**Exemple**

La forme comporte un rectangle englobant de texte de retour de 5 unités plus grande que le tracé.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 