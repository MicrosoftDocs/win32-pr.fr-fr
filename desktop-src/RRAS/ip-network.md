---
title: Structure de IP_NETWORK (RTM. h)
description: La \_ structure du réseau IP décrit une adresse réseau IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- IP_NETWORK de la structure RAS
- Point d’accès RAS du pointeur de structure PIP_NETWORK
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742477"
---
# <a name="ip_network-structure"></a><span data-ttu-id="1f106-105">\_Structure de réseau IP</span><span class="sxs-lookup"><span data-stu-id="1f106-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="1f106-106">\[Cette API a été remplacée par l’API du [Gestionnaire de table de routage version 2](about-routing-table-manager-version-2.md) et n’est pas disponible au-delà de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f106-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1f106-107">Les applications doivent utiliser l’API du gestionnaire de table de routage version 2.\]</span><span class="sxs-lookup"><span data-stu-id="1f106-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1f106-108">La structure du **\_ réseau IP** décrit une adresse réseau IP.</span><span class="sxs-lookup"><span data-stu-id="1f106-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f106-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f106-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="1f106-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1f106-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f106-111">**N \_ numéro Netnumber**</span><span class="sxs-lookup"><span data-stu-id="1f106-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1f106-112">Spécifie le numéro de réseau IP exprimé comme une adresse IP dans l’ordre des octets de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1f106-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="1f106-113">**N \_ masque réseau**</span><span class="sxs-lookup"><span data-stu-id="1f106-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="1f106-114">Spécifie le masque de réseau.</span><span class="sxs-lookup"><span data-stu-id="1f106-114">Specifies the network mask.</span></span> <span data-ttu-id="1f106-115">Appliquez ce masque à l’adresse IP afin d’extraire l’adresse réseau.</span><span class="sxs-lookup"><span data-stu-id="1f106-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="1f106-116">Le masque de réseau est dans l’ordre des octets de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1f106-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f106-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f106-117">Requirements</span></span>



| <span data-ttu-id="1f106-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f106-118">Requirement</span></span> | <span data-ttu-id="1f106-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f106-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1f106-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f106-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f106-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f106-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="1f106-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f106-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f106-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f106-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1f106-124">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1f106-124">End of server support</span></span><br/>    | <span data-ttu-id="1f106-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f106-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1f106-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f106-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f106-127"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f106-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f106-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f106-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f106-129">Référence de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="1f106-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1f106-130">Structures de la version 1 du gestionnaire de tables de routage</span><span class="sxs-lookup"><span data-stu-id="1f106-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="1f106-131">**\_itinéraire IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="1f106-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





