---
title: macro Max (Minwindef. h)
description: La macro Max compare deux valeurs et retourne la plus grande. Le type de données peut être n’importe quel type de données numérique, signé ou non signé. Le type de données des arguments et la valeur de retour sont les mêmes.
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- Fenêtre multimédia Max Windows
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508478"
---
# <a name="max-macro"></a><span data-ttu-id="a1590-106">max (macro)</span><span class="sxs-lookup"><span data-stu-id="a1590-106">max macro</span></span>

<span data-ttu-id="a1590-107">La macro **Max** compare deux valeurs et retourne la plus grande.</span><span class="sxs-lookup"><span data-stu-id="a1590-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="a1590-108">Le type de données peut être n’importe quel type de données numérique, signé ou non signé.</span><span class="sxs-lookup"><span data-stu-id="a1590-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="a1590-109">Le type de données des arguments et la valeur de retour sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="a1590-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1590-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1590-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="a1590-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1590-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1590-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="a1590-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="a1590-113">Spécifie la première des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="a1590-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="a1590-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="a1590-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="a1590-115">Spécifie la deuxième des deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="a1590-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1590-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1590-116">Return value</span></span>

<span data-ttu-id="a1590-117">La valeur de retour est la plus grande des deux valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a1590-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1590-118">Notes</span><span class="sxs-lookup"><span data-stu-id="a1590-118">Remarks</span></span>

<span data-ttu-id="a1590-119">La macro **Max** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="a1590-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="a1590-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1590-120">Requirements</span></span>



| <span data-ttu-id="a1590-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1590-121">Requirement</span></span> | <span data-ttu-id="a1590-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1590-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1590-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1590-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a1590-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1590-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1590-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1590-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a1590-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1590-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a1590-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1590-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1590-128"><dt>Minwindef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1590-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





