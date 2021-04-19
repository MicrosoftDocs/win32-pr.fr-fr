---
title: fonction glClipPlane (GL. h)
description: La fonction glClipPlane spécifie un plan par rapport auquel toute la géométrie est découpée.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- glClipPlane fonction OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527572"
---
# <a name="glclipplane-function"></a><span data-ttu-id="084d8-104">glClipPlane fonction)</span><span class="sxs-lookup"><span data-stu-id="084d8-104">glClipPlane function</span></span>

<span data-ttu-id="084d8-105">La fonction **glClipPlane** spécifie un plan par rapport auquel toute la géométrie est découpée.</span><span class="sxs-lookup"><span data-stu-id="084d8-105">The **glClipPlane** function specifies a plane against which all geometry is clipped.</span></span>

## <a name="syntax"></a><span data-ttu-id="084d8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="084d8-106">Syntax</span></span>


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="084d8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="084d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084d8-108">*verticale*</span><span class="sxs-lookup"><span data-stu-id="084d8-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="084d8-109">Plan de découpage positionné.</span><span class="sxs-lookup"><span data-stu-id="084d8-109">The clipping plane that is being positioned.</span></span> <span data-ttu-id="084d8-110">Les noms symboliques de la forme \_ plan du clip GL \_ *i*, où *i* est un nombre entier compris entre 0 et \_ le nombre maximal \_ de clips de la comptabilité \_ -1, sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="084d8-110">Symbolic names of the form GL\_CLIP\_PLANE *i*, where *i* is an integer between 0 and GL\_MAX\_CLIP\_PLANES - 1, are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="084d8-111">*Sommaire*</span><span class="sxs-lookup"><span data-stu-id="084d8-111">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="084d8-112">Adresse d’un tableau de quatre valeurs à virgule flottante double précision.</span><span class="sxs-lookup"><span data-stu-id="084d8-112">The address of an array of four double-precision floating-point values.</span></span> <span data-ttu-id="084d8-113">Ces valeurs sont interprétées comme une équation plan.</span><span class="sxs-lookup"><span data-stu-id="084d8-113">These values are interpreted as a plane equation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="084d8-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="084d8-114">Return value</span></span>

<span data-ttu-id="084d8-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="084d8-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="084d8-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="084d8-116">Error codes</span></span>

<span data-ttu-id="084d8-117">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="084d8-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="084d8-118">Nom</span><span class="sxs-lookup"><span data-stu-id="084d8-118">Name</span></span>                                                                                                  | <span data-ttu-id="084d8-119">Signification</span><span class="sxs-lookup"><span data-stu-id="084d8-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="084d8-120"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="084d8-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="084d8-121">le *plan* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="084d8-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="084d8-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="084d8-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="084d8-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="084d8-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="084d8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="084d8-124">Remarks</span></span>

<span data-ttu-id="084d8-125">La géométrie est toujours découpée par rapport aux limites d’un frustum à six plans en *x*, *y* et *z*.</span><span class="sxs-lookup"><span data-stu-id="084d8-125">Geometry is always clipped against the boundaries of a six-plane frustum in *x*, *y*, and *z*.</span></span> <span data-ttu-id="084d8-126">La fonction **glClipPlane** permet de spécifier des plans supplémentaires, pas nécessairement perpendiculairement à l’axe des *x*, à l’axe *y* ou à l’axe *z*, par rapport auquel toutes les géométries sont découpées.</span><span class="sxs-lookup"><span data-stu-id="084d8-126">The **glClipPlane** function allows the specification of additional planes, not necessarily perpendicular to the *x-* axis, *y-* axis, or *z*-axis, against which all geometry is clipped.</span></span> <span data-ttu-id="084d8-127">Vous pouvez spécifier jusqu’à un \_ nombre maximal de \_ plans de captures de l’élément GL \_ , où le \_ nombre maximal \_ \_ de plans de clip GL est d’au moins six dans toutes les implémentations.</span><span class="sxs-lookup"><span data-stu-id="084d8-127">Up to GL\_MAX\_CLIP\_PLANES planes can be specified, where GL\_MAX\_CLIP\_PLANES is at least six in all implementations.</span></span> <span data-ttu-id="084d8-128">Étant donné que la zone de découpage obtenue est l’intersection des demi-espaces définis, elle est toujours convexe.</span><span class="sxs-lookup"><span data-stu-id="084d8-128">Because the resulting clipping region is the intersection of the defined half-spaces, it is always convex.</span></span>

<span data-ttu-id="084d8-129">La fonction **glClipPlane** spécifie un demi-espace à l’aide d’une équation de plan à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="084d8-129">The **glClipPlane** function specifies a half-space using a four-component plane equation.</span></span> <span data-ttu-id="084d8-130">Quand vous appelez **glClipPlane**,*Equation* est transformé par l’inverse de la matrice modelview et stocké dans les coordonnées oculaire obtenues.</span><span class="sxs-lookup"><span data-stu-id="084d8-130">When you call **glClipPlane**,*equation* is transformed by the inverse of the modelview matrix and stored in the resulting eye coordinates.</span></span> <span data-ttu-id="084d8-131">Les modifications ultérieures apportées à la matrice modelview n’ont aucun effet sur les composants d’équation plan stocké.</span><span class="sxs-lookup"><span data-stu-id="084d8-131">Subsequent changes to the modelview matrix have no effect on the stored plane-equation components.</span></span> <span data-ttu-id="084d8-132">Si le produit scalaire des coordonnées oculaires d’un vertex avec les composants de l’équation du plan stocké est positif ou zéro, le vertex est en rapport avec ce plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="084d8-132">If the dot product of the eye coordinates of a vertex with the stored plane equation components is positive or zero, the vertex is in with respect to that clipping plane.</span></span> <span data-ttu-id="084d8-133">Sinon, elle est en sortie.</span><span class="sxs-lookup"><span data-stu-id="084d8-133">Otherwise, it is out.</span></span>

<span data-ttu-id="084d8-134">Utilisez les fonctions [**glEnable**](glenable.md) et [**glDisable**](gldisable.md) pour activer et désactiver les plans de découpage.</span><span class="sxs-lookup"><span data-stu-id="084d8-134">Use the [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions to enable and disable clipping planes.</span></span> <span data-ttu-id="084d8-135">Appelez les plans de découpage avec l’argument GL \_ clip \_ plan *i*, où *i* est le numéro de plan.</span><span class="sxs-lookup"><span data-stu-id="084d8-135">Call clipping planes with the argument GL\_CLIP\_PLANE *i*, where *i* is the plane number.</span></span>

<span data-ttu-id="084d8-136">Par défaut, tous les plans de découpage sont définis en tant que (0, 0, 0, 0) dans les coordonnées oculaires et sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="084d8-136">By default, all clipping planes are defined as (0,0,0,0) in eye coordinates and are disabled.</span></span>

<span data-ttu-id="084d8-137">C’est toujours le cas dans le cadre du \_ plan de clip GL \_ *i* = GL \_ clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="084d8-137">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="084d8-138">Les fonctions suivantes récupèrent les informations relatives à **glClipPlane**:</span><span class="sxs-lookup"><span data-stu-id="084d8-138">The following functions retrieve information related to **glClipPlane**:</span></span>

[<span data-ttu-id="084d8-139">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="084d8-139">**glGetClipPlane**</span></span>](glgetclipplane.md)

<span data-ttu-id="084d8-140">[**glIsEnabled**](glisenabled.md) avec argument GL \_ clip \_ plan *i*</span><span class="sxs-lookup"><span data-stu-id="084d8-140">[**glIsEnabled**](glisenabled.md) with argument GL\_CLIP\_PLANE *i*</span></span>

## <a name="requirements"></a><span data-ttu-id="084d8-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="084d8-141">Requirements</span></span>



| <span data-ttu-id="084d8-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="084d8-142">Requirement</span></span> | <span data-ttu-id="084d8-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="084d8-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="084d8-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="084d8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="084d8-145">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="084d8-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="084d8-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="084d8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="084d8-147">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="084d8-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="084d8-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="084d8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="084d8-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="084d8-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="084d8-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="084d8-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="084d8-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="084d8-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="084d8-152">DLL</span><span class="sxs-lookup"><span data-stu-id="084d8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="084d8-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="084d8-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="084d8-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="084d8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084d8-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="084d8-155">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="084d8-156">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="084d8-156">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="084d8-157">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="084d8-157">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="084d8-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="084d8-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="084d8-159">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="084d8-159">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="084d8-160">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="084d8-160">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





