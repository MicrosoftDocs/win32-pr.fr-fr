---
title: À propos des fonctions DrawDib
description: À propos des fonctions DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- vidéo pour Windows (VFW), DrawDib
- VFW (vidéo pour Windows), DrawDib
- DrawDib, à propos de
- DrawDib, tables de couleurs
- DrawDib, mode de transfert
- DrawDib, adaptateurs d’affichage
- DrawDib, étirement d’image
- DrawDib, images compressées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e03b41d5af776c39f7d100e9478bd408011d61d8e3d661cb80bd9ab52f08c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942087"
---
# <a name="about-the-drawdib-functions"></a>À propos des fonctions DrawDib

Collectivement, les fonctions DrawDib sont similaires à la fonction [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) en ce qu’elles fournissent des fonctionnalités d’étirement et de tramage d’image. Toutefois, les fonctions DrawDib prennent en charge la décompression d’image, la diffusion de données et un plus grand nombre de cartes d’affichage.

Il est utile d’utiliser les fonctions DrawDib dans certaines circonstances. Toutefois, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) est plus diversifié que les fonctions DrawDib et doit être utilisé lorsque les fonctions DrawDib ne peuvent pas fournir la fonctionnalité souhaitée. La liste suivante décrit les facteurs à prendre en compte pour déterminer s’il faut utiliser les fonctions DrawDib ou **StretchDIBits**.

-   Format des informations de la table des couleurs. Les fonctions DrawDib affichent des images qui utilisent le format de **\_ \_ couleurs DIB RVB** pour leur table de couleurs. Si les images de votre application stockent les informations de table de couleur avec le format **DIB \_ PAL \_** ou les **\_ \_ index PAL DIB** , vous devez utiliser [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) pour les afficher.
-   Mode de transfert. Les fonctions DrawDib requièrent que votre application utilise le mode de transfert **SRCCOPY** . Si votre application utilise [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) avec un mode de transfert autre que **SRCCOPY**, vous devez continuer à utiliser **StretchDIBits**. De même, si vous devez utiliser d’autres opérations raster dans votre application, par exemple XOR, utilisez **StretchDIBits**.
-   Qualité de la lecture des vidéos et des animations. Vous pouvez utiliser les fonctions DrawDib pour les applications de streaming de données, telles que celles qui lisent des clips vidéo et des séquences animées. Les fonctions DrawDib sont plus performantes que les [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) en ce qu’elles fournissent des images de qualité supérieure et améliorent le mouvement pendant la lecture.
-   Affichez les adaptateurs. Les fonctions DrawDib prennent en charge un plus grand nombre d’adaptateurs d’affichage que [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ne prend en charge. Les fonctions DrawDib prennent en charge les adaptateurs de couleurs VGA qui fournissent des palettes de 16 couleurs utilisant une profondeur d’image de 4 bits, des adaptateurs SVGA qui fournissent des palettes de 256 de couleurs à l’aide de la profondeur d’image 8 bits et des adaptateurs d’affichage de couleurs vraies qui fournissent des milliers de couleurs utilisant des profondeur d’image 16 bits, 24 bits et 32

    Les fonctions DrawDib améliorent également la vitesse et la qualité de l’affichage des images sur les adaptateurs d’affichage avec des fonctionnalités plus limitées. Par exemple, lors de l’utilisation d’un adaptateur d’affichage 8 bits, DrawDib fonctionne efficacement pour les images de couleur vraies sur 256 couleurs. Ils détrament également les images 8 bits lors de l’utilisation d’adaptateurs d’affichage 4 bits.

-   Étirement d’image. Comme [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits), les fonctions DrawDib utilisent des rectangles de source et de destination pour contrôler la partie d’une image qui est affichée. Vous pouvez rogner des parties indésirables d’une image ou étirer une image en faisant varier la position et la taille des rectangles source et de destination. Si un pilote d’affichage ne prend pas en charge l’étirement d’image, les fonctions DrawDib offrent des fonctionnalités d’étirement plus efficaces que **StretchDIBits**.
-   Images compressées. Les fonctions DrawDib dessineront tout format pour lequel vous avez un décompresseur, y compris l’encodage de longueur d’exécution (RLE), Cinepak et 411 YUV. Windows comprend des décompresseurs RLE et Cinepak qui peuvent éventuellement être installés.
-   Le codec Indeo n’est plus pris en charge dans Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 