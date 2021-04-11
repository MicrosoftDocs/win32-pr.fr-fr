---
title: gluNewQuadric, fonction (Glu. h)
description: La fonction gluNewQuadric crée un objet quadric.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- gluNewQuadric fonction OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942356"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="dab8e-104">gluNewQuadric fonction)</span><span class="sxs-lookup"><span data-stu-id="dab8e-104">gluNewQuadric function</span></span>

<span data-ttu-id="dab8e-105">La fonction **gluNewQuadric** crée un objet quadric.</span><span class="sxs-lookup"><span data-stu-id="dab8e-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab8e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dab8e-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="dab8e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dab8e-107">Parameters</span></span>

<span data-ttu-id="dab8e-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="dab8e-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab8e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dab8e-109">Remarks</span></span>

<span data-ttu-id="dab8e-110">La fonction **gluNewQuadric** crée et retourne un pointeur vers un nouvel objet quadric.</span><span class="sxs-lookup"><span data-stu-id="dab8e-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="dab8e-111">Reportez-vous à cet objet lors de l’appel de fonctions de contrôle et de rendu quadric.</span><span class="sxs-lookup"><span data-stu-id="dab8e-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="dab8e-112">Une valeur de retour de zéro signifie qu’il n’y a pas assez de mémoire à allouer à l’objet.</span><span class="sxs-lookup"><span data-stu-id="dab8e-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab8e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dab8e-113">Requirements</span></span>



| <span data-ttu-id="dab8e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dab8e-114">Requirement</span></span> | <span data-ttu-id="dab8e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dab8e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dab8e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dab8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dab8e-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dab8e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dab8e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dab8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dab8e-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dab8e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dab8e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="dab8e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dab8e-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab8e-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dab8e-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dab8e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="dab8e-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dab8e-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dab8e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dab8e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dab8e-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dab8e-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab8e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dab8e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab8e-127">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="dab8e-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="dab8e-128">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="dab8e-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="dab8e-129">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="dab8e-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="dab8e-130">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="dab8e-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="dab8e-131">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="dab8e-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="dab8e-132">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="dab8e-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="dab8e-133">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="dab8e-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="dab8e-134">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="dab8e-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="dab8e-135">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="dab8e-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="dab8e-136">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="dab8e-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





