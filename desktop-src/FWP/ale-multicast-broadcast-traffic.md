---
title: Trafic de diffusion/multidiffusion ALE
description: Tout le trafic de multidiffusion et de diffusion entrant au niveau des couches d’application de la couche application (ALE) est mappé à un flux ALE global.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309894"
---
# <a name="ale-multicastbroadcast-traffic"></a><span data-ttu-id="2cadf-103">Trafic de diffusion/multidiffusion ALE</span><span class="sxs-lookup"><span data-stu-id="2cadf-103">ALE Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="2cadf-104">Tout le trafic de multidiffusion et de diffusion entrant au niveau des couches d’application de la couche application (ALE) est mappé à un [flux ALE](ale-stateful-filtering.md)global.</span><span class="sxs-lookup"><span data-stu-id="2cadf-104">All inbound multicast and broadcast traffic at the Application Layer Enforcement (ALE) layers is mapped to one global [ALE flow](ale-stateful-filtering.md).</span></span> <span data-ttu-id="2cadf-105">Le trafic de réponse pour les paquets de multidiffusion et de diffusion entrants est classé au niveau de la couche [**FWPM d' \_ authentification ALE de couche \_ ALE \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) , et des flux ALE distincts sont créés pour chaque réponse.</span><span class="sxs-lookup"><span data-stu-id="2cadf-105">Response traffic for inbound multicast and broadcast packets is classified at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and separate ALE flows are created for each response.</span></span>

<span data-ttu-id="2cadf-106">Le trafic de multidiffusion et de diffusion en sortie sur les couches ALE crée un flux ALE de 4 secondes.</span><span class="sxs-lookup"><span data-stu-id="2cadf-106">Outbound multicast and broadcast traffic at the ALE layers creates a 4-second ALE flow.</span></span> <span data-ttu-id="2cadf-107">Par défaut, l’autorisation d’un paquet de multidiffusion ou de diffusion ALE de diffusion en sortie autorise le trafic entrant, qu’il s’agisse de monodiffusion, de multidiffusion ou de diffusion, depuis n’importe quelle adresse distante jusqu’à 4 secondes.</span><span class="sxs-lookup"><span data-stu-id="2cadf-107">By default, the authorization of an outbound multicast or broadcast ALE packet will permit inbound traffic, whether unicast, multicast, or broadcast, from any remote address for up to 4 seconds.</span></span> <span data-ttu-id="2cadf-108">Ce flux ALE peut uniquement être actualisé ou maintenu actif par le trafic sortant suivant qui correspond au flux ALE.</span><span class="sxs-lookup"><span data-stu-id="2cadf-108">Such an ALE flow can only be refreshed or kept alive by subsequent outbound traffic that matches the ALE flow.</span></span>

> [!Note]  
> <span data-ttu-id="2cadf-109">La durée de vie de 4 secondes est spécifiée par les options Set d’appel FWPM de l' [**\_ \_ option Set Connect de la \_ \_ \_ \_ couche \_ V {4 \| 6}**](built-in-callout-identifiers.md)de la légende intégrée.</span><span class="sxs-lookup"><span data-stu-id="2cadf-109">The 4-second lifetime is specified by the built-in callout [**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}**](built-in-callout-identifiers.md).</span></span> <span data-ttu-id="2cadf-110">Pour modifier la durée de vie par défaut de 4 secondes, ajoutez un filtre qui fait référence aux options de l' **ensemble de légendes FWPM appel de \_ \_ \_ \_ \_ \_ couche \_ V {4 \| 6}** .</span><span class="sxs-lookup"><span data-stu-id="2cadf-110">To alter the 4-second default lifetime, add a filter that references the **FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V{4\|6}** callout.</span></span> <span data-ttu-id="2cadf-111">Pour plus d’informations, consultez [Personnalisation du fluide ALE](ale-flow-customization.md) .</span><span class="sxs-lookup"><span data-stu-id="2cadf-111">See [ALE Flow Customization](ale-flow-customization.md) for more information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2cadf-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2cadf-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cadf-113">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="2cadf-113">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="2cadf-114">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="2cadf-114">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="2cadf-115">Filtrage avec état ALE</span><span class="sxs-lookup"><span data-stu-id="2cadf-115">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="2cadf-116">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="2cadf-116">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="2cadf-117">Personnalisation du fluide ALE</span><span class="sxs-lookup"><span data-stu-id="2cadf-117">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 




