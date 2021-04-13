---
description: La fonction SetBoolInBlob définit une valeur booléenne à un emplacement donné au sein d’un objet BLOB.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: SetBoolInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528641"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="34153-103">SetBoolInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="34153-103">SetBoolInBlob function</span></span>

<span data-ttu-id="34153-104">La fonction **SetBoolInBlob** définit une valeur booléenne à un emplacement donné au sein d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="34153-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="34153-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34153-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="34153-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34153-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34153-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34153-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34153-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="34153-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="34153-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34153-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34153-110">Pointeur vers le nom du **propriétaire** de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="34153-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="34153-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34153-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34153-112">Pointeur vers le nom de la **catégorie** d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="34153-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="34153-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34153-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34153-114">Pointeur vers le nom de la **balise** d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="34153-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="34153-115">Valeur *booléenne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34153-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34153-116">Valeur booléenne définie à l’emplacement donné.</span><span class="sxs-lookup"><span data-stu-id="34153-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34153-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34153-117">Return value</span></span>

<span data-ttu-id="34153-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="34153-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="34153-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="34153-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="34153-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34153-120">Requirements</span></span>



| <span data-ttu-id="34153-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34153-121">Requirement</span></span> | <span data-ttu-id="34153-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="34153-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34153-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34153-123">Minimum supported client</span></span><br/> | <span data-ttu-id="34153-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34153-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="34153-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34153-125">Minimum supported server</span></span><br/> | <span data-ttu-id="34153-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34153-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34153-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="34153-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="34153-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="34153-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="34153-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="34153-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="34153-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34153-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="34153-131">DLL</span><span class="sxs-lookup"><span data-stu-id="34153-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34153-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34153-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34153-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34153-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34153-134">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="34153-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="34153-135">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="34153-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="34153-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




