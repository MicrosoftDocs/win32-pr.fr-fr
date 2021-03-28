---
title: Niveaux de fonctionnalités des ressources en mosaïque
description: Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les \_ valeurs de niveau de ressources en mosaïque d3d11 \_ \_ .
ms.assetid: E6A6565B-079B-47DB-A80C-CA5B5413BA32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2282cde1dfc8c4249672d18e303a4529338d4fbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939718"
---
# <a name="tiled-resources-features-tiers"></a><span data-ttu-id="7a721-103">Niveaux de fonctionnalités des ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="7a721-103">Tiled resources features tiers</span></span>

<span data-ttu-id="7a721-104">Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les valeurs de [**\_ niveau de \_ ressources \_ en mosaïque d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="7a721-104">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span>

<span data-ttu-id="7a721-105">Pour déterminer si le matériel et les pilotes prennent en charge les ressources en mosaïque et au niveau du niveau, transmettez la [**d3d11 \_ fonctionnalité \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) à la valeur du paramètre *Feature* de [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="7a721-105">To query whether the hardware and driver support tiled resources and at what tier level, pass the [**D3D11\_FEATURE\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) value to the *Feature* parameter of [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport).</span></span> <span data-ttu-id="7a721-106">En outre, transmettez un pointeur vers la structure de données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ options1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) vers le paramètre *pFeatureSupportData* , puis transmettez la taille de la de données de la **\_ fonctionnalité \_ \_ \_** d3d11 à la structure d3d11 au paramètre *options1* .</span><span class="sxs-lookup"><span data-stu-id="7a721-106">Also, pass a pointer to the [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1) structure to the *pFeatureSupportData* parameter, and pass the size of the **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1** structure to the *FeatureSupportDataSize* parameter.</span></span> <span data-ttu-id="7a721-107">**CheckFeatureSupport** retourne le niveau de couche sous la forme d’une valeur de [**niveau de \_ \_ ressources \_ en mosaïque d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) dans le membre **TiledResourcesTier** des données de la **\_ fonctionnalité d3d11 \_ \_ d3d11 \_ options1**.</span><span class="sxs-lookup"><span data-stu-id="7a721-107">**CheckFeatureSupport** returns the tier level as a [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) value in the **TiledResourcesTier** member of **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS1**.</span></span>

<span data-ttu-id="7a721-108">Cette section décrit ces deux niveaux.</span><span class="sxs-lookup"><span data-stu-id="7a721-108">This section describes these two tiers.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7a721-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="7a721-109">In this section</span></span>



| <span data-ttu-id="7a721-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7a721-110">Topic</span></span>                           | <span data-ttu-id="7a721-111">Description</span><span class="sxs-lookup"><span data-stu-id="7a721-111">Description</span></span>                                       |
|---------------------------------|---------------------------------------------------|
| [<span data-ttu-id="7a721-112">Niveau 1</span><span class="sxs-lookup"><span data-stu-id="7a721-112">Tier 1</span></span>](tier-1.md)<br/> | <span data-ttu-id="7a721-113">Cette section décrit la prise en charge de niveau 1.</span><span class="sxs-lookup"><span data-stu-id="7a721-113">This section describes tier 1 support.</span></span><br/> |
| [<span data-ttu-id="7a721-114">Niveau 2</span><span class="sxs-lookup"><span data-stu-id="7a721-114">Tier 2</span></span>](tier-2.md)<br/> | <span data-ttu-id="7a721-115">Cette section décrit le support de niveau 2.</span><span class="sxs-lookup"><span data-stu-id="7a721-115">This section describes tier 2 support.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7a721-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a721-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a721-117">Ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="7a721-117">Tiled resources</span></span>](tiled-resources.md)
</dt> </dl>

 

 





