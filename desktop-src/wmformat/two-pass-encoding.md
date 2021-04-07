---
title: Encodage Two-Pass
description: Encodage Two-Pass
ms.assetid: 354cd0a5-9a64-4171-9604-694e60b382ad
keywords:
- Windows Media Format SDK, encodage en deux passes
- Windows Media Format SDK, encodage 2 passe
- codecs, encodage en deux passes
- codecs, encodage à 2 passes
- encodage en deux passes, à propos de
- 2-encodage Pass, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6764f80857447e122c97c69683243a65da7e83b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028970"
---
# <a name="two-pass-encoding"></a><span data-ttu-id="e34b6-109">Encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="e34b6-109">Two-Pass Encoding</span></span>

<span data-ttu-id="e34b6-110">L’encodage en deux passes est une méthode d’encodage disponible avec certains codecs, comme le codec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="e34b6-110">Two-pass encoding is an encoding method available with some codecs, like the Windows Media Video 9 codec.</span></span> <span data-ttu-id="e34b6-111">Lorsque vous utilisez l’encodage en deux passes, le codec traite tous les exemples du flux à deux reprises.</span><span class="sxs-lookup"><span data-stu-id="e34b6-111">When you use two-pass encoding, the codec processes all of the samples for the stream twice.</span></span> <span data-ttu-id="e34b6-112">Lors du premier passage, le codec rassemble des informations sur le contenu du flux.</span><span class="sxs-lookup"><span data-stu-id="e34b6-112">On the first pass, the codec gathers information about the content of the stream.</span></span> <span data-ttu-id="e34b6-113">Lors de la deuxième passe, le codec utilise les informations collectées lors du premier passage pour optimiser le processus d’encodage du flux.</span><span class="sxs-lookup"><span data-stu-id="e34b6-113">On the second pass, the codec uses the information gathered on the first pass to optimize the encoding process for the stream.</span></span>

<span data-ttu-id="e34b6-114">Dans le mode d’encodage à taux binaire constant, les fichiers qui sont codés en deux passes sont généralement plus efficaces que les fichiers encodés en une seule passe.</span><span class="sxs-lookup"><span data-stu-id="e34b6-114">In the Constant Bit Rate encoding mode, files that are encoded in two passes are generally more efficient than files encoded in a single pass.</span></span> <span data-ttu-id="e34b6-115">Le VBR basé sur la qualité, qui est une passe, produit une qualité plus cohérente que le VBR basé sur la vitesse du bit, ce qui correspond à deux passes.</span><span class="sxs-lookup"><span data-stu-id="e34b6-115">Quality-based VBR, which is one pass, produces more consistent quality than bit-rate-based VBR, which is two-pass.</span></span>

<span data-ttu-id="e34b6-116">Vous ne pouvez pas utiliser un encodage en deux passes sur des flux Live.</span><span class="sxs-lookup"><span data-stu-id="e34b6-116">You cannot use two-pass encoding on live streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e34b6-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e34b6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e34b6-118">**Fonctionnalités du codec**</span><span class="sxs-lookup"><span data-stu-id="e34b6-118">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="e34b6-119">**Utilisation de l’encodage Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="e34b6-119">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




