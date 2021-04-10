---
title: Méthode IMemoryAllocator Free
description: La méthode Free libère la mémoire allouée par la méthode Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Stockage structuré de méthode libre
- Free, méthode stockage structuré, interface IMemoryAllocator
- Stockage structuré de l’interface IMemoryAllocator, méthode libre
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032458"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="9c01b-106">IMemoryAllocator :: Free, méthode</span><span class="sxs-lookup"><span data-stu-id="9c01b-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="9c01b-107">La méthode **Free** libère la mémoire allouée par la méthode [**allocate**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="9c01b-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c01b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c01b-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="9c01b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c01b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c01b-110">*va*</span><span class="sxs-lookup"><span data-stu-id="9c01b-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="9c01b-111">Pointeur vers la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="9c01b-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c01b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c01b-112">Requirements</span></span>



| <span data-ttu-id="9c01b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c01b-113">Requirement</span></span> | <span data-ttu-id="9c01b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c01b-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c01b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c01b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9c01b-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c01b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9c01b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c01b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9c01b-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c01b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c01b-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9c01b-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c01b-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c01b-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





