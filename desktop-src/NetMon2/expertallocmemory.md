---
description: La fonction ExpertAllocMemory alloue de la mémoire à l’expert.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: ExpertAllocMemory, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750108"
---
# <a name="expertallocmemory-function"></a><span data-ttu-id="55bfc-103">ExpertAllocMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="55bfc-103">ExpertAllocMemory function</span></span>

<span data-ttu-id="55bfc-104">La fonction **ExpertAllocMemory** alloue de la mémoire à l’expert.</span><span class="sxs-lookup"><span data-stu-id="55bfc-104">The **ExpertAllocMemory** function allocates memory for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bfc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55bfc-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="55bfc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55bfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bfc-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="55bfc-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="55bfc-108">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="55bfc-108">Unique expert identifier.</span></span> <span data-ttu-id="55bfc-109">Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="55bfc-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="55bfc-110">*nBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55bfc-110">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55bfc-111">Mémoire allouée, mesurée en octets.</span><span class="sxs-lookup"><span data-stu-id="55bfc-111">Allocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="55bfc-112">*perror* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="55bfc-112">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55bfc-113">Indicateur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="55bfc-113">Error indicator.</span></span> <span data-ttu-id="55bfc-114">Si la fonction échoue, le paramètre *nBytes* contient le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="55bfc-114">If the function fails, the *nBytes* parameter contains the error code.</span></span> <span data-ttu-id="55bfc-115">Si le code d’erreur est NMERR \_ expert \_ Terminate, l’expert doit le nettoyer et le renvoyer immédiatement.</span><span class="sxs-lookup"><span data-stu-id="55bfc-115">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean-up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55bfc-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55bfc-116">Return value</span></span>

<span data-ttu-id="55bfc-117">Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="55bfc-117">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="55bfc-118">Si la fonction échoue, la valeur de retour est **null** et *perror* fournit un code d’erreur qui indique la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="55bfc-118">If the function is unsuccessful, the return value is **NULL**, and *pError* provides an error code that indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="55bfc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="55bfc-119">Remarks</span></span>

<span data-ttu-id="55bfc-120">Il est important de noter qu’un expert doit utiliser les fonctions d’allocation de mémoire Moniteur réseau (y compris [ExpertReallocMemory](expertreallocmemory.md)) pour la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="55bfc-120">It is important to note that an expert should use the Network Monitor memory allocation functions (including [ExpertReallocMemory](expertreallocmemory.md)) for memory management.</span></span> <span data-ttu-id="55bfc-121">Si votre expert échoue au moment de l’exécution, l’utilisation de ces fonctions permettra à Moniteur réseau de libérer la mémoire qu’il a allouée.</span><span class="sxs-lookup"><span data-stu-id="55bfc-121">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bfc-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55bfc-122">Requirements</span></span>



| <span data-ttu-id="55bfc-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55bfc-123">Requirement</span></span> | <span data-ttu-id="55bfc-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="55bfc-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55bfc-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55bfc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55bfc-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55bfc-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55bfc-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55bfc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55bfc-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55bfc-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55bfc-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="55bfc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bfc-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="55bfc-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="55bfc-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="55bfc-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="55bfc-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55bfc-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="55bfc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="55bfc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bfc-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bfc-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




