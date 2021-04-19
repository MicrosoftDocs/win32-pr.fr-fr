---
description: La fonction GetFrameDstAddressOffset retourne l’offset à l’adresse de destination d’un frame donné.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: GetFrameDstAddressOffset, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517231"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="0dc2d-103">GetFrameDstAddressOffset fonction)</span><span class="sxs-lookup"><span data-stu-id="0dc2d-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="0dc2d-104">La fonction **GetFrameDstAddressOffset** retourne l’offset à l’adresse de destination d’un frame donné.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dc2d-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="0dc2d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dc2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc2d-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc2d-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2d-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="0dc2d-109">*AddressType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc2d-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2d-110">Type de l’adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-110">Type of the destination address.</span></span> <span data-ttu-id="0dc2d-111">Spécifiez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0dc2d-111">Specify one of the following values:</span></span>

<span data-ttu-id="0dc2d-112">type d’adresse Ethernet adresse type adresse \_ \_ \_ \_ IP \_ type adresse IPX type d’adresse TOKENRING type d’adresse \_ \_ \_ \_ \_ FDDI adresse \_ type XNS adresse type de l’adresse \_ \_ \_ \_ IP \_ type \_ ATM.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="0dc2d-113">*AddressLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc2d-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc2d-114">Longueur de l’adresse de destination, en octets.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc2d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dc2d-115">Return value</span></span>

<span data-ttu-id="0dc2d-116">Si la fonction réussit, la valeur de retour est le décalage (en octets) du type d’adresse demandé.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="0dc2d-117">Si la fonction échoue, la valeur de retour est moins un (-1).</span><span class="sxs-lookup"><span data-stu-id="0dc2d-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc2d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0dc2d-118">Remarks</span></span>

<span data-ttu-id="0dc2d-119">Si le paramètre *AddressType* est défini sur le \_ type d’adresse \_ Ethernet, la valeur de retour de la fonction **GetFrameDstAddressOffset** est toujours égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="0dc2d-120">Le décalage d’une adresse Ethernet est toujours égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0dc2d-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="0dc2d-121">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameDstAddressOffset** .</span><span class="sxs-lookup"><span data-stu-id="0dc2d-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc2d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dc2d-122">Requirements</span></span>



| <span data-ttu-id="0dc2d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dc2d-123">Requirement</span></span> | <span data-ttu-id="0dc2d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dc2d-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc2d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc2d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc2d-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc2d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0dc2d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc2d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc2d-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc2d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0dc2d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0dc2d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc2d-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2d-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0dc2d-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0dc2d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="0dc2d-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2d-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0dc2d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0dc2d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dc2d-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dc2d-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




