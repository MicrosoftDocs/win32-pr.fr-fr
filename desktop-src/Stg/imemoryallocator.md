---
title: IMemoryAllocator, classe
description: Implémenté par l’allocateur de mémoire pour la fonction StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Stockage structuré de la classe IMemoryAllocator
- Stockage structuré de la classe IMemoryAllocator, Description
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384764"
---
# <a name="imemoryallocator-class"></a><span data-ttu-id="ae2a7-105">IMemoryAllocator, classe</span><span class="sxs-lookup"><span data-stu-id="ae2a7-105">IMemoryAllocator class</span></span>

<span data-ttu-id="ae2a7-106">La classe **IMemoryAllocator** est implémentée par l’allocateur de mémoire pour la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="ae2a7-106">The **IMemoryAllocator** class is implemented by the memory allocator for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="methods"></a><span data-ttu-id="ae2a7-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ae2a7-107">Methods</span></span>



| <span data-ttu-id="ae2a7-108">Nom</span><span class="sxs-lookup"><span data-stu-id="ae2a7-108">Name</span></span>                                                     | <span data-ttu-id="ae2a7-109">Description</span><span class="sxs-lookup"><span data-stu-id="ae2a7-109">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae2a7-110">**Lui**</span><span class="sxs-lookup"><span data-stu-id="ae2a7-110">**Allocate**</span></span>](imemoryallocator-allocate.md)<br/> | <span data-ttu-id="ae2a7-111">Alloue de la mémoire pour la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) lorsque la fonction convertit un type de données **SERIALIZEDPROPERTYVALUE** en un type de données **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="ae2a7-111">Allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span><br/> |
| [<span data-ttu-id="ae2a7-112">**Gratuit**</span><span class="sxs-lookup"><span data-stu-id="ae2a7-112">**Free**</span></span>](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | <span data-ttu-id="ae2a7-113">Libère la mémoire allouée par la méthode [**allocate**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="ae2a7-113">Frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span><br/>                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ae2a7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ae2a7-114">Remarks</span></span>

<span data-ttu-id="ae2a7-115">Cette classe est utilisée uniquement par la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .</span><span class="sxs-lookup"><span data-stu-id="ae2a7-115">This class is only used by the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2a7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae2a7-116">Requirements</span></span>



| <span data-ttu-id="ae2a7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae2a7-117">Requirement</span></span> | <span data-ttu-id="ae2a7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae2a7-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2a7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae2a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2a7-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae2a7-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ae2a7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae2a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2a7-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae2a7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ae2a7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae2a7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae2a7-124"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae2a7-124"><dt>Ole32.lib</dt></span></span> </dl> |



 

