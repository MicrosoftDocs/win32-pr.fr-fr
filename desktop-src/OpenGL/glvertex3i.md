---
title: fonction glVertex3i (GL. h)
description: Spécifie un sommet. | fonction glVertex3i (GL. h)
ms.assetid: 5f757065-cbe9-401a-855b-f0a9308ae204
keywords:
- glVertex3i fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e216c35a354daead228d6043d2129f6d30d400
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953592"
---
# <a name="glvertex3i-function"></a><span data-ttu-id="d9f03-105">glVertex3i fonction)</span><span class="sxs-lookup"><span data-stu-id="d9f03-105">glVertex3i function</span></span>

<span data-ttu-id="d9f03-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="d9f03-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f03-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9f03-107">Syntax</span></span>


```C++
void WINAPI glVertex3i(
   GLint x,
   GLint y,
   GLint z
);
```



## <a name="parameters"></a><span data-ttu-id="d9f03-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9f03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9f03-109">*x*</span><span class="sxs-lookup"><span data-stu-id="d9f03-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f03-110">Spécifie la coordonnée x d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="d9f03-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d9f03-111">*y*</span><span class="sxs-lookup"><span data-stu-id="d9f03-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f03-112">Spécifie la coordonnée y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="d9f03-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="d9f03-113">*z*</span><span class="sxs-lookup"><span data-stu-id="d9f03-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="d9f03-114">Spécifie la coordonnée z d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="d9f03-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9f03-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d9f03-115">Return value</span></span>

<span data-ttu-id="d9f03-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d9f03-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f03-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d9f03-117">Remarks</span></span>

<span data-ttu-id="d9f03-118">Les commandes de fonction glVertex sont utilisées dans les paires [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pour spécifier les sommets de points, de lignes et de polygones.</span><span class="sxs-lookup"><span data-stu-id="d9f03-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="d9f03-119">Les coordonnées de couleur actuelle, normale et de texture sont associées au vertex lorsque glVertex est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9f03-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="d9f03-120">Si seuls *x* et *y* sont spécifiés, *z* a pour valeur par défaut 0,0 et *w* a la valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="d9f03-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="d9f03-121">Lorsque *x*, *y* et *z* sont spécifiés, *w* a pour valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="d9f03-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="d9f03-122">L’appel de glVertex en dehors d’une paire de / **glEnd** glBegin entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="d9f03-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f03-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9f03-123">Requirements</span></span>



| <span data-ttu-id="d9f03-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9f03-124">Requirement</span></span> | <span data-ttu-id="d9f03-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9f03-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f03-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9f03-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f03-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9f03-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d9f03-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9f03-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f03-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9f03-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9f03-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9f03-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9f03-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9f03-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d9f03-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d9f03-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9f03-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9f03-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9f03-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d9f03-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9f03-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9f03-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f03-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9f03-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f03-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d9f03-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d9f03-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="d9f03-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="d9f03-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="d9f03-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="d9f03-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d9f03-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d9f03-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="d9f03-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="d9f03-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="d9f03-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="d9f03-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="d9f03-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="d9f03-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="d9f03-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





