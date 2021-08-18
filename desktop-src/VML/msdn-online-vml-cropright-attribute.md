---
title: Attribut VML de VML
description: Attribut VML de VML
ms.assetid: 1e2bd8e8-3d56-435d-bfaf-fb07f6b6fba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d695bb3fd9e88c3357343860dcbbff820e5a49a22100d59fe46c502b642e31d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796299"
---
# <a name="vml-cropright-attribute"></a>Attribut VML de VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit le pourcentage de suppression d’image du côté droit. En lecture/écriture. **VgNumber**.

**S’applique à**

[ImageData](msdn-online-vml-imagedata-element.md)

**Syntaxe de balise**

<v : *Element* CropRight = " *expression* " >

**Syntaxe du script**

*Element* . CropRight = "*expression*"

*expression* = *Element*. CropRight

**Remarques**

La quantité de rognage peut être comprise entre-1,0 et 1,0. La valeur par défaut est 0. Notez que la valeur 1 n’affiche aucune image. Les valeurs négatives entraînent le redimensionnement de l’image à partir du bord en cours de rognage (l’espace vide entre l’image et le bord rogné est rempli par la couleur de remplissage de la forme). Les valeurs positives inférieures à 1 entraînent l’étirement de l’image restante pour l’adapter à la forme.

*Attribut standard VML*

**Exemple**

L’image est retirée du côté droit de 20% de la largeur. L’espace vide entre l’image et le bord droit est rempli par la couleur de remplissage de la forme.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="blue"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropright="-.2" src="kids.jpg"/>
   </v:shape>
```





 

 