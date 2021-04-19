---
title: MpThreatQuery, fonction (MpClient. h)
description: Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpThreatQuery
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510955"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="5c892-104">MpThreatQuery fonction)</span><span class="sxs-lookup"><span data-stu-id="5c892-104">MpThreatQuery function</span></span>

<span data-ttu-id="5c892-105">Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="5c892-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c892-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c892-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5c892-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c892-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c892-108">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c892-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c892-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="5c892-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="5c892-110">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="5c892-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="5c892-111">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="5c892-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5c892-112">*ThreatID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c892-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c892-113">Type : **\_ ID MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="5c892-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="5c892-114">Identificateur de menace pour lequel des informations sont demandées.</span><span class="sxs-lookup"><span data-stu-id="5c892-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="5c892-115">*ppThreatInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5c892-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c892-116">Type : \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="5c892-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="5c892-117">Retourne un pointeur vers une structure d’informations sur les menaces, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="5c892-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="5c892-118">La structure contient des informations telles que l’ID de menace, le nom et la gravité.</span><span class="sxs-lookup"><span data-stu-id="5c892-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="5c892-119">*ppThreatLocalizedInfo* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5c892-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c892-120">Type : \**PMPTHREAT \_ \_ informations \* localisées* _</span><span class="sxs-lookup"><span data-stu-id="5c892-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="5c892-121">Retourne un pointeur vers une structure contenant des informations localisées sur la menace.</span><span class="sxs-lookup"><span data-stu-id="5c892-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="5c892-122">Vous pouvez passer _ *null*\* si vous n’êtes pas intéressé par les informations localisées relatives à la menace.</span><span class="sxs-lookup"><span data-stu-id="5c892-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="5c892-123">Consultez [**\_ \_ informations localisées MPTHREAT**](mpthreat-localized-info.md).</span><span class="sxs-lookup"><span data-stu-id="5c892-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c892-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c892-124">Return value</span></span>

<span data-ttu-id="5c892-125">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5c892-125">Type: **HRESULT**</span></span>

<span data-ttu-id="5c892-126">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c892-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="5c892-127">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="5c892-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="5c892-128">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5c892-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c892-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c892-129">Requirements</span></span>



| <span data-ttu-id="5c892-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c892-130">Requirement</span></span> | <span data-ttu-id="5c892-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c892-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c892-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c892-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5c892-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c892-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5c892-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c892-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5c892-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c892-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c892-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c892-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c892-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c892-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c892-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5c892-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c892-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c892-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c892-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c892-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c892-141">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="5c892-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="5c892-142">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="5c892-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="5c892-143">**\_informations MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="5c892-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="5c892-144">**\_informations localisées \_ MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="5c892-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





