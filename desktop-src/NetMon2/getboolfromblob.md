---
description: Récupère une valeur booléenne nommée à partir d’un objet BLOB.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: GetBoolFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531650"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="98fcd-103">GetBoolFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="98fcd-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="98fcd-104">La fonction **GetBoolFromBlob** récupère une valeur booléenne nommée à partir d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="98fcd-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="98fcd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98fcd-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="98fcd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98fcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fcd-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98fcd-108">Handle d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="98fcd-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="98fcd-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98fcd-110">Pointeur vers le nom du propriétaire de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="98fcd-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="98fcd-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98fcd-112">Pointeur vers le nom de la catégorie d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="98fcd-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="98fcd-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98fcd-114">Pointeur vers le nom de la balise d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="98fcd-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="98fcd-115">*pBool* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98fcd-116">Pointeur vers la valeur booléenne de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="98fcd-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fcd-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98fcd-117">Return value</span></span>

<span data-ttu-id="98fcd-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="98fcd-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="98fcd-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="98fcd-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fcd-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98fcd-120">Requirements</span></span>



| <span data-ttu-id="98fcd-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98fcd-121">Requirement</span></span> | <span data-ttu-id="98fcd-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="98fcd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98fcd-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98fcd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98fcd-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="98fcd-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98fcd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98fcd-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98fcd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98fcd-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="98fcd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="98fcd-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="98fcd-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="98fcd-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98fcd-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="98fcd-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98fcd-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="98fcd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="98fcd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98fcd-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98fcd-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98fcd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98fcd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fcd-134">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-135">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="98fcd-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="98fcd-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




