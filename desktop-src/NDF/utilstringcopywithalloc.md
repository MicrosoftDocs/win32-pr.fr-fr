---
title: UtilStringCopyWithAlloc, fonction (Ndattributils. h)
description: Alloue et copie une chaîne source.
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc fonction NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511753"
---
# <a name="utilstringcopywithalloc-function"></a><span data-ttu-id="56276-104">UtilStringCopyWithAlloc fonction)</span><span class="sxs-lookup"><span data-stu-id="56276-104">UtilStringCopyWithAlloc function</span></span>

<span data-ttu-id="56276-105">La fonction **UtilStringCopyWithAlloc** alloue et copie une chaîne source.</span><span class="sxs-lookup"><span data-stu-id="56276-105">The **UtilStringCopyWithAlloc** function allocates and copies a source string.</span></span>

## <a name="syntax"></a><span data-ttu-id="56276-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56276-106">Syntax</span></span>


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a><span data-ttu-id="56276-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56276-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56276-108">*Mémoire tampon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="56276-108">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56276-109">Tapez : \**LPWStr \** _</span><span class="sxs-lookup"><span data-stu-id="56276-109">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="56276-110">Emplacement de stockage du pointeur vers la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="56276-110">The location where the pointer to the allocated memory is stored.</span></span> <span data-ttu-id="56276-111">Quand vous n’en avez plus besoin, elle doit être libérée avec [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="56276-111">When no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span> <span data-ttu-id="56276-112">Cette mémoire tampon se termine toujours par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="56276-112">This buffer is always null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="56276-113">*BufferMax* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56276-113">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56276-114">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="56276-114">Type: **UINT**</span></span>

<span data-ttu-id="56276-115">Nombre maximal de caractères à lire à partir de la *source*.</span><span class="sxs-lookup"><span data-stu-id="56276-115">The maximum number of characters to read from *Source*.</span></span>

</dd> <dt>

<span data-ttu-id="56276-116">*Source* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56276-116">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56276-117">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="56276-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="56276-118">Chaîne à copier.</span><span class="sxs-lookup"><span data-stu-id="56276-118">The string to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56276-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56276-119">Return value</span></span>

<span data-ttu-id="56276-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="56276-120">Type: **HRESULT**</span></span>

<span data-ttu-id="56276-121">Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="56276-121">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="56276-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="56276-122">Return code</span></span>                                                                                  | <span data-ttu-id="56276-123">Description</span><span class="sxs-lookup"><span data-stu-id="56276-123">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="56276-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="56276-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="56276-125">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="56276-125">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="56276-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="56276-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="56276-127">Un ou plusieurs paramètres n’ont pas été fournis correctement.</span><span class="sxs-lookup"><span data-stu-id="56276-127">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56276-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56276-128">Requirements</span></span>



| <span data-ttu-id="56276-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56276-129">Requirement</span></span> | <span data-ttu-id="56276-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="56276-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="56276-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56276-131">Minimum supported client</span></span><br/> | <span data-ttu-id="56276-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56276-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="56276-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56276-133">Minimum supported server</span></span><br/> | <span data-ttu-id="56276-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56276-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="56276-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="56276-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="56276-136"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="56276-136"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56276-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56276-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56276-138">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="56276-138">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[<span data-ttu-id="56276-139">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="56276-139">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
</dt> <dt>

[<span data-ttu-id="56276-140">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="56276-140">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> </dl>

 

