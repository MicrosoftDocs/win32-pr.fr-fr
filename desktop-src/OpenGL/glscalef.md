---
title: fonction glScalef (GL. h)
description: Les fonctions glScaled et glScalef multiplient la matrice actuelle par une matrice de mise à l’échelle générale. | fonction glScalef (GL. h)
ms.assetid: bf039bbc-7669-4282-b629-71440b798cb1
keywords:
- glScalef fonction OpenGL
topic_type:
- apiref
api_name:
- glScalef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eda183b763f22736370dd5c9ea13ca8793243e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104563857"
---
# <a name="glscalef-function"></a><span data-ttu-id="cdc8d-105">glScalef fonction)</span><span class="sxs-lookup"><span data-stu-id="cdc8d-105">glScalef function</span></span>

<span data-ttu-id="cdc8d-106">Les fonctions [**glScaled**](glscaled.md) et **glScalef** multiplient la matrice actuelle par une matrice de mise à l’échelle générale.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-106">The [**glScaled**](glscaled.md) and **glScalef** functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc8d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdc8d-107">Syntax</span></span>


```C++
void WINAPI glScalef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="cdc8d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdc8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc8d-109">*x*</span><span class="sxs-lookup"><span data-stu-id="cdc8d-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc8d-110">Facteurs d’échelle le long de l’axe *x* .</span><span class="sxs-lookup"><span data-stu-id="cdc8d-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="cdc8d-111">*y*</span><span class="sxs-lookup"><span data-stu-id="cdc8d-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc8d-112">Facteurs d’échelle le long de l’axe *y* .</span><span class="sxs-lookup"><span data-stu-id="cdc8d-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="cdc8d-113">*z*</span><span class="sxs-lookup"><span data-stu-id="cdc8d-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc8d-114">Facteurs d’échelle le long de l’axe *z* .</span><span class="sxs-lookup"><span data-stu-id="cdc8d-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc8d-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cdc8d-115">Return value</span></span>

<span data-ttu-id="cdc8d-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cdc8d-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cdc8d-117">Error codes</span></span>

<span data-ttu-id="cdc8d-118">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc8d-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cdc8d-119">Nom</span><span class="sxs-lookup"><span data-stu-id="cdc8d-119">Name</span></span>                                                                                                  | <span data-ttu-id="cdc8d-120">Signification</span><span class="sxs-lookup"><span data-stu-id="cdc8d-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdc8d-121"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cdc8d-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cdc8d-122">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cdc8d-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cdc8d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cdc8d-123">Remarks</span></span>

<span data-ttu-id="cdc8d-124">La fonction **glScalef** produit une mise à l’échelle générale le long des axes *x*, *y* et *z* .</span><span class="sxs-lookup"><span data-stu-id="cdc8d-124">The **glScalef** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="cdc8d-125">Les trois arguments indiquent les facteurs d’échelle souhaités le long de chacun des trois axes.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="cdc8d-126">La matrice résultante apparaît dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-126">The resulting matrix appears in the following image.</span></span>

![Diagramme montrant la matrice des facteurs d’échelle le long des axes x, y et z.](images/scale01.png)

<span data-ttu-id="cdc8d-128">La matrice actuelle (voir [**glMatrixMode**](glmatrixmode.md)) est multipliée par cette matrice de mise à l’échelle, le produit remplaçant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="cdc8d-129">Autrement dit, si M est la matrice active et S est la matrice d’échelle, M est remplacé par M S.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="cdc8d-130">Si le mode matriciel est GL \_ MODELVIEW ou GL \_ projection, tous les objets dessinés après l’appel de **glScalef** sont mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScalef** is called are scaled.</span></span> <span data-ttu-id="cdc8d-131">Utilisez [**glPushMatrix**](glpushmatrix.md) et [**glPopMatrix**](glpopmatrix.md) pour enregistrer et restaurer le système de coordonnées non mis à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="cdc8d-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="cdc8d-132">Si des facteurs de mise à l’échelle autres que 1,0 sont appliqués à la matrice modelview et que l’éclairage est activé, la normalisation automatique des normales doit probablement également être activée ([**glEnable**](glenable.md) et [**glDisable**](gldisable.md) avec l’argument GL \_ Normalize).</span><span class="sxs-lookup"><span data-stu-id="cdc8d-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="cdc8d-133">Les fonctions suivantes récupèrent les informations relatives à **glScalef**:</span><span class="sxs-lookup"><span data-stu-id="cdc8d-133">The following functions retrieve information related to **glScalef**:</span></span>

<span data-ttu-id="cdc8d-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="cdc8d-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="cdc8d-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="cdc8d-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="cdc8d-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="cdc8d-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="cdc8d-137">matrice de texture [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="cdc8d-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc8d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdc8d-138">Requirements</span></span>



| <span data-ttu-id="cdc8d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdc8d-139">Requirement</span></span> | <span data-ttu-id="cdc8d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdc8d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc8d-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdc8d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc8d-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdc8d-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cdc8d-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdc8d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc8d-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdc8d-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cdc8d-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdc8d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc8d-146"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc8d-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cdc8d-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cdc8d-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdc8d-148"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdc8d-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cdc8d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cdc8d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdc8d-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdc8d-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc8d-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdc8d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc8d-152">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-154">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-155">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-156">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-157">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-158">**glRotated**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-159">**glRotatef**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="cdc8d-160">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="cdc8d-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





