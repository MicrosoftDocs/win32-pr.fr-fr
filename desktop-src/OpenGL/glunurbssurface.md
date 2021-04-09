---
title: gluNurbsSurface, fonction (Glu. h)
description: La fonction gluNurbsSurface définit la forme d’une surface de courbe B-spline rationnelle non uniforme (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941642"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="edc52-104">gluNurbsSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="edc52-104">gluNurbsSurface function</span></span>

<span data-ttu-id="edc52-105">La fonction **gluNurbsSurface** définit la forme d’une surface de courbe B-spline rationnelle non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="edc52-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc52-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edc52-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="edc52-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edc52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc52-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="edc52-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-109">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="edc52-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="edc52-110">*nombre de sknot \_*</span><span class="sxs-lookup"><span data-stu-id="edc52-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-111">Nombre de nœuds dans la direction du paramétrique *u* .</span><span class="sxs-lookup"><span data-stu-id="edc52-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-112">*sknot*</span><span class="sxs-lookup"><span data-stu-id="edc52-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-113">Tableau de valeurs de nœud nondecreasing *sknot \_ Count* dans la direction paramétrique *u* .</span><span class="sxs-lookup"><span data-stu-id="edc52-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-114">*nombre de tknot \_*</span><span class="sxs-lookup"><span data-stu-id="edc52-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-115">Nombre de nœuds dans la direction paramétrique *v* .</span><span class="sxs-lookup"><span data-stu-id="edc52-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-116">*tknot*</span><span class="sxs-lookup"><span data-stu-id="edc52-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-117">Tableau de valeurs de nœud nondecreasing *tknot \_ Count* dans la direction paramétrique *v* .</span><span class="sxs-lookup"><span data-stu-id="edc52-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-118">*s \_ Stride*</span><span class="sxs-lookup"><span data-stu-id="edc52-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-119">Décalage (sous la forme d’un nombre de valeurs de point precisionfloating unique) entre des points de contrôle successifs dans la direction du paramétrique *u* dans *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="edc52-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-120">*t \_ Stride*</span><span class="sxs-lookup"><span data-stu-id="edc52-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-121">Décalage (en valeurs uniques de point precisionfloating) entre des points de contrôle successifs dans la direction paramétrique *v* dans *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="edc52-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-122">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="edc52-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-123">Tableau contenant des points de contrôle pour la surface NURBS.</span><span class="sxs-lookup"><span data-stu-id="edc52-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="edc52-124">Les décalages entre les points de contrôle successifs dans les directions paramétriques *u* et *v* sont fournis par *s \_ Stride* et *t \_ Stride*.</span><span class="sxs-lookup"><span data-stu-id="edc52-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-125">*sorder*</span><span class="sxs-lookup"><span data-stu-id="edc52-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-126">Ordre de la surface de la courbe NURBS dans la direction paramétrique *u* .</span><span class="sxs-lookup"><span data-stu-id="edc52-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="edc52-127">L’ordre est supérieur à un degré. par conséquent, une surface qui est cubique en *u* a un ordre *u* de 4.</span><span class="sxs-lookup"><span data-stu-id="edc52-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-128">*torder*</span><span class="sxs-lookup"><span data-stu-id="edc52-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-129">Ordre de la surface de la courbe NURBS dans la direction paramétrique *v* .</span><span class="sxs-lookup"><span data-stu-id="edc52-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="edc52-130">L’ordre est supérieur à un degré. par conséquent, une surface cubique en *v* a un ordre *v* de 4.</span><span class="sxs-lookup"><span data-stu-id="edc52-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="edc52-131">*type*</span><span class="sxs-lookup"><span data-stu-id="edc52-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="edc52-132">Type de l’aire.</span><span class="sxs-lookup"><span data-stu-id="edc52-132">The type of the surface.</span></span> <span data-ttu-id="edc52-133">Le paramètre de *type* peut être n’importe lequel des types d’évaluateurs à deux dimensions valides (tels que GL \_ map2 \_ vertex \_ 3 ou GL \_ map2 \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="edc52-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc52-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="edc52-134">Return value</span></span>

<span data-ttu-id="edc52-135">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="edc52-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="edc52-136">Notes</span><span class="sxs-lookup"><span data-stu-id="edc52-136">Remarks</span></span>

<span data-ttu-id="edc52-137">Utilisez **gluNurbsSurface** dans une définition de surface NURBS pour décrire la forme d’une surface NURBS (avant tout rognage).</span><span class="sxs-lookup"><span data-stu-id="edc52-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="edc52-138">Pour marquer le début d’une définition de surface NURBS, utilisez la fonction [**gluBeginSurface**](glubeginsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="edc52-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="edc52-139">Pour marquer la fin d’une définition de surface NURBS, utilisez la fonction [**gluEndSurface**](gluendsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="edc52-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="edc52-140">Appelez **gluNurbsSurface** dans une définition de surface NURBS uniquement.</span><span class="sxs-lookup"><span data-stu-id="edc52-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="edc52-141">Vous associez les coordonnées de position, de texture et de couleur à une surface en les présentant comme un **gluNurbsSurface** distinct entre une paire de  / **gluEndSurface** gluBeginSurface.</span><span class="sxs-lookup"><span data-stu-id="edc52-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="edc52-142">Au sein d’une paire **gluBeginSurface** / **gluEndSurface** unique, vous ne pouvez effectuer qu’un seul appel à **gluNurbsSurface** pour les données de couleur, de position et de texture.</span><span class="sxs-lookup"><span data-stu-id="edc52-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="edc52-143">Effectuez un seul appel pour décrire la position de l’aire (un *type* de map2 de comptabilité GL \_ \_ \_ , vertex 3 ou map2 du GL de \_ \_ vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="edc52-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="edc52-144">Vous pouvez supprimer une surface NURBS en utilisant les fonctions [**gluNurbsCurve**](glunurbscurve.md) et [**gluPwlCurve**](glupwlcurve.md) entre les appels à [**gluBeginTrim**](glubegintrim.md) et [**gluEndTrim**](gluendtrim.md).</span><span class="sxs-lookup"><span data-stu-id="edc52-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="edc52-145">Un **gluNurbsSurface** avec des nœuds de *\_ nombre de sknot* dans les nœuds direction *u* et *\_ nombre de tknot* dans la direction *v* avec les commandes *sorder* et *torder* doit avoir les points de contrôle (*sknot \_ Count*  - *sorder*) multipied par (*tknot \_ Count*  - *torder*).</span><span class="sxs-lookup"><span data-stu-id="edc52-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc52-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edc52-146">Requirements</span></span>



| <span data-ttu-id="edc52-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edc52-147">Requirement</span></span> | <span data-ttu-id="edc52-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="edc52-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="edc52-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edc52-149">Minimum supported client</span></span><br/> | <span data-ttu-id="edc52-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edc52-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="edc52-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edc52-151">Minimum supported server</span></span><br/> | <span data-ttu-id="edc52-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="edc52-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="edc52-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="edc52-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc52-154"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="edc52-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="edc52-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="edc52-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="edc52-156"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edc52-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="edc52-157">DLL</span><span class="sxs-lookup"><span data-stu-id="edc52-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edc52-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edc52-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc52-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edc52-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc52-160">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="edc52-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="edc52-161">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="edc52-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="edc52-162">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="edc52-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="edc52-163">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="edc52-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="edc52-164">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="edc52-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="edc52-165">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="edc52-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="edc52-166">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="edc52-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





