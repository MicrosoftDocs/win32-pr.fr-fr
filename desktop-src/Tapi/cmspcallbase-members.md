---
description: La liste suivante contient les membres CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Membres CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203022"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="89481-103">Membres CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="89481-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="89481-104">Type de membre</span><span class="sxs-lookup"><span data-stu-id="89481-104">Member type</span></span>                   | <span data-ttu-id="89481-105">Nom</span><span class="sxs-lookup"><span data-stu-id="89481-105">Name</span></span>             | <span data-ttu-id="89481-106">Description</span><span class="sxs-lookup"><span data-stu-id="89481-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89481-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="89481-107">IUnknown</span></span>                      | <span data-ttu-id="89481-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="89481-108">\*m\_pFTM</span></span>        | <span data-ttu-id="89481-109">Pointeur vers le marshaleur libre de threads.</span><span class="sxs-lookup"><span data-stu-id="89481-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="89481-110">CMSPAddress\*</span><span class="sxs-lookup"><span data-stu-id="89481-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="89481-111">\*m \_ pMSPAddress</span><span class="sxs-lookup"><span data-stu-id="89481-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="89481-112">Pointeur vers l’objet d’adresse MSP.</span><span class="sxs-lookup"><span data-stu-id="89481-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="89481-113">Il est utilisé pour récupérer les terminaux par défaut si l’application ne la sélectionne pas.</span><span class="sxs-lookup"><span data-stu-id="89481-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="89481-114">Il comporte également un refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), et non AddRef) afin que l’adresse agrégée ne disparaissent pas pendant que l’appel est toujours actif, mais que l’adresse de l’interface TAPI 3 n’est pas AddRef’ed.</span><span class="sxs-lookup"><span data-stu-id="89481-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="89481-115">\_handle MSP</span><span class="sxs-lookup"><span data-stu-id="89481-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="89481-116">\*m \_ htCall</span><span class="sxs-lookup"><span data-stu-id="89481-116">\*m\_htCall</span></span>      | <span data-ttu-id="89481-117">Handle de l’appel de TAPI3's.</span><span class="sxs-lookup"><span data-stu-id="89481-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="89481-118">Utilisé pour déclencher des événements d’appel.</span><span class="sxs-lookup"><span data-stu-id="89481-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="89481-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="89481-119">DWORD</span></span>                         | <span data-ttu-id="89481-120">m \_ dwMediaType</span><span class="sxs-lookup"><span data-stu-id="89481-120">m\_dwMediaType</span></span>   | <span data-ttu-id="89481-121">Masque de rébinaire des types de média sur cet appel.</span><span class="sxs-lookup"><span data-stu-id="89481-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="89481-122">CMSPArray <ITStream \*></span><span class="sxs-lookup"><span data-stu-id="89481-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="89481-123">\_flux m</span><span class="sxs-lookup"><span data-stu-id="89481-123">m\_Streams</span></span>       | <span data-ttu-id="89481-124">Liste des objets de flux dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="89481-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="89481-125">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="89481-125">CMSPCritSection</span></span>               | <span data-ttu-id="89481-126">\_verrou m</span><span class="sxs-lookup"><span data-stu-id="89481-126">m\_lock</span></span>          | <span data-ttu-id="89481-127">Verrou qui protège les listes de flux.</span><span class="sxs-lookup"><span data-stu-id="89481-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="89481-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89481-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89481-129">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="89481-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



