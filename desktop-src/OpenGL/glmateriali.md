---
title: fonction glMateriali (GL. h)
description: La fonction TheglMateriali spécifie les paramètres de matériau pour le modèle d’éclairage.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- glMateriali fonction OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512557"
---
# <a name="glmateriali-function"></a><span data-ttu-id="c0b64-104">glMateriali fonction)</span><span class="sxs-lookup"><span data-stu-id="c0b64-104">glMateriali function</span></span>

<span data-ttu-id="c0b64-105">La fonction **glMateriali** spécifie les paramètres de matériau pour le modèle d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="c0b64-105">The **glMateriali** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b64-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0b64-106">Syntax</span></span>


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="c0b64-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0b64-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b64-108">*se*</span><span class="sxs-lookup"><span data-stu-id="c0b64-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b64-109">Face ou faces mises à jour.</span><span class="sxs-lookup"><span data-stu-id="c0b64-109">The face or faces that are being updated.</span></span> <span data-ttu-id="c0b64-110">Il doit s’agir de l’une des valeurs suivantes : recto GL, arrière-plan GL, arrière- \_ \_ plan GL \_ et GL \_ .</span><span class="sxs-lookup"><span data-stu-id="c0b64-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="c0b64-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="c0b64-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b64-112">Paramètre de matériau à valeur unique de la face ou des visages mis à jour.</span><span class="sxs-lookup"><span data-stu-id="c0b64-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="c0b64-113">Doit être une \_ éclat GL.</span><span class="sxs-lookup"><span data-stu-id="c0b64-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="c0b64-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0b64-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="c0b64-115">Signification</span><span class="sxs-lookup"><span data-stu-id="c0b64-115">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="c0b64-116"><dt>**\_éclat GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b64-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="c0b64-117">Le paramètre *param* est un entier unique qui spécifie l’exposant spéculaire RVBA du matériau.</span><span class="sxs-lookup"><span data-stu-id="c0b64-117">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="c0b64-118">Les valeurs entières sont mappées directement.</span><span class="sxs-lookup"><span data-stu-id="c0b64-118">Integer values are mapped directly.</span></span> <span data-ttu-id="c0b64-119">Seules les valeurs de la plage \[ 0, 128 \] sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="c0b64-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="c0b64-120">L’exposant spéculaire par défaut pour les matériaux frontaux et à face arrière est 0.</span><span class="sxs-lookup"><span data-stu-id="c0b64-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c0b64-121">*param*</span><span class="sxs-lookup"><span data-stu-id="c0b64-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b64-122">Valeur à laquelle définir la brillance du GL de paramètres \_ .</span><span class="sxs-lookup"><span data-stu-id="c0b64-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b64-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c0b64-123">Return value</span></span>

<span data-ttu-id="c0b64-124">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c0b64-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0b64-125">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c0b64-125">Error codes</span></span>

<span data-ttu-id="c0b64-126">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b64-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c0b64-127">Nom</span><span class="sxs-lookup"><span data-stu-id="c0b64-127">Name</span></span>                                                                                              | <span data-ttu-id="c0b64-128">Signification</span><span class="sxs-lookup"><span data-stu-id="c0b64-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0b64-129"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b64-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="c0b64-130">L’une des *visages* ou l' *pname* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="c0b64-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="c0b64-131"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b64-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="c0b64-132">Un exposant spéculaire en dehors de la plage comprise entre \[ 0 et 128 \] a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0b64-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c0b64-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c0b64-133">Remarks</span></span>

<span data-ttu-id="c0b64-134">La fonction **glMateriali** affecte des valeurs aux paramètres de la documentation.</span><span class="sxs-lookup"><span data-stu-id="c0b64-134">The **glMateriali** function assigns values to material parameters.</span></span> <span data-ttu-id="c0b64-135">Il existe deux ensembles de paramètres de matériau correspondants.</span><span class="sxs-lookup"><span data-stu-id="c0b64-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="c0b64-136">L’un, le jeu de face *avant* , est utilisé pour ombrer des points, des lignes, des bitmaps et tous les polygones (lorsque l’éclairage à deux côtés est désactivé), ou simplement des polygones frontaux (lorsque l’éclairage à deux côtés est activé).</span><span class="sxs-lookup"><span data-stu-id="c0b64-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="c0b64-137">L’autre jeu, *arrière-plan*, est utilisé pour ombrer les polygones de l’arrière-plan uniquement lorsque l’éclairage à deux côtés est activé.</span><span class="sxs-lookup"><span data-stu-id="c0b64-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="c0b64-138">Reportez-vous à [**glLightModel**](gllightmodel-functions.md) pour plus d’informations sur les calculs d’éclairage unilatéraux et à deux côtés.</span><span class="sxs-lookup"><span data-stu-id="c0b64-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="c0b64-139">La fonction **glMateriali** accepte trois arguments.</span><span class="sxs-lookup"><span data-stu-id="c0b64-139">The **glMateriali** function takes three arguments.</span></span> <span data-ttu-id="c0b64-140">La première, *face*, spécifie si les documents \_ frontaux, les \_ documents de retour GL, ou \_ les \_ documents frontaux et Back GL \_ sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="c0b64-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="c0b64-141">Le deuxième, *pname*, spécifie quels paramètres dans un ou les deux jeux seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="c0b64-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="c0b64-142">Le troisième, *param*, spécifie la valeur qui sera assignée au paramètre spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0b64-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="c0b64-143">Les paramètres de matériau sont utilisés dans l’équation d’éclairage qui est éventuellement appliquée à chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="c0b64-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="c0b64-144">L’équation est présentée dans [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c0b64-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="c0b64-145">Les paramètres de matériau peuvent être mis à jour à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c0b64-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="c0b64-146">En particulier, **glMateriali** peut être appelé entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c0b64-146">In particular, **glMateriali** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="c0b64-147">Toutefois, si un seul paramètre de matériau doit être modifié par vertex, [**glColorMaterial**](glcolormaterial.md) est préférable à **glMateriali**.</span><span class="sxs-lookup"><span data-stu-id="c0b64-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMateriali**.</span></span>

<span data-ttu-id="c0b64-148">La fonction suivante récupère des informations relatives à **glMateriali**:</span><span class="sxs-lookup"><span data-stu-id="c0b64-148">The following function retrieves information related to **glMateriali**:</span></span>

[<span data-ttu-id="c0b64-149">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="c0b64-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="c0b64-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b64-150">Requirements</span></span>



| <span data-ttu-id="c0b64-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0b64-151">Requirement</span></span> | <span data-ttu-id="c0b64-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0b64-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b64-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0b64-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b64-154">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0b64-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0b64-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0b64-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b64-156">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0b64-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0b64-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0b64-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b64-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b64-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c0b64-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0b64-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0b64-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b64-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0b64-161">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b64-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b64-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b64-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b64-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0b64-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b64-164">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="c0b64-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="c0b64-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="c0b64-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="c0b64-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="c0b64-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





