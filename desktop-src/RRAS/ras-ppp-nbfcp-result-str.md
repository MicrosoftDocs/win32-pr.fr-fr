---
title: Structure RAS_PPP_NBFCP_RESULT (rassapi. h)
description: La \_ \_ \_ structure de résultat RAS PPP NBFCP est utilisée pour signaler le résultat d’une opération de projection d’une fréquence d’accès PPP NetBEUI (NBF) pour un port.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103999"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="a2bad-104">\_Structure des résultats RAS PPP \_ NBFCP \_</span><span class="sxs-lookup"><span data-stu-id="a2bad-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="a2bad-105">\[La structure des **\_ \_ \_ résultats ppp ppp NBFCP** n’est pas prise en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="a2bad-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="a2bad-106">La structure de **\_ \_ \_ résultat RAS PPP NBFCP** est utilisée pour signaler le résultat d’une opération de projection d’une fréquence d’accès PPP NetBEUI (NBF) pour un port.</span><span class="sxs-lookup"><span data-stu-id="a2bad-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bad-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2bad-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="a2bad-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a2bad-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2bad-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="a2bad-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="a2bad-110">Indique les résultats de l’opération de projection NBF.</span><span class="sxs-lookup"><span data-stu-id="a2bad-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="a2bad-111">La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszWksta** contient le nom de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="a2bad-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="a2bad-112">En cas d’échec de l’opération de projection, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="a2bad-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="a2bad-113">**dwNetBiosError**</span><span class="sxs-lookup"><span data-stu-id="a2bad-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="a2bad-114">Ignorer ce membre sur le serveur ; elle s’applique uniquement au client.</span><span class="sxs-lookup"><span data-stu-id="a2bad-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="a2bad-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="a2bad-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="a2bad-116">Ignorer ce membre sur le serveur ; elle s’applique uniquement au client.</span><span class="sxs-lookup"><span data-stu-id="a2bad-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="a2bad-117">**wszWksta**</span><span class="sxs-lookup"><span data-stu-id="a2bad-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="a2bad-118">Chaîne Unicode terminée par le caractère null qui spécifie le nom NetBIOS de la station de travail cliente RAS.</span><span class="sxs-lookup"><span data-stu-id="a2bad-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2bad-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2bad-119">Requirements</span></span>



| <span data-ttu-id="a2bad-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2bad-120">Requirement</span></span> | <span data-ttu-id="a2bad-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2bad-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2bad-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2bad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a2bad-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2bad-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a2bad-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2bad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a2bad-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2bad-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2bad-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a2bad-126">End of client support</span></span><br/>    | <span data-ttu-id="a2bad-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2bad-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="a2bad-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a2bad-128">End of server support</span></span><br/>    | <span data-ttu-id="a2bad-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2bad-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a2bad-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2bad-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2bad-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2bad-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2bad-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2bad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2bad-133">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="a2bad-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a2bad-134">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="a2bad-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="a2bad-135">**\_Port RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a2bad-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="a2bad-136">**résultat de la \_ projection PPP RAS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2bad-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="a2bad-137">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a2bad-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





