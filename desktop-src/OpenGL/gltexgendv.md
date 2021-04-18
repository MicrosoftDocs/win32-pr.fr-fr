---
title: fonction glTexGendv (GL. h)
description: Contrôle la génération des coordonnées de texture. | fonction glTexGendv (GL. h)
ms.assetid: fe0e28e4-50d3-473f-a290-7745a1718618
keywords:
- glTexGendv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexGendv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccae96a6289d2172115763b6b6117bf184e2eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104567601"
---
# <a name="gltexgendv-function"></a><span data-ttu-id="14309-105">glTexGendv fonction)</span><span class="sxs-lookup"><span data-stu-id="14309-105">glTexGendv function</span></span>

<span data-ttu-id="14309-106">Contrôle la génération des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="14309-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="14309-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14309-107">Syntax</span></span>


```C++
void WINAPI glTexGendv(
         GLenum   coord,
         GLenum   pname,
   const GLdouble *params
);
```



## <a name="parameters"></a><span data-ttu-id="14309-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14309-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14309-109">*coordonnées*</span><span class="sxs-lookup"><span data-stu-id="14309-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="14309-110">Coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="14309-110">A texture coordinate.</span></span> <span data-ttu-id="14309-111">Il doit s’agir de l’une des valeurs suivantes : GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="14309-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="14309-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="14309-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="14309-113">Nom symbolique de la fonction de génération de coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="14309-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="14309-114">*params*</span><span class="sxs-lookup"><span data-stu-id="14309-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="14309-115">Tableau qui contient les coefficients pour la fonction de génération de texture correspondante.</span><span class="sxs-lookup"><span data-stu-id="14309-115">An array that contains the coefficients for the corresponding texture generation function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14309-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14309-116">Return value</span></span>

<span data-ttu-id="14309-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="14309-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14309-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="14309-118">Error codes</span></span>

<span data-ttu-id="14309-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="14309-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="14309-120">Nom</span><span class="sxs-lookup"><span data-stu-id="14309-120">Name</span></span>                                                                                                  | <span data-ttu-id="14309-121">Signification</span><span class="sxs-lookup"><span data-stu-id="14309-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14309-122"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14309-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="14309-123">*Coord* ou *pname* n’était pas une valeur définie acceptée, ou l' *pname* était le \_ \_ mode de la génération de texture GL \_ et les *paramètres* n’étaient pas une valeur définie acceptée.</span><span class="sxs-lookup"><span data-stu-id="14309-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="14309-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14309-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="14309-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="14309-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="14309-126">Notes</span><span class="sxs-lookup"><span data-stu-id="14309-126">Remarks</span></span>

<span data-ttu-id="14309-127">La fonction **glTexGen** sélectionne une fonction de génération de coordonnée de texture ou fournit des coefficients pour l’une des fonctions.</span><span class="sxs-lookup"><span data-stu-id="14309-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="14309-128">Le paramètre *Coord* nomme une des coordonnées de la texture (s, t, r, q) et doit être l’un des symboles suivants : GL \_ s, GL \_ t, GL \_ r ou GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="14309-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="14309-129">Le paramètre *pname* doit être l’une des trois constantes symboliques suivantes : \_ mode de la génération de texture GL \_ \_ , plan d' \_ objet GL \_ ou \_ plan oculaire GL \_ .</span><span class="sxs-lookup"><span data-stu-id="14309-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="14309-130">Si *pname* est un plan \_ d’objet GL \_ ou un \_ plan oculaire GL \_ , *param* contient des coefficients pour la fonction de génération de texture correspondante.</span><span class="sxs-lookup"><span data-stu-id="14309-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="14309-131">Si la fonction de génération de texture \_ est \_ linéaire d’objet linéaire, la fonction</span><span class="sxs-lookup"><span data-stu-id="14309-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="14309-132">! [Équation représentant la fonction glTexGen lorsque la fonction de génération de texture est GL_OBJECT_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="14309-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="14309-133">est utilisé, où g est la valeur calculée pour la coordonnée nommée dans Coord ; P1, P2, P3 et P4 sont les quatre valeurs fournies dans params. et x ?, y ?, z ? et w ? sont les coordonnées d’objet du vertex.</span><span class="sxs-lookup"><span data-stu-id="14309-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="14309-134">Vous pouvez utiliser cette fonction pour texturer la carte à l’aide du niveau de mer comme plan de référence (défini par P1, P2, P3 et P4).</span><span class="sxs-lookup"><span data-stu-id="14309-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="14309-135">La \_ \_ fonction de génération de coordonnées linéaires de l’objet GL calcule l’altitude d’un sommet de terrain en tant que distance par rapport au niveau de la mer ; cette altitude est utilisée pour indexer l’image de texture pour mapper la neige blanche sur les pics et le gazon vert sur Foothills, par exemple.</span><span class="sxs-lookup"><span data-stu-id="14309-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="14309-136">Si la fonction de génération de texture \_ est \_ linéaire pour le GL, la fonction</span><span class="sxs-lookup"><span data-stu-id="14309-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="14309-137">! [Équation représentant la fonction glTexGen lorsque la fonction de génération de texture est GL_EYE_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="14309-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="14309-138">est utilisé, où</span><span class="sxs-lookup"><span data-stu-id="14309-138">is used, where</span></span>

![Équation représentant les coordonnées oculaires du vertex.](images/tex03.png)

<span data-ttu-id="14309-140">et x ?, y ?, z ? et w ? les coordonnées oculaires du vertex, P1, P2, P3 et P4 sont les valeurs fournies dans *param*, et M est la matrice modelview quand vous **callglTexGen**.</span><span class="sxs-lookup"><span data-stu-id="14309-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you **callglTexGen**.</span></span> <span data-ttu-id="14309-141">Si M est mal conditionné ou singulier, les coordonnées de texture générées par la fonction résultante peuvent être inexactes ou non définies.</span><span class="sxs-lookup"><span data-stu-id="14309-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="14309-142">Notez que les valeurs dans *param* définissent un plan de référence en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="14309-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="14309-143">La matrice modelview appliquée peut ne pas être la même en vigueur lorsque les sommets du polygone sont transformés.</span><span class="sxs-lookup"><span data-stu-id="14309-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="14309-144">Cette fonction établit un champ de coordonnées de texture qui peut produire des lignes de contour dynamiques sur les objets mobiles.</span><span class="sxs-lookup"><span data-stu-id="14309-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="14309-145">Si *pname* est la \_ \_ carte de sphère GL et que le *repère* est GL \_ S ou GL \_ t, des coordonnées de texture s et T sont générées comme suit.</span><span class="sxs-lookup"><span data-stu-id="14309-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="14309-146">Prenons le vecteur d’unité qui pointe de l’origine vers le vertex du polygone (en coordonnées oculaires).</span><span class="sxs-lookup"><span data-stu-id="14309-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="14309-147">Supposons que n est la normale actuelle, après la transformation en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="14309-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="14309-148">Let f = (FX () FY () FZ) T est le vecteur de réflexion de telle sorte que</span><span class="sxs-lookup"><span data-stu-id="14309-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Équation qui montre le vecteur de réflexion comme fonction du vecteur d’unité et normal actuel.](images/tex05.png)

<span data-ttu-id="14309-150">Enfin, laissez</span><span class="sxs-lookup"><span data-stu-id="14309-150">Finally, let</span></span>

![Équation qui présente m en tant que fonction du vecteur de réflexion.](images/tex07.png)

<span data-ttu-id="14309-152">Les valeurs assignées aux coordonnées de texture i et t sont</span><span class="sxs-lookup"><span data-stu-id="14309-152">Then the values assigned to the i and t texture coordinates are</span></span>

![Équation présentant les valeurs affectées aux coordonnées de texture i et t.](images/tex06.png)

<span data-ttu-id="14309-154">Vous pouvez activer ou désactiver une fonction de génération de coordonnées de texture à l’aide de [**glEnable**](glenable.md) ou [**glDisable**](gldisable.md) avec l’un des noms de coordonnées de texture symbolique (GL \_ texture \_ GEN \_ S, GL \_ texture \_ GEN \_ T, GL \_ texture \_ GEN \_ R ou GL \_ texture \_ GEN \_ Q) comme argument.</span><span class="sxs-lookup"><span data-stu-id="14309-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="14309-155">Lorsque cette fonction est activée, la coordonnée de texture spécifiée est calculée en fonction de la fonction de génération associée à cette coordonnée.</span><span class="sxs-lookup"><span data-stu-id="14309-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="14309-156">Lorsque cette fonction est désactivée, les vertex suivants prennent la coordonnée de texture spécifiée à partir de l’ensemble actuel de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="14309-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="14309-157">Initialement, toutes les fonctions de génération de texture sont définies sur GL \_ Eye \_ linéaire et sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="14309-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="14309-158">Les deux équations de plan s sont (1,0, 0, 0); les deux équations du plan t sont (0, 1, 0, 0); et toutes les équations du plan r et q sont (0,0).</span><span class="sxs-lookup"><span data-stu-id="14309-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="14309-159">Les fonctions suivantes récupèrent les informations relatives à glTexGen :</span><span class="sxs-lookup"><span data-stu-id="14309-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="14309-160">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="14309-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="14309-161">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ S</span><span class="sxs-lookup"><span data-stu-id="14309-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="14309-162">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="14309-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="14309-163">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ R</span><span class="sxs-lookup"><span data-stu-id="14309-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="14309-164">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ Q</span><span class="sxs-lookup"><span data-stu-id="14309-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="14309-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14309-165">Requirements</span></span>



| <span data-ttu-id="14309-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14309-166">Requirement</span></span> | <span data-ttu-id="14309-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="14309-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14309-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14309-168">Minimum supported client</span></span><br/> | <span data-ttu-id="14309-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14309-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14309-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14309-170">Minimum supported server</span></span><br/> | <span data-ttu-id="14309-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14309-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14309-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="14309-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="14309-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="14309-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="14309-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14309-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="14309-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14309-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14309-176">DLL</span><span class="sxs-lookup"><span data-stu-id="14309-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14309-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14309-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14309-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14309-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14309-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="14309-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="14309-180">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="14309-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="14309-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="14309-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="14309-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="14309-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="14309-183">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="14309-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="14309-184">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="14309-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="14309-185">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="14309-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="14309-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="14309-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="14309-187">glTexParameter</span><span class="sxs-lookup"><span data-stu-id="14309-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="14309-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="14309-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="14309-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="14309-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





