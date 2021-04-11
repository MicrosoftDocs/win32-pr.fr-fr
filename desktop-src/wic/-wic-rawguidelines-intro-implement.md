---
description: Instructions générales pour l’implémentation de codecs BRUTs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Instructions générales pour l’implémentation de codecs BRUTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204212"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="ae118-103">Instructions générales pour l’implémentation de codecs BRUTs</span><span class="sxs-lookup"><span data-stu-id="ae118-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="ae118-104">Par rapport aux types d’images non BRUTes, tels que JPEG ou TIFF, il existe deux différences notables dans la façon dont les formats d’images BRUTes sont censés se comporter dans Windows :</span><span class="sxs-lookup"><span data-stu-id="ae118-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="ae118-105">La plupart des formats d’images BRUTs sont supposés être « en lecture seule » et ne prendront probablement pas en charge l’encodage de pixel au format brut.</span><span class="sxs-lookup"><span data-stu-id="ae118-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="ae118-106">Toutefois, étant donné que Windows Imaging Component (WIC) requiert un encodeur pour prendre en charge les métadonnées en écriture différée, les auteurs de codec brut doivent envisager d’implémenter au moins une classe de codeur squelette.</span><span class="sxs-lookup"><span data-stu-id="ae118-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="ae118-107">Le décodage d’une image brute de taille réelle peut prendre beaucoup de temps par rapport à d’autres formats.</span><span class="sxs-lookup"><span data-stu-id="ae118-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="ae118-108">Pour cette raison, Microsoft recommande de prendre certaines approches pour réduire la latence du décodage et garantir la prise en charge des scénarios tels que le rendu rapide des miniatures et des préversions.</span><span class="sxs-lookup"><span data-stu-id="ae118-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="ae118-109">Par exemple, tous les auteurs de codec brut doivent implémenter l’interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , qui fournit un mécanisme pour notifier le décodeur à l’avance de la taille de la bitmap cible, ce qui permet d’optimiser le décodage vers une plus petite taille d’image de sortie.</span><span class="sxs-lookup"><span data-stu-id="ae118-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae118-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae118-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ae118-111">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="ae118-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ae118-112">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="ae118-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="ae118-113">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="ae118-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="ae118-114">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="ae118-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



