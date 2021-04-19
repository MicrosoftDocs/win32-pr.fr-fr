---
title: gluPwlCurve, fonction (Glu. h)
description: La fonction gluPwlCurve décrit une courbe de découpage NURBS B-spline (NURBS) par morceaux linéaire non uniforme.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510990"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="b6baa-104">gluPwlCurve fonction)</span><span class="sxs-lookup"><span data-stu-id="b6baa-104">gluPwlCurve function</span></span>

<span data-ttu-id="b6baa-105">La fonction **gluPwlCurve** décrit une courbe de découpage NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) par morceaux linéaire non uniforme.</span><span class="sxs-lookup"><span data-stu-id="b6baa-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6baa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6baa-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="b6baa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6baa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6baa-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="b6baa-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="b6baa-109">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="b6baa-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b6baa-110">*count*</span><span class="sxs-lookup"><span data-stu-id="b6baa-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="b6baa-111">Nombre de points sur la courbe.</span><span class="sxs-lookup"><span data-stu-id="b6baa-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="b6baa-112">*array*</span><span class="sxs-lookup"><span data-stu-id="b6baa-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="b6baa-113">Tableau contenant les points de courbe.</span><span class="sxs-lookup"><span data-stu-id="b6baa-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="b6baa-114">*progrès*</span><span class="sxs-lookup"><span data-stu-id="b6baa-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="b6baa-115">Décalage (nombre de valeurs à virgule flottante simple précision) entre des points sur la courbe.</span><span class="sxs-lookup"><span data-stu-id="b6baa-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="b6baa-116">*type*</span><span class="sxs-lookup"><span data-stu-id="b6baa-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b6baa-117">Type de courbe.</span><span class="sxs-lookup"><span data-stu-id="b6baa-117">The type of curve.</span></span> <span data-ttu-id="b6baa-118">Il doit s’agir \_ de Glu Map1 \_ Trim \_ 2 ou de Glu \_ Map1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="b6baa-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6baa-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6baa-119">Return value</span></span>

<span data-ttu-id="b6baa-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b6baa-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6baa-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b6baa-121">Remarks</span></span>

<span data-ttu-id="b6baa-122">La fonction **gluPwlCurve** décrit une courbe de rognage linéaire par morceaux pour une surface NURBS.</span><span class="sxs-lookup"><span data-stu-id="b6baa-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="b6baa-123">Une courbe linéaire par morceaux se compose d’une liste de coordonnées de points dans l’espace de paramètres pour la surface NURBS à tronquer.</span><span class="sxs-lookup"><span data-stu-id="b6baa-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="b6baa-124">Ces points sont reliés par des segments de ligne pour former une courbe.</span><span class="sxs-lookup"><span data-stu-id="b6baa-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="b6baa-125">Si la courbe est une approximation d’une courbe réelle, les points doivent être suffisamment proches pour que le tracé résultant apparaisse courbé au niveau de la résolution utilisée dans l’application.</span><span class="sxs-lookup"><span data-stu-id="b6baa-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="b6baa-126">Si le *type* est Glu \_ Map1 \_ Trim \_ 2, il décrit une courbe dans l’espace de paramètres à deux dimensions (*u* et *v*).</span><span class="sxs-lookup"><span data-stu-id="b6baa-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="b6baa-127">S’il s’agit \_ de Glu Map1 \_ Trim \_ 3, il décrit une courbe dans un espace de paramètre homogène à deux dimensions (*u*, *v* et *w*).</span><span class="sxs-lookup"><span data-stu-id="b6baa-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="b6baa-128">Pour plus d’informations sur les courbes de suppression, consultez [**gluBeginTrim**](glubegintrim.md).</span><span class="sxs-lookup"><span data-stu-id="b6baa-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6baa-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6baa-129">Requirements</span></span>



| <span data-ttu-id="b6baa-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6baa-130">Requirement</span></span> | <span data-ttu-id="b6baa-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6baa-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6baa-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6baa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b6baa-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6baa-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b6baa-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6baa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b6baa-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6baa-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6baa-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6baa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6baa-137"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6baa-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b6baa-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b6baa-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6baa-139"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6baa-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b6baa-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b6baa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6baa-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6baa-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6baa-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6baa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6baa-143">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="b6baa-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="b6baa-144">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="b6baa-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="b6baa-145">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="b6baa-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="b6baa-146">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="b6baa-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





