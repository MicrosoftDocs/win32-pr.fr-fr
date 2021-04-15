---
title: fonction glLightModelfv (GL. h)
description: La fonction glLightModelfv définit les paramètres du modèle d’éclairage.
ms.assetid: a62bcf3b-1769-48a3-8121-8f2b41266183
keywords:
- glLightModelfv fonction OpenGL
topic_type:
- apiref
api_name:
- glLightModelfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c20aea0851c542fd0d2c81de26da21a692fdb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508309"
---
# <a name="gllightmodelfv-function"></a><span data-ttu-id="fd03b-104">glLightModelfv fonction)</span><span class="sxs-lookup"><span data-stu-id="fd03b-104">glLightModelfv function</span></span>

<span data-ttu-id="fd03b-105">La fonction [**glLightModelfv**](gllightfv.md) définit les paramètres du modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="fd03b-105">The [**glLightModelfv**](gllightfv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd03b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd03b-106">Syntax</span></span>


```C++
void WINAPI glLightModelfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="fd03b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd03b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd03b-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="fd03b-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fd03b-109">Paramètre de modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="fd03b-109">A lighting model parameter.</span></span> <span data-ttu-id="fd03b-110">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="fd03b-110">The following values are accepted.</span></span>



| <span data-ttu-id="fd03b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd03b-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="fd03b-112">Signification</span><span class="sxs-lookup"><span data-stu-id="fd03b-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="fd03b-113"><dt>**ambiant (GL \_ Light \_ Model) \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="fd03b-114">Le paramètre *params* contient quatre valeurs à virgule flottante qui spécifient l’intensité RVBA ambiante de l’ensemble de la scène.</span><span class="sxs-lookup"><span data-stu-id="fd03b-114">The *params* parameter contains four floating-point values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="fd03b-115">Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="fd03b-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="fd03b-116">Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="fd03b-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="fd03b-117">Les valeurs entières et à virgule flottante ne sont pas ancrées.</span><span class="sxs-lookup"><span data-stu-id="fd03b-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="fd03b-118">L’intensité de la scène ambiante par défaut est (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="fd03b-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="fd03b-119"><dt>**\_ \_ visionneuse locale du modèle de lumière \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="fd03b-120">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie le mode de calcul des angles de réflexion spéculaire.</span><span class="sxs-lookup"><span data-stu-id="fd03b-120">The *params* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="fd03b-121">Si *param* est égal à 0 (ou 0,0), les angles de réflexion spéculaire prennent le sens de la vue comme étant parallèle et dans la direction de l’axe-*z* , indépendamment de l’emplacement du vertex en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="fd03b-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="fd03b-122">Sinon, les réflexions spéculaires sont calculées à partir de l’origine du système de coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="fd03b-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="fd03b-123">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="fd03b-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="fd03b-124"><dt>**\_ \_ côté 2 du modèle GL clair \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="fd03b-125">Le paramètre *params* est une valeur à virgule flottante unique qui spécifie si les polygones doivent effectuer des calculs d’éclairage à un ou deux côtés.</span><span class="sxs-lookup"><span data-stu-id="fd03b-125">The *params* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="fd03b-126">Elle n’a aucun effet sur les calculs d’éclairage pour les points, les lignes ou les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="fd03b-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="fd03b-127">Si *param* est égal à 0 (ou 0,0), un éclairage à un seul côté est spécifié et seuls les paramètres de matière première sont utilisés dans l’équation d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="fd03b-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="fd03b-128">Dans le cas contraire, l’éclairage à deux côtés est spécifié.</span><span class="sxs-lookup"><span data-stu-id="fd03b-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="fd03b-129">Dans ce cas, les sommets des polygones de l’arrière-plan sont allumés à l’aide des paramètres de la matière arrière et les normales sont inversées avant l’évaluation de l’équation d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="fd03b-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="fd03b-130">Les sommets des polygones frontaux sont toujours éclaircis à l’aide des paramètres du matériau avant, sans aucune modification de leurs normales.</span><span class="sxs-lookup"><span data-stu-id="fd03b-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="fd03b-131">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="fd03b-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd03b-132">*params*</span><span class="sxs-lookup"><span data-stu-id="fd03b-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fd03b-133">Pointeur vers la ou les valeurs dans lesquelles les *paramètres* seront définis.</span><span class="sxs-lookup"><span data-stu-id="fd03b-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd03b-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd03b-134">Return value</span></span>

<span data-ttu-id="fd03b-135">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fd03b-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fd03b-136">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fd03b-136">Error codes</span></span>

<span data-ttu-id="fd03b-137">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fd03b-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fd03b-138">Nom</span><span class="sxs-lookup"><span data-stu-id="fd03b-138">Name</span></span>                                                                                                  | <span data-ttu-id="fd03b-139">Signification</span><span class="sxs-lookup"><span data-stu-id="fd03b-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd03b-140"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fd03b-141">*pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="fd03b-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="fd03b-142"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fd03b-143">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fd03b-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fd03b-144">Notes</span><span class="sxs-lookup"><span data-stu-id="fd03b-144">Remarks</span></span>

<span data-ttu-id="fd03b-145">La fonction **glLightModelfv** définit le paramètre de modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="fd03b-145">The **glLightModelfv** function sets lighting model parameter.</span></span> <span data-ttu-id="fd03b-146">Le paramètre *pname* nomme un paramètre et *param* donne la nouvelle valeur. la ou les valeurs des paramètres de la source lumineuse individuelle.</span><span class="sxs-lookup"><span data-stu-id="fd03b-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="fd03b-147">En mode RVBA, la couleur éclaircie d’un vertex est égale à la somme de l’intensité de l’émission du matériau, du produit de la réflectivité ambiante du matériau et de l’intensité ambiante du modèle d’éclairage de la scène, ainsi que de la contribution de chaque source de lumière activée.</span><span class="sxs-lookup"><span data-stu-id="fd03b-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="fd03b-148">Chaque source de lumière contribue à la somme de trois termes : ambiant, diffuse et spéculaire.</span><span class="sxs-lookup"><span data-stu-id="fd03b-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="fd03b-149">La contribution source de la lumière ambiante est le produit de la réflexion ambiante du matériau et de l’intensité ambiante de la lumière.</span><span class="sxs-lookup"><span data-stu-id="fd03b-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="fd03b-150">La contribution à la source de lumière diffuse est le produit de la réflexion diffuse de matériau, l’intensité diffuse de la lumière et le produit scalaire du vertex normal avec le vecteur normalisé du vertex à la source de lumière.</span><span class="sxs-lookup"><span data-stu-id="fd03b-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="fd03b-151">La contribution à la source de lumière spéculaire est le produit de la réflexion spéculaire, de l’intensité spéculaire de la lumière et du produit scalaire des vecteurs de vertex à oculaire normalisés et de sommets à la lumière, élevé à la puissance de la brillance du matériau.</span><span class="sxs-lookup"><span data-stu-id="fd03b-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="fd03b-152">Les trois contributions à la source lumineuse sont atténuées de manière égale en fonction de la distance entre le sommet et la source de lumière, et de la direction de la source de lumière, de la répartition de l’exposant et de l’angle de coupure.</span><span class="sxs-lookup"><span data-stu-id="fd03b-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="fd03b-153">Tous les produits scalaires sont remplacés par zéro s’ils correspondent à une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="fd03b-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="fd03b-154">Le composant alpha de la couleur éclaircie résultante est défini sur la valeur alpha de la réflexion de diffusion matérielle.</span><span class="sxs-lookup"><span data-stu-id="fd03b-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="fd03b-155">En mode d’index des couleurs, la valeur de l’index clair d’un vertex est comprise entre l’ambiant et les valeurs spéculaires transmises à [**glMaterial**](glmaterial-functions.md) à l’aide d' \_ index de couleur GL \_ .</span><span class="sxs-lookup"><span data-stu-id="fd03b-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="fd03b-156">Coefficients diffus et spéculaire, calculés avec une pondération (. 30,. 59, .11) des couleurs de la lumière, la brillance du matériau et les mêmes équations de réflexion et d’atténuation que dans le cas RVBA, déterminez le degré au-dessus de l’index résultant.</span><span class="sxs-lookup"><span data-stu-id="fd03b-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="fd03b-157">Les fonctions suivantes récupèrent les informations relatives à la fonction **glLightModelfv** :</span><span class="sxs-lookup"><span data-stu-id="fd03b-157">The following functions retrieve information related to the **glLightModelfv** function:</span></span>

<span data-ttu-id="fd03b-158">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ \_ visionneuse locale glGet avec argument GL Light Model \_</span><span class="sxs-lookup"><span data-stu-id="fd03b-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="fd03b-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Light \_ Model \_ deux \_ côtés</span><span class="sxs-lookup"><span data-stu-id="fd03b-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="fd03b-160">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Lighting</span><span class="sxs-lookup"><span data-stu-id="fd03b-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="fd03b-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd03b-161">Requirements</span></span>



| <span data-ttu-id="fd03b-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd03b-162">Requirement</span></span> | <span data-ttu-id="fd03b-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd03b-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd03b-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd03b-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fd03b-165">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd03b-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fd03b-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd03b-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fd03b-167">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd03b-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd03b-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd03b-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd03b-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fd03b-170">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd03b-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd03b-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd03b-172">DLL</span><span class="sxs-lookup"><span data-stu-id="fd03b-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd03b-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd03b-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd03b-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd03b-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd03b-175">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fd03b-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fd03b-176">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fd03b-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fd03b-177">**glLight**</span><span class="sxs-lookup"><span data-stu-id="fd03b-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="fd03b-178">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="fd03b-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





