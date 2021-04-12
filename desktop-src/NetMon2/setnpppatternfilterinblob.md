---
description: Définit le filtre de correspondance du modèle d’objet BLOB.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: SetNPPPatternFilterInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526751"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="1eeb3-103">SetNPPPatternFilterInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="1eeb3-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="1eeb3-104">La fonction **SetNPPPatternFilterInBlob** définit le filtre de correspondance du modèle d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eeb3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eeb3-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1eeb3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1eeb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eeb3-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb3-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb3-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb3-109">*pExpression* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1eeb3-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb3-110">Pointeur vers une structure d' [expression](expression.md) qui définit l’expression de filtre définie.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="1eeb3-111">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1eeb3-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1eeb3-112">Handle d’un objet BLOB d’erreurs qui spécifie à quel endroit de l’objet BLOB d’origine l’erreur (le cas échéant) s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eeb3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1eeb3-113">Return value</span></span>

<span data-ttu-id="1eeb3-114">Si la fonction **SetNPPPatternFilterInBlob** réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1eeb3-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eeb3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1eeb3-116">Remarks</span></span>

<span data-ttu-id="1eeb3-117">Les correspondances de modèle filtrent les données stockées dans la catégorie de **configuration** de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="1eeb3-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eeb3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1eeb3-118">Requirements</span></span>



| <span data-ttu-id="1eeb3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1eeb3-119">Requirement</span></span> | <span data-ttu-id="1eeb3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1eeb3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eeb3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eeb3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1eeb3-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1eeb3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1eeb3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1eeb3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1eeb3-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1eeb3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1eeb3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1eeb3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eeb3-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb3-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1eeb3-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1eeb3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1eeb3-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb3-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1eeb3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1eeb3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eeb3-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eeb3-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eeb3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eeb3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eeb3-132">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-139">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="1eeb3-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="1eeb3-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




