---
title: Type de bitmap
description: Type de bitmap
ms.assetid: 208df4b9-d1be-49ff-bc0b-2e000608e9c7
keywords:
- Lecteur Windows Media Skins mobiles, bitmaps
- habillages, images bitmap
- informations de référence sur les apparences, les bitmaps
- bitmaps dans les apparences, types
- bitmaps dans les apparences, valeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602a436b5f4428b897672607265098104a9c1b0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193292"
---
# <a name="bitmap-type"></a>Type de bitmap

Le tableau suivant indique les valeurs qui sont valides pour le type de bitmap. Seul le type d’arrière-plan est requis ; d’autres sont facultatives et sont liées à différentes utilisations possibles des images.



| Valeur       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contexte  | Obligatoire. Image sur laquelle toutes les images de bouton sont superposées. Les dimensions de l’image d’arrière-plan de base incluent la largeur et la hauteur complètes de l’écran. Il s’agit également du fichier dans lequel sont affichées les images pour les États naturels des boutons et des trackbars. (Les boutons enfoncés et désactivés ne font pas partie de cette image.)                                                                                                                                                                                                                                                                                           |
| Désactivé    | Obligatoire. Indique que le déclenchement du bouton n’a aucun effet. Définit une image qui s’affiche lorsque la fonctionnalité de joueur spécifique n’est pas disponible pour l’utilisateur. Vous devez fournir une valeur de coordonnées pour indiquer la position de l’angle supérieur gauche de cette image par rapport à l’image d’arrière-plan.                                                                                                                                                                                                                                                                                                                |
| Un push      | Obligatoire. Définit une image qui s’affiche lorsque l’utilisateur exécute un push sur un bouton. Utilisez Push pour fournir des commentaires visuels à l’utilisateur lorsqu’il appuie sur un bouton. Vous devez fournir une valeur de coordonnées pour indiquer la position de l’angle supérieur gauche de cette image par rapport à l’image d’arrière-plan.                                                                                                                                                                                                                                                                                                                              |
| Région      | Définit les images qui utilisent des zones colorées pour représenter la zone de réponse TAP pour les boutons de type d’accès : PushHit, ToggleHit, 2PushHit. Si vous utilisez les boutons de type d’accès, vous devez fournir une image de région. ce fichier image utilise des couleurs de Palette de Windows spécifiques pour chaque contrôle. Les couleurs sont définies par des nombres représentant la valeur de rouge, de vert et de bleu pour la région. Cette image n’est jamais visible par l’utilisateur. Vous devez également fournir une valeur de coordonnées pour indiquer la position de l’angle supérieur gauche de cette image par rapport à l’image d’arrière-plan.                                                      |
| SeekThumb   | Définit une image que vous allez utiliser conjointement avec un TrackBar pour indiquer la position actuelle dans l’élément multimédia. Par exemple, si la chanson d’une chanson est demi-finie, l’image SeekThumb est affichée au milieu du TrackBar. En appuyant sur l’image SeekThumb et en la faisant glisser, l’utilisateur peut redémarrer l’élément multimédia à n’importe quelle position, appelée *recherche*. L’image du TrackBar lui-même est définie dans l’image d’arrière-plan. L’image SeekThumb n’est pas incluse dans la section bitmaps du fichier de définition d’apparence, mais elle est spécifiée dans le cadre de la définition de TrackBar dans la section TrackBars. |
| Super       | Définit l’image désactivée pour un TrackBar. Il peut également contenir d’autres images pour le bouton muet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| VolumeThumb | Définit une image à utiliser conjointement avec un TrackBar pour indiquer la position du volume. En appuyant sur l’image VolumeThumb et en la faisant glisser, l’utilisateur peut modifier le niveau du volume. L’image du TrackBar lui-même est définie dans l’image d’arrière-plan. L’image VolumeThumb n’est pas incluse dans la section bitmaps du fichier de définition d’apparence, mais elle est spécifiée dans le cadre de la définition de TrackBar dans la section TrackBars.                                                                                                                                                                                      |



 

> [!Note]  
> les types de zone et de Super bitmap sont déconseillés dans les habillages pour Lecteur Windows Media 10 Mobile ou version ultérieure.

 

Notez que le nom de fichier et le type de fichier ne sont pas nécessairement les mêmes. Vous pouvez appeler le fichier faisant l’objet d’un push comme vous le souhaitez, mais il est toujours référencé dans d’autres emplacements. Par exemple, dans la section Buttons, vous aurez un élément tel que :


```C++
Pushed @ 50,60

```



Cela fait référence au type du fichier, et non au nom du fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Images bitmap**](bitmaps.md)
</dt> </dl>

 

 




