---
description: Méthodes virtuelles pures CMSPCallBase-ces méthodes doivent être substituées par des classes dérivées.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase des méthodes virtuelles pures
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094457"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="48469-103">CMSPCallBase des méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="48469-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="48469-104">Ces méthodes doivent être remplacées par des classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="48469-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="48469-105">CMSPCallBase des méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="48469-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="48469-106">Description</span><span class="sxs-lookup"><span data-stu-id="48469-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48469-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="48469-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="48469-108">Méthode de AddRef privée pour l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="48469-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="48469-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="48469-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="48469-110">Méthode de mise en sortie privée pour l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="48469-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="48469-111">**Rein**</span><span class="sxs-lookup"><span data-stu-id="48469-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="48469-112">Appelée par l’objet d’adresse MSP (dans la méthode [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) pour initialiser l’objet d’appel MSP.</span><span class="sxs-lookup"><span data-stu-id="48469-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="48469-113">**Correct**</span><span class="sxs-lookup"><span data-stu-id="48469-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="48469-114">Appelé par l’objet d’adresse MSP pour arrêter l’appel..</span><span class="sxs-lookup"><span data-stu-id="48469-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="48469-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="48469-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="48469-116">Appelée par [**CreateStream,**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) pour créer un objet de flux.</span><span class="sxs-lookup"><span data-stu-id="48469-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="48469-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="48469-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="48469-118">Appelée par [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) pour créer un objet de flux.</span><span class="sxs-lookup"><span data-stu-id="48469-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="48469-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="48469-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="48469-120">Appelé par l’application pour supprimer un flux de l’appel</span><span class="sxs-lookup"><span data-stu-id="48469-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="48469-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="48469-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48469-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="48469-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
