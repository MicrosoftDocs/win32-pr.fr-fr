---
title: MpManagerVersionQuery, fonction (MpClient. h)
description: Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpManagerVersionQuery
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509336"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="c3cd1-104">MpManagerVersionQuery fonction)</span><span class="sxs-lookup"><span data-stu-id="c3cd1-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="c3cd1-105">Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="c3cd1-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cd1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3cd1-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c3cd1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3cd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3cd1-108">*hMpHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3cd1-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cd1-109">Type : **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="c3cd1-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="c3cd1-110">Handle de l’interface du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="c3cd1-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="c3cd1-111">Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="c3cd1-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c3cd1-112">*pVersionInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c3cd1-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cd1-113">Type : **PMPVERSION \_ info**</span><span class="sxs-lookup"><span data-stu-id="c3cd1-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="c3cd1-114">Pointeur vers une structure qui contient des informations de version sur différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="c3cd1-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="c3cd1-115">Consultez [**MPVERSION \_ info**](mpversion-info.md).</span><span class="sxs-lookup"><span data-stu-id="c3cd1-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3cd1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3cd1-116">Return value</span></span>

<span data-ttu-id="c3cd1-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c3cd1-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c3cd1-118">Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c3cd1-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="c3cd1-119">Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec.</span><span class="sxs-lookup"><span data-stu-id="c3cd1-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="c3cd1-120">L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c3cd1-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cd1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3cd1-121">Requirements</span></span>



| <span data-ttu-id="c3cd1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3cd1-122">Requirement</span></span> | <span data-ttu-id="c3cd1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3cd1-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cd1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3cd1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c3cd1-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3cd1-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c3cd1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3cd1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c3cd1-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3cd1-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c3cd1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3cd1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3cd1-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3cd1-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3cd1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c3cd1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3cd1-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3cd1-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3cd1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3cd1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cd1-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="c3cd1-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="c3cd1-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="c3cd1-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="c3cd1-135">**\_informations MPVERSION**</span><span class="sxs-lookup"><span data-stu-id="c3cd1-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





