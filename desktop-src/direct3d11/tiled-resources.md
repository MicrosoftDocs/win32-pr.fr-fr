---
title: Ressources en mosaïque
description: Les ressources en mosaïque peuvent être considérées comme des ressources logiques volumineuses qui utilisent de petites quantités de mémoire physique.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839433"
---
# <a name="tiled-resources"></a><span data-ttu-id="50b4a-103">Ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="50b4a-103">Tiled resources</span></span>

<span data-ttu-id="50b4a-104">Les ressources en mosaïque peuvent être considérées comme des ressources logiques volumineuses qui utilisent de petites quantités de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="50b4a-104">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span>

<span data-ttu-id="50b4a-105">Cette section décrit les raisons pour lesquelles des ressources en mosaïque sont nécessaires et comment créer et utiliser des ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="50b4a-105">This section describes why tiled resources are needed and how you create and use tiled resources.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50b4a-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="50b4a-106">In this section</span></span>



| <span data-ttu-id="50b4a-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="50b4a-107">Topic</span></span>                                                                                   | <span data-ttu-id="50b4a-108">Description</span><span class="sxs-lookup"><span data-stu-id="50b4a-108">Description</span></span>                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50b4a-109">Pourquoi les ressources en mosaïque sont-elles nécessaires ?</span><span class="sxs-lookup"><span data-stu-id="50b4a-109">Why are tiled resources needed?</span></span>](why-are-tiled-resources-needed-.md)<br/>       | <span data-ttu-id="50b4a-110">Les ressources en mosaïque sont nécessaires afin que la mémoire de l’unité de traitement graphique (GPU) soit gaspillée pour stocker des régions de surfaces inaccessibles par l’application, et le matériel peut comprendre comment filtrer sur des vignettes adjacentes.</span><span class="sxs-lookup"><span data-stu-id="50b4a-110">Tiled resources are needed so less graphics processing unit (GPU) memory is wasted storing regions of surfaces that the application knows will not be accessed, and the hardware can understand how to filter across adjacent tiles.</span></span><br/>     |
| [<span data-ttu-id="50b4a-111">Création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="50b4a-111">Creating tiled resources</span></span>](creating-tiled-resources.md)<br/>                     | <span data-ttu-id="50b4a-112">Les ressources en mosaïque sont créées en spécifiant l’indicateur de [**\_ \_ \_ mosaïque diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) quand vous créez une ressource.</span><span class="sxs-lookup"><span data-stu-id="50b4a-112">Tiled resources are created by specifying the [**D3D11\_RESOURCE\_MISC\_TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag when you create a resource.</span></span><br/>                                                                                          |
| [<span data-ttu-id="50b4a-113">API de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="50b4a-113">Tiled Resource APIs</span></span>](tiled-resource-apis.md)<br/>                               | <span data-ttu-id="50b4a-114">Les API décrites dans cette section fonctionnent avec les ressources en mosaïque et le pool de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="50b4a-114">The APIs described in this section work with tiled resources and tile pool.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="50b4a-115">Accès du pipeline aux ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="50b4a-115">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)<br/> | <span data-ttu-id="50b4a-116">Les ressources en mosaïque peuvent être utilisées dans les vues de ressource de nuanceur (SRV), les affichages de cible de rendu (RTV), les vues de stencil de profondeur (DSV) et les vues d’accès non ordonnées (UAV), ainsi que certains points de liaison où les vues ne sont pas utilisées, telles que les liaisons de mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="50b4a-116">Tiled resources can be used in shader resource views (SRV), render target views (RTV), depth stencil views (DSV) and unordered access views (UAV), as well as some bind points where views aren't used, such as vertex buffer bindings.</span></span> <br/> |
| [<span data-ttu-id="50b4a-117">Niveaux de fonctionnalités des ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="50b4a-117">Tiled resources features tiers</span></span>](tiled-resources-features-tiers.md)<br/>         | <span data-ttu-id="50b4a-118">Direct3D 11,2 expose la prise en charge des ressources en mosaïque dans deux niveaux avec les valeurs de [**\_ niveau de \_ ressources \_ en mosaïque d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) .</span><span class="sxs-lookup"><span data-stu-id="50b4a-118">Direct3D 11.2 exposes tiled resources support in two tiers with the [**D3D11\_TILED\_RESOURCES\_TIER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) values.</span></span> <br/>                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="50b4a-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50b4a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b4a-120">Ressources</span><span class="sxs-lookup"><span data-stu-id="50b4a-120">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





