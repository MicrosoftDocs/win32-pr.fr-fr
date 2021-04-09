---
description: Cette section de rubriques fournit aux développeurs des conseils sur la façon d’implémenter des codecs de format de fichier image qui fonctionnent dans l’infrastructure WIC (Windows Imaging Component).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Comment écrire un codec WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865550"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Comment écrire un codec WIC-Enabled

Cette section de rubriques fournit aux développeurs des conseils sur la façon d’implémenter des codecs de format de fichier image qui fonctionnent dans l’infrastructure WIC (Windows Imaging Component).

<dl>

[Introduction](-wic-howtowriteacodec-intro.md)  
[Fonctionnement du composant WIC (Windows Imaging Component)](-wic-howwicworks.md)  
<dl>

[Découverte et arbitrage](-wic-howwicworks.md)  
[Décodage](-wic-howwicworks.md)  
[Encodage](-wic-howwicworks.md)  
[Durée de vie d’un codec](-wic-howwicworks.md)  
[Guide pratique pour activer un codec dans WIC](-wic-howwicworks.md)  
[Prise en charge du cloisonnement multithread dans WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implémentation d’un décodeur WIC-Enabled</a><dl>

[Interfaces de décodeur](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implémentation d’un encodeur WIC-Enabled</a>  
<dl>

[Interfaces d’encodeur](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Installation et inscription du codec</a>  
<dl>

[Inscription d’un codec](-wic-codecinstallandreg.md)  
<dl>

[Entrées générales du Registre](-wic-generalregentries.md)  
[Entrées de Registre spécifiques à l’encodeur](-wic-encoderregentries.md)  
<dl>

[Inscription d’un format de conteneur avec des enregistreurs de métadonnées](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Entrées de Registre spécifiques à l’encodeur</a>  
<dl>

[Inscription d’un nouveau format de conteneur avec des lecteurs de métadonnées](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Intégration à la Galerie et à l’Explorateur Windows Vista</a>  
<dl>

[Magasin de propriétés Windows](-wic-integrationregentries.md)  
[Galerie de photos Windows Vista](-wic-integrationregentries.md)  
[Cache de miniatures Windows Vista](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Mise à jour du cache de miniatures lors de l’installation d’un codec</a> [mettant votre WIC-Enabled codec à la disposition des utilisateurs](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">conclusion</a>  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Introduction (écriture d’un CODEC WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



