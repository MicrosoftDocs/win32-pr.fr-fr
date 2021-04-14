---
title: Attribut gain de VML
description: Attribut gain de VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382310"
---
# <a name="vml-gain-attribute"></a>Attribut gain de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’intensité de toutes les couleurs d’une image. En lecture/écriture. **VgNumber**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *élément* gain = " *expression* " >

**Syntaxe du script**

*Element* . gain = "*expression*"

*expression* = *Element*. gain

**Remarques**

Cet attribut définit la luminosité du blanc de couleur, en affectant toutes les autres couleurs. Les valeurs sont comprises entre 0 et Infinity. La valeur par défaut est 1,0. La valeur 0 n’affiche aucune image. Les valeurs supérieures à 1 éclaircissent l’image et les valeurs inférieures à 1 rendent l’image plus claire.

Cet attribut peut être utilisé pour créer des effets intéressants.

*Attribut standard VML*

**Exemple**

L’image s’affiche avec toutes les couleurs tendant vers le gris.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 