---
description: Les énumérations suivantes sont utilisées pour spécifier des informations sur la façon dont les ressources sont créées et accessibles pendant le rendu.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Énumérations de ressources (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033786"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a><span data-ttu-id="1652b-103">Énumérations de ressources (graphiques Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="1652b-103">Resource Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="1652b-104">Les énumérations suivantes sont utilisées pour spécifier des informations sur la façon dont les ressources sont créées et accessibles pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="1652b-104">The following enumerations are used to specify information about how resources are created and accessed during rendering.</span></span>



| <span data-ttu-id="1652b-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="1652b-105">Enumeration</span></span>                                                     | <span data-ttu-id="1652b-106">Description</span><span class="sxs-lookup"><span data-stu-id="1652b-106">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1652b-107">**\_Indicateur de liaison D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-107">**D3D10\_BIND\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | <span data-ttu-id="1652b-108">Identifie la manière dont une ressource sera utilisée par le pipeline et détermine la ou les étapes de pipeline auxquelles une ressource peut être liée.</span><span class="sxs-lookup"><span data-stu-id="1652b-108">Identifies how a resource will be used by the pipeline and determines which pipeline stage(s) a resource can be bound to.</span></span> |
| [<span data-ttu-id="1652b-109">**\_Indicateur d' \_ accès au processeur D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-109">**D3D10\_CPU\_ACCESS\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | <span data-ttu-id="1652b-110">Spécifie les types d’accès de l’UC autorisés pour une ressource.</span><span class="sxs-lookup"><span data-stu-id="1652b-110">Specifies the types of CPU access allowed for a resource.</span></span>                                                                 |
| [<span data-ttu-id="1652b-111">**\_Dimension DSV \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="1652b-111">**D3D10\_DSV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | <span data-ttu-id="1652b-112">Spécifie comment accéder à une ressource qui est utilisée dans une vue de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="1652b-112">Specifies how to access a resource that is used in a depth-stencil view.</span></span>                                                  |
| [<span data-ttu-id="1652b-113">**Carte de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-113">**D3D10\_MAP**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | <span data-ttu-id="1652b-114">Identifie une ressource à mapper pour la lecture et l’écriture par l’UC.</span><span class="sxs-lookup"><span data-stu-id="1652b-114">Identifies a resource to be mapped for reading and writing by the CPU.</span></span>                                                    |
| [<span data-ttu-id="1652b-115">**\_Indicateur de carte de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-115">**D3D10\_MAP\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | <span data-ttu-id="1652b-116">Spécifie la façon dont l’UC doit répondre à toutes les méthodes cartographiques lorsque le GPU n’est pas encore terminé avec la ressource.</span><span class="sxs-lookup"><span data-stu-id="1652b-116">Specifies how the CPU should respond to any Map methods when the GPU is not yet finished with the resource.</span></span>               |
| [<span data-ttu-id="1652b-117">**\_Dimension de ressource D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-117">**D3D10\_RESOURCE\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | <span data-ttu-id="1652b-118">Identifie le type de ressource en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="1652b-118">Identifies the type of resource that is in use.</span></span>                                                                           |
| [<span data-ttu-id="1652b-119">**\_ \_ Indicateur div de la ressource D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-119">**D3D10\_RESOURCE\_MISC\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | <span data-ttu-id="1652b-120">Identifie les options de création de ressources moins courantes.</span><span class="sxs-lookup"><span data-stu-id="1652b-120">Identifies less common resource creation options.</span></span>                                                                         |
| [<span data-ttu-id="1652b-121">**\_Dimension D3D10 RTV \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-121">**D3D10\_RTV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | <span data-ttu-id="1652b-122">Spécifie comment accéder à une ressource utilisée dans une vue de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="1652b-122">Specifies how to access a resource used in a render target view.</span></span>                                                          |
| [<span data-ttu-id="1652b-123">**Utilisation de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="1652b-123">**D3D10\_USAGE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | <span data-ttu-id="1652b-124">Identifie la manière dont une ressource est supposée être lue et écrite par l’UC et/ou le GPU.</span><span class="sxs-lookup"><span data-stu-id="1652b-124">Identifies how a resource is expected to be read and written by the CPU and/or the GPU.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="1652b-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1652b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1652b-126">Référence de ressource</span><span class="sxs-lookup"><span data-stu-id="1652b-126">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



