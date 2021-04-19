---
description: La fonction GetPreviousProtocolOffsetByName retourne l’instance précédente d’un protocole donné.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: GetPreviousProtocolOffsetByName, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544616"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="4dd7a-103">GetPreviousProtocolOffsetByName fonction)</span><span class="sxs-lookup"><span data-stu-id="4dd7a-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="4dd7a-104">La fonction **GetPreviousProtocolOffsetByName** retourne l’instance précédente d’un protocole donné.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd7a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dd7a-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="4dd7a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dd7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd7a-107">*hFrame* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4dd7a-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd7a-108">Handle vers le frame.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="4dd7a-109">*dwStartOffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4dd7a-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd7a-110">Décalage dans le frame.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="4dd7a-111">*szProtocolName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4dd7a-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd7a-112">Nom du protocole que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="4dd7a-113">*pdwPreviousOffset* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4dd7a-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd7a-114">Pointeur vers une **valeur DWORD** qui contient l’offset au protocole précédent (si la fonction est réussie).</span><span class="sxs-lookup"><span data-stu-id="4dd7a-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd7a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4dd7a-115">Return value</span></span>

<span data-ttu-id="4dd7a-116">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4dd7a-117">Si la fonction échoue, la valeur de retour est le protocole NMERR \_ est \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd7a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4dd7a-118">Remarks</span></span>

<span data-ttu-id="4dd7a-119">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler **GetPreviousProtocolOffsetByName**.</span><span class="sxs-lookup"><span data-stu-id="4dd7a-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd7a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4dd7a-120">Requirements</span></span>



| <span data-ttu-id="4dd7a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dd7a-121">Requirement</span></span> | <span data-ttu-id="4dd7a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dd7a-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd7a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dd7a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd7a-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dd7a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4dd7a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dd7a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd7a-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dd7a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4dd7a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dd7a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd7a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7a-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4dd7a-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4dd7a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dd7a-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7a-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="4dd7a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4dd7a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dd7a-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dd7a-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




