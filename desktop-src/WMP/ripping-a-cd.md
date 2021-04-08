---
title: Extraction d’un CD
description: Extraction d’un CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, à propos de
- extraction de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840457"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="ff601-112">Extraction d’un CD</span><span class="sxs-lookup"><span data-stu-id="ff601-112">Ripping a CD</span></span>

<span data-ttu-id="ff601-113">Il existe deux façons d’extraire un CD à l’aide du contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ff601-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="ff601-114">Le lecteur Windows Media 9 peut extraire des CD à l’aide de **IWMPPlayerServices :: setTaskPane**.</span><span class="sxs-lookup"><span data-stu-id="ff601-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="ff601-115">Le lecteur Windows Media 11 introduit l’interface **IWMPCdromRip** pour l’extraction des CD.</span><span class="sxs-lookup"><span data-stu-id="ff601-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="ff601-116">Cette interface offre plus de fonctionnalités que **IWMPPlayerServices :: setTaskPane**, et il est recommandé d’utiliser **IWMPCdromRip** si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="ff601-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="ff601-117">Les sections suivantes décrivent comment extraire un CD à l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ff601-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="ff601-118">Extraction à l’aide de l’interface IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="ff601-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="ff601-119">Extraction à l’aide de IWMPPlayerServices :: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="ff601-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="ff601-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff601-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff601-121">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="ff601-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




