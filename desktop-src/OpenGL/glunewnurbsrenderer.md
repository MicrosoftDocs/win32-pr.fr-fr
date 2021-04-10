---
title: gluNewNurbsRenderer, fonction (Glu. h)
description: La fonction gluNewNurbsRenderer crée un objet NURBS B-spline (NURBS) non uniforme.
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- gluNewNurbsRenderer fonction OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942357"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="caef1-104">gluNewNurbsRenderer fonction)</span><span class="sxs-lookup"><span data-stu-id="caef1-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="caef1-105">La fonction **gluNewNurbsRenderer** crée un objet NURBS b-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="caef1-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="caef1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caef1-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="caef1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caef1-107">Parameters</span></span>

<span data-ttu-id="caef1-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="caef1-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="caef1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="caef1-109">Remarks</span></span>

<span data-ttu-id="caef1-110">La fonction **gluNewNurbsRenderer** crée et retourne un pointeur vers un nouvel objet NURBS.</span><span class="sxs-lookup"><span data-stu-id="caef1-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="caef1-111">Reportez-vous à cet objet lors de l’appel des fonctions de contrôle et de rendu NURBS.</span><span class="sxs-lookup"><span data-stu-id="caef1-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="caef1-112">Une valeur de retour de zéro signifie qu’il n’y a pas assez de mémoire à allouer à l’objet.</span><span class="sxs-lookup"><span data-stu-id="caef1-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="caef1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caef1-113">Requirements</span></span>



| <span data-ttu-id="caef1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caef1-114">Requirement</span></span> | <span data-ttu-id="caef1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="caef1-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="caef1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caef1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="caef1-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caef1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="caef1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caef1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="caef1-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caef1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="caef1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="caef1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="caef1-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="caef1-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="caef1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="caef1-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="caef1-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="caef1-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="caef1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="caef1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caef1-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caef1-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caef1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caef1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caef1-127">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="caef1-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="caef1-128">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="caef1-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="caef1-129">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="caef1-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="caef1-130">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="caef1-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="caef1-131">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="caef1-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="caef1-132">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="caef1-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





