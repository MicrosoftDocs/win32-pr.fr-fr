---
description: Configuration requise pour les codecs BRUTs pour Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Configuration requise pour les codecs BRUTs pour Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520018"
---
# <a name="raw-codec-requirements-for-windows-7"></a>Configuration requise pour les codecs BRUTs pour Windows 7

Les fonctionnalités de codec suivantes sont requises au minimum :

Toutes les fonctionnalités requises pour la prise en charge de l’interpréteur de commandes et de la Galerie de photos Windows Vista : miniature, aperçu et rotation (persistante). Le traitement brut doit avoir comme valeur par défaut les paramètres appropriés.

La prise en charge des métadonnées principales (à la fois en lecture et en écriture), les métadonnées non EXIF, ainsi que les métadonnées EXIF, doit être conservée dans des formats de fichiers BRUTs sans utiliser de fichiers side-car.

Prise en charge de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Pour Windows 7, WIC (Windows Imaging Component) WIC exige que toutes les interfaces de paramètre exposées par [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) soient implémentées.

Prise en charge de l’état d’orientation :

-   les rotations d’image d’une étape de 90 doivent être appliquées à l’aide de la méthode [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Les applications et Windows utilisent cette méthode pour faire pivoter les images (et les miniatures et les aperçus mis en cache).
-   L’application de la rotation à l’aide de cette API doit également être conservée par le codec (voir plus haut dans ce document).
-   Les applications peuvent utiliser les fonctionnalités de rotation de l’API [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , mais le codec ne sérialise pas les paramètres de rotation sur cette API, donc les rotations effectuées à l’aide de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) ne sont pas conservées.

Prise en charge de l’extraction des miniatures et des aperçus rapides. Si la taille de la dimension de pixel maximale de l’aperçu (largeur ou hauteur) est inférieure à 1024 pixels, Windows Vista demande un rendu pour l’aperçu de l’écran :

-   La méthode [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) doit prendre en charge au moins les modes [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) et [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) pour permettre un rendu plus rapide des miniatures et des aperçus que le mode de qualité totale.
-   Windows appellera [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) avec la taille de résolution d’écran demandée.
-   Les tailles de résolution d’écran doivent être prises en charge dans l’API ci-dessus.
-   Un traitement cohérent des images de la miniature, de l’aperçu et des bits d’image complète à partir de [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) est nécessaire.

Formats de pixel HDR (High dynamique Range).

Impression XPS (XML Paper Specification).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



