---
description: Définit le déclencheur d’objet BLOB.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: SetNPPTriggerInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201581"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="65893-103">SetNPPTriggerInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="65893-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="65893-104">La fonction **SetNPPTriggerInBlob** définit le déclencheur d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="65893-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="65893-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65893-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="65893-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65893-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65893-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65893-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="65893-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="65893-109">*pTrigger* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65893-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65893-110">Pointeur vers la valeur du déclencheur.</span><span class="sxs-lookup"><span data-stu-id="65893-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="65893-111">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65893-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65893-112">Handle d’un objet BLOB d’erreurs qui spécifie à quel endroit de l’objet BLOB d’origine l’erreur (le cas échéant) s’est produite.</span><span class="sxs-lookup"><span data-stu-id="65893-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65893-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65893-113">Return value</span></span>

<span data-ttu-id="65893-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="65893-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="65893-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="65893-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="65893-116">Notes</span><span class="sxs-lookup"><span data-stu-id="65893-116">Remarks</span></span>

<span data-ttu-id="65893-117">Ces données de déclencheur sont stockées dans la catégorie de **déclencheur** de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="65893-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="65893-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65893-118">Requirements</span></span>



| <span data-ttu-id="65893-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65893-119">Requirement</span></span> | <span data-ttu-id="65893-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="65893-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65893-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65893-121">Minimum supported client</span></span><br/> | <span data-ttu-id="65893-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65893-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65893-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65893-123">Minimum supported server</span></span><br/> | <span data-ttu-id="65893-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65893-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65893-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="65893-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="65893-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="65893-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="65893-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65893-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="65893-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65893-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="65893-129">DLL</span><span class="sxs-lookup"><span data-stu-id="65893-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65893-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65893-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65893-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65893-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65893-132">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="65893-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="65893-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-139">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="65893-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="65893-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




