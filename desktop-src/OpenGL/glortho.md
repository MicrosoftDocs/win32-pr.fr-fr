---
title: fonction glOrtho (GL. h)
description: La fonction glOrtho multiplie la matrice actuelle par une matrice orthographique.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- glOrtho fonction OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104565798"
---
# <a name="glortho-function"></a><span data-ttu-id="77a1c-104">glOrtho fonction)</span><span class="sxs-lookup"><span data-stu-id="77a1c-104">glOrtho function</span></span>

<span data-ttu-id="77a1c-105">La fonction **glOrtho** multiplie la matrice actuelle par une matrice orthographique.</span><span class="sxs-lookup"><span data-stu-id="77a1c-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a1c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77a1c-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="77a1c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77a1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77a1c-108">*gauche*</span><span class="sxs-lookup"><span data-stu-id="77a1c-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="77a1c-109">Coordonnées du plan de découpage vertical gauche.</span><span class="sxs-lookup"><span data-stu-id="77a1c-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="77a1c-110">*Oui*</span><span class="sxs-lookup"><span data-stu-id="77a1c-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="77a1c-111">Coordonnées du plan de découpage vertical theright.</span><span class="sxs-lookup"><span data-stu-id="77a1c-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="77a1c-112">*ballon*</span><span class="sxs-lookup"><span data-stu-id="77a1c-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="77a1c-113">Coordonnées du plan de découpage horizontal inférieur.</span><span class="sxs-lookup"><span data-stu-id="77a1c-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="77a1c-114">*top*</span><span class="sxs-lookup"><span data-stu-id="77a1c-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="77a1c-115">Coordonnées des plans de découpage horizontal supérieurs.</span><span class="sxs-lookup"><span data-stu-id="77a1c-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="77a1c-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="77a1c-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="77a1c-117">Distances avec le plan de découpage de profondeur le plus proche.</span><span class="sxs-lookup"><span data-stu-id="77a1c-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="77a1c-118">Cette distance est négative si le plan doit être placé derrière la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="77a1c-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="77a1c-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="77a1c-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="77a1c-120">Distances avec le plan de découpage de profondeur le plus éloigné.</span><span class="sxs-lookup"><span data-stu-id="77a1c-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="77a1c-121">Cette distance est négative si le plan doit être placé derrière la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="77a1c-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77a1c-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="77a1c-122">Return value</span></span>

<span data-ttu-id="77a1c-123">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="77a1c-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77a1c-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="77a1c-124">Error codes</span></span>

<span data-ttu-id="77a1c-125">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="77a1c-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="77a1c-126">Nom</span><span class="sxs-lookup"><span data-stu-id="77a1c-126">Name</span></span>                                                                                                  | <span data-ttu-id="77a1c-127">Signification</span><span class="sxs-lookup"><span data-stu-id="77a1c-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77a1c-128"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77a1c-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="77a1c-129">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="77a1c-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="77a1c-130">Notes</span><span class="sxs-lookup"><span data-stu-id="77a1c-130">Remarks</span></span>

<span data-ttu-id="77a1c-131">La fonction **glOrtho** décrit une matrice de perspective qui produit une projection parallèle.</span><span class="sxs-lookup"><span data-stu-id="77a1c-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="77a1c-132">Les paramètres (*gauche*, *bas*, *proche*) et (*droite*, *haut*, *near*) spécifient les points sur le plan de découpage proche qui sont mappés aux angles inférieur gauche et supérieur droit de la fenêtre, respectivement, en supposant que l’œil se trouve à (0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="77a1c-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="77a1c-133">Le paramètre *Far* spécifie l’emplacement du plan de découpage Far.</span><span class="sxs-lookup"><span data-stu-id="77a1c-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="77a1c-134">*ZNear* et *zFar* peuvent être positifs ou négatifs.</span><span class="sxs-lookup"><span data-stu-id="77a1c-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="77a1c-135">La matrice correspondante est présentée dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="77a1c-135">The corresponding matrix is shown in the following image.</span></span>

![Diagramme montrant la matrice de perspective décrite par la fonction glOrtho.](images/ortho1.png)

<span data-ttu-id="77a1c-137">where</span><span class="sxs-lookup"><span data-stu-id="77a1c-137">where</span></span>

![Équations décrivant la matrice de perspective.](images/ortho2.png)

<span data-ttu-id="77a1c-139">La matrice actuelle est multipliée par cette matrice avec le résultat qui remplace la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="77a1c-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="77a1c-140">Autrement dit, si M est la matrice active et O est la matrice ortho, M est remplacé par M O.</span><span class="sxs-lookup"><span data-stu-id="77a1c-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="77a1c-141">Utilisez [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix** pour enregistrer et restaurer la pile de matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="77a1c-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="77a1c-142">Utilisez [**glMatrixMode**](glmatrixmode.md) pour définir la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="77a1c-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="77a1c-143">Les fonctions suivantes récupèrent les informations relatives à **glOrtho**:</span><span class="sxs-lookup"><span data-stu-id="77a1c-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="77a1c-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="77a1c-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="77a1c-145">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="77a1c-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="77a1c-146">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="77a1c-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="77a1c-147">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="77a1c-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="77a1c-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77a1c-148">Requirements</span></span>



| <span data-ttu-id="77a1c-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77a1c-149">Requirement</span></span> | <span data-ttu-id="77a1c-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="77a1c-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77a1c-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77a1c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="77a1c-152">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77a1c-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="77a1c-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77a1c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="77a1c-154">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77a1c-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77a1c-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="77a1c-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="77a1c-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="77a1c-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="77a1c-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="77a1c-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="77a1c-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77a1c-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="77a1c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="77a1c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77a1c-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77a1c-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a1c-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77a1c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a1c-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="77a1c-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="77a1c-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="77a1c-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="77a1c-164">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="77a1c-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="77a1c-165">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="77a1c-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="77a1c-166">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="77a1c-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="77a1c-167">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="77a1c-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="77a1c-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="77a1c-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





