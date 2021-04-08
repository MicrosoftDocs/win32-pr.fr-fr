---
title: SNB (Objidl. h)
description: Un bloc de nom de chaîne (SNB) est un pointeur vers un tableau de pointeurs vers des chaînes, qui se termine par un pointeur NULL.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941900"
---
# <a name="snb"></a><span data-ttu-id="b7575-104">SNB</span><span class="sxs-lookup"><span data-stu-id="b7575-104">SNB</span></span>

<span data-ttu-id="b7575-105">Un bloc de nom de chaîne (**SNB**) est un pointeur vers un tableau de pointeurs vers des chaînes, qui se termine par un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="b7575-105">A string name block (**SNB**) is a pointer to an array of pointers to strings, that ends in a **NULL** pointer.</span></span> <span data-ttu-id="b7575-106">Les blocs de nom de chaîne sont utilisés par l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et par les appels de fonction qui ouvrent des objets de stockage.</span><span class="sxs-lookup"><span data-stu-id="b7575-106">String name blocks are used by the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and by function calls that open storage objects.</span></span> <span data-ttu-id="b7575-107">Les chaînes pointent vers les objets de stockage contenus ou les flux qui doivent être exclus dans les appels ouverts.</span><span class="sxs-lookup"><span data-stu-id="b7575-107">The strings point to contained storage objects or streams that are to be excluded in the open calls.</span></span>


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

<span data-ttu-id="b7575-108">**SNB**</span><span class="sxs-lookup"><span data-stu-id="b7575-108">**SNB**</span></span>
</dt> <dd>

<span data-ttu-id="b7575-109">\[\_marshaling de câble (wireSNB)\]</span><span class="sxs-lookup"><span data-stu-id="b7575-109">\[wire\_marshal(wireSNB)\]</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7575-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b7575-110">Remarks</span></span>

<span data-ttu-id="b7575-111">Le **SNB** doit être créé en allouant un bloc de mémoire contigu dans lequel les pointeurs vers les chaînes sont suivis d’un pointeur **null** , qui est ensuite suivi des chaînes réelles.</span><span class="sxs-lookup"><span data-stu-id="b7575-111">The **SNB** should be created by allocating a contiguous block of memory in which the pointers to strings are followed by a **NULL** pointer, which is then followed by the actual strings.</span></span>

<span data-ttu-id="b7575-112">Le marshaling d’un **SNB** est basé sur l’hypothèse que le **SNB** qui a été passé a été créé de cette façon.</span><span class="sxs-lookup"><span data-stu-id="b7575-112">The marshaling of an **SNB** is based on the assumption that the **SNB** that was passed in was created in this way.</span></span> <span data-ttu-id="b7575-113">Bien qu’il puisse être stocké d’une autre manière, les **SNB** créés de cette manière ont l’avantage d’exiger une seule opération d’allocation et de libérer de la mémoire pour toutes les chaînes.</span><span class="sxs-lookup"><span data-stu-id="b7575-113">Although it could be stored in other ways, the **SNB** created in this manner has the advantage of requiring only one allocation operation and one freeing of memory for all the strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7575-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7575-114">Requirements</span></span>



| <span data-ttu-id="b7575-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7575-115">Requirement</span></span> | <span data-ttu-id="b7575-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7575-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7575-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7575-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7575-118">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7575-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b7575-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7575-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7575-120">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7575-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b7575-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7575-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7575-122"><dt>Objidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7575-122"><dt>Objidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7575-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="b7575-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7575-124"><dt>Objidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7575-124"><dt>Objidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7575-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7575-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7575-126">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="b7575-126">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





