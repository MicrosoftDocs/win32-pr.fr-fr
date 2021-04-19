---
title: Structure de IP_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ structure d' \_ adresse IP de tronçon suivant \_ contient l’adresse du routeur de tronçon suivant pour un itinéraire IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS de la structure RAS
- PIP_NEXT_HOP_ADDRESS de la structure RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511583"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="1a9d7-105">Structure d’adresse IP de \_ \_ tronçon suivant \_</span><span class="sxs-lookup"><span data-stu-id="1a9d7-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="1a9d7-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1a9d7-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="1a9d7-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1a9d7-108">La structure d' **adresse IP de \_ \_ tronçon \_ suivant** contient l’adresse du routeur de tronçon suivant pour un itinéraire IP.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a9d7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a9d7-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="1a9d7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1a9d7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1a9d7-111">**N \_ numéro Netnumber**</span><span class="sxs-lookup"><span data-stu-id="1a9d7-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1a9d7-112">Spécifie l’adresse réseau IP exprimée sous la forme d’une adresse IP dans l’ordre des octets de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="1a9d7-113">**N \_ masque réseau**</span><span class="sxs-lookup"><span data-stu-id="1a9d7-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="1a9d7-114">Spécifie le masque de réseau.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-114">Specifies the network mask.</span></span> <span data-ttu-id="1a9d7-115">Appliquez ce masque à l’adresse IP afin d’extraire l’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="1a9d7-116">Le masque de réseau est dans l’ordre des octets de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a9d7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1a9d7-117">Remarks</span></span>

<span data-ttu-id="1a9d7-118">La structure d' **\_ \_ \_ adresse de tronçon suivant IP** est un typedef de la structure de [**\_ réseau IP**](ip-network.md) .</span><span class="sxs-lookup"><span data-stu-id="1a9d7-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="1a9d7-119">Le typedef se trouve dans RTM. h.</span><span class="sxs-lookup"><span data-stu-id="1a9d7-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a9d7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a9d7-120">Requirements</span></span>



| <span data-ttu-id="1a9d7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a9d7-121">Requirement</span></span> | <span data-ttu-id="1a9d7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a9d7-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1a9d7-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a9d7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a9d7-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a9d7-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="1a9d7-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a9d7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a9d7-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a9d7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1a9d7-127">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1a9d7-127">End of server support</span></span><br/>    | <span data-ttu-id="1a9d7-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1a9d7-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1a9d7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a9d7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a9d7-130"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a9d7-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a9d7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a9d7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a9d7-132">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="1a9d7-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1a9d7-133">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="1a9d7-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="1a9d7-134">**\_réseau IP**</span><span class="sxs-lookup"><span data-stu-id="1a9d7-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="1a9d7-135">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="1a9d7-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





