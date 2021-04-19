---
description: La fonction GetNetworkInfoFromBlob récupère les informations réseau à partir d’un objet BLOB donné.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: GetNetworkInfoFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529502"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="59a0d-103">GetNetworkInfoFromBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="59a0d-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="59a0d-104">La fonction **GetNetworkInfoFromBlob** récupère les informations réseau à partir d’un objet BLOB donné.</span><span class="sxs-lookup"><span data-stu-id="59a0d-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59a0d-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="59a0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a0d-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59a0d-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59a0d-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="59a0d-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="59a0d-109">*lpNetworkInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59a0d-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59a0d-110">Pointeur vers la structure [NETWORKINFO](networkinfo.md) allouée par l’utilisateur qui est remplie.</span><span class="sxs-lookup"><span data-stu-id="59a0d-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a0d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59a0d-111">Return value</span></span>

<span data-ttu-id="59a0d-112">Si la fonction **GetNetworkInfoFromBlob** réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="59a0d-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="59a0d-113">Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="59a0d-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a0d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="59a0d-114">Remarks</span></span>

<span data-ttu-id="59a0d-115">Les informations réseau sont stockées dans la section BLOB **NetworkInfo** de la catégorie **propriétaire** NPP d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="59a0d-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a0d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59a0d-116">Requirements</span></span>



| <span data-ttu-id="59a0d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59a0d-117">Requirement</span></span> | <span data-ttu-id="59a0d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="59a0d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59a0d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59a0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59a0d-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59a0d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="59a0d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59a0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59a0d-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59a0d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59a0d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="59a0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59a0d-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="59a0d-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="59a0d-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59a0d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="59a0d-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59a0d-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="59a0d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="59a0d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59a0d-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59a0d-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59a0d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59a0d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a0d-130">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-131">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-132">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-133">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-135">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-136">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-137">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-138">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="59a0d-139">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="59a0d-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




