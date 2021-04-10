---
title: MpThreatEnumerate, fonction (MpClient. h)
description: Retourne des informations sur la menace suivante dans la liste d’énumération. Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpThreatEnumerate
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942495"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="0f236-105">MpThreatEnumerate fonction)</span><span class="sxs-lookup"><span data-stu-id="0f236-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="0f236-106">Retourne des informations sur la menace suivante dans la liste d’énumération.</span><span class="sxs-lookup"><span data-stu-id="0f236-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="0f236-107">Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.</span><span class="sxs-lookup"><span data-stu-id="0f236-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f236-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f236-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0f236-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f236-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f236-110">*hThreatEnumHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f236-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f236-111">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="0f236-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="0f236-112">Handle vers un contexte d’énumération des menaces retourné par [**MpThreatOpen**](mpthreatopen.md).</span><span class="sxs-lookup"><span data-stu-id="0f236-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f236-113">*ppThreatInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0f236-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f236-114">Type : \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="0f236-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="0f236-115">Retourne un pointeur vers une structure d’informations sur les menaces, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="0f236-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="0f236-116">La structure contient des informations telles que l’ID de menace, le nom et la gravité.</span><span class="sxs-lookup"><span data-stu-id="0f236-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f236-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f236-117">Return value</span></span>

<span data-ttu-id="0f236-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f236-118">Type: **HRESULT**</span></span>

<span data-ttu-id="0f236-119">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f236-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="0f236-120">S’il n’y a plus d’éléments à retourner, la valeur de retour est **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="0f236-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="0f236-121">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="0f236-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="0f236-122">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0f236-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f236-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f236-123">Requirements</span></span>



| <span data-ttu-id="0f236-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f236-124">Requirement</span></span> | <span data-ttu-id="0f236-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f236-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f236-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f236-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f236-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f236-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0f236-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f236-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f236-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f236-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f236-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f236-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f236-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f236-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f236-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0f236-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f236-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f236-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f236-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f236-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f236-135">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="0f236-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="0f236-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="0f236-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="0f236-137">**\_informations MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="0f236-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





