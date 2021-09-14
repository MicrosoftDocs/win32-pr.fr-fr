---
description: La classe CImageDisplay est une classe d’assistance pour les convertisseurs vidéo GDI pour gérer le format d’affichage.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: CImageDisplay, classe (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010095"
---
# <a name="cimagedisplay-class"></a>CImageDisplay, classe

![cimagedisplayclasshierarchy](images/wutil06.png)

La `CImageDisplay` classe est une classe d’assistance pour les convertisseurs vidéo GDI pour gérer le format d’affichage. L’objet stocke une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) qui décrit le mode d’affichage actuel, qui est initialisé dans la méthode du constructeur de l’objet. La méthode **CheckMediaType** de l’objet vérifie si un type de média proposé peut être rendu efficacement à l’aide de GDI.



| Variables membres protégées                                       | Description                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_affichage m**](cimagedisplay-m-display.md)                    | Structure **VIDEOINFO** qui décrit le format d’affichage actuel.                     |
| Méthodes protégées                                                | Description                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Valide les masques de couleur dans une structure **VIDEOINFO** .                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Calcule le nombre de bits zéro au début d’un champ de bits spécifié.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Retourne le nombre de bits définis sur 1 dans un champ de bits spécifié.                          |
| M&#233;thodes publiques                                                   | Description                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Valide une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Détermine si un type de média proposé est compatible avec le format d’affichage.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Valide les entrées de palette dans une structure **VIDEOINFO** .                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Vérifie si un format **VIDEOINFO** spécifié est compatible avec le format d’affichage. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Méthode de constructeur.                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | Récupère les masques de couleur pour un format **VIDEOINFO** spécifié.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Récupère les masques de couleur pour le format d’affichage actuel.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Récupère la profondeur en bits du mode d’affichage actuel.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Récupère un format vidéo qui décrit le mode d’affichage actuel.                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Retermines si le format d’affichage actuel est en palette.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Met à jour le format vidéo de l’objet pour qu’il corresponde à l’affichage spécifié                       |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




