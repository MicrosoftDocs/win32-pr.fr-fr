---
description: La fonction GetNPPAddressFilterFromBlob remplit le filtre d’adresse donné avec les informations stockées dans l’objet BLOB.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: GetNPPAddressFilterFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952885"
---
# <a name="getnppaddressfilterfromblob-function"></a><span data-ttu-id="fa261-103">GetNPPAddressFilterFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="fa261-103">GetNPPAddressFilterFromBlob function</span></span>

<span data-ttu-id="fa261-104">La fonction **GetNPPAddressFilterFromBlob** remplit le filtre d’adresse donné avec les informations stockées dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="fa261-104">The **GetNPPAddressFilterFromBlob** function fills in the given address filter with information stored in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa261-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa261-105">Syntax</span></span>


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="fa261-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa261-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa261-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa261-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa261-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="fa261-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="fa261-109">*pAddressTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa261-109">*pAddressTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa261-110">Pointeur vers la table d’adresses allouées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fa261-110">Pointer to the user-allocated address table.</span></span>

</dd> <dt>

<span data-ttu-id="fa261-111">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fa261-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa261-112">Handle vers un objet BLOB d’erreurs qui spécifie où l’erreur (le cas échéant) dans l’objet BLOB d’origine s’est produite.</span><span class="sxs-lookup"><span data-stu-id="fa261-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa261-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa261-113">Return value</span></span>

<span data-ttu-id="fa261-114">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fa261-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fa261-115">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="fa261-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa261-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fa261-116">Remarks</span></span>

<span data-ttu-id="fa261-117">Les informations d’adresse sont stockées dans la section de **configuration** de la catégorie **propriétaire** de l’objet BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="fa261-117">The address information is stored in the **Config** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa261-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa261-118">Requirements</span></span>



| <span data-ttu-id="fa261-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa261-119">Requirement</span></span> | <span data-ttu-id="fa261-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa261-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa261-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa261-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fa261-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa261-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa261-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa261-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fa261-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa261-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa261-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa261-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa261-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa261-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="fa261-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa261-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa261-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa261-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa261-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fa261-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa261-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa261-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa261-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa261-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa261-132">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-132">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="fa261-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="fa261-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




