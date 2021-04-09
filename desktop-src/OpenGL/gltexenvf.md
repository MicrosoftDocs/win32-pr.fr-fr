---
title: fonction glTexEnvf (GL. h)
description: La fonction glTexEnvf définit un paramètre d’environnement de texture.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- glTexEnvf fonction OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741125"
---
# <a name="gltexenvf-function"></a><span data-ttu-id="92dcd-104">glTexEnvf fonction)</span><span class="sxs-lookup"><span data-stu-id="92dcd-104">glTexEnvf function</span></span>

<span data-ttu-id="92dcd-105">La fonction **glTexEnvf** définit un paramètre d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="92dcd-105">The **glTexEnvf** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="92dcd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92dcd-106">Syntax</span></span>


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="92dcd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92dcd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92dcd-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="92dcd-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="92dcd-109">Environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="92dcd-109">A texture environment.</span></span> <span data-ttu-id="92dcd-110">Doit être une \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="92dcd-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="92dcd-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="92dcd-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="92dcd-112">Nom symbolique d’un paramètre d’environnement de texture à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="92dcd-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="92dcd-113">Doit être le \_ mode env de la texture GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="92dcd-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="92dcd-114">*param*</span><span class="sxs-lookup"><span data-stu-id="92dcd-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="92dcd-115">Une constante symbolique unique, l’une des \_ modules comptabilité GL, \_ décalque GL, \_ mélange GL ou \_ remplacement GL.</span><span class="sxs-lookup"><span data-stu-id="92dcd-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92dcd-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="92dcd-116">Return value</span></span>

<span data-ttu-id="92dcd-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="92dcd-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92dcd-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="92dcd-118">Error codes</span></span>

<span data-ttu-id="92dcd-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="92dcd-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="92dcd-120">Nom</span><span class="sxs-lookup"><span data-stu-id="92dcd-120">Name</span></span>                                                                                                  | <span data-ttu-id="92dcd-121">Signification</span><span class="sxs-lookup"><span data-stu-id="92dcd-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92dcd-122"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92dcd-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="92dcd-123">*target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque les *paramètres* devaient avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.</span><span class="sxs-lookup"><span data-stu-id="92dcd-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="92dcd-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92dcd-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="92dcd-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="92dcd-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="92dcd-126">Notes</span><span class="sxs-lookup"><span data-stu-id="92dcd-126">Remarks</span></span>

<span data-ttu-id="92dcd-127">Un environnement de texture spécifie la manière dont les valeurs de texture sont interprétées lorsqu’un fragment est texturé.</span><span class="sxs-lookup"><span data-stu-id="92dcd-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="92dcd-128">Le paramètre *cible* doit être de la \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="92dcd-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="92dcd-129">Le paramètre *pname* est le \_ mode de texture GL \_ env \_ .</span><span class="sxs-lookup"><span data-stu-id="92dcd-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="92dcd-130">Trois fonctions de texture sont définies : \_ module de comptabilité GL, \_ décalque GL et fusion du GL \_ .</span><span class="sxs-lookup"><span data-stu-id="92dcd-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="92dcd-131">Une fonction de texture agit sur le fragment pour être texturée à l’aide de la valeur d’image de texture qui s’applique au fragment (voir [**glTexParameter**](gltexparameter-functions.md)) et produit une couleur RVBA pour ce fragment.</span><span class="sxs-lookup"><span data-stu-id="92dcd-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="92dcd-132">Le tableau suivant montre comment la couleur RVBA est produite pour chacune des trois fonctions de texture qui peuvent être choisies.</span><span class="sxs-lookup"><span data-stu-id="92dcd-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="92dcd-133">*C* est une triple des valeurs de couleur (RGB) et *a* est la valeur alpha associée.</span><span class="sxs-lookup"><span data-stu-id="92dcd-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="92dcd-134">Les valeurs RVBA extraites d’une image de texture sont comprises dans la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="92dcd-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="92dcd-135">L’indice *f* fait référence au fragment entrant, l’indice *t* à l’image de texture, l’indice *c* à la couleur de l’environnement de texture et l’indice *v* indique une valeur produite par la fonction de texture.</span><span class="sxs-lookup"><span data-stu-id="92dcd-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="92dcd-136">Une image de texture peut avoir jusqu’à quatre composants par élément de texture (consultez [**glTexImage1D**](glteximage1d.md) et [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="92dcd-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="92dcd-137">Dans une image à un composant, lt indique que seul un composant.</span><span class="sxs-lookup"><span data-stu-id="92dcd-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="92dcd-138">Une image à deux composants utilise *L ?*</span><span class="sxs-lookup"><span data-stu-id="92dcd-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="92dcd-139">et *un ?*</span><span class="sxs-lookup"><span data-stu-id="92dcd-139">and *A?*</span></span> <span data-ttu-id="92dcd-140">.</span><span class="sxs-lookup"><span data-stu-id="92dcd-140">.</span></span> <span data-ttu-id="92dcd-141">Une image à trois composants a uniquement une valeur de couleur, *C ?*</span><span class="sxs-lookup"><span data-stu-id="92dcd-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="92dcd-142">.</span><span class="sxs-lookup"><span data-stu-id="92dcd-142">.</span></span> <span data-ttu-id="92dcd-143">Une image à quatre composants a-t-elle une valeur de couleur *C ?*</span><span class="sxs-lookup"><span data-stu-id="92dcd-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="92dcd-144">et une valeur alpha *A ?*</span><span class="sxs-lookup"><span data-stu-id="92dcd-144">and an alpha value *A?*</span></span> <span data-ttu-id="92dcd-145">.</span><span class="sxs-lookup"><span data-stu-id="92dcd-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="92dcd-146">Nombre de composants</span><span class="sxs-lookup"><span data-stu-id="92dcd-146">Number of components</span></span></th>
<th><span data-ttu-id="92dcd-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="92dcd-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="92dcd-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="92dcd-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="92dcd-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="92dcd-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="92dcd-150">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92dcd-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="92dcd-151"><em>C<sub>v</sub> </em>  =  <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="92dcd-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="92dcd-153">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="92dcd-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="92dcd-154"><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-154"><em>C</em> <em><sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="92dcd-155"><em>) C<sub>f</sub> </em> + <em></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="92dcd-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92dcd-157"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="92dcd-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="92dcd-158"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="92dcd-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="92dcd-159">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92dcd-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="92dcd-160"><em>C<sub>v</sub> </em>  =  <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="92dcd-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="92dcd-162">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="92dcd-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="92dcd-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="92dcd-164"><em>) C<sub>f</sub> </em> + <em></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="92dcd-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92dcd-166"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="92dcd-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="92dcd-167"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="92dcd-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="92dcd-168">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92dcd-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="92dcd-169"><em>C<sub>v</sub> </em>  =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="92dcd-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="92dcd-171"><em>C<sub>v</sub> </em>  =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="92dcd-172">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="92dcd-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="92dcd-173"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="92dcd-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="92dcd-174"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="92dcd-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="92dcd-175">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="92dcd-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="92dcd-176"><em>C<sub>v</sub> </em>  =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="92dcd-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="92dcd-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="92dcd-178"><em>C<sub>v</sub> </em> = (1- <em>A ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="92dcd-179"><em>) C<sub>f</sub> </em> + <em>A ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="92dcd-180"><em>Secteur?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="92dcd-181">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="92dcd-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="92dcd-182"><em>Un<sub>v</sub> </em>  =  <em>R ?</em></span><span class="sxs-lookup"><span data-stu-id="92dcd-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="92dcd-183"><em>Un<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="92dcd-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="92dcd-184"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="92dcd-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="92dcd-185">Le \_ mode de la texture GL \_ env \_ est défini par défaut sur le module comptabilité GL \_ .</span><span class="sxs-lookup"><span data-stu-id="92dcd-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="92dcd-186">La fonction suivante récupère des informations relatives à **glTexEnvf**:</span><span class="sxs-lookup"><span data-stu-id="92dcd-186">The following function retrieves information related to **glTexEnvf**:</span></span>

[<span data-ttu-id="92dcd-187">**glTexGetEnvfv**</span><span class="sxs-lookup"><span data-stu-id="92dcd-187">**glTexGetEnvfv**</span></span>](glgettexenvfv.md)

## <a name="requirements"></a><span data-ttu-id="92dcd-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92dcd-188">Requirements</span></span>



| <span data-ttu-id="92dcd-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92dcd-189">Requirement</span></span> | <span data-ttu-id="92dcd-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="92dcd-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92dcd-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92dcd-191">Minimum supported client</span></span><br/> | <span data-ttu-id="92dcd-192">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92dcd-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="92dcd-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92dcd-193">Minimum supported server</span></span><br/> | <span data-ttu-id="92dcd-194">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92dcd-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92dcd-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="92dcd-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="92dcd-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="92dcd-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="92dcd-197">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="92dcd-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="92dcd-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92dcd-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="92dcd-199">DLL</span><span class="sxs-lookup"><span data-stu-id="92dcd-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92dcd-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92dcd-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92dcd-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92dcd-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92dcd-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="92dcd-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="92dcd-203">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="92dcd-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="92dcd-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="92dcd-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="92dcd-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="92dcd-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="92dcd-206">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="92dcd-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





