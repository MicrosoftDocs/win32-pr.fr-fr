---
description: La fonction BERGetInteger décode un entier encodé BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: BERGetInteger, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867026"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="a538e-103">BERGetInteger fonction)</span><span class="sxs-lookup"><span data-stu-id="a538e-103">BERGetInteger function</span></span>

<span data-ttu-id="a538e-104">La fonction **BERGetInteger** décode un entier encodé Ber.</span><span class="sxs-lookup"><span data-stu-id="a538e-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a538e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a538e-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="a538e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a538e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a538e-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="a538e-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="a538e-108">Pointeur vers l’entier décodé.</span><span class="sxs-lookup"><span data-stu-id="a538e-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="a538e-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="a538e-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="a538e-110">Pointeur vers le pointeur vers la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="a538e-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="a538e-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="a538e-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="a538e-112">Pointeur vers la longueur d’en-tête retournée.</span><span class="sxs-lookup"><span data-stu-id="a538e-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="a538e-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="a538e-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="a538e-114">Pointeur vers la longueur des données.</span><span class="sxs-lookup"><span data-stu-id="a538e-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="a538e-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="a538e-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="a538e-116">Pointeur vers le pointeur vers l’entrée BER suivante.</span><span class="sxs-lookup"><span data-stu-id="a538e-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a538e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a538e-117">Return value</span></span>

<span data-ttu-id="a538e-118">Si la fonction réussit (autrement dit, si un entier encodé BER valide est trouvé et converti), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="a538e-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="a538e-119">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="a538e-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a538e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a538e-120">Requirements</span></span>



| <span data-ttu-id="a538e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a538e-121">Requirement</span></span> | <span data-ttu-id="a538e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a538e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a538e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a538e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a538e-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a538e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a538e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a538e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a538e-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a538e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a538e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a538e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a538e-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a538e-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="a538e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a538e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a538e-130"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a538e-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="a538e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a538e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a538e-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a538e-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




