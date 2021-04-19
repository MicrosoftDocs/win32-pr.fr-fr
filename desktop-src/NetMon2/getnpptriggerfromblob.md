---
description: La fonction GetNPPTriggerFromBlob récupère le déclencheur à partir de l’objet BLOB donné.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: GetNPPTriggerFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544617"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="616d3-103">GetNPPTriggerFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="616d3-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="616d3-104">La fonction **GetNPPTriggerFromBlob** récupère le déclencheur à partir de l’objet BLOB donné.</span><span class="sxs-lookup"><span data-stu-id="616d3-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="616d3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="616d3-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="616d3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="616d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="616d3-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="616d3-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="616d3-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="616d3-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="616d3-109">*pTrigger* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="616d3-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="616d3-110">Pointeur désignant la valeur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="616d3-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="616d3-111">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="616d3-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="616d3-112">Handle vers un objet BLOB d’erreurs qui spécifie où l’erreur (le cas échéant) dans l’objet BLOB d’origine s’est produite.</span><span class="sxs-lookup"><span data-stu-id="616d3-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="616d3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="616d3-113">Return value</span></span>

<span data-ttu-id="616d3-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="616d3-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="616d3-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="616d3-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="616d3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="616d3-116">Remarks</span></span>

<span data-ttu-id="616d3-117">Les informations de déclencheur sont stockées dans la catégorie de **déclencheur** de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="616d3-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="616d3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="616d3-118">Requirements</span></span>



| <span data-ttu-id="616d3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="616d3-119">Requirement</span></span> | <span data-ttu-id="616d3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="616d3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="616d3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="616d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="616d3-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="616d3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="616d3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="616d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="616d3-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="616d3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="616d3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="616d3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="616d3-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="616d3-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="616d3-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="616d3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="616d3-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="616d3-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="616d3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="616d3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="616d3-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616d3-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="616d3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="616d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616d3-132">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-133">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-135">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-136">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-137">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-139">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="616d3-140">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="616d3-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




