---
title: Structure RAS_PPP_IPCP_RESULT (rassapi. h)
description: La \_ structure du \_ résultat IPCP PPP IPX \_ est utilisée pour signaler le résultat d’une opération de projection IP (Internet Protocol) ppp pour un port.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508642"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="eb2fa-104">\_Structure du \_ résultat IPCP PPP \_ IPX</span><span class="sxs-lookup"><span data-stu-id="eb2fa-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="eb2fa-105">\[La structure du **\_ \_ \_ résultat IPCP PPP IPX** n’est pas prise en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="eb2fa-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="eb2fa-106">La structure du **\_ \_ \_ résultat IPCP PPP IPX** est utilisée pour signaler le résultat d’une opération de projection IP (Internet Protocol) ppp pour un port.</span><span class="sxs-lookup"><span data-stu-id="eb2fa-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2fa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb2fa-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="eb2fa-108">Membres</span><span class="sxs-lookup"><span data-stu-id="eb2fa-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb2fa-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="eb2fa-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="eb2fa-110">Indique les résultats de l’opération de projection IP.</span><span class="sxs-lookup"><span data-stu-id="eb2fa-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="eb2fa-111">La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszAddress** est valide.</span><span class="sxs-lookup"><span data-stu-id="eb2fa-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="eb2fa-112">En cas d’échec de l’opération de projection, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="eb2fa-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="eb2fa-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="eb2fa-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="eb2fa-114">Chaîne Unicode terminée par le caractère null qui spécifie l’adresse IP affectée au client distant.</span><span class="sxs-lookup"><span data-stu-id="eb2fa-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="eb2fa-115">Cette chaîne se présente sous la forme \*a ***.** _b_* _._ *_c_*_._ \* _d_.</span><span class="sxs-lookup"><span data-stu-id="eb2fa-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb2fa-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb2fa-116">Requirements</span></span>



| <span data-ttu-id="eb2fa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb2fa-117">Requirement</span></span> | <span data-ttu-id="eb2fa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb2fa-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2fa-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb2fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2fa-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb2fa-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="eb2fa-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb2fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2fa-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb2fa-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="eb2fa-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="eb2fa-123">End of client support</span></span><br/>    | <span data-ttu-id="eb2fa-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb2fa-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="eb2fa-125">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="eb2fa-125">End of server support</span></span><br/>    | <span data-ttu-id="eb2fa-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb2fa-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="eb2fa-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb2fa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb2fa-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb2fa-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb2fa-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb2fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb2fa-130">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="eb2fa-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="eb2fa-131">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="eb2fa-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="eb2fa-132">**\_Port RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="eb2fa-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="eb2fa-133">**résultat de la \_ projection PPP RAS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb2fa-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="eb2fa-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="eb2fa-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





