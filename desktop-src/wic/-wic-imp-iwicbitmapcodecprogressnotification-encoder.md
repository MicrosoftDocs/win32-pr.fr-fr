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
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="071c3-103">Implémentation de IWICBitmapCodecProgressNotification (encodeur)</span><span class="sxs-lookup"><span data-stu-id="071c3-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="071c3-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="071c3-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="071c3-105">Bien que l’interface [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) soit facultative, il est recommandé de l’implémenter sur la classe d’encodeur au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="071c3-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="071c3-106">Cette interface est décrite plus en détail dans [implémentation de IWICBitmapCodecProgressNotification (décodeur)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="071c3-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="071c3-107">L’implémentation est la même pour le décodeur et l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="071c3-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="071c3-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="071c3-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="071c3-109">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="071c3-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="071c3-110">Implémentation de IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="071c3-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="071c3-111">Implémentation de IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="071c3-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="071c3-112">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="071c3-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="071c3-113">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="071c3-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="071c3-114">Implémentation de IWICBitmapCodecProgressNotification (décodeur)</span><span class="sxs-lookup"><span data-stu-id="071c3-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



