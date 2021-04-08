---
description: La fonction GetDwordFromBlob récupère la valeur DWORD nommée à partir d’un objet BLOB.
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: GetDwordFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112223"
---
# <a name="getdwordfromblob-function"></a><span data-ttu-id="b67d0-103">GetDwordFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="b67d0-103">GetDwordFromBlob function</span></span>

<span data-ttu-id="b67d0-104">La fonction **GetDwordFromBlob** récupère la valeur **DWORD** nommée à partir d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="b67d0-104">The **GetDwordFromBlob** function retrieves the named **DWORD** value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="b67d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b67d0-105">Syntax</span></span>


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a><span data-ttu-id="b67d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b67d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b67d0-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d0-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="b67d0-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b67d0-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d0-110">Pointeur vers le nom du propriétaire de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="b67d0-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="b67d0-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d0-112">Pointeur vers le nom de la catégorie d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="b67d0-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="b67d0-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d0-114">Pointeur vers le nom de la balise d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="b67d0-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="b67d0-115">*pDword* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-115">*pDword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b67d0-116">Pointeur vers la valeur **DWORD** de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="b67d0-116">Pointer to the **DWORD** value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b67d0-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b67d0-117">Return value</span></span>

<span data-ttu-id="b67d0-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b67d0-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b67d0-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b67d0-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b67d0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b67d0-120">Requirements</span></span>



| <span data-ttu-id="b67d0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b67d0-121">Requirement</span></span> | <span data-ttu-id="b67d0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b67d0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b67d0-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b67d0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b67d0-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b67d0-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b67d0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b67d0-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b67d0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b67d0-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b67d0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b67d0-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b67d0-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b67d0-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b67d0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b67d0-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b67d0-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b67d0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b67d0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b67d0-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b67d0-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b67d0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b67d0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b67d0-134">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-134">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="b67d0-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="b67d0-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




