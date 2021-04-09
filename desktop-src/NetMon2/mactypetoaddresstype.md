---
description: La fonction MacTypeToAddressType convertit un type MAC donné en type d’adresse.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: MacTypeToAddressType, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862858"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="bda9f-103">MacTypeToAddressType fonction)</span><span class="sxs-lookup"><span data-stu-id="bda9f-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="bda9f-104">La fonction **MacTypeToAddressType** convertit un type Mac donné en type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="bda9f-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bda9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bda9f-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="bda9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bda9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bda9f-107">*MacType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bda9f-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bda9f-108">Type MAC à convertir.</span><span class="sxs-lookup"><span data-stu-id="bda9f-108">MAC type to be converted.</span></span> <span data-ttu-id="bda9f-109">Spécifiez l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bda9f-109">Specify one of the following values:</span></span>

<span data-ttu-id="bda9f-110">type MAC Ethernet Mac type \_ \_ \_ \_ TOKENRING \_ type \_ de Mac FDDI</span><span class="sxs-lookup"><span data-stu-id="bda9f-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bda9f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bda9f-111">Return value</span></span>

<span data-ttu-id="bda9f-112">Si la fonction réussit, la valeur de retour est l’un des types d’adresses suivants.</span><span class="sxs-lookup"><span data-stu-id="bda9f-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="bda9f-113">type d’adresse Ethernet adresse type adresse \_ \_ \_ \_ TOKENRING \_ type \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="bda9f-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="bda9f-114">Si la fonction échoue, le type MAC est inconnu, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="bda9f-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="bda9f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="bda9f-115">Remarks</span></span>

<span data-ttu-id="bda9f-116">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **MacTypeToAddressType** .</span><span class="sxs-lookup"><span data-stu-id="bda9f-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda9f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bda9f-117">Requirements</span></span>



| <span data-ttu-id="bda9f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bda9f-118">Requirement</span></span> | <span data-ttu-id="bda9f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bda9f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bda9f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bda9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bda9f-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bda9f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bda9f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bda9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bda9f-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bda9f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bda9f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bda9f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bda9f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bda9f-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="bda9f-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bda9f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bda9f-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bda9f-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="bda9f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bda9f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bda9f-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bda9f-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




