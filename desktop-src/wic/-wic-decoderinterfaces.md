---
description: Interfaces de décodeur
ms.assetid: b88517cc-06fe-4d83-a6a9-76e1f34293f4
title: Interfaces de décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef90ca2dd521c15460295505a6d5b7ea451c4dba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521169"
---
# <a name="decoder-interfaces"></a>Interfaces de décodeur

les tableaux suivants présentent les interfaces implémentées par les décodeurs Windows Component (WIC) et le diagramme de classes affiche la hiérarchie d’héritage.

Interfaces de décodeur Container-Level



| Interface                                                                                       | Responsabilités                             | Implémentation                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)                                             | Services au niveau du conteneur                     | Obligatoire                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) | Notification de progression & la prise en charge de l’annulation | Recommandé                                                                |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)                                 | Énumération des métadonnées                         | Facultatif (requis uniquement pour les formats qui prennent en charge les métadonnées au niveau du conteneur) |



 

Interfaces de décodeur Frame-Level



| Interface                                                           | Responsabilités          | Implémentation                |
|---------------------------------------------------------------------|---------------------------|-------------------------------|
| [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)         | Services au niveau de la trame      | Obligatoire                      |
| [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)     | Énumération des métadonnées      | Obligatoire                      |
| [IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md) | Transformations du décodeur natif | Recommandé                   |
| [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)                       | Services de traitement brut   | Obligatoire pour les formats bruts uniquement |



 

![hiérarchie d’héritage de l’interface WIC](graphics/wicinterfaces.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Implémentation d’un décodeur WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



