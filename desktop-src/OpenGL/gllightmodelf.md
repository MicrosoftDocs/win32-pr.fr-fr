---
title: fonction glLightModelf (GL. h)
description: La fonction glLightModelf définit les paramètres du modèle d’éclairage.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- glLightModelf fonction OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032382"
---
# <a name="gllightmodelf-function"></a><span data-ttu-id="431cc-104">glLightModelf fonction)</span><span class="sxs-lookup"><span data-stu-id="431cc-104">glLightModelf function</span></span>

<span data-ttu-id="431cc-105">La fonction **glLightModelf** définit les paramètres du modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="431cc-105">The **glLightModelf** function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="431cc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="431cc-106">Syntax</span></span>


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a><span data-ttu-id="431cc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="431cc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="431cc-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="431cc-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="431cc-109">Paramètre de modèle d’éclairage à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="431cc-109">A single-valued lighting model parameter.</span></span> <span data-ttu-id="431cc-110">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="431cc-110">The following values are accepted.</span></span>



| <span data-ttu-id="431cc-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="431cc-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="431cc-112">Signification</span><span class="sxs-lookup"><span data-stu-id="431cc-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="431cc-113"><dt>**\_ \_ visionneuse locale du modèle de lumière \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-113"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="431cc-114">Le paramètre *param* est une valeur à virgule flottante unique qui spécifie le mode de calcul des angles de réflexion spéculaire.</span><span class="sxs-lookup"><span data-stu-id="431cc-114">The *param* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="431cc-115">Si *param* est égal à 0 (ou 0,0), les angles de réflexion spéculaire prennent le sens de la vue comme étant parallèle et dans la direction de l’axe-*z* , indépendamment de l’emplacement du vertex en coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="431cc-115">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="431cc-116">Sinon, les réflexions spéculaires sont calculées à partir de l’origine du système de coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="431cc-116">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="431cc-117">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="431cc-117">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="431cc-118"><dt>**\_ \_ côté 2 du modèle GL clair \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-118"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="431cc-119">Le paramètre *param* est une valeur à virgule flottante unique qui spécifie si les polygones doivent effectuer des calculs d’éclairage à un ou deux côtés.</span><span class="sxs-lookup"><span data-stu-id="431cc-119">The *param* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="431cc-120">Elle n’a aucun effet sur les calculs d’éclairage pour les points, les lignes ou les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="431cc-120">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="431cc-121">Si *param* est égal à 0 (ou 0,0), un éclairage à un seul côté est spécifié et seuls les paramètres de matière première sont utilisés dans l’équation d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="431cc-121">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="431cc-122">Dans le cas contraire, l’éclairage à deux côtés est spécifié.</span><span class="sxs-lookup"><span data-stu-id="431cc-122">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="431cc-123">Dans ce cas, les sommets des polygones de l’arrière-plan sont allumés à l’aide des paramètres de la matière arrière et les normales sont inversées avant l’évaluation de l’équation d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="431cc-123">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="431cc-124">Les sommets des polygones frontaux sont toujours éclaircis à l’aide des paramètres du matériau avant, sans aucune modification de leurs normales.</span><span class="sxs-lookup"><span data-stu-id="431cc-124">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="431cc-125">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="431cc-125">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="431cc-126">*param*</span><span class="sxs-lookup"><span data-stu-id="431cc-126">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="431cc-127">Valeur dans laquelle *param* sera défini.</span><span class="sxs-lookup"><span data-stu-id="431cc-127">The value to which *param* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="431cc-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="431cc-128">Return value</span></span>

<span data-ttu-id="431cc-129">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="431cc-129">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="431cc-130">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="431cc-130">Error codes</span></span>

<span data-ttu-id="431cc-131">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="431cc-131">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="431cc-132">Nom</span><span class="sxs-lookup"><span data-stu-id="431cc-132">Name</span></span>                                                                                                  | <span data-ttu-id="431cc-133">Signification</span><span class="sxs-lookup"><span data-stu-id="431cc-133">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="431cc-134"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-134"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="431cc-135">*pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="431cc-135">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="431cc-136"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="431cc-137">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="431cc-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="431cc-138">Notes</span><span class="sxs-lookup"><span data-stu-id="431cc-138">Remarks</span></span>

<span data-ttu-id="431cc-139">La fonction **glLightModelf** définit le paramètre de modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="431cc-139">The **glLightModelf** function sets lighting model parameter.</span></span> <span data-ttu-id="431cc-140">Le paramètre *pname* nomme un paramètre et *param* donne la nouvelle valeur. la ou les valeurs des paramètres de la source lumineuse individuelle.</span><span class="sxs-lookup"><span data-stu-id="431cc-140">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="431cc-141">En mode RVBA, la couleur éclaircie d’un vertex est égale à la somme de l’intensité de l’émission du matériau, du produit de la réflectivité ambiante du matériau et de l’intensité ambiante du modèle d’éclairage de la scène, ainsi que de la contribution de chaque source de lumière activée.</span><span class="sxs-lookup"><span data-stu-id="431cc-141">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="431cc-142">Chaque source de lumière contribue à la somme de trois termes : ambiant, diffuse et spéculaire.</span><span class="sxs-lookup"><span data-stu-id="431cc-142">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="431cc-143">La contribution source de la lumière ambiante est le produit de la réflexion ambiante du matériau et de l’intensité ambiante de la lumière.</span><span class="sxs-lookup"><span data-stu-id="431cc-143">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="431cc-144">La contribution à la source de lumière diffuse est le produit de la réflexion diffuse de matériau, l’intensité diffuse de la lumière et le produit scalaire du vertex normal avec le vecteur normalisé du vertex à la source de lumière.</span><span class="sxs-lookup"><span data-stu-id="431cc-144">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="431cc-145">La contribution à la source de lumière spéculaire est le produit de la réflexion spéculaire, de l’intensité spéculaire de la lumière et du produit scalaire des vecteurs de vertex à oculaire normalisés et de sommets à la lumière, élevé à la puissance de la brillance du matériau.</span><span class="sxs-lookup"><span data-stu-id="431cc-145">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="431cc-146">Les trois contributions à la source lumineuse sont atténuées de manière égale en fonction de la distance entre le sommet et la source de lumière, et de la direction de la source de lumière, de la répartition de l’exposant et de l’angle de coupure.</span><span class="sxs-lookup"><span data-stu-id="431cc-146">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="431cc-147">Tous les produits scalaires sont remplacés par zéro s’ils correspondent à une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="431cc-147">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="431cc-148">Le composant alpha de la couleur éclaircie résultante est défini sur la valeur alpha de la réflexion de diffusion matérielle.</span><span class="sxs-lookup"><span data-stu-id="431cc-148">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="431cc-149">En mode d’index des couleurs, la valeur de l’index clair d’un vertex est comprise entre l’ambiant et les valeurs spéculaires transmises à [**glMaterial**](glmaterial-functions.md) à l’aide d' \_ index de couleur GL \_ .</span><span class="sxs-lookup"><span data-stu-id="431cc-149">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="431cc-150">Coefficients diffus et spéculaire, calculés avec une pondération (. 30,. 59, .11) des couleurs de la lumière, la brillance du matériau et les mêmes équations de réflexion et d’atténuation que dans le cas RVBA, déterminez le degré au-dessus de l’index résultant.</span><span class="sxs-lookup"><span data-stu-id="431cc-150">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="431cc-151">Les fonctions suivantes récupèrent les informations relatives à la fonction **glLightModelf** :</span><span class="sxs-lookup"><span data-stu-id="431cc-151">The following functions retrieve information related to the **glLightModelf** function:</span></span>

<span data-ttu-id="431cc-152">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ \_ visionneuse locale glGet avec argument GL Light Model \_</span><span class="sxs-lookup"><span data-stu-id="431cc-152">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="431cc-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Light \_ Model \_ deux \_ côtés</span><span class="sxs-lookup"><span data-stu-id="431cc-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="431cc-154">[**glIsEnabled**](glisenabled.md) avec argument GL \_ Lighting</span><span class="sxs-lookup"><span data-stu-id="431cc-154">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="431cc-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="431cc-155">Requirements</span></span>



| <span data-ttu-id="431cc-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="431cc-156">Requirement</span></span> | <span data-ttu-id="431cc-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="431cc-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="431cc-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="431cc-158">Minimum supported client</span></span><br/> | <span data-ttu-id="431cc-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="431cc-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="431cc-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="431cc-160">Minimum supported server</span></span><br/> | <span data-ttu-id="431cc-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="431cc-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="431cc-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="431cc-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="431cc-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="431cc-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="431cc-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="431cc-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="431cc-166">DLL</span><span class="sxs-lookup"><span data-stu-id="431cc-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431cc-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431cc-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431cc-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="431cc-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431cc-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="431cc-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="431cc-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="431cc-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="431cc-171">**glLight**</span><span class="sxs-lookup"><span data-stu-id="431cc-171">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="431cc-172">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="431cc-172">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





