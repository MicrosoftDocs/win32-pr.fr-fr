---
title: fonction glFrustum (GL. h)
description: La fonction glFrustum multiplie la matrice actuelle par une matrice de perspective.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- glFrustum fonction OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104566459"
---
# <a name="glfrustum-function"></a><span data-ttu-id="7d880-104">glFrustum fonction)</span><span class="sxs-lookup"><span data-stu-id="7d880-104">glFrustum function</span></span>

<span data-ttu-id="7d880-105">La fonction **glFrustum** multiplie la matrice actuelle par une matrice de perspective.</span><span class="sxs-lookup"><span data-stu-id="7d880-105">The **glFrustum** function multiplies the current matrix by a perspective matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d880-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d880-106">Syntax</span></span>


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="7d880-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d880-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d880-108">*gauche*</span><span class="sxs-lookup"><span data-stu-id="7d880-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="7d880-109">Coordonnée du plan de découpage vertical gauche.</span><span class="sxs-lookup"><span data-stu-id="7d880-109">The coordinate for the left-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="7d880-110">*Oui*</span><span class="sxs-lookup"><span data-stu-id="7d880-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="7d880-111">Coordonnée du plan de découpage vertical à droite.</span><span class="sxs-lookup"><span data-stu-id="7d880-111">The coordinate for the right-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="7d880-112">*ballon*</span><span class="sxs-lookup"><span data-stu-id="7d880-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="7d880-113">Coordonnée du plan de découpage inférieur horizontal.</span><span class="sxs-lookup"><span data-stu-id="7d880-113">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="7d880-114">*top*</span><span class="sxs-lookup"><span data-stu-id="7d880-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="7d880-115">Coordonnée du plan de découpage inférieur horizontal.</span><span class="sxs-lookup"><span data-stu-id="7d880-115">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="7d880-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="7d880-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="7d880-117">Les distances par le plan de découpage près de profondeur.</span><span class="sxs-lookup"><span data-stu-id="7d880-117">The distances to the near-depth clipping plane.</span></span> <span data-ttu-id="7d880-118">Doit être positif.</span><span class="sxs-lookup"><span data-stu-id="7d880-118">Must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="7d880-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="7d880-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="7d880-120">Distances avec les plans de découpage de profondeur lointaine.</span><span class="sxs-lookup"><span data-stu-id="7d880-120">The distances to the far-depth clipping planes.</span></span> <span data-ttu-id="7d880-121">Doit être positif.</span><span class="sxs-lookup"><span data-stu-id="7d880-121">Must be positive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d880-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7d880-122">Return value</span></span>

<span data-ttu-id="7d880-123">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7d880-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7d880-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7d880-124">Error codes</span></span>

<span data-ttu-id="7d880-125">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7d880-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7d880-126">Nom</span><span class="sxs-lookup"><span data-stu-id="7d880-126">Name</span></span>                                                                                                  | <span data-ttu-id="7d880-127">Signification</span><span class="sxs-lookup"><span data-stu-id="7d880-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7d880-128"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d880-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7d880-129">*zNear* ou *zFar* n’était pas postitive.</span><span class="sxs-lookup"><span data-stu-id="7d880-129">*zNear* or *zFar* was not postitive.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="7d880-130"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d880-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7d880-131">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7d880-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7d880-132">Notes</span><span class="sxs-lookup"><span data-stu-id="7d880-132">Remarks</span></span>

<span data-ttu-id="7d880-133">La fonction **glFrustum** décrit une matrice de perspective qui produit une projection de perspective.</span><span class="sxs-lookup"><span data-stu-id="7d880-133">The **glFrustum** function describes a perspective matrix that produces a perspective projection.</span></span> <span data-ttu-id="7d880-134">Les paramètres (*gauche*, *bas*, *zNear*) et (*Right*, *Top*, *zNear*) spécifient les points sur le plan de découpage proche qui sont mappés aux angles inférieur gauche et supérieur droit de la fenêtre, respectivement, en supposant que l’œil se trouve à (0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="7d880-134">The (*left*, *bottom*, *zNear*) and (*right*, *top*, *zNear*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0).</span></span> <span data-ttu-id="7d880-135">Le paramètre *zFar* spécifie l’emplacement du plan de découpage Far.</span><span class="sxs-lookup"><span data-stu-id="7d880-135">The *zFar* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="7d880-136">*ZNear* et *zFar* doivent être positifs.</span><span class="sxs-lookup"><span data-stu-id="7d880-136">Both *zNear* and *zFar* must be positive.</span></span> <span data-ttu-id="7d880-137">La matrice correspondante est présentée dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="7d880-137">The corresponding matrix is shown in the following image.</span></span>

![Diagramme montrant la matrice de perspective qui produit une projection de perspective.](images/frust01.png)![Équations présentant la fonction glFrustum qui décrit une matrice de perspective.](images/frust02.png)

<span data-ttu-id="7d880-140">La fonction **glFrustum** multiplie la matrice actuelle par cette matrice, avec le résultat qui remplace la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="7d880-140">The **glFrustum** function multiplies the current matrix by this matrix, with the result replacing the current matrix.</span></span> <span data-ttu-id="7d880-141">Autrement dit, si M est la matrice actuelle et que F est la matrice de perspective frustum, **glFrustum** remplace M par m F.</span><span class="sxs-lookup"><span data-stu-id="7d880-141">That is, if M is the current matrix and F is the frustum perspective matrix, then **glFrustum** replaces M with M   F.</span></span>

<span data-ttu-id="7d880-142">Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer la pile de matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="7d880-142">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the current matrix stack.</span></span>

<span data-ttu-id="7d880-143">La précision de la mémoire tampon de profondeur est affectée par les valeurs spécifiées pour *zNear* et *zFar*.</span><span class="sxs-lookup"><span data-stu-id="7d880-143">Depth-buffer precision is affected by the values specified for *zNear* and *zFar*.</span></span> <span data-ttu-id="7d880-144">Plus le rapport entre *zFar* et *zNear* est élevé, moins le tampon de profondeur est en effet à distinguer les surfaces proches les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="7d880-144">The greater the ratio of *zFar* to *zNear* is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other.</span></span> <span data-ttu-id="7d880-145">Si</span><span class="sxs-lookup"><span data-stu-id="7d880-145">If</span></span>

![Équation qui indique le rapport entre le haut et le bas.](images/frust03.png)

<span data-ttu-id="7d880-147">le *Journal* 2 (*r*) bits de précision du tampon de profondeur est perdu.</span><span class="sxs-lookup"><span data-stu-id="7d880-147">roughly *log* 2 (*r*) bits of depth buffer precision are lost.</span></span> <span data-ttu-id="7d880-148">Étant donné que *r* approche l’infini comme *zNear* approche de zéro, vous ne devez jamais définir *zNear* à zéro.</span><span class="sxs-lookup"><span data-stu-id="7d880-148">Because *r* approaches infinity as *zNear* approaches zero, you should never set *zNear* to zero.</span></span>

<span data-ttu-id="7d880-149">Les fonctions suivantes récupèrent des informations sur **glFrustum**:</span><span class="sxs-lookup"><span data-stu-id="7d880-149">The following functions retrieve information about **glFrustum**:</span></span>

<span data-ttu-id="7d880-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="7d880-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="7d880-151">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="7d880-151">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="7d880-152">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="7d880-152">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="7d880-153">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="7d880-153">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="7d880-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d880-154">Requirements</span></span>



| <span data-ttu-id="7d880-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d880-155">Requirement</span></span> | <span data-ttu-id="7d880-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d880-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d880-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d880-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7d880-158">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d880-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7d880-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d880-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7d880-160">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d880-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d880-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d880-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d880-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d880-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7d880-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7d880-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d880-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d880-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7d880-165">DLL</span><span class="sxs-lookup"><span data-stu-id="7d880-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d880-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d880-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d880-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d880-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d880-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7d880-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7d880-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7d880-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7d880-170">**glGet**</span><span class="sxs-lookup"><span data-stu-id="7d880-170">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7d880-171">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="7d880-171">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="7d880-172">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="7d880-172">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="7d880-173">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="7d880-173">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="7d880-174">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="7d880-174">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="7d880-175">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="7d880-175">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="7d880-176">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="7d880-176">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





