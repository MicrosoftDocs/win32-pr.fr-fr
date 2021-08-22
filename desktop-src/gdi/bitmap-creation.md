---
description: Pour créer une image bitmap, utilisez la fonction CreateBitmap, CreateBitmapIndirect ou CreateCompatibleBitmap, CreateDIBitmap et CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Création d’une image bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038257"
---
# <a name="bitmap-creation"></a>Création d’une image bitmap

Pour créer une image bitmap, utilisez la fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)et [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Ces fonctions vous permettent de spécifier la largeur et la hauteur, en pixels, de l’image bitmap. La fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) et [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) vous permettent également de spécifier le nombre de plans de couleur et le nombre de bits requis pour identifier la couleur. En revanche, les fonctions [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) et [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) utilisent un contexte de périphérique spécifié pour obtenir le nombre de plans de couleur et le nombre de bits requis pour identifier la couleur.

La fonction [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crée une image bitmap dépendante de l’appareil à partir d’une image bitmap indépendante du périphérique. Il contient une table des couleurs qui décrit comment les valeurs de pixel correspondent aux valeurs de couleur RVB. Pour plus d’informations, consultez [bitmaps dépendantes](device-dependent-bitmaps.md) de l’appareil et [bitmaps indépendantes du périphérique](device-independent-bitmaps.md).

Une fois la bitmap créée, vous ne pouvez pas modifier sa taille, le nombre de plans de couleurs ou le nombre de bits requis pour identifier la couleur.

Lorsque vous n’avez plus besoin d’une image bitmap, appelez la fonction [**SupprimerObjet**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) pour la supprimer.

 

 



