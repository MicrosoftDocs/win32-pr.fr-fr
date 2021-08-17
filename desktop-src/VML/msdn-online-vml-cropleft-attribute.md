---
title: VML CropLeft (attribut)
description: VML CropLeft (attribut)
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26112aa969e95c6bfb1ec715024aca9eb17b2dbfc2d7d214fb3679cf7ab77447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754849"
---
# <a name="vml-cropleft-attribute"></a>VML CropLeft (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le pourcentage de suppression d’image du côté gauche. En lecture/écriture. **VgNumber**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* CropLeft = " *expression* " >

**Syntaxe du script**

*Element* . CropLeft = "*expression*"

*expression* = *élément*. CropLeft

**Remarques**

La quantité de rognage peut être comprise entre-1,0 et 1,0. La valeur par défaut est 0. Notez que la valeur 1 n’affiche aucune image. Les valeurs négatives entraînent le redimensionnement de l’image à partir du bord en cours de rognage (l’espace vide entre l’image et le bord rogné est rempli par la couleur de remplissage de la forme). Les valeurs positives inférieures à 1 entraînent l’étirement de l’image restante pour l’adapter à la forme.

*Attribut standard VML*

**Exemple**

20% de l’image seront supprimés du côté gauche et l’image restante sera étirée pour s’ajuster à la forme.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 