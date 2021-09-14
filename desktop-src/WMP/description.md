---
title: Description (Lecteur Windows Media SDK)
description: Description
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Lecteur Windows Media Apparences mobiles, section Description
- apparences, section Description
- référence pour les apparences, section Description
- Section Description dans les apparences
- fichiers de définition d’apparence, section Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008478"
---
# <a name="description-windows-media-player-sdk"></a>Description (Lecteur Windows Media SDK)

quand vous créez une apparence pour Lecteur Windows Media série 9 pour Windows Mobile 2003 ou version ultérieure, vous devez inclure une section Description. La section Description vous permet de spécifier la largeur et la hauteur de l’affichage, la résolution d’affichage et l’orientation d’affichage pour laquelle l’apparence a été conçue. La section Description doit apparaître dans le fichier de définition d’apparence avant toute autre section, et juste après la déclaration de version initiale.

La section Description du fichier de définition d’apparence doit commencer par la ligne suivante :


```C++
[ Description ]

```



Vous devez ensuite ajouter des informations sur les dimensions de l’apparence et la résolution d’affichage. L’exemple suivant montre comment spécifier des dimensions :


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Cela spécifie que vous avez conçu l’apparence pour afficher 240 pixels de large, 320 pixels de haut et avec une résolution d’affichage de 96 ppp. Notez que cela implique une orientation en mode portrait.

Vous pouvez éventuellement spécifier le mode d’orientation pour lequel vous avez conçu l’apparence dans la section Description. L’exemple suivant montre comment spécifier l’orientation :


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



Le tableau suivant répertorie les valeurs que vous pouvez utiliser pour l’orientation.



| Orientation | Description                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Paysage   | La largeur de l’apparence est supérieure à la hauteur de l’apparence. L’affichage est orienté horizontalement.   |
| Portrait    | La hauteur de l’apparence est supérieure à la largeur de l’apparence. L’affichage est orienté verticalement. |
| Carré      | La hauteur de l’apparence est égale à la largeur de l’apparence. L’affichage n’a aucune orientation.                    |



 

> [!Note]  
> Lecteur Windows Media 9 Series pour Windows Mobile 2003 affiche uniquement une apparence particulière lorsque la section description spécifiée dans le fichier de définition d’apparence correspond à l’état actuel de l’appareil.

 

Veillez à toujours spécifier les dimensions, la résolution et l’orientation appropriées pour lesquelles votre apparence a été créée. Par exemple, si les dimensions spécifiées par votre apparence décrivent une orientation paysage, votre apparence n’est pas disponible lorsque l’appareil est en mode portrait, même si vous spécifiez portrait dans la ligne orientation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




