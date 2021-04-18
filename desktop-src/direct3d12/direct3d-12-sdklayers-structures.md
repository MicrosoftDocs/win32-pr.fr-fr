---
title: Structures de couche de débogage
description: Les structures suivantes sont déclarées dans d3d12sdklayers. h.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106533544"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="2af76-103">Structures de couche de débogage</span><span class="sxs-lookup"><span data-stu-id="2af76-103">Debug Layer Structures</span></span>

<span data-ttu-id="2af76-104">Les structures suivantes sont déclarées dans d3d12sdklayers. h.</span><span class="sxs-lookup"><span data-stu-id="2af76-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2af76-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="2af76-105">In this section</span></span>



| <span data-ttu-id="2af76-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="2af76-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="2af76-107">Description</span><span class="sxs-lookup"><span data-stu-id="2af76-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2af76-108">**\_Liste de commandes de débogage D3D12 \_ \_ \_ \_ \_ paramètres de validation basés sur GPU \_**</span><span class="sxs-lookup"><span data-stu-id="2af76-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="2af76-109">Décrit les paramètres par liste de commandes utilisés par GPU-Based validation.</span><span class="sxs-lookup"><span data-stu-id="2af76-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="2af76-110">**D3D12 \_ déboguer les \_ \_ \_ paramètres de validation basés sur GPU \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2af76-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="2af76-111">Décrit les paramètres utilisés par la validation de GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="2af76-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="2af76-112">**\_Facteur de \_ \_ performance de \_ ralentissement du GPU de \_ l’appareil de débogage D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="2af76-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="2af76-113">Décrit la quantité de ralentissement artificiel insérée par le périphérique de débogage pour simuler des cartes graphiques de moindre performance.</span><span class="sxs-lookup"><span data-stu-id="2af76-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="2af76-114">**\_Filtre de \_ file d’attente d’informations D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="2af76-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="2af76-115">Filtre de messages de débogage ; contient une liste de types de messages à autoriser ou refuser.</span><span class="sxs-lookup"><span data-stu-id="2af76-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="2af76-116">**Description du filtre de la \_ \_ file d’attente D3D12 info \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2af76-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="2af76-117">Autorisez ou refusez que certains types de messages passent par un filtre.</span><span class="sxs-lookup"><span data-stu-id="2af76-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="2af76-118">**\_Message D3D12**</span><span class="sxs-lookup"><span data-stu-id="2af76-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="2af76-119">Message de débogage dans la file d’attente d’informations.</span><span class="sxs-lookup"><span data-stu-id="2af76-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="2af76-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2af76-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2af76-121">Configuration de l’environnement de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2af76-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="2af76-122">Référence de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="2af76-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="2af76-123">Référence de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="2af76-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





