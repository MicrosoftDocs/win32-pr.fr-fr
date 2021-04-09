---
title: fonction glVertex2iv (GL. h)
description: Spécifie un sommet. | fonction glVertex2iv (GL. h)
ms.assetid: 3b88bf7d-5743-4ac0-a79f-5f450b488bd2
keywords:
- glVertex2iv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex2iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594c50ff1e30184d5a7292c5b639f16a48f0820b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043058"
---
# <a name="glvertex2iv-function"></a><span data-ttu-id="c6c38-105">glVertex2iv fonction)</span><span class="sxs-lookup"><span data-stu-id="c6c38-105">glVertex2iv function</span></span>

<span data-ttu-id="c6c38-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="c6c38-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c38-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6c38-107">Syntax</span></span>


```C++
void WINAPI glVertex2iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="c6c38-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6c38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c38-109">*v*</span><span class="sxs-lookup"><span data-stu-id="c6c38-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c38-110">Pointeur vers un tableau de deux éléments.</span><span class="sxs-lookup"><span data-stu-id="c6c38-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="c6c38-111">Les éléments sont les coordonnées x et y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="c6c38-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c38-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c6c38-112">Return value</span></span>

<span data-ttu-id="c6c38-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c6c38-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c38-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6c38-114">Requirements</span></span>



| <span data-ttu-id="c6c38-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6c38-115">Requirement</span></span> | <span data-ttu-id="c6c38-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6c38-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c38-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6c38-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c38-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6c38-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6c38-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6c38-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c38-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6c38-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6c38-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6c38-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c38-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c38-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c6c38-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6c38-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6c38-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6c38-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6c38-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c6c38-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6c38-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6c38-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c38-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6c38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c38-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c6c38-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c6c38-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="c6c38-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c6c38-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c6c38-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="c6c38-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c6c38-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c6c38-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="c6c38-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c6c38-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c6c38-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="c6c38-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="c6c38-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="c6c38-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c6c38-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





