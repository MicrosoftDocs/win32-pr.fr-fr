---
description: Miniatures et aperçus
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Miniatures et aperçus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086882"
---
# <a name="thumbnails-and-previews"></a>Miniatures et aperçus

Windows Vista et la galerie de photos Windows s’appuient sur le composant WIC (Windows Imaging Component) pour restituer des miniatures et des aperçus rapides des images. Pour prendre en charge le rendu rapide miniature et aperçu, les codecs BRUTs doivent implémenter les interfaces WIC [**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) et [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Pour prendre en charge une expérience utilisateur réactive, il est fortement souhaitable que ces interfaces retournent un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à l’appelant en 200 millisecondes ou moins.

Microsoft recommande vivement que les propriétaires de format de fichier brut génèrent un aperçu prérendu et le cache dans le fichier image. Pour un format de périphérique, cette opération est généralement effectuée au moment de la capture. Toutefois, les préversions peuvent également être régénérées et stockées dans le fichier image chaque fois que les propriétés de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) sont modifiées, si elles ne prennent pas trop de temps pour effectuer cette opération.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



