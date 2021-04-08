---
description: La fonction SetMacAddressInBlob définit l’adresse MAC demandée d’un objet BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: SetMacAddressInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866698"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="1a5ba-103">SetMacAddressInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="1a5ba-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="1a5ba-104">La fonction **SetMacAddressInBlob** définit l’adresse Mac demandée d’un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a5ba-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="1a5ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a5ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a5ba-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5ba-108">Handle vers l’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="1a5ba-109">*pOwnerName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5ba-110">Pointeur vers le nom du **propriétaire** de l’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1a5ba-111">*pCategoryName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5ba-112">Pointeur vers le nom de **catégorie** d’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1a5ba-113">*pTagName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5ba-114">Pointeur vers le nom de **balise** d’objet BLOB qui est défini.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="1a5ba-115">*pMacAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a5ba-116">Pointeur vers l’adresse MAC de l’objet BLOB en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a5ba-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a5ba-117">Return value</span></span>

<span data-ttu-id="1a5ba-118">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1a5ba-119">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1a5ba-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a5ba-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a5ba-120">Requirements</span></span>



| <span data-ttu-id="1a5ba-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a5ba-121">Requirement</span></span> | <span data-ttu-id="1a5ba-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a5ba-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a5ba-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a5ba-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1a5ba-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a5ba-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a5ba-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1a5ba-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a5ba-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a5ba-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a5ba-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a5ba-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a5ba-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1a5ba-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a5ba-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a5ba-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a5ba-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a5ba-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1a5ba-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a5ba-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a5ba-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a5ba-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a5ba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a5ba-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-137">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="1a5ba-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="1a5ba-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




