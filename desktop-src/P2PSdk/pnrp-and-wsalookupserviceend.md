---
description: PNRP utilise la fonction WSALookupServiceEnd pour effectuer les opérations suivantes.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP et WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541859"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="0a91d-103">PNRP et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="0a91d-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="0a91d-104">PNRP utilise la fonction [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a91d-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="0a91d-105">Terminer une requête lancée lors d’un appel précédent à [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="0a91d-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="0a91d-106">Débloquer un appel à [**WSALookupServiceNext**](winsock-nsp-reference-links.md) pour arrêter la recherche</span><span class="sxs-lookup"><span data-stu-id="0a91d-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="0a91d-107">Un appel à [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) met fin à une requête et nettoie le contexte.</span><span class="sxs-lookup"><span data-stu-id="0a91d-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="0a91d-108">Le handle obtenu à partir d’un appel à **WSALookupServiceBegin** doit être passé en tant que paramètre à **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="0a91d-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="0a91d-109">Pour plus d’informations sur PNRP et la fonction [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , consultez [PNRP et WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="0a91d-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a91d-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a91d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a91d-111">PNRP et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="0a91d-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="0a91d-112">Codes d’erreur du NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="0a91d-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="0a91d-113">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="0a91d-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



