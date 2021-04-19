---
title: gluNurbsCurve, fonction (Glu. h)
description: La fonction gluNurbsCurve définit la forme d’une courbe B-spline rationnelle non uniforme (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509517"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="abc82-104">gluNurbsCurve fonction)</span><span class="sxs-lookup"><span data-stu-id="abc82-104">gluNurbsCurve function</span></span>

<span data-ttu-id="abc82-105">La fonction **gluNurbsCurve** définit la forme d’une courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="abc82-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc82-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abc82-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="abc82-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abc82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc82-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="abc82-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-109">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="abc82-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="abc82-110">*nknots*</span><span class="sxs-lookup"><span data-stu-id="abc82-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-111">Nombre de nœuds dans le *nœud*.</span><span class="sxs-lookup"><span data-stu-id="abc82-111">The number of knots in *knot*.</span></span> <span data-ttu-id="abc82-112">Le paramètre *nknots* est égal au nombre de points de contrôle plus l’ordre.</span><span class="sxs-lookup"><span data-stu-id="abc82-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="abc82-113">*noeud*</span><span class="sxs-lookup"><span data-stu-id="abc82-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-114">Tableau de valeurs de nœud nondecreasing *nknots* .</span><span class="sxs-lookup"><span data-stu-id="abc82-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="abc82-115">*progrès*</span><span class="sxs-lookup"><span data-stu-id="abc82-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-116">Offset (sous la forme d’un nombre de valeurs à virgule flottante simple précision) entre des points de contrôle de courbe successifs.</span><span class="sxs-lookup"><span data-stu-id="abc82-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="abc82-117">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="abc82-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-118">Pointeur vers un tableau de points de contrôle.</span><span class="sxs-lookup"><span data-stu-id="abc82-118">A pointer to an array of control points.</span></span> <span data-ttu-id="abc82-119">Les coordonnées doivent être conformes au *type*.</span><span class="sxs-lookup"><span data-stu-id="abc82-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="abc82-120">*order*</span><span class="sxs-lookup"><span data-stu-id="abc82-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-121">Ordre de la courbe NURBS.</span><span class="sxs-lookup"><span data-stu-id="abc82-121">The order of the NURBS curve.</span></span> <span data-ttu-id="abc82-122">Le paramètre *Order* est égal à degree + 1 ; par conséquent, une courbe cubique a un ordre de 4.</span><span class="sxs-lookup"><span data-stu-id="abc82-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="abc82-123">*type*</span><span class="sxs-lookup"><span data-stu-id="abc82-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="abc82-124">Type de la courbe.</span><span class="sxs-lookup"><span data-stu-id="abc82-124">The type of the curve.</span></span> <span data-ttu-id="abc82-125">Si cette courbe est définie au sein d’une paire [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , le type peut être n’importe lequel des types d’évaluateurs unidimensionnels valides (tels que GL \_ Map1 \_ vertex \_ 3 ou GL \_ Map1 \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="abc82-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="abc82-126">Entre une paire [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , les seuls types valides sont Glu \_ Map1 \_ Trim \_ 2 et Glu \_ Map1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="abc82-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc82-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="abc82-127">Return value</span></span>

<span data-ttu-id="abc82-128">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="abc82-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abc82-129">Notes</span><span class="sxs-lookup"><span data-stu-id="abc82-129">Remarks</span></span>

<span data-ttu-id="abc82-130">Quand **gluNurbsCurve** apparaît entre une  / paire de **gluEndCurve** gluBeginCurve, il décrit une courbe à restituer.</span><span class="sxs-lookup"><span data-stu-id="abc82-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="abc82-131">Vous associez les coordonnées de position, de texture et de couleur en les présentant comme un **gluNurbsCurve** distinct entre une paire **gluBeginCurve** / **gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="abc82-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="abc82-132">N’effectuez pas plus d’un appel à **gluNurbsCurve** pour les données de couleur, de position et de texture dans une paire de / **gluEndCurve** gluBeginCurve unique.</span><span class="sxs-lookup"><span data-stu-id="abc82-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="abc82-133">Effectuez un seul appel pour décrire la position de la courbe (un *type* de Map1 de comptabilité GL de \_ \_ vertex \_ 3 ou de Map1 de type GL \_ \_ \_ 4).</span><span class="sxs-lookup"><span data-stu-id="abc82-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="abc82-134">Quand **gluNurbsCurve** apparaît entre une [](glubegintrim.md) / paire de [**gluEndTrim**](gluendtrim.md) gluBeginTrim, il décrit une courbe de rognage sur une surface NURBS.</span><span class="sxs-lookup"><span data-stu-id="abc82-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="abc82-135">Si le *type* est Glu \_ Map1 \_ Trim \_ 2, il décrit une courbe dans l’espace de paramètres à deux dimensions (*u* et *v*).</span><span class="sxs-lookup"><span data-stu-id="abc82-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="abc82-136">S’il s’agit \_ de Glu Map1 \_ Trim \_ 3, il décrit une courbe dans un espace de paramètre homogène à deux dimensions (*u*, *v* et *w*).</span><span class="sxs-lookup"><span data-stu-id="abc82-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="abc82-137">Pour plus d’informations sur les courbes de suppression, consultez **gluBeginTrim**.</span><span class="sxs-lookup"><span data-stu-id="abc82-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="abc82-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="abc82-138">Examples</span></span>

<span data-ttu-id="abc82-139">Les fonctions suivantes affichent une courbe NURBS texturée avec des normales :</span><span class="sxs-lookup"><span data-stu-id="abc82-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="abc82-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abc82-140">Requirements</span></span>



| <span data-ttu-id="abc82-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abc82-141">Requirement</span></span> | <span data-ttu-id="abc82-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="abc82-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="abc82-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abc82-143">Minimum supported client</span></span><br/> | <span data-ttu-id="abc82-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abc82-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="abc82-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abc82-145">Minimum supported server</span></span><br/> | <span data-ttu-id="abc82-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abc82-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="abc82-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="abc82-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc82-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc82-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="abc82-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abc82-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="abc82-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abc82-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="abc82-151">DLL</span><span class="sxs-lookup"><span data-stu-id="abc82-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abc82-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc82-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abc82-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abc82-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc82-154">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="abc82-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="abc82-155">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="abc82-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="abc82-156">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="abc82-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="abc82-157">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="abc82-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="abc82-158">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="abc82-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="abc82-159">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="abc82-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





