---
description: La fonction GetClassIDFromBlob récupère une valeur d’identificateur de classe nommée à partir d’un objet BLOB.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: GetClassIDFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112227"
---
# <a name="getclassidfromblob-function"></a><span data-ttu-id="e5d62-103">GetClassIDFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="e5d62-103">GetClassIDFromBlob function</span></span>

<span data-ttu-id="e5d62-104">La fonction **GetClassIDFromBlob** récupère une valeur d’identificateur de classe nommée à partir d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e5d62-104">The **GetClassIDFromBlob** function retrieves a named class identifier value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d62-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5d62-105">Syntax</span></span>


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="e5d62-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5d62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d62-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e5d62-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="e5d62-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-110">Pointeur vers le nom du propriétaire de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e5d62-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="e5d62-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-112">Pointeur vers le nom de la catégorie d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e5d62-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="e5d62-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-114">Pointeur vers le nom de la balise d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e5d62-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="e5d62-115">*pClsID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-115">*pClsID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-116">Pointeur vers l’identificateur de classe d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="e5d62-116">Pointer to the BLOB class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d62-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5d62-117">Return value</span></span>

<span data-ttu-id="e5d62-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e5d62-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e5d62-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e5d62-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d62-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5d62-120">Requirements</span></span>



| <span data-ttu-id="e5d62-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5d62-121">Requirement</span></span> | <span data-ttu-id="e5d62-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5d62-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d62-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5d62-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d62-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e5d62-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5d62-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d62-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e5d62-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5d62-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d62-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e5d62-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e5d62-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5d62-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e5d62-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d62-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d62-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5d62-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5d62-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d62-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="e5d62-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="e5d62-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




