---
description: La fonction ExpertFreeMemory libère de la mémoire acquise par les appels aux fonctions ExpertAllocMemory et ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: ExpertFreeMemory, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517233"
---
# <a name="expertfreememory-function"></a><span data-ttu-id="1cff1-103">ExpertFreeMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="1cff1-103">ExpertFreeMemory function</span></span>

<span data-ttu-id="1cff1-104">La fonction **ExpertFreeMemory** libère de la mémoire acquise par les appels aux fonctions [**ExpertAllocMemory**](expertallocmemory.md) et [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="1cff1-104">The **ExpertFreeMemory** function frees memory acquired by calls to the [**ExpertAllocMemory**](expertallocmemory.md) and [**ExpertReallocMemory**](expertreallocmemory.md) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cff1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cff1-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="1cff1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cff1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cff1-107">*hExpertKey*</span><span class="sxs-lookup"><span data-stu-id="1cff1-107">*hExpertKey*</span></span> 
</dt> <dd>

<span data-ttu-id="1cff1-108">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="1cff1-108">Unique expert identifier.</span></span> <span data-ttu-id="1cff1-109">Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="1cff1-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1cff1-110">*pMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cff1-110">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cff1-111">Pointeur vers la mémoire que Moniteur réseau alloue.</span><span class="sxs-lookup"><span data-stu-id="1cff1-111">Pointer to the memory that Network Monitor allocates.</span></span> <span data-ttu-id="1cff1-112">Le pointeur *pMemory* peut être retourné par un appel précédent à [**ExpertAllocMemory**](expertallocmemory.md) ou [**ExpertReallocMemory**](expertreallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="1cff1-112">The *pMemory* pointer can be returned by a previous call to [**ExpertAllocMemory**](expertallocmemory.md) or [**ExpertReallocMemory**](expertreallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cff1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cff1-113">Return value</span></span>

<span data-ttu-id="1cff1-114">Si la fonction réussit.</span><span class="sxs-lookup"><span data-stu-id="1cff1-114">If the function is successful.</span></span> <span data-ttu-id="1cff1-115">la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1cff1-115">the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1cff1-116">Si la fonction échoue, la valeur de retour indique la raison de l’échec.</span><span class="sxs-lookup"><span data-stu-id="1cff1-116">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="1cff1-117">Si la valeur de retour est NMERR \_ expert \_ Terminate, l’expert nettoie immédiatement et retourne.</span><span class="sxs-lookup"><span data-stu-id="1cff1-117">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cff1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1cff1-118">Remarks</span></span>

<span data-ttu-id="1cff1-119">Il est important de noter qu’un expert doit utiliser les fonctions d’allocation de mémoire Moniteur réseau pour la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1cff1-119">It is important to note that an expert should use the Network Monitor memory allocation functions for memory management.</span></span> <span data-ttu-id="1cff1-120">Si votre expert échoue au moment de l’exécution, l’utilisation de ces fonctions permettra à Moniteur réseau de libérer la mémoire qu’il a allouée.</span><span class="sxs-lookup"><span data-stu-id="1cff1-120">If your expert fails during run time, using these functions will allow Network Monitor to free the memory it has allocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cff1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cff1-121">Requirements</span></span>



| <span data-ttu-id="1cff1-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cff1-122">Requirement</span></span> | <span data-ttu-id="1cff1-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cff1-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1cff1-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cff1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1cff1-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cff1-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1cff1-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cff1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1cff1-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cff1-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1cff1-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cff1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cff1-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cff1-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1cff1-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1cff1-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cff1-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cff1-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1cff1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1cff1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cff1-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cff1-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




