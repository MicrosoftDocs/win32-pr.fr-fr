---
description: Interfaces d’encodeur
ms.assetid: 02365401-8648-4be1-a447-fabd2cb77355
title: Interfaces d’encodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5367a25f1a2a4caf486711f7569312a436f8f474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203656"
---
# <a name="encoder-interfaces"></a>Interfaces d’encodeur


Les tableaux suivants présentent les interfaces implémentées par les encodeurs WIC (Windows Imaging Component) et le diagramme de classes affiche la hiérarchie d’héritage.

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

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



