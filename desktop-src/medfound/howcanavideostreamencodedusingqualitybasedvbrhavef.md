---
description: Comment un flux vidéo encodé à l’aide de la méthode VBR basée sur la qualité a-t-il moins de frames que le flux d’origine ?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Comment un flux vidéo encodé à l’aide de la méthode VBR basée sur la qualité a-t-il moins de frames que le flux d’origine ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202411"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a><span data-ttu-id="d5bb5-103">Comment un flux vidéo encodé à l’aide de la méthode VBR basée sur la qualité a-t-il moins de frames que le flux d’origine ?</span><span class="sxs-lookup"><span data-stu-id="d5bb5-103">How can a video stream encoded using quality-based VBR have fewer frames than the original stream?</span></span>

<span data-ttu-id="d5bb5-104">Le nombre de frames d’un flux encodé peut être inférieur au nombre de frames de l’original pour l’une des deux raisons suivantes : les images dupliquées et les frames déplacés.</span><span class="sxs-lookup"><span data-stu-id="d5bb5-104">The frame count of an encoded stream can be lower than the frame count of the original for one of two reasons: duplicate frames and dropped frames.</span></span>

<span data-ttu-id="d5bb5-105">En règle générale, l’encodeur ne produit pas de frames qui sont des doublons exacts du frame précédent.</span><span class="sxs-lookup"><span data-stu-id="d5bb5-105">The encoder does not normally produce frames that are exact duplicates of the previous frame.</span></span> <span data-ttu-id="d5bb5-106">Si vous avez besoin d’un échantillon pour chaque frame (requis par certains conteneurs, par exemple), vous pouvez configurer l’encodeur pour produire des frames « factices » en affectant à la propriété [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) la \_ valeur variant true.</span><span class="sxs-lookup"><span data-stu-id="d5bb5-106">If you need to have a sample for every frame (this is required by some containers, for example), you can configure the encoder to produce "dummy" frames by setting the [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="d5bb5-107">L’encodeur supprime les frames lorsqu’il ne peut pas encoder tous les frames sans débordement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d5bb5-107">The encoder drops frames when it cannot encode all of the frames without overflowing the buffer.</span></span> <span data-ttu-id="d5bb5-108">Les frames supprimés ont une incidence sur la qualité du flux, ce qui n’est pas le cas des trames dupliquées.</span><span class="sxs-lookup"><span data-stu-id="d5bb5-108">Dropped frames affect the quality of the stream, duplicate frames do not.</span></span>

<span data-ttu-id="d5bb5-109">Vous pouvez obtenir des statistiques de frame à partir de l’encodeur pour déterminer si des frames ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="d5bb5-109">You can get frame statistics from the encoder to determine whether frames have been dropped.</span></span> <span data-ttu-id="d5bb5-110">Pour plus d’informations, consultez [obtention de statistiques de codage](gettingencodingstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="d5bb5-110">For more information, see [Getting Encoding Statistics](gettingencodingstatistics.md).</span></span>

<span data-ttu-id="d5bb5-111">En règle générale, les flux VBR basés sur la qualité n’auront que moins de frames que l’original s’il y a des images en double (car la vitesse de transmission n’est pas restreinte).</span><span class="sxs-lookup"><span data-stu-id="d5bb5-111">Typically, quality-based VBR streams will only have fewer frames than the original if there are duplicate frames (because the bit rate is not constrained).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5bb5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5bb5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5bb5-113">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="d5bb5-113">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



