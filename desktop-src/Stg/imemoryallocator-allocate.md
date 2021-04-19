---
title: IMemoryAllocator Allocate, méthode
description: La méthode Allocate alloue de la mémoire pour la fonction StgConvertPropertyToVariant lorsque la fonction convertit un type de données SERIALIZEDPROPERTYVALUE en un type de données PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Allouer une méthode stockage structuré
- Allouer une méthode stockage structuré, interface IMemoryAllocator
- Stockage structuré de l’interface IMemoryAllocator, méthode Allocate
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106532044"
---
# <a name="imemoryallocatorallocate-method"></a><span data-ttu-id="9c1d8-106">IMemoryAllocator :: Allocate, méthode</span><span class="sxs-lookup"><span data-stu-id="9c1d8-106">IMemoryAllocator::Allocate method</span></span>

<span data-ttu-id="9c1d8-107">La méthode **allocate** alloue de la mémoire pour la fonction [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) lorsque la fonction convertit un type de données **SERIALIZEDPROPERTYVALUE** en un type de données **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="9c1d8-107">The **Allocate** method allocates memory for the [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) function when the function converts a **SERIALIZEDPROPERTYVALUE** data type to a **PROPVARIANT** data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c1d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c1d8-108">Syntax</span></span>


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="9c1d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c1d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1d8-110">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9c1d8-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1d8-111">Spécifie la taille de la mémoire à allouer.</span><span class="sxs-lookup"><span data-stu-id="9c1d8-111">Specifies the size of memory to be allocated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c1d8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c1d8-112">Requirements</span></span>



| <span data-ttu-id="9c1d8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c1d8-113">Requirement</span></span> | <span data-ttu-id="9c1d8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c1d8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1d8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c1d8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9c1d8-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c1d8-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9c1d8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9c1d8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9c1d8-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9c1d8-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c1d8-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9c1d8-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c1d8-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c1d8-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

