---
title: fonction glVertex2sv (GL. h)
description: Spécifie un sommet. | fonction glVertex2sv (GL. h)
ms.assetid: 4e13356a-a74b-4fb6-a001-1fffc28dd7a1
keywords:
- glVertex2sv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex2sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e865ab8999e08f9c13ad46443ba039be1cda9e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529568"
---
# <a name="glvertex2sv-function"></a><span data-ttu-id="1b36f-105">glVertex2sv fonction)</span><span class="sxs-lookup"><span data-stu-id="1b36f-105">glVertex2sv function</span></span>

<span data-ttu-id="1b36f-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="1b36f-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b36f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b36f-107">Syntax</span></span>


```C++
void WINAPI glVertex2sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="1b36f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b36f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b36f-109">*v*</span><span class="sxs-lookup"><span data-stu-id="1b36f-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="1b36f-110">Pointeur vers un tableau de deux éléments.</span><span class="sxs-lookup"><span data-stu-id="1b36f-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="1b36f-111">Les éléments sont les coordonnées x et y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="1b36f-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b36f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b36f-112">Return value</span></span>

<span data-ttu-id="1b36f-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b36f-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b36f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b36f-114">Requirements</span></span>



| <span data-ttu-id="1b36f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b36f-115">Requirement</span></span> | <span data-ttu-id="1b36f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b36f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b36f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b36f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1b36f-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b36f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1b36f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b36f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1b36f-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b36f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1b36f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b36f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b36f-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b36f-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1b36f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b36f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b36f-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b36f-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b36f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1b36f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b36f-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b36f-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b36f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b36f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b36f-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1b36f-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1b36f-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="1b36f-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="1b36f-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="1b36f-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="1b36f-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1b36f-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1b36f-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="1b36f-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="1b36f-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="1b36f-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="1b36f-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="1b36f-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="1b36f-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="1b36f-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





