---
title: fonction glVertex3iv (GL. h)
description: Spécifie un sommet. | fonction glVertex3iv (GL. h)
ms.assetid: db7e6a93-aaa2-402b-acd5-971c17451314
keywords:
- glVertex3iv fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb0a5db3ebf30722573c9f7d0143b92046c8cb6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535136"
---
# <a name="glvertex3iv-function"></a><span data-ttu-id="20b35-105">glVertex3iv fonction)</span><span class="sxs-lookup"><span data-stu-id="20b35-105">glVertex3iv function</span></span>

<span data-ttu-id="20b35-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="20b35-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="20b35-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20b35-107">Syntax</span></span>


```C++
void WINAPI glVertex3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="20b35-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20b35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20b35-109">*v*</span><span class="sxs-lookup"><span data-stu-id="20b35-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="20b35-110">Pointeur vers un tableau de trois éléments.</span><span class="sxs-lookup"><span data-stu-id="20b35-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="20b35-111">Les éléments sont les coordonnées x, y et z d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="20b35-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20b35-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="20b35-112">Return value</span></span>

<span data-ttu-id="20b35-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="20b35-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="20b35-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20b35-114">Requirements</span></span>



| <span data-ttu-id="20b35-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20b35-115">Requirement</span></span> | <span data-ttu-id="20b35-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="20b35-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20b35-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20b35-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20b35-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20b35-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="20b35-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20b35-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20b35-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20b35-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="20b35-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="20b35-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="20b35-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="20b35-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="20b35-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="20b35-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="20b35-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20b35-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="20b35-125">DLL</span><span class="sxs-lookup"><span data-stu-id="20b35-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20b35-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20b35-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20b35-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20b35-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20b35-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="20b35-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="20b35-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="20b35-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="20b35-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="20b35-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="20b35-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="20b35-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="20b35-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="20b35-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="20b35-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="20b35-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="20b35-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="20b35-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="20b35-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="20b35-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





