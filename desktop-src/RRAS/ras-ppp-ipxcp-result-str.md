---
title: Structure RAS_PPP_IPXCP_RESULT (rassapi. h)
description: La \_ structure du résultat d’accès distant PPP ppp \_ \_ est utilisée pour signaler le résultat d’une opération de projection PPP Internetwork Packet Exchange (IPX) pour un port.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032936"
---
# <a name="ras_ppp_ipxcp_result-structure"></a><span data-ttu-id="c2ba1-104">Structure des résultats du protocole d’accès distant \_ PPP \_ IPXCP \_</span><span class="sxs-lookup"><span data-stu-id="c2ba1-104">RAS\_PPP\_IPXCP\_RESULT structure</span></span>

<span data-ttu-id="c2ba1-105">\[La structure des **\_ \_ \_ résultats IPXCP PPP d’accès distant** n’est pas prise en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="c2ba1-105">\[The **RAS\_PPP\_IPXCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="c2ba1-106">La structure du **\_ \_ \_ résultat d’accès distant PPP ppp** est utilisée pour signaler le résultat d’une opération de projection PPP Internetwork Packet Exchange (IPX) pour un port.</span><span class="sxs-lookup"><span data-stu-id="c2ba1-106">The **RAS\_PPP\_IPXCP\_RESULT** structure is used to report the result of a PPP Internetwork Packet Exchange (IPX) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ba1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2ba1-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="c2ba1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c2ba1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2ba1-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="c2ba1-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="c2ba1-110">Indique les résultats de l’opération de projection IPX.</span><span class="sxs-lookup"><span data-stu-id="c2ba1-110">Indicates the results of the IPX projection operation.</span></span> <span data-ttu-id="c2ba1-111">La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszAddress** est valide.</span><span class="sxs-lookup"><span data-stu-id="c2ba1-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="c2ba1-112">En cas d’échec de l’opération de projection, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="c2ba1-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="c2ba1-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="c2ba1-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="c2ba1-114">Chaîne Unicode terminée par le caractère null qui spécifie l’adresse IPX assignée au client distant.</span><span class="sxs-lookup"><span data-stu-id="c2ba1-114">A null-terminated Unicode string that specifies the IPX address assigned to the remote client.</span></span> <span data-ttu-id="c2ba1-115">Cette chaîne a le \* net \***.** formulaire de _nœud_ .</span><span class="sxs-lookup"><span data-stu-id="c2ba1-115">This string has the \*net\***.**_node_ form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2ba1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2ba1-116">Requirements</span></span>



| <span data-ttu-id="c2ba1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2ba1-117">Requirement</span></span> | <span data-ttu-id="c2ba1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2ba1-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ba1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2ba1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ba1-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2ba1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c2ba1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2ba1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ba1-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2ba1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c2ba1-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c2ba1-123">End of client support</span></span><br/>    | <span data-ttu-id="c2ba1-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c2ba1-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="c2ba1-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c2ba1-125">End of server support</span></span><br/>    | <span data-ttu-id="c2ba1-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c2ba1-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="c2ba1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2ba1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ba1-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ba1-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ba1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2ba1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ba1-130">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="c2ba1-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="c2ba1-131">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="c2ba1-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="c2ba1-132">**\_Port RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c2ba1-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="c2ba1-133">**résultat de la \_ projection PPP RAS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c2ba1-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="c2ba1-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="c2ba1-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





