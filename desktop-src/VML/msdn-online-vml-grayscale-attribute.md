---
title: Attribut de nuances de gris VML
description: Attribut de nuances de gris VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382168"
---
# <a name="vml-grayscale-attribute"></a>Attribut de nuances de gris VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine si une image sera affichée en mode nuances de gris. En lecture/écriture. **VgTriState**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *élément* nuances de gris = « *expression* » >

**Syntaxe du script**

*Element* . nuances de gris = "*expression*"

*expression* = *élément*. nuances de gris

**Remarques**

Si la **valeur est true**, l’image s’affiche en nuances de gris au lieu de la couleur. La valeur par défaut est **False**.

La valeur est basée sur la recommandation CCIR 709, qui privilégie davantage le poids vert et produit des résultats plus agréables pour la couleur naturelle.

*Attribut standard VML*

**Exemple**

L’image sera affichée en nuances de gris au lieu de la couleur.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 