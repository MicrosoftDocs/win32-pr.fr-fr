---
title: fonction glTexGeniv (GL. h)
description: Contrôle la génération des coordonnées de texture. | fonction glTexGeniv (GL. h)
ms.assetid: e95f2844-414a-4fb2-944e-4d0b6e51bdd2
keywords:
- glTexGeniv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexGeniv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05a5981e76c44ea8ee0fe037ac5c28d8c45f5f6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104563941"
---
# <a name="gltexgeniv-function"></a><span data-ttu-id="aa65e-105">glTexGeniv fonction)</span><span class="sxs-lookup"><span data-stu-id="aa65e-105">glTexGeniv function</span></span>

<span data-ttu-id="aa65e-106">Contrôle la génération des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="aa65e-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa65e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa65e-107">Syntax</span></span>


```C++
void WINAPI glTexGeniv(
         GLenum coord,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="aa65e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa65e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa65e-109">*coordonnées*</span><span class="sxs-lookup"><span data-stu-id="aa65e-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="aa65e-110">Coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="aa65e-110">A texture coordinate.</span></span> <span data-ttu-id="aa65e-111">Il doit s’agir de l’une des valeurs suivantes : GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="aa65e-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="aa65e-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="aa65e-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="aa65e-113">Nom symbolique de la fonction de génération de coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="aa65e-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="aa65e-114">*params*</span><span class="sxs-lookup"><span data-stu-id="aa65e-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="aa65e-115">Tableau qui contient les coefficients pour la fonction de génération de texture correspondante.</span><span class="sxs-lookup"><span data-stu-id="aa65e-115">An array that contains the coefficients for the corresponding texture generation function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa65e-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aa65e-116">Return value</span></span>

<span data-ttu-id="aa65e-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="aa65e-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa65e-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="aa65e-118">Error codes</span></span>

<span data-ttu-id="aa65e-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="aa65e-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="aa65e-120">Nom</span><span class="sxs-lookup"><span data-stu-id="aa65e-120">Name</span></span>                                                                                                  | <span data-ttu-id="aa65e-121">Signification</span><span class="sxs-lookup"><span data-stu-id="aa65e-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa65e-122"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa65e-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="aa65e-123">*Coord* ou *pname* n’était pas une valeur définie acceptée, ou l' *pname* était le \_ \_ mode de la génération de texture GL \_ et les *paramètres* n’étaient pas une valeur définie acceptée.</span><span class="sxs-lookup"><span data-stu-id="aa65e-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="aa65e-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa65e-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="aa65e-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="aa65e-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="aa65e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="aa65e-126">Remarks</span></span>

<span data-ttu-id="aa65e-127">La fonction **glTexGen** sélectionne une fonction de génération de coordonnée de texture ou fournit des coefficients pour l’une des fonctions.</span><span class="sxs-lookup"><span data-stu-id="aa65e-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="aa65e-128">Le paramètre *Coord* nomme une des coordonnées de la texture (s, t, r, q) et doit être l’un des symboles suivants : GL \_ s, GL \_ t, GL \_ r ou GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="aa65e-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="aa65e-129">Le paramètre *pname* doit être l’une des trois constantes symboliques suivantes : \_ mode de la génération de texture GL \_ \_ , plan d' \_ objet GL \_ ou \_ plan oculaire GL \_ .</span><span class="sxs-lookup"><span data-stu-id="aa65e-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="aa65e-130">Si *pname* est un plan \_ d’objet GL \_ ou un \_ plan oculaire GL \_ , *param* contient des coefficients pour la fonction de génération de texture correspondante.</span><span class="sxs-lookup"><span data-stu-id="aa65e-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="aa65e-131">Si la fonction de génération de texture \_ est \_ linéaire d’objet linéaire, la fonction</span><span class="sxs-lookup"><span data-stu-id="aa65e-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="aa65e-132">! [Équation représentant la fonction glTexGen lorsque la fonction de génération de texture est GL_OBJECT_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="aa65e-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="aa65e-133">est utilisé, où g est la valeur calculée pour la coordonnée nommée dans Coord ; P1, P2, P3 et P4 sont les quatre valeurs fournies dans params. et x ?, y ?, z ? et w ? sont les coordonnées d’objet du vertex.</span><span class="sxs-lookup"><span data-stu-id="aa65e-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="aa65e-134">Vous pouvez utiliser cette fonction pour texturer la carte à l’aide du niveau de mer comme plan de référence (défini par P1, P2, P3 et P4).</span><span class="sxs-lookup"><span data-stu-id="aa65e-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="aa65e-135">La \_ \_ fonction de génération de coordonnées linéaires de l’objet GL calcule l’altitude d’un sommet de terrain en tant que distance par rapport au niveau de la mer ; cette altitude est utilisée pour indexer l’image de texture pour mapper la neige blanche sur les pics et le gazon vert sur Foothills, par exemple.</span><span class="sxs-lookup"><span data-stu-id="aa65e-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="aa65e-136">Si la fonction de génération de texture \_ est \_ linéaire pour le GL, la fonction</span><span class="sxs-lookup"><span data-stu-id="aa65e-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="aa65e-137">! [Équation représentant la fonction glTexGen lorsque la fonction de génération de texture est GL_EYE_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="aa65e-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="aa65e-138">est utilisé, où</span><span class="sxs-lookup"><span data-stu-id="aa65e-138">is used, where</span></span>

![Équation représentant les coordonnées oculaires du vertex.](images/tex03.png)

<span data-ttu-id="aa65e-140">et x ?, y ?, z ? et w ? les coordonnées oculaires du vertex, P1, P2, P3 et P4 sont les valeurs fournies dans *param*, et M est la matrice modelview quand vous appelez **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="aa65e-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="aa65e-141">Si M est mal conditionné ou singulier, les coordonnées de texture générées par la fonction résultante peuvent être inexactes ou non définies.</span><span class="sxs-lookup"><span data-stu-id="aa65e-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="aa65e-142">Notez que les valeurs dans *param* définissent un plan de référence en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="aa65e-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="aa65e-143">La matrice modelview appliquée peut ne pas être la même en vigueur lorsque les sommets du polygone sont transformés.</span><span class="sxs-lookup"><span data-stu-id="aa65e-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="aa65e-144">Cette fonction établit un champ de coordonnées de texture qui peut produire des lignes de contour dynamiques sur les objets mobiles.</span><span class="sxs-lookup"><span data-stu-id="aa65e-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="aa65e-145">Si *pname* est la \_ \_ carte de sphère GL et que le *repère* est GL \_ S ou GL \_ t, des coordonnées de texture s et T sont générées comme suit.</span><span class="sxs-lookup"><span data-stu-id="aa65e-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="aa65e-146">Prenons le vecteur d’unité qui pointe de l’origine vers le vertex du polygone (en coordonnées oculaires).</span><span class="sxs-lookup"><span data-stu-id="aa65e-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="aa65e-147">Supposons que n est la normale actuelle, après la transformation en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="aa65e-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="aa65e-148">Let f = (FX () FY () FZ) T est le vecteur de réflexion de telle sorte que</span><span class="sxs-lookup"><span data-stu-id="aa65e-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Équation qui montre le vecteur de réflexion comme fonction du vecteur d’unité et normal actuel.](images/tex05.png)

<span data-ttu-id="aa65e-150">Enfin, laissez</span><span class="sxs-lookup"><span data-stu-id="aa65e-150">Finally, let</span></span>

![Équation qui présente m en tant que fonction du vecteur de réflexion.](images/tex07.png)

<span data-ttu-id="aa65e-152">Les valeurs assignées aux coordonnées de texture i et t sont</span><span class="sxs-lookup"><span data-stu-id="aa65e-152">Then the values assigned to the i and t texture coordinates are</span></span>

![Équation présentant les valeurs affectées aux coordonnées de texture i et t.](images/tex06.png)

<span data-ttu-id="aa65e-154">Vous pouvez activer ou désactiver une fonction de génération de coordonnées de texture à l’aide de [**glEnable**](glenable.md) ou [**glDisable**](gldisable.md) avec l’un des noms de coordonnées de texture symbolique (GL \_ texture \_ GEN \_ S, GL \_ texture \_ GEN \_ T, GL \_ texture \_ GEN \_ R ou GL \_ texture \_ GEN \_ Q) comme argument.</span><span class="sxs-lookup"><span data-stu-id="aa65e-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="aa65e-155">Lorsque cette fonction est activée, la coordonnée de texture spécifiée est calculée en fonction de la fonction de génération associée à cette coordonnée.</span><span class="sxs-lookup"><span data-stu-id="aa65e-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="aa65e-156">Lorsque cette fonction est désactivée, les vertex suivants prennent la coordonnée de texture spécifiée à partir de l’ensemble actuel de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="aa65e-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="aa65e-157">Initialement, toutes les fonctions de génération de texture sont définies sur GL \_ Eye \_ linéaire et sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="aa65e-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="aa65e-158">Les deux équations de plan s sont (1,0, 0, 0); les deux équations du plan t sont (0, 1, 0, 0); et toutes les équations du plan r et q sont (0,0).</span><span class="sxs-lookup"><span data-stu-id="aa65e-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="aa65e-159">Les fonctions suivantes récupèrent les informations relatives à glTexGen :</span><span class="sxs-lookup"><span data-stu-id="aa65e-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="aa65e-160">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="aa65e-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="aa65e-161">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ S</span><span class="sxs-lookup"><span data-stu-id="aa65e-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="aa65e-162">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ T</span><span class="sxs-lookup"><span data-stu-id="aa65e-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="aa65e-163">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ R</span><span class="sxs-lookup"><span data-stu-id="aa65e-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="aa65e-164">[**glIsEnabled**](glisenabled.md) avec argument GL \_ texture \_ GEN \_ Q</span><span class="sxs-lookup"><span data-stu-id="aa65e-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="aa65e-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa65e-165">Requirements</span></span>



| <span data-ttu-id="aa65e-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa65e-166">Requirement</span></span> | <span data-ttu-id="aa65e-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa65e-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa65e-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa65e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="aa65e-169">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa65e-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aa65e-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa65e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="aa65e-171">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa65e-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa65e-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa65e-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa65e-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa65e-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aa65e-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aa65e-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa65e-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa65e-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa65e-176">DLL</span><span class="sxs-lookup"><span data-stu-id="aa65e-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa65e-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa65e-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa65e-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa65e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa65e-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aa65e-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aa65e-180">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="aa65e-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aa65e-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="aa65e-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="aa65e-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="aa65e-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="aa65e-183">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="aa65e-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="aa65e-184">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="aa65e-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="aa65e-185">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="aa65e-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="aa65e-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="aa65e-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="aa65e-187">glTexParameter</span><span class="sxs-lookup"><span data-stu-id="aa65e-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="aa65e-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="aa65e-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="aa65e-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="aa65e-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





