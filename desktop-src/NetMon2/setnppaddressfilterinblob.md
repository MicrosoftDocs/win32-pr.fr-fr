---
description: La fonction SetNPPAddressFilterInBlob définit le filtre d’adresse donné dans l’objet BLOB.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: SetNPPAddressFilterInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530257"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="3af3b-103">SetNPPAddressFilterInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="3af3b-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="3af3b-104">La fonction **SetNPPAddressFilterInBlob** définit le filtre d’adresse donné dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="3af3b-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3af3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3af3b-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="3af3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3af3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3af3b-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3af3b-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af3b-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="3af3b-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3af3b-109">*pAddressTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3af3b-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af3b-110">Pointeur vers une structure [**ADDRESSTABLE**](addresstable.md) qui définit la table d’adresses allouées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3af3b-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3af3b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3af3b-111">Return value</span></span>

<span data-ttu-id="3af3b-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3af3b-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3af3b-113">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3af3b-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3af3b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3af3b-114">Requirements</span></span>



| <span data-ttu-id="3af3b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3af3b-115">Requirement</span></span> | <span data-ttu-id="3af3b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3af3b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3af3b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3af3b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3af3b-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3af3b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3af3b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3af3b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3af3b-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3af3b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3af3b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3af3b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3af3b-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3af3b-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3af3b-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3af3b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3af3b-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3af3b-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3af3b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3af3b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3af3b-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3af3b-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af3b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3af3b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af3b-128">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-133">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="3af3b-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="3af3b-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




