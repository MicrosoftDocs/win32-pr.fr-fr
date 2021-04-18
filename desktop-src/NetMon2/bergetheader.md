---
description: La fonction BERGetHeader décode un en-tête Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: BERGetHeader, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519092"
---
# <a name="bergetheader-function"></a><span data-ttu-id="f2371-103">BERGetHeader fonction)</span><span class="sxs-lookup"><span data-stu-id="f2371-103">BERGetHeader function</span></span>

<span data-ttu-id="f2371-104">La fonction **BERGetHeader** décode un en-tête Choice.</span><span class="sxs-lookup"><span data-stu-id="f2371-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2371-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2371-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="f2371-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2371-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2371-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="f2371-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="f2371-108">Pointeur désignant l’en-tête Choice.</span><span class="sxs-lookup"><span data-stu-id="f2371-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="f2371-109">*pTag*</span><span class="sxs-lookup"><span data-stu-id="f2371-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="f2371-110">Pointeur désignant la balise retournée.</span><span class="sxs-lookup"><span data-stu-id="f2371-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="f2371-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="f2371-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="f2371-112">Pointeur vers la longueur d’en-tête retournée.</span><span class="sxs-lookup"><span data-stu-id="f2371-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="f2371-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="f2371-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="f2371-114">Pointeur vers la longueur des données retournées.</span><span class="sxs-lookup"><span data-stu-id="f2371-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="f2371-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="f2371-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="f2371-116">Pointeur vers le contenu d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="f2371-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2371-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2371-117">Return value</span></span>

<span data-ttu-id="f2371-118">Si la fonction réussit (autrement dit, un en-tête de choix BER valide est trouvé), la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="f2371-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="f2371-119">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="f2371-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2371-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2371-120">Requirements</span></span>



| <span data-ttu-id="f2371-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2371-121">Requirement</span></span> | <span data-ttu-id="f2371-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2371-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2371-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2371-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f2371-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2371-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f2371-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2371-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f2371-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2371-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2371-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2371-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2371-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2371-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2371-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f2371-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2371-130"><dt>Analyseur. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2371-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2371-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f2371-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2371-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2371-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




