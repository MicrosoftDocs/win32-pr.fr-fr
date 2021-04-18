---
title: fonction glVertex4fv (GL. h)
description: Spécifie un sommet. | fonction glVertex4fv (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- glVertex4fv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106520274"
---
# <a name="glvertex4fv-function"></a><span data-ttu-id="a8a30-105">glVertex4fv fonction)</span><span class="sxs-lookup"><span data-stu-id="a8a30-105">glVertex4fv function</span></span>

<span data-ttu-id="a8a30-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="a8a30-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a30-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8a30-107">Syntax</span></span>


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="a8a30-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8a30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a30-109">*v*</span><span class="sxs-lookup"><span data-stu-id="a8a30-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="a8a30-110">Pointeur vers un tableau de quatre éléments.</span><span class="sxs-lookup"><span data-stu-id="a8a30-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="a8a30-111">Les éléments sont les coordonnées x, y, z et w d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="a8a30-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a30-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8a30-112">Return value</span></span>

<span data-ttu-id="a8a30-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a8a30-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a30-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8a30-114">Requirements</span></span>



| <span data-ttu-id="a8a30-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8a30-115">Requirement</span></span> | <span data-ttu-id="a8a30-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8a30-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a30-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a30-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a30-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8a30-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a8a30-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8a30-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a30-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8a30-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8a30-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8a30-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8a30-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a30-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a8a30-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8a30-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8a30-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8a30-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8a30-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8a30-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8a30-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8a30-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8a30-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8a30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a30-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a8a30-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a8a30-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="a8a30-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="a8a30-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a8a30-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a8a30-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a8a30-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a8a30-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a8a30-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a8a30-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a8a30-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a8a30-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="a8a30-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="a8a30-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a8a30-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





