---
description: La fonction GetFrameSrcAddressOffset retourne le décalage de l’adresse source des frames.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: GetFrameSrcAddressOffset, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204011"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="762c7-103">GetFrameSrcAddressOffset fonction)</span><span class="sxs-lookup"><span data-stu-id="762c7-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="762c7-104">La fonction **GetFrameSrcAddressOffset** retourne le décalage de l’adresse source du frame.</span><span class="sxs-lookup"><span data-stu-id="762c7-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="762c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="762c7-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="762c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="762c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762c7-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="762c7-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="762c7-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="762c7-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="762c7-109">*Typedadresse*</span><span class="sxs-lookup"><span data-stu-id="762c7-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="762c7-110">Type d’adresse source.</span><span class="sxs-lookup"><span data-stu-id="762c7-110">Source address type.</span></span> <span data-ttu-id="762c7-111">La valeur du paramètre peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="762c7-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="762c7-112">TYPE d’adresse \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="762c7-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="762c7-113">ADRESSE \_ IP du type d’adresse \_</span><span class="sxs-lookup"><span data-stu-id="762c7-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="762c7-114">TYPE d’adresse \_ \_ IPX</span><span class="sxs-lookup"><span data-stu-id="762c7-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="762c7-115">TYPE d’adresse \_ \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="762c7-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="762c7-116">TYPE d’adresse \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="762c7-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="762c7-117">TYPE d’adresse \_ \_ XNS</span><span class="sxs-lookup"><span data-stu-id="762c7-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="762c7-118">TYPE d’adresse \_ \_ IP Vines \_</span><span class="sxs-lookup"><span data-stu-id="762c7-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="762c7-119">TYPE d’adresse \_ \_ ATM</span><span class="sxs-lookup"><span data-stu-id="762c7-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="762c7-120">*AddressLength*</span><span class="sxs-lookup"><span data-stu-id="762c7-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="762c7-121">Pointeur vers une **valeur DWORD**, qui, en retour, contient la longueur de l’adresse, en octets.</span><span class="sxs-lookup"><span data-stu-id="762c7-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762c7-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="762c7-122">Return value</span></span>

<span data-ttu-id="762c7-123">Si la fonction réussit, la valeur de retour est le décalage de l’adresse source.</span><span class="sxs-lookup"><span data-stu-id="762c7-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="762c7-124">Si la fonction échoue, la valeur de retour est moins un (-1).</span><span class="sxs-lookup"><span data-stu-id="762c7-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="762c7-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="762c7-125">Requirements</span></span>



| <span data-ttu-id="762c7-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="762c7-126">Requirement</span></span> | <span data-ttu-id="762c7-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="762c7-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="762c7-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="762c7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="762c7-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="762c7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="762c7-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="762c7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="762c7-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="762c7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="762c7-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="762c7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="762c7-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="762c7-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="762c7-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="762c7-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="762c7-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="762c7-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="762c7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="762c7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="762c7-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="762c7-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




