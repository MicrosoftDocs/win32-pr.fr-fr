---
description: Interfaces d’encodeur
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521165"
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

**Conceptuel**
</dt> <dt>

[Implémentation d’un encodeur WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Implémentation de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



