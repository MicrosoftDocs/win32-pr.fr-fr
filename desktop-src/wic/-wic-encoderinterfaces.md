---
description: Interfaces d’encodeur
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6169dcf55ffafe0bf4c006b45c173ecc7486555fb001456112f8f333a8ccf2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965121"
---
# <a name="encoder-interfaces"></a>Interfaces d’encodeur


les tableaux suivants présentent les interfaces implémentées par les encodeurs de composant Windows Imaging (WIC) et le diagramme de classes affiche la hiérarchie d’héritage.

Interfaces d’encodeur Container-Level



| Interface                                                                                       | Responsabilités                             | Implémentation                                                             |
|-------------------------------------------------------------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------|
| [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)                                             | Services au niveau du conteneur                     | Obligatoire                                                                   |
| [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md) | Notification de progression & la prise en charge de l’annulation | Recommandé                                                                |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)                                 | Services de sérialisation des métadonnées              | Facultatif (requis uniquement pour les formats qui prennent en charge les métadonnées au niveau du conteneur) |



 

Interfaces d’encodeur Frame-Level



| Interface                                                       | Responsabilités                | Implémentation |
|-----------------------------------------------------------------|---------------------------------|----------------|
| [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)     | Services au niveau de la trame            | Obligatoire       |
| [IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md) | Services de sérialisation des métadonnées | Obligatoire       |



 

![hiérarchie d’héritage de l’interface d’encodeur WIC](graphics/wicencoderinterfaces.png)

Vous remarquerez que les interfaces de codeur sont presque des images miroir des interfaces de décodeur et que la plupart des méthodes sur ces interfaces correspondent à des méthodes sur les interfaces de décodeur associées. Maintenant que vous êtes familiarisé avec l’implémentation d’un décodeur avec WIC activé, l’implémentation d’un encodeur prenant en charge WIC vous paraîtra également familière.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation d’un encodeur WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Implémentation de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



