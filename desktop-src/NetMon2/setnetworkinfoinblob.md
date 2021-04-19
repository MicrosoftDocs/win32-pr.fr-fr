---
description: La fonction SetNetworkInfoInBlob remplit la structure NETWORKINFO dans l’objet BLOB.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: SetNetworkInfoInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528223"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="f8918-103">SetNetworkInfoInBlob fonction)</span><span class="sxs-lookup"><span data-stu-id="f8918-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="f8918-104">La fonction **SetNetworkInfoInBlob** remplit la structure **NETWORKINFO** dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="f8918-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8918-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8918-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f8918-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8918-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8918-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8918-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8918-108">Handle vers un objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="f8918-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="f8918-109">*lpNetworkInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8918-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8918-110">Pointeur vers la structure [NETWORKINFO](networkinfo.md) allouée par l’utilisateur que la fonction remplit.</span><span class="sxs-lookup"><span data-stu-id="f8918-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8918-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8918-111">Return value</span></span>

<span data-ttu-id="f8918-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f8918-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f8918-113">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f8918-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8918-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8918-114">Requirements</span></span>



| <span data-ttu-id="f8918-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8918-115">Requirement</span></span> | <span data-ttu-id="f8918-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8918-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8918-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8918-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8918-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8918-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f8918-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8918-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8918-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8918-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f8918-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8918-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8918-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8918-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="f8918-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8918-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8918-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8918-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8918-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f8918-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8918-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8918-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8918-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8918-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8918-128">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-133">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="f8918-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="f8918-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




