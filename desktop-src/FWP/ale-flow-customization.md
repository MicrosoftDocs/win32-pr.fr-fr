---
title: Personnalisation du fluide ALE
description: Le filtrage réseau au niveau des couches de mise en œuvre de la couche application (ALE) de la plateforme de filtrage Windows (WFP) peut être personnalisé en ajoutant des filtres avec des options de classification spécifiques.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314366"
---
# <a name="ale-flow-customization"></a><span data-ttu-id="b1e12-103">Personnalisation du fluide ALE</span><span class="sxs-lookup"><span data-stu-id="b1e12-103">ALE Flow Customization</span></span>

<span data-ttu-id="b1e12-104">Le filtrage réseau au niveau des couches de mise en œuvre de la couche application (ALE) de la plateforme de filtrage Windows (WFP) peut être personnalisé en ajoutant des filtres avec des options de classification spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b1e12-104">Network filtering at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) can be customized by adding filters with specific classify options.</span></span>

## <a name="multicastbroadcast-traffic"></a><span data-ttu-id="b1e12-105">Trafic de multidiffusion/diffusion</span><span class="sxs-lookup"><span data-stu-id="b1e12-105">Multicast/Broadcast Traffic</span></span>

<span data-ttu-id="b1e12-106">Pour bloquer le trafic entrant en fonction des États de multidiffusion ou de diffusion sortants, ajoutez un filtre qui autorise le trafic de multidiffusion et de diffusion en sortie et dont l’option d' [**\_ \_ \_ \_ État de multidiffusion option de classement fwp**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) a la **valeur d' \_ option fwp refuser l' \_ \_ \_ \_ État de multidiffusion**.</span><span class="sxs-lookup"><span data-stu-id="b1e12-106">To block inbound traffic based on outbound multicast or broadcast states, add a filter that authorizes outbound multicast and broadcast traffic and that has the [**FWP\_CLASSIFY\_OPTION\_MULTICAST\_STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_DENY\_MULTICAST\_STATE**.</span></span>

## <a name="remote-peers"></a><span data-ttu-id="b1e12-107">Homologues distants</span><span class="sxs-lookup"><span data-stu-id="b1e12-107">Remote Peers</span></span>

<span data-ttu-id="b1e12-108">Pour ajouter des paquets de réponse provenant de différents pairs au même fluide ALE, ajoutez un filtre dont l’option de [**\_ \_ \_ \_ \_ mappage de source libre de l’option de classement fwp**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) est définie sur la valeur d' **\_ option fwp activer le \_ \_ \_ \_ \_ mappage de source libre**.</span><span class="sxs-lookup"><span data-stu-id="b1e12-108">To add response packets from different peers to the same ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_LOOSE\_SOURCE\_MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option set to **FWP\_OPTION\_VALUE\_ENABLE\_LOOSE\_SOURCE\_MAPPING**.</span></span>

<span data-ttu-id="b1e12-109">Consultez [utilisation des options de classification pour l'](using-classify-options.md) exemple de code.</span><span class="sxs-lookup"><span data-stu-id="b1e12-109">See [Using Classify Options](using-classify-options.md) for code sample.</span></span>

## <a name="ale-flow-lifetime"></a><span data-ttu-id="b1e12-110">Durée de vie du flot ALE</span><span class="sxs-lookup"><span data-stu-id="b1e12-110">ALE Flow Lifetime</span></span>

<span data-ttu-id="b1e12-111">Pour modifier les valeurs du délai d’inactivité d’un fluide ALE, ajoutez un filtre avec l’option de durée de vie de l' [**\_ option de classification fwp \_ \_ \_ \_ Bcast**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) et/ou l’option de durée de vie **\_ \_ \_ \_ monodiffusion option de classement fwp** définie sur la valeur du délai d’inactivité souhaité.</span><span class="sxs-lookup"><span data-stu-id="b1e12-111">To modify the idle timeout values for an ALE flow, add a filter that has the [**FWP\_CLASSIFY\_OPTION\_MCAST\_BCAST\_LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) option and/or the **FWP\_CLASSIFY\_OPTION\_UNICAST\_LIFETIME** option set to the desired idle timeout value.</span></span>

<span data-ttu-id="b1e12-112">Consultez [utilisation des options de classification](using-classify-options.md) pour obtenir un exemple de code.</span><span class="sxs-lookup"><span data-stu-id="b1e12-112">See [Using Classify Options](using-classify-options.md) for a code sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1e12-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1e12-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1e12-114">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="b1e12-114">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="b1e12-115">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="b1e12-115">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="b1e12-116">Filtrage avec état ALE</span><span class="sxs-lookup"><span data-stu-id="b1e12-116">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="b1e12-117">Trafic de diffusion/multidiffusion ALE</span><span class="sxs-lookup"><span data-stu-id="b1e12-117">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="b1e12-118">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="b1e12-118">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="b1e12-119">Utilisation des options de classification</span><span class="sxs-lookup"><span data-stu-id="b1e12-119">Using Classify Options</span></span>](using-classify-options.md)
</dt> </dl>

 

 




