---
title: gluDeleteNurbsRenderer, fonction (Glu. h)
description: La fonction gluDeleteNurbsRenderer détruit un objet NURBS B-spline (NURBS) non uniforme.
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gluDeleteNurbsRenderer fonction OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741420"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="e41d3-104">gluDeleteNurbsRenderer fonction)</span><span class="sxs-lookup"><span data-stu-id="e41d3-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="e41d3-105">La fonction **gluDeleteNurbsRenderer** détruit un objet NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="e41d3-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e41d3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e41d3-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="e41d3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e41d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41d3-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="e41d3-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="e41d3-109">Objet NURBS à détruire (créé avec **gluNewNurbsRenderer**).</span><span class="sxs-lookup"><span data-stu-id="e41d3-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41d3-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e41d3-110">Return value</span></span>

<span data-ttu-id="e41d3-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e41d3-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e41d3-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e41d3-112">Remarks</span></span>

<span data-ttu-id="e41d3-113">La fonction **gluDeleteNurbsRenderer** détruit l’objet NURBS et libère toute mémoire qu’il utilisait.</span><span class="sxs-lookup"><span data-stu-id="e41d3-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="e41d3-114">Une fois que vous avez appelé **gluDeleteNurbsRenderer**, vous ne pouvez plus utiliser *nobj* .</span><span class="sxs-lookup"><span data-stu-id="e41d3-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41d3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e41d3-115">Requirements</span></span>



| <span data-ttu-id="e41d3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e41d3-116">Requirement</span></span> | <span data-ttu-id="e41d3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e41d3-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e41d3-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e41d3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e41d3-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e41d3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e41d3-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e41d3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e41d3-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e41d3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e41d3-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e41d3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e41d3-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="e41d3-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e41d3-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e41d3-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="e41d3-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e41d3-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e41d3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e41d3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e41d3-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e41d3-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41d3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e41d3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41d3-129">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="e41d3-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





