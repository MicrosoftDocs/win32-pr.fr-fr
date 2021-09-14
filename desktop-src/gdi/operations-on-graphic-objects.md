---
description: Une fois qu’une application a créé un DC d’affichage ou d’imprimante, elle peut commencer à dessiner sur l’appareil associé ou, dans le cas du DC de mémoire, il peut commencer à dessiner sur l’image bitmap stockée en mémoire.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Opérations sur les objets graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0574b8527dbf83b4cb4a38163dcf7b33017336
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415911"
---
# <a name="operations-on-graphic-objects"></a>Opérations sur les objets graphiques

Une fois qu’une application a créé un DC d’affichage ou d’imprimante, elle peut commencer à dessiner sur l’appareil associé ou, dans le cas du DC de mémoire, il peut commencer à dessiner sur l’image bitmap stockée en mémoire. Toutefois, avant le début du dessin et parfois lors du dessin, il est souvent nécessaire de remplacer les objets par défaut par de nouveaux objets.

Une application peut examiner les attributs d’un objet par défaut en appelant les fonctions [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) et [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . La fonction **GetCurrentObject** retourne un handle identifiant le stylet, le pinceau, la palette, la bitmap ou la police en cours, et la fonction **GetObject** Initialise une structure contenant les attributs de cet objet.

Certaines imprimantes fournissent des stylets, des pinceaux et des polices résidents qui peuvent être utilisés pour améliorer la vitesse de dessin dans une application. Deux fonctions peuvent être utilisées pour énumérer ces objets : [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) et [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa). Si l’application doit énumérer des stylets résidents ou des pinceaux, elle peut appeler la fonction **EnumObjects** pour examiner les attributs correspondants. Si l’application doit énumérer les polices résidentes, elle peut appeler la fonction **EnumFontFamilies** (qui peut également énumérer les polices GDI).

Une fois qu’une application a déterminé qu’un objet par défaut doit être remplacé, elle crée un nouvel objet en appelant l’une des fonctions de création suivantes.



| Objet graphique | Fonction                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap), [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap), [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Brush          | [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect), [**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush), [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt), [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush), [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush), [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Palette de couleurs  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Police           | [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta), [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Stylet            | [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Région         | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect), [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn), [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Chacune de ces fonctions retourne un handle identifiant un nouvel objet. Une fois qu’une application a extrait un handle, elle doit appeler la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) pour remplacer l’objet par défaut. Toutefois, l’application doit enregistrer le handle identifiant l’objet par défaut et utiliser ce handle pour remplacer le nouvel objet lorsqu’il n’est plus nécessaire. Lorsque l’application termine le dessin avec le nouvel objet, elle doit restaurer l’objet par défaut en appelant la fonction **SelectObject** , puis supprimer le nouvel objet en appelant la fonction [**SupprimerObjet**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) . L’échec de la suppression d’objets entraîne de sérieux problèmes de performances.

 

 



