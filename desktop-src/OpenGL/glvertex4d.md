---
title: fonction glVertex4d (GL. h)
description: Spécifie un sommet. | fonction glVertex4d (GL. h)
ms.assetid: d9203e4f-5ed2-41e7-b619-65cee3132ed9
keywords:
- glVertex4d fonction OpenGL
topic_type:
- apiref
api_name:
- glVertex4d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a28a64c35ff30cc668839899dca4f3dc2958ff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523162"
---
# <a name="glvertex4d-function"></a><span data-ttu-id="b4507-105">glVertex4d fonction)</span><span class="sxs-lookup"><span data-stu-id="b4507-105">glVertex4d function</span></span>

<span data-ttu-id="b4507-106">Spécifie un sommet.</span><span class="sxs-lookup"><span data-stu-id="b4507-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4507-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4507-107">Syntax</span></span>


```C++
void WINAPI glVertex4d(
   GLdouble x,
   GLdouble y,
   GLdouble z,
   GLdouble w
);
```



## <a name="parameters"></a><span data-ttu-id="b4507-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4507-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4507-109">*x*</span><span class="sxs-lookup"><span data-stu-id="b4507-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="b4507-110">Spécifie la coordonnée x d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="b4507-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b4507-111">*y*</span><span class="sxs-lookup"><span data-stu-id="b4507-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="b4507-112">Spécifie la coordonnée y d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="b4507-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b4507-113">*z*</span><span class="sxs-lookup"><span data-stu-id="b4507-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="b4507-114">Spécifie la coordonnée z d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="b4507-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b4507-115">*w*</span><span class="sxs-lookup"><span data-stu-id="b4507-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="b4507-116">Spécifie la coordonnée w d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="b4507-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4507-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4507-117">Return value</span></span>

<span data-ttu-id="b4507-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b4507-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4507-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b4507-119">Remarks</span></span>

<span data-ttu-id="b4507-120">Les commandes de fonction glVertex sont utilisées dans les paires [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pour spécifier les sommets de points, de lignes et de polygones.</span><span class="sxs-lookup"><span data-stu-id="b4507-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="b4507-121">Les coordonnées de couleur actuelle, normale et de texture sont associées au vertex lorsque glVertex est appelé.</span><span class="sxs-lookup"><span data-stu-id="b4507-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="b4507-122">Si seuls *x* et *y* sont spécifiés, *z* a pour valeur par défaut 0,0 et *w* a la valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="b4507-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="b4507-123">Lorsque *x*, *y* et *z* sont spécifiés, *w* a pour valeur par défaut 1,0.</span><span class="sxs-lookup"><span data-stu-id="b4507-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="b4507-124">L’appel de glVertex en dehors d’une paire de / **glEnd** glBegin entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="b4507-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4507-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4507-125">Requirements</span></span>



| <span data-ttu-id="b4507-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4507-126">Requirement</span></span> | <span data-ttu-id="b4507-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4507-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4507-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4507-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4507-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4507-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b4507-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4507-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4507-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4507-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4507-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4507-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4507-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4507-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b4507-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4507-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4507-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4507-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b4507-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b4507-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4507-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4507-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4507-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4507-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4507-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b4507-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b4507-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b4507-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b4507-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b4507-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="b4507-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b4507-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b4507-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b4507-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b4507-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="b4507-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="b4507-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="b4507-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="b4507-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b4507-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





