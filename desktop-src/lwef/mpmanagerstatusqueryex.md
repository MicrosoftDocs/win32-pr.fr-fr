---
title: MpManagerStatusQueryEx, fonction (MpClient. h)
description: Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants. | MpManagerStatusQueryEx, fonction (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerStatusQueryEx
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522932"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="a9169-105">MpManagerStatusQueryEx fonction)</span><span class="sxs-lookup"><span data-stu-id="a9169-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="a9169-106">Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="a9169-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9169-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9169-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a9169-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9169-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9169-109">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9169-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9169-110">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="a9169-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="a9169-111">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="a9169-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="a9169-112">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="a9169-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a9169-113">*dwFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9169-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9169-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a9169-114">Type: **DWORD**</span></span>

<span data-ttu-id="a9169-115">Contrôle les informations de requête retournées.</span><span class="sxs-lookup"><span data-stu-id="a9169-115">Controls which query information is returned.</span></span> <span data-ttu-id="a9169-116">Certaines informations sont coûteuses et peuvent ne pas être nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a9169-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="a9169-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9169-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="a9169-118">Signification</span><span class="sxs-lookup"><span data-stu-id="a9169-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="a9169-119"><dt>**indicateurs de requête d’État du pack d' \_ état \_ \_ \_ aucun**</dt></span><span class="sxs-lookup"><span data-stu-id="a9169-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="a9169-120">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9169-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="a9169-121"><dt>**\_indicateur de requête d’État MP \_ \_ \_ nostate**</dt></span><span class="sxs-lookup"><span data-stu-id="a9169-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="a9169-122">Ne pas interroger les informations d’État.</span><span class="sxs-lookup"><span data-stu-id="a9169-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a9169-123">*pStatusInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a9169-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9169-124">Type : **PMPSTATUS \_ info**</span><span class="sxs-lookup"><span data-stu-id="a9169-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="a9169-125">Pointeur vers une structure qui retourne les informations d’État relatives aux dernières analyses, aux menaces actives et à l’état des différents composants.</span><span class="sxs-lookup"><span data-stu-id="a9169-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="a9169-126">Consultez [**MPSTATUS \_ info**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="a9169-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9169-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a9169-127">Return value</span></span>

<span data-ttu-id="a9169-128">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a9169-128">Type: **HRESULT**</span></span>

<span data-ttu-id="a9169-129">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9169-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="a9169-130">Cet appel de fonction est garanti, même si un service anti-programme malveillant n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a9169-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="a9169-131">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="a9169-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="a9169-132">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a9169-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9169-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9169-133">Requirements</span></span>



| <span data-ttu-id="a9169-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9169-134">Requirement</span></span> | <span data-ttu-id="a9169-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9169-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9169-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9169-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a9169-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9169-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a9169-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9169-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a9169-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9169-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9169-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9169-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9169-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9169-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9169-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a9169-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9169-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9169-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9169-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9169-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9169-145">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="a9169-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="a9169-146">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="a9169-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="a9169-147">**\_informations MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="a9169-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





