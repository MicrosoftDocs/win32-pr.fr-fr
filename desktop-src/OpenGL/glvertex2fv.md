---
title: fonction glVertex2fv (GL. h)
description: Spécifie un sommet. | fonction glVertex2fv (GL. h)
ms.assetid: bae32d27-2a19-40d5-a3f7-0e7a41918034
keywords:
- glVertex2fv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd7a57aff2166f3605d7007cd194f5cff04784
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523135"
---
# <a name="glvertex2fv-function"></a><span data-ttu-id="e2541-105">glVertex2fv fonction)</span><span class="sxs-lookup"><span data-stu-id="e2541-105">glVertex2fv function</span></span>

<span data-ttu-id="e2541-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="e2541-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2541-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2541-107">Syntax</span></span>


```C++
void WINAPI glVertex2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="e2541-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2541-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2541-109">*v*</span><span class="sxs-lookup"><span data-stu-id="e2541-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="e2541-110">Pointeur vers un tableau de deux éléments.</span><span class="sxs-lookup"><span data-stu-id="e2541-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="e2541-111">Les éléments sont les coordonnées x et y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="e2541-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2541-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2541-112">Return value</span></span>

<span data-ttu-id="e2541-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e2541-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2541-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2541-114">Requirements</span></span>



| <span data-ttu-id="e2541-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2541-115">Requirement</span></span> | <span data-ttu-id="e2541-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2541-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2541-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2541-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e2541-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2541-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e2541-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2541-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e2541-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2541-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2541-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2541-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2541-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2541-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e2541-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2541-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2541-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2541-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e2541-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e2541-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2541-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2541-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2541-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2541-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2541-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e2541-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e2541-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="e2541-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="e2541-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="e2541-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="e2541-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e2541-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e2541-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="e2541-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e2541-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="e2541-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="e2541-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="e2541-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="e2541-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="e2541-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





