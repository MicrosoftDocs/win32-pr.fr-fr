---
title: macro min (Minwindef. h)
description: La macro min compare deux valeurs et en retourne une plus petite. Le type de données peut être n’importe quel type de données numérique, signé ou non signé. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- Windows-macro-multimédia min.
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743925"
---
# <a name="min-macro"></a><span data-ttu-id="ea67e-106">min (macro)</span><span class="sxs-lookup"><span data-stu-id="ea67e-106">min macro</span></span>

<span data-ttu-id="ea67e-107">La macro **min** compare deux valeurs et en retourne une plus petite.</span><span class="sxs-lookup"><span data-stu-id="ea67e-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="ea67e-108">Le type de données peut être n’importe quel type de données numérique, signé ou non signé.</span><span class="sxs-lookup"><span data-stu-id="ea67e-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="ea67e-109">Le type de données des arguments et la valeur de retour sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="ea67e-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea67e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea67e-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="ea67e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea67e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea67e-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="ea67e-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="ea67e-113">Spécifie la première des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea67e-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="ea67e-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="ea67e-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="ea67e-115">Spécifie la deuxième des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea67e-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea67e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea67e-116">Return value</span></span>

<span data-ttu-id="ea67e-117">La valeur de retour est la plus petite des deux valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="ea67e-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea67e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ea67e-118">Remarks</span></span>

<span data-ttu-id="ea67e-119">La macro **min** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="ea67e-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="ea67e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea67e-120">Requirements</span></span>



| <span data-ttu-id="ea67e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea67e-121">Requirement</span></span> | <span data-ttu-id="ea67e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea67e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea67e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea67e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea67e-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea67e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ea67e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea67e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea67e-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea67e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea67e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea67e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea67e-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea67e-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





