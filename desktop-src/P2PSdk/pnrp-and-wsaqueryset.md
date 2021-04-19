---
description: PNRP utilise la structure WSAQUERYSET conjointement avec diverses fonctions pour faciliter la résolution des noms et l’énumération des noms et des clouds.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP et WSAQUERYSET (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518783"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="86b85-103">PNRP et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="86b85-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="86b85-104">PNRP utilise la structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) conjointement avec diverses fonctions pour faciliter la résolution des noms et l’énumération des noms et des clouds.</span><span class="sxs-lookup"><span data-stu-id="86b85-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="86b85-105">Pour obtenir la définition complète des fonctions [**WSAQUERYSET**](winsock-nsp-reference-links.md) ou Windows Sockets, consultez leurs définitions respectives dans la documentation de l’API Windows Sockets 2 dans le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="86b85-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="86b85-106">WSAQUERYSET et WSASetService</span><span class="sxs-lookup"><span data-stu-id="86b85-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="86b85-107">La fonction [**WSASetService**](winsock-nsp-reference-links.md) utilise la structure **WSAQUERYSET** pour inscrire ou supprimer des noms d’homologue.</span><span class="sxs-lookup"><span data-stu-id="86b85-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="86b85-108">La page [PNRP et WSASetService](pnrp-and-wsasetservice.md) explique comment utiliser la structure **WSAQUERYSET** avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="86b85-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="86b85-109">WSAQUERYSET et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="86b85-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="86b85-110">La structure [**WSAQUERYSET**](winsock-nsp-reference-links.md) est largement utilisée avec les fonctions **WSALookupServiceBegin**, **WSALookupServiceNext** et **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="86b85-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="86b85-111">Les détails sur la façon dont ces fonctions utilisent la structure **WSAQUERYSET** sont détaillés dans les pages de référence suivantes :</span><span class="sxs-lookup"><span data-stu-id="86b85-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="86b85-112">PNRP et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="86b85-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="86b85-113">PNRP et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="86b85-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="86b85-114">PNRP et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="86b85-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="86b85-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86b85-115">Requirements</span></span>



| <span data-ttu-id="86b85-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86b85-116">Requirement</span></span> | <span data-ttu-id="86b85-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="86b85-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="86b85-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86b85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86b85-119">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86b85-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="86b85-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86b85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86b85-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86b85-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="86b85-122">Version</span><span class="sxs-lookup"><span data-stu-id="86b85-122">Version</span></span><br/>                  | <span data-ttu-id="86b85-123">Windows XP avec SP1 avec le Pack de mise en réseau avancée pour Windows XP</span><span class="sxs-lookup"><span data-stu-id="86b85-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="86b85-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="86b85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="86b85-125"><dt>P2P. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b85-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86b85-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86b85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b85-127">PNRP et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="86b85-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="86b85-128">PNRP et WSASetService</span><span class="sxs-lookup"><span data-stu-id="86b85-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




