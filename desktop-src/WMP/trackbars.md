---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Lecteur Windows Media Skins mobiles, trackbars
- habillages, trackbars
- informations de référence sur les habillages, trackbars
- trackbars dans les habillages, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb311994ccdfb48eb1ea9e010b268cdef13fd1fc8a2154d491f6e4103a91ec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762669"
---
# <a name="trackbars"></a>Trackbars

Un TrackBar affiche une image qui change par petits incréments. Les Trackbars sont utilisés pour les contrôles de volume et les contrôles de position de lecture. Vous pouvez utiliser trackbars pour afficher des informations sur l’élément multimédia en cours ou pour permettre à l’utilisateur de modifier les paramètres ou la position de lecture. Par exemple, vous pouvez utiliser un TrackBar pour permettre à l’utilisateur d’ajuster le volume, et un autre TrackBar qui peut montrer à l’utilisateur la position de lecture actuelle. Trackbars ont une image Thumb qui définit le paramètre actuel de la valeur TrackBar.

La section Trackbars du fichier de définition d’apparence doit commencer par cette ligne :


```C++
[ Trackbars ]

```



Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacun des trackbars dans votre apparence.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



Vous pouvez utiliser le modèle suivant pour la section Trackbars de votre fichier de définition d’apparence :


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



Vous devez utiliser l’ordre suivant pour les informations de TrackBar pour chaque ligne dans la section Trackbars (chaque partie de la ligne est requise) :

1.  [TrackBar, type](trackbar-type.md)
2.  [Emplacement de la barre de TrackBar](trackbar-location.md)
3.  [Source de l’image pour le TrackBar désactivé](image-source-for-disabled-trackbar.md)
4.  [Source de l’image Thumb](thumb-image-source.md)
5.  [Taille de curseur](thumb-size.md)

Pour obtenir un exemple de code Trackbars, consultez la [section exemple de Trackbars](sample-trackbars-section.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




