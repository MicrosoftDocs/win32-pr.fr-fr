---
description: Utilisation du filtre tee Smart
ms.assetid: d2828269-6841-41a8-8d45-f864c7e85857
title: Utilisation du filtre tee Smart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5260469634c613fe05c25eb9f55e24e108e8c434
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534352"
---
# <a name="using-the-smart-tee-filter"></a><span data-ttu-id="e34f4-103">Utilisation du filtre tee Smart</span><span class="sxs-lookup"><span data-stu-id="e34f4-103">Using the Smart Tee Filter</span></span>

<span data-ttu-id="e34f4-104">Si un filtre de capture a des codes confidentiels de capture et de prévisualisation distincts, vous pouvez effectuer une capture à partir d’un tout en visualisant l’un de l’autre.</span><span class="sxs-lookup"><span data-stu-id="e34f4-104">If a capture filter has separate capture and preview pins, you can capture from one while previewing from the other.</span></span> <span data-ttu-id="e34f4-105">Toutefois, si le filtre n’a pas de pin d’aperçu, vous pouvez faire la même chose en incluant le filtre [tee intelligent](smart-tee-filter.md) dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="e34f4-105">But if the filter has no preview pin, you can do the same thing by including the [Smart Tee](smart-tee-filter.md) filter in the graph.</span></span> <span data-ttu-id="e34f4-106">Ce filtre fractionne les données de l’épingle de capture en deux flux identiques, l’un pour la capture et l’autre pour l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="e34f4-106">This filter splits data from the capture pin into two identical streams, one for capture and one for preview.</span></span> <span data-ttu-id="e34f4-107">Le diagramme suivant illustre ce processus.</span><span class="sxs-lookup"><span data-stu-id="e34f4-107">The following diagram illustrates this process.</span></span>

![capturer le graphique avec un filtre tee intelligent](images/vidcap05.png)

<span data-ttu-id="e34f4-109">La méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) insère automatiquement le filtre tee intelligent si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e34f4-109">The [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method automatically inserts the Smart Tee Filter if it is required.</span></span> <span data-ttu-id="e34f4-110">Toutefois, si vous utilisez des méthodes **IGraphBuilder** pour créer votre graphique, et non pas **RenderStream**, vous devrez peut-être insérer le filtre tee intelligent.</span><span class="sxs-lookup"><span data-stu-id="e34f4-110">However, if you use **IGraphBuilder** methods to build your graph, and not **RenderStream**, you may need to insert the Smart Tee filter.</span></span>

<span data-ttu-id="e34f4-111">Avant de rendre des codes confidentiels sur le filtre de capture, vérifiez si le filtre a une broche d’aperçu ou un code PIN de port vidéo.</span><span class="sxs-lookup"><span data-stu-id="e34f4-111">Before you render pins on the capture filter, check whether the filter has a preview pin or a video port pin.</span></span> <span data-ttu-id="e34f4-112">Si ce n’est pas le cas, et que vous souhaitez afficher un aperçu, ajoutez le filtre tee intelligent au graphique et connectez-le à l’épingle de capture sur le filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="e34f4-112">If it does not, and you wish to preview, add the Smart Tee filter to the graph and connect it to the capture pin on the capture filter.</span></span>

> [!Note]  
> <span data-ttu-id="e34f4-113">Vous pouvez traiter un code PIN de port vidéo (VP) comme un type de code PIN de préversion, de sorte qu’un filtre avec un code PIN de VP n’a pas besoin d’un filtre de tee intelligent.</span><span class="sxs-lookup"><span data-stu-id="e34f4-113">You can treat a video port (VP) pin as a kind of preview pin, so a filter with a VP pin does not need a Smart Tee filter.</span></span> <span data-ttu-id="e34f4-114">Toutefois, les pin de vice-président ont d’autres exigences spéciales.</span><span class="sxs-lookup"><span data-stu-id="e34f4-114">However, VP pins have some other special requirements.</span></span> <span data-ttu-id="e34f4-115">Pour plus d’informations, consultez [pin port Video](video-port-pins.md).</span><span class="sxs-lookup"><span data-stu-id="e34f4-115">For more information, see [Video Port Pins](video-port-pins.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e34f4-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e34f4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e34f4-117">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="e34f4-117">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="e34f4-118">Combinaison de la capture vidéo et de l’aperçu</span><span class="sxs-lookup"><span data-stu-id="e34f4-118">Combining Video Capture and Preview</span></span>](combining-video-capture-and-preview.md)
</dt> <dt>

[<span data-ttu-id="e34f4-119">Utilisation des catégories de code confidentiel</span><span class="sxs-lookup"><span data-stu-id="e34f4-119">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 



