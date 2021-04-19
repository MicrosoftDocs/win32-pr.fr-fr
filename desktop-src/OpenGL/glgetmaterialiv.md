---
title: fonction glGetMaterialiv (GL. h)
description: Les fonctions glGetMaterialfv et glGetMaterialiv retournent des paramètres Material. | fonction glGetMaterialiv (GL. h)
ms.assetid: 459cbe8a-a51a-496e-bdd1-89b8cf486a46
keywords:
- glGetMaterialiv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f09e1a315d4929ebb92f3b0e59ed6762a7fe4b35
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106525830"
---
# <a name="glgetmaterialiv-function"></a><span data-ttu-id="c1aa9-105">glGetMaterialiv fonction)</span><span class="sxs-lookup"><span data-stu-id="c1aa9-105">glGetMaterialiv function</span></span>

<span data-ttu-id="c1aa9-106">Les fonctions [**glGetMaterialfv**](glgetmaterialfv.md) et **glGetMaterialiv** retournent des paramètres Material.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-106">The [**glGetMaterialfv**](glgetmaterialfv.md) and **glGetMaterialiv** functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1aa9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1aa9-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialiv(
   GLenum face,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="c1aa9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1aa9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1aa9-109">*se*</span><span class="sxs-lookup"><span data-stu-id="c1aa9-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="c1aa9-110">Spécifie les deux documents en cours d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="c1aa9-111">\_Les arrière-plan \_ du GL ou du GL sont acceptés, représentant respectivement les matériaux avant et arrière.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="c1aa9-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="c1aa9-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c1aa9-113">Paramètre Material à retourner.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-113">The material parameter to return.</span></span> <span data-ttu-id="c1aa9-114">Les valeurs suivantes sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-114">The following values are accepted.</span></span>



| <span data-ttu-id="c1aa9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1aa9-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="c1aa9-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c1aa9-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="c1aa9-117"><dt>**ambiant du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="c1aa9-118">Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la réflexion ambiante du matériau.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="c1aa9-119">Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="c1aa9-120">Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="c1aa9-121"><dt>**\_diffusion GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="c1aa9-122">Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la réflexion diffuse du matériau.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="c1aa9-123">Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="c1aa9-124">Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="c1aa9-125"><dt>**\_spéculaire GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="c1aa9-126">Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant la réflectivité spéculaire du matériau.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="c1aa9-127">Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="c1aa9-128">Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="c1aa9-129"><dt>**\_émission GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="c1aa9-130">Le paramètre *params* retourne quatre valeurs entières ou à virgule flottante représentant l’intensité lumineuse émise du matériau.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="c1aa9-131">Les valeurs entières, quand elles sont demandées, sont mappées de façon linéaire à partir de la représentation interne à virgule flottante, de sorte que 1,0 correspond à la valeur entière représentable la plus positive, et-1,0 correspond à la valeur entière représentable la plus négative.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="c1aa9-132">Si la valeur interne est en dehors de la plage \[ -1, 1 \] , la valeur de retour de l’entier correspondant n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="c1aa9-133"><dt>**\_éclat GL**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="c1aa9-134">Le paramètre *params* retourne un entier ou une valeur à virgule flottante représentant l’exposant spéculaire du matériau.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="c1aa9-135">Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant la valeur à virgule flottante interne à la valeur entière la plus proche.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="c1aa9-136"><dt>**\_index de couleurs GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="c1aa9-137">Le paramètre *params* retourne trois valeurs entières ou à virgule flottante représentant les index ambiant, diffus et spéculaire du matériau.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="c1aa9-138">Utilisez ces index uniquement pour l’éclairage d’index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="c1aa9-139">(Les autres paramètres sont utilisés uniquement pour l’éclairage RVBA.) Les valeurs entières, quand elles sont demandées, sont calculées en arrondissant les valeurs à virgule flottante internes aux valeurs entières les plus proches.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="c1aa9-140">*params*</span><span class="sxs-lookup"><span data-stu-id="c1aa9-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="c1aa9-141">Retourne les données demandées.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1aa9-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c1aa9-142">Return value</span></span>

<span data-ttu-id="c1aa9-143">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c1aa9-144">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c1aa9-144">Error codes</span></span>

<span data-ttu-id="c1aa9-145">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c1aa9-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c1aa9-146">Nom</span><span class="sxs-lookup"><span data-stu-id="c1aa9-146">Name</span></span>                                                                                                  | <span data-ttu-id="c1aa9-147">Signification</span><span class="sxs-lookup"><span data-stu-id="c1aa9-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1aa9-148"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c1aa9-149">la *cible* ou la *requête* n’était pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="c1aa9-150"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c1aa9-151">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c1aa9-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c1aa9-152">Notes</span><span class="sxs-lookup"><span data-stu-id="c1aa9-152">Remarks</span></span>

<span data-ttu-id="c1aa9-153">La fonction **glGetMaterial** *retourne dans les paramètres la* valeur ou les valeurs du paramètre *pname* de la *facette* matérielle.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="c1aa9-154">Si une erreur est générée, aucune modification n’est apportée au contenu des *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="c1aa9-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1aa9-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1aa9-155">Requirements</span></span>



| <span data-ttu-id="c1aa9-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1aa9-156">Requirement</span></span> | <span data-ttu-id="c1aa9-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1aa9-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1aa9-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1aa9-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c1aa9-159">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1aa9-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c1aa9-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1aa9-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c1aa9-161">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1aa9-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1aa9-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1aa9-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1aa9-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c1aa9-164">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1aa9-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1aa9-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1aa9-166">DLL</span><span class="sxs-lookup"><span data-stu-id="c1aa9-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1aa9-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1aa9-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1aa9-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1aa9-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1aa9-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c1aa9-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c1aa9-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c1aa9-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c1aa9-171">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c1aa9-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





