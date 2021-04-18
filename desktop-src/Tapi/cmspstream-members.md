---
description: La liste suivante contient les membres CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Membres CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115603"
---
# <a name="cmspstream-members"></a><span data-ttu-id="bec4e-103">Membres CMSPStream</span><span class="sxs-lookup"><span data-stu-id="bec4e-103">CMSPStream Members</span></span>



| <span data-ttu-id="bec4e-104">Type de membre</span><span class="sxs-lookup"><span data-stu-id="bec4e-104">Member type</span></span>                     | <span data-ttu-id="bec4e-105">Nom</span><span class="sxs-lookup"><span data-stu-id="bec4e-105">Name</span></span>                | <span data-ttu-id="bec4e-106">Description</span><span class="sxs-lookup"><span data-stu-id="bec4e-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bec4e-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="bec4e-107">IUnknown</span></span>                        | <span data-ttu-id="bec4e-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="bec4e-108">\*m\_pFTM</span></span>           | <span data-ttu-id="bec4e-109">Pointeur vers le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="bec4e-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="bec4e-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="bec4e-110">DWORD</span></span>                           | <span data-ttu-id="bec4e-111">m \_ dwState</span><span class="sxs-lookup"><span data-stu-id="bec4e-111">m\_dwState</span></span>          | <span data-ttu-id="bec4e-112">État actuel du flux.</span><span class="sxs-lookup"><span data-stu-id="bec4e-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="bec4e-113">HANDLE</span><span class="sxs-lookup"><span data-stu-id="bec4e-113">HANDLE</span></span>                          | <span data-ttu-id="bec4e-114">m \_ hAddress</span><span class="sxs-lookup"><span data-stu-id="bec4e-114">m\_hAddress</span></span>         | <span data-ttu-id="bec4e-115">Adresse sur laquelle ce flux est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bec4e-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="bec4e-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="bec4e-116">DWORD</span></span>                           | <span data-ttu-id="bec4e-117">m \_ dwMediaType</span><span class="sxs-lookup"><span data-stu-id="bec4e-117">m\_dwMediaType</span></span>      | <span data-ttu-id="bec4e-118">[**Type de média**](tapimediatype--constants.md) de ce flux (audio, vidéo, etc.).</span><span class="sxs-lookup"><span data-stu-id="bec4e-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="bec4e-119">DIRECTION du TERMINAL \_</span><span class="sxs-lookup"><span data-stu-id="bec4e-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="bec4e-120">\_direction m</span><span class="sxs-lookup"><span data-stu-id="bec4e-120">m\_Direction</span></span>        | <span data-ttu-id="bec4e-121">[**Direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) de ce flux (entrant ou sortant).</span><span class="sxs-lookup"><span data-stu-id="bec4e-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="bec4e-122">CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="bec4e-122">CMSPCallBase</span></span>                    | <span data-ttu-id="bec4e-123">\*m \_ pMSPCall</span><span class="sxs-lookup"><span data-stu-id="bec4e-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="bec4e-124">Pointeur vers l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="bec4e-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="bec4e-125">IGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="bec4e-125">IGraphBuilder</span></span>                   | <span data-ttu-id="bec4e-126">\*m \_ pIGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="bec4e-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="bec4e-127">Pointeur vers les interfaces d’objet de graphique.</span><span class="sxs-lookup"><span data-stu-id="bec4e-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="bec4e-128">Appel</span><span class="sxs-lookup"><span data-stu-id="bec4e-128">IMediaControl</span></span>                   | <span data-ttu-id="bec4e-129">\*m \_ pIMediaControl</span><span class="sxs-lookup"><span data-stu-id="bec4e-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="bec4e-130">Pointeur vers l’interface de contrôle de média.</span><span class="sxs-lookup"><span data-stu-id="bec4e-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="bec4e-131">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="bec4e-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="bec4e-132">\_terminaux m</span><span class="sxs-lookup"><span data-stu-id="bec4e-132">m\_Terminals</span></span>        | <span data-ttu-id="bec4e-133">Liste des terminaux sur le flux.</span><span class="sxs-lookup"><span data-stu-id="bec4e-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="bec4e-134">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="bec4e-134">CMSPCritSection</span></span>                 | <span data-ttu-id="bec4e-135">\_verrou m</span><span class="sxs-lookup"><span data-stu-id="bec4e-135">m\_lock</span></span>             | <span data-ttu-id="bec4e-136">Verrou qui protège l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="bec4e-136">The lock that protects the stream object.</span></span> <span data-ttu-id="bec4e-137">L’objet de flux ne doit jamais acquérir le verrou, puis appeler une méthode MSPCall qui peut être verrouillée.</span><span class="sxs-lookup"><span data-stu-id="bec4e-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bec4e-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bec4e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bec4e-139">**CMSPStream**</span><span class="sxs-lookup"><span data-stu-id="bec4e-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



