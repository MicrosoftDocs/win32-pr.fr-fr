---
title: gluNewTess, fonction (Glu. h)
description: La fonction gluNewTess crée un objet pavage.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- gluNewTess fonction OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106539009"
---
# <a name="glunewtess-function"></a><span data-ttu-id="e9c61-104">gluNewTess fonction)</span><span class="sxs-lookup"><span data-stu-id="e9c61-104">gluNewTess function</span></span>

<span data-ttu-id="e9c61-105">La fonction **gluNewTess** crée un objet pavage.</span><span class="sxs-lookup"><span data-stu-id="e9c61-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c61-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9c61-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="e9c61-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9c61-107">Parameters</span></span>

<span data-ttu-id="e9c61-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="e9c61-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9c61-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e9c61-109">Remarks</span></span>

<span data-ttu-id="e9c61-110">La fonction **gluNewTess** crée et retourne un pointeur vers un nouvel objet pavage.</span><span class="sxs-lookup"><span data-stu-id="e9c61-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="e9c61-111">Fait référence à cet objet lors de l’appel de fonctions de pavage.</span><span class="sxs-lookup"><span data-stu-id="e9c61-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="e9c61-112">Une valeur de retour de zéro signifie qu’il n’y a pas assez de mémoire à allouer à l’objet.</span><span class="sxs-lookup"><span data-stu-id="e9c61-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c61-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9c61-113">Requirements</span></span>



| <span data-ttu-id="e9c61-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9c61-114">Requirement</span></span> | <span data-ttu-id="e9c61-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9c61-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c61-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9c61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c61-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9c61-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e9c61-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9c61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c61-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9c61-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e9c61-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9c61-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c61-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c61-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e9c61-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9c61-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9c61-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9c61-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9c61-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e9c61-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9c61-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9c61-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c61-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9c61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c61-127">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="e9c61-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="e9c61-128">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="e9c61-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="e9c61-129">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="e9c61-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





