---
title: Structure de IPX_NETWORK (RTM. h)
description: La \_ structure réseau IPX décrit une adresse réseau IPX.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- IPX_NETWORK de la structure RAS
- Point d’accès RAS du pointeur de structure PIPX_NETWORK
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941638"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="f835a-105">\_Structure de réseau IPX</span><span class="sxs-lookup"><span data-stu-id="f835a-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="f835a-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f835a-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f835a-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="f835a-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f835a-108">La **structure \_ réseau IPX** décrit une adresse réseau IPX.</span><span class="sxs-lookup"><span data-stu-id="f835a-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="f835a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f835a-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="f835a-110">Membres</span><span class="sxs-lookup"><span data-stu-id="f835a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f835a-111">**N \_ numéro Netnumber**</span><span class="sxs-lookup"><span data-stu-id="f835a-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="f835a-112">Contient le numéro de réseau IPX dans l’ordre des octets de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f835a-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f835a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f835a-113">Requirements</span></span>



| <span data-ttu-id="f835a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f835a-114">Requirement</span></span> | <span data-ttu-id="f835a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f835a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f835a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f835a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f835a-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f835a-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="f835a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f835a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f835a-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f835a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f835a-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f835a-120">End of server support</span></span><br/>    | <span data-ttu-id="f835a-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f835a-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f835a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f835a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f835a-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f835a-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f835a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f835a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f835a-125">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="f835a-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f835a-126">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="f835a-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="f835a-127">**\_itinéraire IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="f835a-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





