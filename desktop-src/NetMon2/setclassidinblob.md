---
description: La fonction SetClassIDInBlob définit la valeur de l’identificateur de classe nommée d’un objet BLOB.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: SetClassIDInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518421"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="c9537-103">SetClassIDInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="c9537-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="c9537-104">La fonction **SetClassIDInBlob** définit la valeur de l’identificateur de classe nommée d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9537-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9537-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9537-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="c9537-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9537-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9537-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9537-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9537-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="c9537-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="c9537-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9537-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9537-110">Pointeur vers le nom du **propriétaire** de l’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="c9537-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="c9537-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9537-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9537-112">Pointeur vers le nom de **catégorie** d’objet BLOB défini.</span><span class="sxs-lookup"><span data-stu-id="c9537-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="c9537-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9537-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9537-114">Pointeur vers le nom de **balise** d’objet BLOB défini.</span><span class="sxs-lookup"><span data-stu-id="c9537-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="c9537-115">*pClsID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9537-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9537-116">Pointeur vers l’identificateur de classe de l’objet BLOB défini.</span><span class="sxs-lookup"><span data-stu-id="c9537-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9537-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9537-117">Return value</span></span>

<span data-ttu-id="c9537-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c9537-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c9537-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c9537-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9537-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9537-120">Requirements</span></span>



| <span data-ttu-id="c9537-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9537-121">Requirement</span></span> | <span data-ttu-id="c9537-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9537-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9537-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9537-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c9537-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9537-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c9537-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9537-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c9537-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9537-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9537-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9537-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9537-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9537-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c9537-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9537-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9537-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9537-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9537-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c9537-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9537-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9537-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9537-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9537-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9537-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="c9537-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="c9537-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




