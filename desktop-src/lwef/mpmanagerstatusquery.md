---
title: MpManagerStatusQuery, fonction (MpClient. h)
description: Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants. | MpManagerStatusQuery, fonction (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerStatusQuery
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321877"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="ee486-105">MpManagerStatusQuery fonction)</span><span class="sxs-lookup"><span data-stu-id="ee486-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="ee486-106">\[**MpManagerStatusQuery** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="ee486-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ee486-107">Utilisez plutôt [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span><span class="sxs-lookup"><span data-stu-id="ee486-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="ee486-108">Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="ee486-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee486-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee486-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ee486-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee486-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee486-111">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee486-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee486-112">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ee486-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="ee486-113">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="ee486-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="ee486-114">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="ee486-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ee486-115">*pStatusInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ee486-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee486-116">Type : **PMPSTATUS \_ info**</span><span class="sxs-lookup"><span data-stu-id="ee486-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="ee486-117">Pointeur vers une structure qui retourne les informations d’État relatives aux dernières analyses, aux menaces actives et à l’état des différents composants.</span><span class="sxs-lookup"><span data-stu-id="ee486-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="ee486-118">Consultez [**MPSTATUS \_ info**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="ee486-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee486-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee486-119">Return value</span></span>

<span data-ttu-id="ee486-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee486-120">Type: **HRESULT**</span></span>

<span data-ttu-id="ee486-121">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ee486-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="ee486-122">Cet appel de fonction est garanti, même si un service anti-programme malveillant n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ee486-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="ee486-123">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="ee486-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="ee486-124">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ee486-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee486-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee486-125">Requirements</span></span>



| <span data-ttu-id="ee486-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee486-126">Requirement</span></span> | <span data-ttu-id="ee486-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee486-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee486-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee486-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ee486-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee486-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ee486-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee486-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ee486-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee486-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee486-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee486-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee486-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee486-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee486-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ee486-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee486-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee486-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee486-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee486-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee486-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="ee486-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="ee486-138">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="ee486-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="ee486-139">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="ee486-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="ee486-140">**\_informations MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="ee486-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





