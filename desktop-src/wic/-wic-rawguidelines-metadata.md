---
description: Prise en charge des métadonnées
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Prise en charge des métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529352"
---
# <a name="metadata-support"></a>Prise en charge des métadonnées

Les formats BRUTs doivent également prendre en charge les scénarios courants de lecture et d’écriture des métadonnées pour les images dans Windows. Microsoft a développé un ensemble de fournisseurs de métadonnées natifs pour les métadonnées EXIF (Exchangeable Image File), IPTC (International Press Telecommunications Council) et XMP (Extensible Metadata Platform) qui sont actuellement appelés uniquement pour les conteneurs TIFF et JPEG. Si l’image brute est stockée dans l’un de ces formats de conteneur, il est recommandé d’utiliser les fournisseurs de métadonnées intégrés Windows. Toutefois, l’auteur du codec est chargé de la configurer correctement. Pour les fichiers BRUTs qui ne sont pas basés sur un conteneur TIFF, il peut être nécessaire d’implémenter des enregistreurs EXIF, IPTC ou XMP, car les lecteurs et les Writers intégrés s’attendent à ce que les données soient conformes aux spécifications de disposition sur disque EXIF, IPTC et XMP. Les auteurs de codec peuvent également implémenter leurs propres fournisseurs pour toutes les métadonnées personnalisées.

En raison de l’architecture du composant WIC (Windows Imaging Component), les enregistreurs de métadonnées peuvent être appelés uniquement par le biais d’une instance d’un encodeur d’image. Par conséquent, les propriétaires de format brut doivent créer au moins un encodeur [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , même si l’encodage réel des pixels dans un format brut n’est pas implémenté. L’auteur du codec doit appeler les gestionnaires de métadonnées appropriés :

-   [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) sur le décodeur et le décodeur de trame, le cas échéant.
-   [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sur l’encodeur et l’encodeur de trame, le cas échéant.

Pour prendre en charge tous les scénarios anticipés dans les applications d’imagerie de Windows Vista, il est recommandé que les fournisseurs de codec prennent en charge les éléments suivants au minimum :

-   Lecture EXIF
-   Écriture EXIF partielle (pour autoriser les mises à jour pour capturer la date et l’heure)
-   Lecture et écriture XMP (y compris éventuellement le noyau IPTC pour XMP)
-   IPTC IIMv4 lecture et écriture

La majeure partie de l’accès aux métadonnées (lecture et écriture) dans Windows Vista se produit via l’interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) ou [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Par conséquent, pour participer aux expériences de métadonnées Windows Vista, les auteurs de codec brut doivent implémenter les méthodes [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) et [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

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

 

 



