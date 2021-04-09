---
description: La fonction BERGetString décode une chaîne encodée BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: BERGetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864805"
---
# <a name="bergetstring-function"></a><span data-ttu-id="9d1cb-103">BERGetString fonction)</span><span class="sxs-lookup"><span data-stu-id="9d1cb-103">BERGetString function</span></span>

<span data-ttu-id="9d1cb-104">La fonction **BERGetString** décode une chaîne encodée Ber.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-104">The **BERGetString** function decodes a BER-encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d1cb-105">Syntax</span></span>


```C++
BOOL BERGetString(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="9d1cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d1cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d1cb-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="9d1cb-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9d1cb-108">Pointeur vers la chaîne décodée.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-108">Pointer to the string that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="9d1cb-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="9d1cb-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9d1cb-110">Pointeur vers le pointeur de la chaîne décodée.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-110">Pointer to the pointer of the decoded string.</span></span>

</dd> <dt>

<span data-ttu-id="9d1cb-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="9d1cb-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9d1cb-112">Pointeur vers la longueur d’en-tête retournée.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="9d1cb-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="9d1cb-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="9d1cb-114">Pointeur vers la longueur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-114">Pointer to the string length.</span></span>

</dd> <dt>

<span data-ttu-id="9d1cb-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="9d1cb-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="9d1cb-116">Pointeur vers le pointeur de l’entrée BER suivante.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-116">Pointer to the pointer of the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d1cb-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d1cb-117">Return value</span></span>

<span data-ttu-id="9d1cb-118">Si la fonction réussit (autrement dit, si une chaîne codée BER valide est décodée), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-118">If the function is successful (that is, if a valid BER-encoded string is decoded), the return value is **TRUE**.</span></span>

<span data-ttu-id="9d1cb-119">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="9d1cb-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d1cb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d1cb-120">Requirements</span></span>



| <span data-ttu-id="9d1cb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d1cb-121">Requirement</span></span> | <span data-ttu-id="9d1cb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d1cb-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1cb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d1cb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1cb-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d1cb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9d1cb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d1cb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1cb-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d1cb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d1cb-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d1cb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d1cb-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d1cb-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d1cb-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d1cb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d1cb-130"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d1cb-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d1cb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9d1cb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1cb-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d1cb-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




