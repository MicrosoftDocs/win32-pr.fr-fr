---
description: La fonction ExpertReallocMemory augmente ou diminue la quantité de mémoire allouée par Moniteur réseau.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: ExpertReallocMemory, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514786"
---
# <a name="expertreallocmemory-function"></a><span data-ttu-id="b3c86-103">ExpertReallocMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="b3c86-103">ExpertReallocMemory function</span></span>

<span data-ttu-id="b3c86-104">La fonction **ExpertReallocMemory** augmente ou diminue la quantité de mémoire allouée par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="b3c86-104">The **ExpertReallocMemory** function increases or decreases the amount of memory allocated by Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c86-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3c86-105">Syntax</span></span>


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a><span data-ttu-id="b3c86-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3c86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c86-107">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c86-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c86-108">Identificateur unique transmis à l’expert lors de l' [**exécution**](run.md) ou de la [**configuration**](configure.md).</span><span class="sxs-lookup"><span data-stu-id="b3c86-108">Unique identifier passed to the expert at [**Run**](run.md) or [**Configure**](configure.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3c86-109">*pOriginalMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c86-109">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c86-110">Pointeur vers la mémoire allouée par Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="b3c86-110">Pointer to the memory allocated by Network Monitor.</span></span> <span data-ttu-id="b3c86-111">Le pointeur *pOriginalMemory* peut être retourné par un appel précédent à [**ExpertAllocMemory**](expertallocmemory.md) ou **ExpertReallocMemory**.</span><span class="sxs-lookup"><span data-stu-id="b3c86-111">The *pOriginalMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or **ExpertReallocMemory**.</span></span>

</dd> <dt>

<span data-ttu-id="b3c86-112">*nBytes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3c86-112">*nBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c86-113">Taille de la mémoire réallouée.</span><span class="sxs-lookup"><span data-stu-id="b3c86-113">Size of reallocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="b3c86-114">*perror* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3c86-114">*pError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c86-115">Au retour, code d’erreur si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="b3c86-115">On return, an error code if the function fails.</span></span> <span data-ttu-id="b3c86-116">Si le code d’erreur est NMERR \_ expert \_ Terminate, l’expert doit le nettoyer et le retourner immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b3c86-116">If the error code is NMERR\_EXPERT\_TERMINATE, the expert must clean up and return immediately.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c86-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3c86-117">Return value</span></span>

<span data-ttu-id="b3c86-118">Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="b3c86-118">If the function is successful, the return value is a pointer to the allocated memory.</span></span>

<span data-ttu-id="b3c86-119">Si la fonction échoue, la valeur de retour est **null** et *perror* (s’il s’agit d’une valeur non **null** ) indique la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="b3c86-119">If the function is unsuccessful, the return value is **NULL**, and *pError* (if it is a non-**NULL** value) indicates the reason for the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c86-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b3c86-120">Remarks</span></span>

<span data-ttu-id="b3c86-121">Il est important de noter qu’un expert doit utiliser les fonctions d’allocation de mémoire Moniteur réseau pour la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b3c86-121">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="b3c86-122">Si votre expert échoue au moment de l’exécution, l’utilisation de ces fonctions permettra à Moniteur réseau de libérer la mémoire qu’il a allouée.</span><span class="sxs-lookup"><span data-stu-id="b3c86-122">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c86-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3c86-123">Requirements</span></span>



| <span data-ttu-id="b3c86-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3c86-124">Requirement</span></span> | <span data-ttu-id="b3c86-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3c86-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c86-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c86-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c86-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c86-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b3c86-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3c86-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c86-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3c86-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b3c86-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3c86-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c86-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c86-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b3c86-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3c86-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3c86-133"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c86-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3c86-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c86-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c86-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c86-135"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




