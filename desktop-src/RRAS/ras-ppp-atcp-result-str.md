---
title: Structure RAS_PPP_ATCP_RESULT (rassapi. h)
description: La \_ \_ \_ structure de résultat du protocole ATCP PPP RAS est utilisée pour signaler le résultat d’une opération de projection de protocole AppleTalk pour un port.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942234"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="17f80-104">\_Structure de résultat du protocole ATCP PPP RAS \_ \_</span><span class="sxs-lookup"><span data-stu-id="17f80-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="17f80-105">\[La structure du **\_ résultat du protocole \_ ATCP \_ PPP RAS** n’est pas prise en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="17f80-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="17f80-106">La structure de résultat du protocole **\_ \_ ATCP \_ PPP RAS** est utilisée pour signaler le résultat d’une opération de projection de protocole AppleTalk pour un port.</span><span class="sxs-lookup"><span data-stu-id="17f80-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f80-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17f80-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="17f80-108">Membres</span><span class="sxs-lookup"><span data-stu-id="17f80-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="17f80-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="17f80-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="17f80-110">Spécifie une valeur qui indique les résultats de l’opération de projection AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="17f80-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="17f80-111">La valeur aucune \_ erreur indique la réussite, auquel cas le membre **wszAddress** est valide.</span><span class="sxs-lookup"><span data-stu-id="17f80-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="17f80-112">Si l’opération de projection échoue, **dwError** est un code d’erreur de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="17f80-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="17f80-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="17f80-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="17f80-114">Spécifie une chaîne Unicode terminée par le caractère null qui spécifie l’adresse IP affectée au client distant.</span><span class="sxs-lookup"><span data-stu-id="17f80-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17f80-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17f80-115">Requirements</span></span>



| <span data-ttu-id="17f80-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17f80-116">Requirement</span></span> | <span data-ttu-id="17f80-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="17f80-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17f80-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f80-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17f80-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17f80-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="17f80-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17f80-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17f80-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17f80-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="17f80-122">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="17f80-122">End of client support</span></span><br/>    | <span data-ttu-id="17f80-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="17f80-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="17f80-124">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="17f80-124">End of server support</span></span><br/>    | <span data-ttu-id="17f80-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="17f80-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="17f80-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="17f80-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="17f80-127"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f80-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f80-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17f80-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f80-129">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="17f80-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="17f80-130">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="17f80-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="17f80-131">**résultat de la \_ projection PPP RAS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="17f80-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





