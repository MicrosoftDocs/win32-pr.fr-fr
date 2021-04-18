---
description: La fonction CompareAddresses compare deux adresses, ce qui indique que l’une des adresses est supérieure, inférieure ou égale à l’autre adresse.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: CompareAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526140"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="ffc78-103">CompareAddresses fonction)</span><span class="sxs-lookup"><span data-stu-id="ffc78-103">CompareAddresses function</span></span>

<span data-ttu-id="ffc78-104">La fonction **CompareAddresses** compare deux adresses, ce qui indique que l’une des adresses est supérieure, inférieure ou égale à l’autre adresse.</span><span class="sxs-lookup"><span data-stu-id="ffc78-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffc78-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="ffc78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffc78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc78-107">*lpAddress1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffc78-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc78-108">Pointeur vers la première adresse.</span><span class="sxs-lookup"><span data-stu-id="ffc78-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="ffc78-109">*lpAddress2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ffc78-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc78-110">Pointeur vers la deuxième adresse.</span><span class="sxs-lookup"><span data-stu-id="ffc78-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffc78-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffc78-111">Return value</span></span>

<span data-ttu-id="ffc78-112">Si les adresses sont identiques, la fonction retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="ffc78-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="ffc78-113">Si le paramètre *lpAddress1* spécifie une adresse qui est inférieure à l’adresse que le paramètre *lpAddress2* spécifie, la valeur de retour est un nombre négatif.</span><span class="sxs-lookup"><span data-stu-id="ffc78-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="ffc78-114">Si le paramètre *lpAddress1* spécifie une adresse qui est supérieure à l’adresse que le paramètre *lpAddress2* spécifie, la valeur de retour est un nombre positif.</span><span class="sxs-lookup"><span data-stu-id="ffc78-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffc78-115">Notes</span><span class="sxs-lookup"><span data-stu-id="ffc78-115">Remarks</span></span>

<span data-ttu-id="ffc78-116">Une adresse qui est inférieure à une autre adresse indique un frame précédent.</span><span class="sxs-lookup"><span data-stu-id="ffc78-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="ffc78-117">Une adresse supérieure à une autre adresse indique une trame ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ffc78-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="ffc78-118">Moniteur réseau fournit deux autres fonctions, [CompareFrameDestAddress](compareframedestaddress.md) et [CompareFrameSourceAddress](compareframesourceaddress.md), que vous pouvez utiliser pour comparer des adresses.</span><span class="sxs-lookup"><span data-stu-id="ffc78-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="ffc78-119">La fonction **CompareFrameDestAddress** compare une adresse donnée à l’adresse de destination du frame, et la fonction **CompareFrameSourceAddress** compare une adresse donnée à l’adresse source du frame.</span><span class="sxs-lookup"><span data-stu-id="ffc78-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc78-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffc78-120">Requirements</span></span>



| <span data-ttu-id="ffc78-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffc78-121">Requirement</span></span> | <span data-ttu-id="ffc78-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffc78-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc78-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffc78-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ffc78-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffc78-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ffc78-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffc78-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ffc78-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffc78-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ffc78-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffc78-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffc78-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffc78-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ffc78-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffc78-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="ffc78-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffc78-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ffc78-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ffc78-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffc78-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffc78-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffc78-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffc78-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc78-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="ffc78-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="ffc78-135">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="ffc78-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




