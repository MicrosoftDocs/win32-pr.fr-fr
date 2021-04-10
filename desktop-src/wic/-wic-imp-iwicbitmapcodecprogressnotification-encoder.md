---
description: Implémentation de IWICBitmapCodecProgressNotification (encodeur)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implémentation de IWICBitmapCodecProgressNotification (encodeur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867337"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a>Implémentation de IWICBitmapCodecProgressNotification (encodeur)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Bien que l’interface [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) soit facultative, il est recommandé de l’implémenter sur la classe d’encodeur au niveau du conteneur. Cette interface est décrite plus en détail dans [implémentation de IWICBitmapCodecProgressNotification (décodeur)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md). L’implémentation est la même pour le décodeur et l’encodeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[Implémentation de IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Implémentation de IWICBitmapCodecProgressNotification (décodeur)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



