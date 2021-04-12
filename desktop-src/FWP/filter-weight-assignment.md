---
title: Affectation de poids de filtre
description: Chaque filtre de la plateforme de filtrage Windows (WFP) est associé à un poids, qui est utilisé pendant l’arbitrage des filtres.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/26/2020
ms.locfileid: "104381705"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="d319c-103">Affectation de poids de filtre</span><span class="sxs-lookup"><span data-stu-id="d319c-103">Filter Weight Assignment</span></span>

<span data-ttu-id="d319c-104">Chaque filtre de la plateforme de filtrage Windows (WFP) est associé à un poids, qui est utilisé pendant l' [arbitrage des filtres](filter-arbitration.md).</span><span class="sxs-lookup"><span data-stu-id="d319c-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="d319c-105">Le poids de filtre utilisé par le moteur de filtrage de base (BFE) est de type [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="d319c-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="d319c-106">Les appelants ont trois options lors de l’ajout de filtres.</span><span class="sxs-lookup"><span data-stu-id="d319c-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="d319c-107">Définissez le poids sur un [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="d319c-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="d319c-108">BFE utilise le poids fourni tel quel.</span><span class="sxs-lookup"><span data-stu-id="d319c-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="d319c-109">Définissez le poids sur [**fwp \_ vide**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="d319c-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="d319c-110">BFE génère automatiquement un poids dans la plage \[ 0, 2 ⁶ ⁰).</span><span class="sxs-lookup"><span data-stu-id="d319c-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="d319c-111">Définissez le poids sur un [**\_ UINT8 UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) dans la plage \[ 0, 15 \] .</span><span class="sxs-lookup"><span data-stu-id="d319c-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="d319c-112">BFE utilise le poids fourni comme identificateur de plage de poids.</span><span class="sxs-lookup"><span data-stu-id="d319c-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="d319c-113">BFE génère automatiquement les bits de poids faible 60 (exactement comme si le poids avait été défini sur [**fwp \_ vide**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), puis utilise la valeur fournie pour définir les 4 bits de poids fort.</span><span class="sxs-lookup"><span data-stu-id="d319c-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="d319c-114">Cela permet aux appelants de diviser manuellement l’espace de poids en 16 plages, tout en continuant à utiliser la pondération automatique au sein d’une plage.</span><span class="sxs-lookup"><span data-stu-id="d319c-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="d319c-115">Lorsque deux ou plusieurs légendes sont inscrites sur la même sous-couche, des problèmes peuvent se produire lorsque le même poids est affecté aux filtres.</span><span class="sxs-lookup"><span data-stu-id="d319c-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="d319c-116">Ce problème peut être évité en faisant en sorte que les légendes créent leur propre sous-couche à l’aide de [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span><span class="sxs-lookup"><span data-stu-id="d319c-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d319c-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d319c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d319c-118">**Identificateurs de poids de filtre**</span><span class="sxs-lookup"><span data-stu-id="d319c-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




