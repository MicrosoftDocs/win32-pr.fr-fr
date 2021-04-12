---
title: Structure de IPX_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ structure d' \_ adresse de tronçon suivant IPX \_ contient l’adresse du routeur de tronçon suivant pour un itinéraire IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- IPX_NEXT_HOP_ADDRESS de la structure RAS
- Point d’accès RAS du pointeur de structure PIPX_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464202"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="4402a-105">\_Structure d' \_ adresse de tronçon suivant IPX \_</span><span class="sxs-lookup"><span data-stu-id="4402a-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="4402a-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4402a-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="4402a-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="4402a-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="4402a-108">La structure d' **\_ \_ \_ adresse de tronçon suivant IPX** contient l’adresse du routeur de tronçon suivant pour un itinéraire IPX.</span><span class="sxs-lookup"><span data-stu-id="4402a-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="4402a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4402a-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="4402a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4402a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="4402a-111">**NHA \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="4402a-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="4402a-112">Spécifie l’adresse MAC du routeur du tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="4402a-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4402a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4402a-113">Requirements</span></span>



| <span data-ttu-id="4402a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4402a-114">Requirement</span></span> | <span data-ttu-id="4402a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4402a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4402a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4402a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4402a-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4402a-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="4402a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4402a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4402a-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4402a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4402a-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="4402a-120">End of server support</span></span><br/>    | <span data-ttu-id="4402a-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4402a-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="4402a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4402a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4402a-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4402a-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4402a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4402a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4402a-125">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="4402a-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="4402a-126">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="4402a-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="4402a-127">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="4402a-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





