---
title: fonction glMaterialiv (GL. h)
description: La fonction glMaterialiv spécifie les paramètres de matériau pour le modèle d’éclairage.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- glMaterialfv fonction OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95f12a5d34357a3436ffd6725ad2f1d56901e700
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384467"
---
# <a name="glmaterialiv-function"></a><span data-ttu-id="27312-104">glMaterialiv fonction)</span><span class="sxs-lookup"><span data-stu-id="27312-104">glMaterialiv function</span></span>

<span data-ttu-id="27312-105">La fonction **glMaterialiv** spécifie les paramètres de matériau pour le modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="27312-105">The **glMaterialiv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="27312-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27312-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="27312-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27312-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27312-108">*se*</span><span class="sxs-lookup"><span data-stu-id="27312-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="27312-109">Face ou faces mises à jour.</span><span class="sxs-lookup"><span data-stu-id="27312-109">The face or faces that are being updated.</span></span> <span data-ttu-id="27312-110">Il doit s’agir de l’une des valeurs suivantes : recto GL, arrière-plan GL, arrière- \_ \_ plan GL \_ et GL \_ .</span><span class="sxs-lookup"><span data-stu-id="27312-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="27312-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="27312-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="27312-112">Paramètre Material de la face ou des visages en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="27312-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="27312-113">Les paramètres qui peuvent être spécifiés à l’aide de [**glMaterialiv**](glmaterialfv.md)et leurs interprétations par l’équation d’éclairage sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="27312-113">The parameters that can be specified using [**glMaterialiv**](glmaterialfv.md), and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="27312-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="27312-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="27312-115">Signification</span><span class="sxs-lookup"><span data-stu-id="27312-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="27312-116"><dt>**ambiant du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="27312-117">Le paramètre params contient quatre valeurs entières qui spécifient la réflectivité RVBA ambiante du matériau.</span><span class="sxs-lookup"><span data-stu-id="27312-117">The params parameter contains four integer values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="27312-118">Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="27312-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="27312-119">Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="27312-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="27312-120">Les valeurs entières et à virgule flottante ne sont pas ancrées.</span><span class="sxs-lookup"><span data-stu-id="27312-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="27312-121">La réflectivité ambiante par défaut pour les matériaux frontaux et à face arrière est (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="27312-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="27312-122"><dt>**\_diffusion GL**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="27312-123">Le paramètre params contient quatre valeurs entières qui spécifient la réflexion RVBA diffuse du matériau.</span><span class="sxs-lookup"><span data-stu-id="27312-123">The params parameter contains four integer values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="27312-124">Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="27312-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="27312-125">Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="27312-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="27312-126">Les valeurs entières et à virgule flottante ne sont pas ancrées.</span><span class="sxs-lookup"><span data-stu-id="27312-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="27312-127">La réflectivité diffuse par défaut pour les matériaux avant et arrière est (0,8, 0,8, 0,8, 1,0).</span><span class="sxs-lookup"><span data-stu-id="27312-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="27312-128"><dt>**\_spéculaire GL**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="27312-129">Le paramètre params contient quatre valeurs entières qui spécifient la réflexion RVBA spéculaire du matériau.</span><span class="sxs-lookup"><span data-stu-id="27312-129">The params parameter contains four integer values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="27312-130">Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="27312-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="27312-131">Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="27312-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="27312-132">Les valeurs entières et à virgule flottante ne sont pas ancrées.</span><span class="sxs-lookup"><span data-stu-id="27312-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="27312-133">La réflectivité spéculaire par défaut pour les matériaux avant et arrière est (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="27312-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="27312-134"><dt>**\_émission GL**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="27312-135">Le paramètre params contient quatre valeurs entières qui spécifient l’intensité de la lumière émise par le RVBA du matériau.</span><span class="sxs-lookup"><span data-stu-id="27312-135">The params parameter contains four integer values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="27312-136">Les valeurs entières sont mappées de façon linéaire de telle sorte que la valeur représentable la plus positive corresponde à 1,0, et la valeur représentable la plus négative correspond à-1,0.</span><span class="sxs-lookup"><span data-stu-id="27312-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="27312-137">Les valeurs à virgule flottante sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="27312-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="27312-138">Les valeurs entières et à virgule flottante ne sont pas ancrées.</span><span class="sxs-lookup"><span data-stu-id="27312-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="27312-139">L’intensité d’émission par défaut pour les matériaux frontaux et à face arrière est (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="27312-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="27312-140"><dt>**\_éclat GL**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="27312-141">Le paramètre *param* est un entier unique qui spécifie l’exposant spéculaire RVBA du matériau.</span><span class="sxs-lookup"><span data-stu-id="27312-141">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="27312-142">Les valeurs entières sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="27312-142">Integer values are mapped directly.</span></span> <span data-ttu-id="27312-143">Seules les valeurs de la plage \[ 0, 128 \] sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="27312-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="27312-144">L’exposant spéculaire par défaut pour les matériaux frontaux et à face arrière est 0.</span><span class="sxs-lookup"><span data-stu-id="27312-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="27312-145"><dt>**\_ambiants \_ et \_ DIFFUSes du GL**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="27312-146">Équivalent à l’appel de [**glMaterial**](glmaterial-functions.md) à deux reprises avec les mêmes valeurs de paramètres, une fois avec le GL \_ ambiant et une fois avec la \_ diffusion GL.</span><span class="sxs-lookup"><span data-stu-id="27312-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="27312-147"><dt>**\_index de couleurs GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="27312-148">Le paramètre params contient trois valeurs entières spécifiant les index de couleurs pour l’éclairage ambiant, diffus et spéculaire.</span><span class="sxs-lookup"><span data-stu-id="27312-148">The params parameter contains three integer values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="27312-149">Ces trois valeurs, et la \_ brillance GL, sont les seules valeurs de matériau utilisées par l’équation d’éclairage du mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="27312-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="27312-150">Reportez-vous à [**glLightModel**](gllightmodel-functions.md) pour une discussion sur l’éclairage d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="27312-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="27312-151">*params*</span><span class="sxs-lookup"><span data-stu-id="27312-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="27312-152">Valeur à laquelle définir la brillance du GL de paramètres \_ .</span><span class="sxs-lookup"><span data-stu-id="27312-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27312-153">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="27312-153">Return value</span></span>

<span data-ttu-id="27312-154">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="27312-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27312-155">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="27312-155">Error codes</span></span>

<span data-ttu-id="27312-156">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="27312-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="27312-157">Nom</span><span class="sxs-lookup"><span data-stu-id="27312-157">Name</span></span>                                                                                              | <span data-ttu-id="27312-158">Signification</span><span class="sxs-lookup"><span data-stu-id="27312-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27312-159"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="27312-160">L’une des *visages* ou l' *pname* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="27312-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="27312-161"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27312-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="27312-162">Un exposant spéculaire en dehors de la plage comprise entre \[ 0 et 128 \] a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="27312-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="27312-163">Notes</span><span class="sxs-lookup"><span data-stu-id="27312-163">Remarks</span></span>

<span data-ttu-id="27312-164">La fonction [**glMaterialiv**](glmaterialf.md) affecte des valeurs aux paramètres de la documentation.</span><span class="sxs-lookup"><span data-stu-id="27312-164">The [**glMaterialiv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="27312-165">Il existe deux ensembles de paramètres de matériau correspondants.</span><span class="sxs-lookup"><span data-stu-id="27312-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="27312-166">L’un, le jeu de face *avant* , est utilisé pour ombrer des points, des lignes, des bitmaps et tous les polygones (lorsque l’éclairage à deux côtés est désactivé), ou simplement des polygones frontaux (lorsque l’éclairage à deux côtés est activé).</span><span class="sxs-lookup"><span data-stu-id="27312-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="27312-167">L’autre jeu, *arrière-plan*, est utilisé pour ombrer les polygones de l’arrière-plan uniquement lorsque l’éclairage à deux côtés est activé.</span><span class="sxs-lookup"><span data-stu-id="27312-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="27312-168">Reportez-vous à [**glLightModel**](gllightmodel-functions.md) pour plus d’informations sur les calculs d’éclairage unilatéraux et à deux côtés.</span><span class="sxs-lookup"><span data-stu-id="27312-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="27312-169">La fonction [**glMaterialiv**](glmaterialf.md) accepte trois arguments.</span><span class="sxs-lookup"><span data-stu-id="27312-169">The [**glMaterialiv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="27312-170">La première, *face*, spécifie si les documents \_ frontaux, les \_ documents de retour GL, ou \_ les \_ documents frontaux et Back GL \_ sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="27312-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="27312-171">Le deuxième, *pname*, spécifie quels paramètres dans un ou les deux jeux seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="27312-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="27312-172">Le troisième, *param*, spécifie la valeur qui sera assignée au paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="27312-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="27312-173">Les paramètres de matériau sont utilisés dans l’équation d’éclairage qui est éventuellement appliquée à chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="27312-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="27312-174">L’équation est présentée dans [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="27312-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="27312-175">Les paramètres de matériau peuvent être mis à jour à tout moment.</span><span class="sxs-lookup"><span data-stu-id="27312-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="27312-176">En particulier, [**glMaterialiv**](glmaterialf.md) peut être appelé entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="27312-176">In particular, [**glMaterialiv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="27312-177">Toutefois, si un seul paramètre de matériau doit être modifié par vertex, [**glColorMaterial**](glcolormaterial.md) est préférable à **glMaterialiv**.</span><span class="sxs-lookup"><span data-stu-id="27312-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialiv**.</span></span>

<span data-ttu-id="27312-178">La fonction suivante récupère des informations relatives à [**glMaterialiv**](glmaterialf.md):</span><span class="sxs-lookup"><span data-stu-id="27312-178">The following function retrieves information related to [**glMaterialiv**](glmaterialf.md):</span></span>

[<span data-ttu-id="27312-179">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="27312-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="27312-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27312-180">Requirements</span></span>



| <span data-ttu-id="27312-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27312-181">Requirement</span></span> | <span data-ttu-id="27312-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="27312-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27312-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27312-183">Minimum supported client</span></span><br/> | <span data-ttu-id="27312-184">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27312-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="27312-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27312-185">Minimum supported server</span></span><br/> | <span data-ttu-id="27312-186">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27312-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="27312-187">En-tête</span><span class="sxs-lookup"><span data-stu-id="27312-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="27312-188"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="27312-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="27312-189">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="27312-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="27312-190"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27312-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="27312-191">DLL</span><span class="sxs-lookup"><span data-stu-id="27312-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27312-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27312-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27312-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27312-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27312-194">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="27312-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="27312-195">**glLight**</span><span class="sxs-lookup"><span data-stu-id="27312-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="27312-196">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="27312-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





