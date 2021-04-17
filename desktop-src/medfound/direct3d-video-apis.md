---
description: API vidéo Direct3D 9
ms.assetid: 2f5f46a0-f21f-4e57-9297-bad2b791da52
title: API vidéo Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7346741b5e78f052b7c895ca417735614930d35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524556"
---
# <a name="direct3d-9-video-apis"></a><span data-ttu-id="6b8e7-103">API vidéo Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="6b8e7-103">Direct3D 9 Video APIs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b8e7-104">Les applications du Windows Store doivent utiliser Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-104">Windows Store apps must use Microsoft Direct3D 11.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="6b8e7-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="6b8e7-105">In this section</span></span>



| <span data-ttu-id="6b8e7-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="6b8e7-106">Topic</span></span>                                                                       | <span data-ttu-id="6b8e7-107">Description</span><span class="sxs-lookup"><span data-stu-id="6b8e7-107">Description</span></span>                                                                                                                                 |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b8e7-108">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="6b8e7-108">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)<br/> | <span data-ttu-id="6b8e7-109">Décrit le contenu vidéo : les fonctionnalités de protection qu’un pilote Graphics peut fournir.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-109">Describes video content–protection capabilities that a graphics driver can provide.</span></span><br/>                                              |
| [<span data-ttu-id="6b8e7-110">Prise en charge de la superposition matérielle</span><span class="sxs-lookup"><span data-stu-id="6b8e7-110">Hardware Overlay Support</span></span>](hardware-overlay-support.md)<br/>         | <span data-ttu-id="6b8e7-111">Décrit comment utiliser les superpositions de matériel dans Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-111">Describes how to use hardware overlays in Direct3D 9.</span></span><br/>                                                                            |
| [<span data-ttu-id="6b8e7-112">Rapport de sollicitation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="6b8e7-112">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)<br/>       | <span data-ttu-id="6b8e7-113">La création de rapports sur la sollicitation de la mémoire permet à une application Direct3D de déterminer quand sa plage de travail de la mémoire vidéo est devenue trop importante.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-113">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span><br/>     |
| [<span data-ttu-id="6b8e7-114">Interfaces vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b8e7-114">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)<br/>       | <span data-ttu-id="6b8e7-115">Décrit les interfaces vidéo de Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-115">Describes the Microsoft Direct3D 9 video interfaces.</span></span><br/>                                                                             |
| [<span data-ttu-id="6b8e7-116">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b8e7-116">Direct3D Video Structures</span></span>](direct3d-video-structures.md)<br/>       | <span data-ttu-id="6b8e7-117">Décrit les structures utilisées par les interfaces vidéo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-117">Describes the structures used by the Direct3D 9 video interfaces.</span></span><br/>                                                                |
| [<span data-ttu-id="6b8e7-118">Énumérations de vidéos Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b8e7-118">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)<br/>   | <span data-ttu-id="6b8e7-119">Décrit les énumérations utilisées par les interfaces vidéo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b8e7-119">Describes the enumerations used by the Direct3D 9 video interfaces.</span></span><br/>                                                              |
| [<span data-ttu-id="6b8e7-120">Commandes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="6b8e7-120">Content Protection Commands</span></span>](content-protection-commands.md)<br/>   | <span data-ttu-id="6b8e7-121">Répertorie les commandes pour la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="6b8e7-121">Lists the commands for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span><br/> |
| [<span data-ttu-id="6b8e7-122">Requêtes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="6b8e7-122">Content Protection Queries</span></span>](content-protection-queries.md)<br/>     | <span data-ttu-id="6b8e7-123">Répertorie les requêtes pour la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="6b8e7-123">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="6b8e7-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b8e7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b8e7-125">Guide de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b8e7-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




