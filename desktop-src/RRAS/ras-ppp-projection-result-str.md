---
title: Structure RAS_PPP_PROJECTION_RESULT (rassapi. h)
description: La \_ structure du \_ résultat de projection PPP RAS \_ est utilisée pour signaler les résultats des différentes opérations de projection PPP pour un port.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741796"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="06002-104">\_Structure du \_ résultat de projection PPP RAS \_</span><span class="sxs-lookup"><span data-stu-id="06002-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="06002-105">\[La structure du **\_ \_ \_ résultat de projection PPP RAS** n’est pas prise en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="06002-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="06002-106">La structure du **\_ \_ \_ résultat de projection PPP RAS** est utilisée pour signaler les résultats des différentes opérations de projection PPP pour un port.</span><span class="sxs-lookup"><span data-stu-id="06002-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="06002-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06002-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="06002-108">Membres</span><span class="sxs-lookup"><span data-stu-id="06002-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="06002-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="06002-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="06002-110">Structure [**de \_ \_ \_ résultat NBFCP PPP d’accès distant**](ras-ppp-nbfcp-result-str.md) qui signale le résultat d’une opération de projection d’une fréquence d’images NetBEUI PPP (NBF).</span><span class="sxs-lookup"><span data-stu-id="06002-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="06002-111">**adressesIP**</span><span class="sxs-lookup"><span data-stu-id="06002-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="06002-112">Structure [**de \_ \_ \_ résultat IPCP PPP IPX**](ras-ppp-ipcp-result-str.md) qui signale le résultat d’une opération de projection IP (Internet Protocol) ppp.</span><span class="sxs-lookup"><span data-stu-id="06002-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="06002-113">**‡**</span><span class="sxs-lookup"><span data-stu-id="06002-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="06002-114">Structure [**de \_ \_ \_ résultat RAS PPP IPXCP**](ras-ppp-ipxcp-result-str.md) qui signale le résultat d’une opération de projection PPP IPX (Internetwork Packet Exchange).</span><span class="sxs-lookup"><span data-stu-id="06002-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="06002-115">**at**</span><span class="sxs-lookup"><span data-stu-id="06002-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="06002-116">Structure [**de \_ \_ \_ résultat du protocole ATCP PPP RAS**](ras-ppp-atcp-result-str.md) .</span><span class="sxs-lookup"><span data-stu-id="06002-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06002-117">Notes</span><span class="sxs-lookup"><span data-stu-id="06002-117">Remarks</span></span>

<span data-ttu-id="06002-118">Cette structure signale les résultats de la projection pour les protocoles NetBEUI, TCP/IP et IPX.</span><span class="sxs-lookup"><span data-stu-id="06002-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="06002-119">Chaque structure PPP a un membre **dwError** qui indique si les autres informations de la structure sont valides.</span><span class="sxs-lookup"><span data-stu-id="06002-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="06002-120">Si **dwError** n’est pas une \_ erreur, les autres informations sont valides.</span><span class="sxs-lookup"><span data-stu-id="06002-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="06002-121">Si **dwError** est l’un des codes d’erreur dans Winerror. h ou Raserror. h, les autres informations ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="06002-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="06002-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06002-122">Requirements</span></span>



| <span data-ttu-id="06002-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06002-123">Requirement</span></span> | <span data-ttu-id="06002-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="06002-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06002-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06002-125">Minimum supported client</span></span><br/> | <span data-ttu-id="06002-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06002-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="06002-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06002-127">Minimum supported server</span></span><br/> | <span data-ttu-id="06002-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06002-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="06002-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="06002-129">End of client support</span></span><br/>    | <span data-ttu-id="06002-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="06002-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="06002-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="06002-131">End of server support</span></span><br/>    | <span data-ttu-id="06002-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06002-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="06002-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="06002-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="06002-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06002-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06002-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06002-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06002-136">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="06002-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="06002-137">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="06002-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="06002-138">**\_Port RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="06002-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="06002-139">**\_résultat du protocole \_ ATCP PPP RAS \_**</span><span class="sxs-lookup"><span data-stu-id="06002-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="06002-140">**\_résultat du protocole \_ IPCP PPP RAS \_**</span><span class="sxs-lookup"><span data-stu-id="06002-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="06002-141">**\_résultat RAS PPP \_ IPXCP \_**</span><span class="sxs-lookup"><span data-stu-id="06002-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="06002-142">**\_résultat de \_ NBFCP \_ PPP RAS**</span><span class="sxs-lookup"><span data-stu-id="06002-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="06002-143">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="06002-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





