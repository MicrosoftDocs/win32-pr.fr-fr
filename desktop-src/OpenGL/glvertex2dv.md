---
title: fonction glVertex2dv (GL. h)
description: Spécifie un sommet. | fonction glVertex2dv (GL. h)
ms.assetid: b685d0aa-2874-4ad9-a20c-86823e9ad00b
keywords:
- glVertex2dv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4839fa650302a67c98a0aef3d227dfafa8ddb688
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953607"
---
# <a name="glvertex2dv-function"></a><span data-ttu-id="3e59d-105">glVertex2dv fonction)</span><span class="sxs-lookup"><span data-stu-id="3e59d-105">glVertex2dv function</span></span>

<span data-ttu-id="3e59d-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="3e59d-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e59d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e59d-107">Syntax</span></span>


```C++
void WINAPI glVertex2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="3e59d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e59d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e59d-109">*v*</span><span class="sxs-lookup"><span data-stu-id="3e59d-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="3e59d-110">Pointeur vers un tableau de deux éléments.</span><span class="sxs-lookup"><span data-stu-id="3e59d-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="3e59d-111">Les éléments sont les coordonnées x et y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="3e59d-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e59d-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3e59d-112">Return value</span></span>

<span data-ttu-id="3e59d-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3e59d-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e59d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e59d-114">Requirements</span></span>



| <span data-ttu-id="3e59d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e59d-115">Requirement</span></span> | <span data-ttu-id="3e59d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e59d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e59d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e59d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e59d-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e59d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3e59d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e59d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e59d-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e59d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e59d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e59d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e59d-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e59d-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3e59d-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e59d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e59d-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e59d-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3e59d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e59d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e59d-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e59d-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e59d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e59d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e59d-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3e59d-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3e59d-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3e59d-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3e59d-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3e59d-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="3e59d-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3e59d-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3e59d-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="3e59d-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3e59d-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="3e59d-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3e59d-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="3e59d-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3e59d-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3e59d-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





