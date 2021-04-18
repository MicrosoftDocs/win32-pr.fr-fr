---
title: fonction glVertex3fv (GL. h)
description: Spécifie un sommet. | fonction glVertex3fv (GL. h)
ms.assetid: d8790ffe-73b1-49d8-a7f5-2117177573ac
keywords:
- glVertex3fv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3bcbe73d071bc18e3a1a58ef2f505fa9bd6a3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522916"
---
# <a name="glvertex3fv-function"></a><span data-ttu-id="5fdaa-105">glVertex3fv fonction)</span><span class="sxs-lookup"><span data-stu-id="5fdaa-105">glVertex3fv function</span></span>

<span data-ttu-id="5fdaa-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="5fdaa-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fdaa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fdaa-107">Syntax</span></span>


```C++
void WINAPI glVertex3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="5fdaa-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fdaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fdaa-109">*v*</span><span class="sxs-lookup"><span data-stu-id="5fdaa-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="5fdaa-110">Pointeur vers un tableau de trois éléments.</span><span class="sxs-lookup"><span data-stu-id="5fdaa-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="5fdaa-111">Les éléments sont les coordonnées x, y et z d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="5fdaa-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fdaa-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5fdaa-112">Return value</span></span>

<span data-ttu-id="5fdaa-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5fdaa-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fdaa-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fdaa-114">Requirements</span></span>



| <span data-ttu-id="5fdaa-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fdaa-115">Requirement</span></span> | <span data-ttu-id="5fdaa-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fdaa-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdaa-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fdaa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5fdaa-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fdaa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5fdaa-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fdaa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5fdaa-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fdaa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5fdaa-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5fdaa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fdaa-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fdaa-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5fdaa-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5fdaa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fdaa-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fdaa-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5fdaa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5fdaa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fdaa-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fdaa-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fdaa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fdaa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fdaa-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="5fdaa-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="5fdaa-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





