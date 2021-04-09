---
title: UtilLoadStringWithAlloc, fonction (Ndattributils. h)
description: Alloue et charge une chaîne à partir de la table de ressources.
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc fonction NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e13930fe9bb11ae9c9456152c823491eabc462
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106501"
---
# <a name="utilloadstringwithalloc-function"></a><span data-ttu-id="0582d-104">UtilLoadStringWithAlloc fonction)</span><span class="sxs-lookup"><span data-stu-id="0582d-104">UtilLoadStringWithAlloc function</span></span>

<span data-ttu-id="0582d-105">La fonction **UtilLoadStringWithAlloc** alloue et charge une chaîne à partir de la table de ressources.</span><span class="sxs-lookup"><span data-stu-id="0582d-105">The **UtilLoadStringWithAlloc** function allocates and loads a string out of the resource table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0582d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0582d-106">Syntax</span></span>


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a><span data-ttu-id="0582d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0582d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0582d-108">*uID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0582d-108">*uID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0582d-109">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="0582d-109">Type: **UINT**</span></span>

<span data-ttu-id="0582d-110">Identificateur de de la chaîne à charger.</span><span class="sxs-lookup"><span data-stu-id="0582d-110">Identifier of of the string to be loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0582d-111">*ppwzBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0582d-111">*ppwzBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0582d-112">Tapez : \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="0582d-112">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="0582d-113">Emplacement où la chaîne qui vient d’être allouée sera placée.</span><span class="sxs-lookup"><span data-stu-id="0582d-113">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="0582d-114">La chaîne doit être libérée à l’aide de [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) lorsqu’elle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0582d-114">The string must be freed using [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) when it is no longer needed.</span></span>

</dd> <dt>

<span data-ttu-id="0582d-115">*cchBufferMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0582d-115">*cchBufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0582d-116">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="0582d-116">Type: **UINT**</span></span>

<span data-ttu-id="0582d-117">Nombre maximal de caractères à charger à partir de la table de ressources.</span><span class="sxs-lookup"><span data-stu-id="0582d-117">The maximum number of characters to load from the resource table.</span></span> <span data-ttu-id="0582d-118">Si la chaîne de ressource dépasse le nombre de caractères spécifié, elle est tronquée et se termine par null.</span><span class="sxs-lookup"><span data-stu-id="0582d-118">If the resource string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="0582d-119">Ce paramètre ne peut pas être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="0582d-119">This parameter may not be set to zero.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0582d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0582d-120">Return value</span></span>

<span data-ttu-id="0582d-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0582d-121">Type: **HRESULT**</span></span>

<span data-ttu-id="0582d-122">Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="0582d-122">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0582d-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0582d-123">Return code</span></span>                                                                                  | <span data-ttu-id="0582d-124">Description</span><span class="sxs-lookup"><span data-stu-id="0582d-124">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0582d-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0582d-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0582d-126">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0582d-126">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="0582d-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0582d-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0582d-128">Un ou plusieurs paramètres n’ont pas été fournis correctement.</span><span class="sxs-lookup"><span data-stu-id="0582d-128">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0582d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0582d-129">Requirements</span></span>



| <span data-ttu-id="0582d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0582d-130">Requirement</span></span> | <span data-ttu-id="0582d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="0582d-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0582d-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0582d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0582d-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0582d-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0582d-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0582d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0582d-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0582d-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0582d-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="0582d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0582d-137"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="0582d-137"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0582d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0582d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0582d-139">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="0582d-139">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="0582d-140">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="0582d-140">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="0582d-141">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="0582d-141">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

