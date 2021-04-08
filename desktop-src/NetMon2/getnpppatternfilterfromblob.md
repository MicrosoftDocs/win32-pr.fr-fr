---
description: La fonction GetNPPPatternFilterFromBlob récupère le filtre de correspondance de modèle à partir d’un objet BLOB spécifique.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: GetNPPPatternFilterFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750084"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="0f01d-103">GetNPPPatternFilterFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="0f01d-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="0f01d-104">La fonction **GetNPPPatternFilterFromBlob** récupère le filtre de correspondance de modèle à partir d’un objet BLOB spécifique.</span><span class="sxs-lookup"><span data-stu-id="0f01d-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f01d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f01d-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="0f01d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f01d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f01d-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f01d-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f01d-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="0f01d-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="0f01d-109">*pExpression* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0f01d-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f01d-110">Pointeur vers l’expression de filtre.</span><span class="sxs-lookup"><span data-stu-id="0f01d-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="0f01d-111">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0f01d-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f01d-112">Handle vers un objet BLOB d’erreurs qui spécifie où l’erreur (le cas échéant) dans l’objet BLOB d’origine s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0f01d-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f01d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f01d-113">Return value</span></span>

<span data-ttu-id="0f01d-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0f01d-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0f01d-115">Si la fonction échoue, la valeur de retour est un NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0f01d-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f01d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0f01d-116">Remarks</span></span>

<span data-ttu-id="0f01d-117">Les informations de filtre de correspondance de modèle sont stockées dans la catégorie de **configuration** de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="0f01d-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f01d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f01d-118">Requirements</span></span>



| <span data-ttu-id="0f01d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f01d-119">Requirement</span></span> | <span data-ttu-id="0f01d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f01d-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f01d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f01d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f01d-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f01d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0f01d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f01d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f01d-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f01d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f01d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f01d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f01d-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f01d-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="0f01d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0f01d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f01d-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f01d-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f01d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0f01d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f01d-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f01d-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f01d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f01d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f01d-132">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-138">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="0f01d-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="0f01d-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




