---
description: La fonction SetDwordInBlob définit la valeur DWORD nommée d’un objet BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: SetDwordInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517013"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="1811d-103">SetDwordInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="1811d-103">SetDwordInBlob function</span></span>

<span data-ttu-id="1811d-104">La fonction **SetDwordInBlob** définit la valeur **DWORD** nommée d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="1811d-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1811d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1811d-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="1811d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1811d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1811d-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1811d-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811d-108">Handle d’un objet BLOB en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="1811d-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="1811d-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1811d-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811d-110">Pointeur vers le nom du **propriétaire** de l’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1811d-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1811d-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1811d-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811d-112">Pointeur vers le nom de **catégorie** d’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1811d-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1811d-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1811d-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811d-114">Pointeur vers le nom de **balise** d’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1811d-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1811d-115">*Valeur DWORD* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1811d-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811d-116">Valeur **DWORD** de l’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1811d-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1811d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1811d-117">Return value</span></span>

<span data-ttu-id="1811d-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1811d-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1811d-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1811d-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1811d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1811d-120">Requirements</span></span>



| <span data-ttu-id="1811d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1811d-121">Requirement</span></span> | <span data-ttu-id="1811d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1811d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1811d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1811d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1811d-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1811d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1811d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1811d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1811d-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1811d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1811d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1811d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1811d-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1811d-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1811d-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1811d-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1811d-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1811d-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1811d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1811d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1811d-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1811d-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1811d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1811d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1811d-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="1811d-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="1811d-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




