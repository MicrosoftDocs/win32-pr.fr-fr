---
title: Attribut de nuances de gris VML
description: Attribut de nuances de gris VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683371e2441ffa93f96dc8f727e4eed293954b1897267db8848aa39ffa497af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099209"
---
# <a name="vml-grayscale-attribute"></a>Attribut de nuances de gris VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

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



 

 