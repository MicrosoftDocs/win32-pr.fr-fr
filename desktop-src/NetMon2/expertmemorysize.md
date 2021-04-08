---
description: La fonction ExpertMemorySize retourne la quantité de mémoire allouée par la fonction ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: ExpertMemorySize, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57c83bc3e9535550086c9732b33a71a357e4da42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862018"
---
# <a name="expertmemorysize-function"></a><span data-ttu-id="7a23f-103">ExpertMemorySize fonction)</span><span class="sxs-lookup"><span data-stu-id="7a23f-103">ExpertMemorySize function</span></span>

<span data-ttu-id="7a23f-104">La fonction **ExpertMemorySize** retourne la quantité de mémoire allouée par la fonction [ExpertAllocMemory](expertallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="7a23f-104">The **ExpertMemorySize** function returns the amount of memory allocated by the [ExpertAllocMemory](expertallocmemory.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a23f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a23f-105">Syntax</span></span>


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a><span data-ttu-id="7a23f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a23f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a23f-107">*hExpertKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a23f-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a23f-108">Identificateur d’expert unique.</span><span class="sxs-lookup"><span data-stu-id="7a23f-108">Unique expert identifier.</span></span> <span data-ttu-id="7a23f-109">Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="7a23f-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7a23f-110">*pOriginalMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a23f-110">*pOriginalMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a23f-111">Pointeur vers l’adresse mémoire de l’expert alloué par [ExpertAllocMemory](expertallocmemory.md).</span><span class="sxs-lookup"><span data-stu-id="7a23f-111">Pointer to the memory address of the expert allocated by [ExpertAllocMemory](expertallocmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a23f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a23f-112">Return value</span></span>

<span data-ttu-id="7a23f-113">La fonction retourne la quantité de mémoire allouée en octets.</span><span class="sxs-lookup"><span data-stu-id="7a23f-113">The function returns the amount of allocated memory   in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a23f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7a23f-114">Remarks</span></span>

<span data-ttu-id="7a23f-115">Pour plus d’informations sur le type de données **size \_ T** renvoyé par **ExpertMemorySize** , consultez types de données.</span><span class="sxs-lookup"><span data-stu-id="7a23f-115">For information on the **SIZE\_T** data type that **ExpertMemorySize** returns, see Data Types.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a23f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a23f-116">Requirements</span></span>



| <span data-ttu-id="7a23f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a23f-117">Requirement</span></span> | <span data-ttu-id="7a23f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a23f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a23f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a23f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a23f-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a23f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7a23f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a23f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a23f-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a23f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a23f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a23f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a23f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a23f-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7a23f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a23f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a23f-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a23f-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a23f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a23f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a23f-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a23f-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




