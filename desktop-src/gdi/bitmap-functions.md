---
description: Les fonctions suivantes sont utilisées avec les bitmaps.
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: Fonctions bitmap (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991289"
---
# <a name="bitmap-functions-windows-gdi"></a>Fonctions bitmap (Windows GDI)

Les fonctions suivantes sont utilisées avec les bitmaps.



| Fonction                                                 | Description                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | Affiche une image bitmap avec des pixels transparents ou translucides.  |
| [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | Effectue un transfert de bloc de bits.                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | Crée une image bitmap.                                              |
| [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | Crée une image bitmap.                                              |
| [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | Crée une bitmap compatible avec un appareil.                     |
| [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | Crée une bitmap dépendante de l’appareil à partir d’un DIB.            |
| [**CreateDIBSection**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | Crée un DIB dans lequel les applications peuvent écrire directement.         |
| [**ExtFloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | Remplit une zone de la surface d’affichage avec le pinceau actuel.   |
| [**GetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | Obtient les dimensions d’une image bitmap.                               |
| [**GetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | Récupère les valeurs de couleur RVB d’une bitmap de section DIB.          |
| [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | Copie une image bitmap dans une mémoire tampon.                                 |
| [**GetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | Obtient la valeur de couleur RVB du pixel à une coordonnée donnée.   |
| [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | Obtient le mode d’étirement actuel.                              |
| [**GradientFill**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | Remplit les structures de rectangles et de triangles.                       |
| [**LoadBitmap**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | Charge une bitmap à partir du fichier exécutable d’un module.                |
| [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | Combine les données de couleur dans les bitmaps sources et de destination. |
| [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | Effectue un transfert de bloc de bits.                                 |
| [**SetBitmapDimensionEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | Définit les dimensions préférées sur une image bitmap.                     |
| [**SetDIBColorTable**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | Définit les valeurs RVB dans un DIB.                                      |
| [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | Définit les pixels dans une bitmap à l’aide des données de couleur d’un DIB.       |
| [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | Définit les pixels dans un rectangle à l’aide des données de couleur d’un DIB.    |
| [**SetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | Définit la couleur d’un pixel.                                    |
| [**SetPixelV**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | Définit un pixel sur la meilleure approximation d’une couleur.             |
| [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | Définit le mode d’étirement de la bitmap.                               |
| [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | Copie une image bitmap et l’étire ou la compresse.                |
| [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | Copie les données de couleur dans un DIB.                                |
| [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | Effectue un transfert par bloc de bits des données de couleur.                   |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Les fonctions suivantes sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Microsoft Windows :

-   [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**GetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**SetBitmapBits**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



