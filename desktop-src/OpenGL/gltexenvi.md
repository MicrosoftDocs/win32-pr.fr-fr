---
title: fonction glTexEnvi (GL. h)
description: La fonction glTexEnvi définit un paramètre d’environnement de texture.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- glTexEnvi fonction OpenGL
topic_type:
- apiref
api_name:
- glTexEnvi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013b0e4805042ed0967e02df83f143d8bcfd991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512357"
---
# <a name="gltexenvi-function"></a><span data-ttu-id="4d745-104">glTexEnvi fonction)</span><span class="sxs-lookup"><span data-stu-id="4d745-104">glTexEnvi function</span></span>

<span data-ttu-id="4d745-105">La fonction **glTexEnvi** définit un paramètre d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="4d745-105">The **glTexEnvi** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d745-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d745-106">Syntax</span></span>


```C++
void WINAPI glTexEnvi(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="4d745-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d745-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d745-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="4d745-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="4d745-109">Environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="4d745-109">A texture environment.</span></span> <span data-ttu-id="4d745-110">Doit être une \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="4d745-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="4d745-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="4d745-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="4d745-112">Nom symbolique d’un paramètre d’environnement de texture à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="4d745-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="4d745-113">Doit être le \_ mode env de la texture GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4d745-113">Must be GL\_TEXTURE\_ENV\_MODE.</span></span>

</dd> <dt>

<span data-ttu-id="4d745-114">*param*</span><span class="sxs-lookup"><span data-stu-id="4d745-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="4d745-115">Une constante symbolique unique, l’une des \_ modules comptabilité GL, \_ décalque GL, \_ mélange GL ou \_ remplacement GL.</span><span class="sxs-lookup"><span data-stu-id="4d745-115">A single symbolic constant, one of GL\_MODULATE, GL\_DECAL, GL\_BLEND, or GL\_REPLACE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d745-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4d745-116">Return value</span></span>

<span data-ttu-id="4d745-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4d745-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d745-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4d745-118">Error codes</span></span>

<span data-ttu-id="4d745-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4d745-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4d745-120">Nom</span><span class="sxs-lookup"><span data-stu-id="4d745-120">Name</span></span>                                                                                                  | <span data-ttu-id="4d745-121">Signification</span><span class="sxs-lookup"><span data-stu-id="4d745-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d745-122"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d745-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="4d745-123">*target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque les *paramètres* devaient avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.</span><span class="sxs-lookup"><span data-stu-id="4d745-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="4d745-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d745-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="4d745-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4d745-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="4d745-126">Notes</span><span class="sxs-lookup"><span data-stu-id="4d745-126">Remarks</span></span>

<span data-ttu-id="4d745-127">Un environnement de texture spécifie la manière dont les valeurs de texture sont interprétées lorsqu’un fragment est texturé.</span><span class="sxs-lookup"><span data-stu-id="4d745-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="4d745-128">Le paramètre *cible* doit être de la \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="4d745-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="4d745-129">Le paramètre *pname* est le \_ mode de texture GL \_ env \_ .</span><span class="sxs-lookup"><span data-stu-id="4d745-129">The *pname* parameter is GL\_TEXTURE\_ENV\_MODE.</span></span> <span data-ttu-id="4d745-130">Trois fonctions de texture sont définies : \_ module de comptabilité GL, \_ décalque GL et fusion du GL \_ .</span><span class="sxs-lookup"><span data-stu-id="4d745-130">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="4d745-131">Une fonction de texture agit sur le fragment pour être texturée à l’aide de la valeur d’image de texture qui s’applique au fragment (voir [**glTexParameter**](gltexparameter-functions.md)) et produit une couleur RVBA pour ce fragment.</span><span class="sxs-lookup"><span data-stu-id="4d745-131">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="4d745-132">Le tableau suivant montre comment la couleur RVBA est produite pour chacune des trois fonctions de texture qui peuvent être choisies.</span><span class="sxs-lookup"><span data-stu-id="4d745-132">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="4d745-133">*C* est une triple des valeurs de couleur (RGB) et *a* est la valeur alpha associée.</span><span class="sxs-lookup"><span data-stu-id="4d745-133">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="4d745-134">Les valeurs RVBA extraites d’une image de texture sont comprises dans la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="4d745-134">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="4d745-135">L’indice *f* fait référence au fragment entrant, l’indice *t* à l’image de texture, l’indice *c* à la couleur de l’environnement de texture et l’indice *v* indique une valeur produite par la fonction de texture.</span><span class="sxs-lookup"><span data-stu-id="4d745-135">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="4d745-136">Une image de texture peut avoir jusqu’à quatre composants par élément de texture (consultez [**glTexImage1D**](glteximage1d.md) et [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="4d745-136">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="4d745-137">Dans une image à un composant, lt indique que seul un composant.</span><span class="sxs-lookup"><span data-stu-id="4d745-137">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="4d745-138">Une image à deux composants utilise *L ?*</span><span class="sxs-lookup"><span data-stu-id="4d745-138">A two-component image uses *L?*</span></span>  <span data-ttu-id="4d745-139">et *un ?*</span><span class="sxs-lookup"><span data-stu-id="4d745-139">and *A?*</span></span> <span data-ttu-id="4d745-140">.</span><span class="sxs-lookup"><span data-stu-id="4d745-140">.</span></span> <span data-ttu-id="4d745-141">Une image à trois composants a uniquement une valeur de couleur, *C ?*</span><span class="sxs-lookup"><span data-stu-id="4d745-141">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="4d745-142">.</span><span class="sxs-lookup"><span data-stu-id="4d745-142">.</span></span> <span data-ttu-id="4d745-143">Une image à quatre composants a-t-elle une valeur de couleur *C ?*</span><span class="sxs-lookup"><span data-stu-id="4d745-143">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="4d745-144">et une valeur alpha *A ?*</span><span class="sxs-lookup"><span data-stu-id="4d745-144">and an alpha value *A?*</span></span> <span data-ttu-id="4d745-145">.</span><span class="sxs-lookup"><span data-stu-id="4d745-145">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4d745-146">Nombre de composants</span><span class="sxs-lookup"><span data-stu-id="4d745-146">Number of components</span></span></th>
<th><span data-ttu-id="4d745-147">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="4d745-147">GL_MODULATE</span></span></th>
<th><span data-ttu-id="4d745-148">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="4d745-148">GL_DECAL</span></span></th>
<th><span data-ttu-id="4d745-149">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="4d745-149">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4d745-150">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4d745-150">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4d745-151"><em>C<sub>v</sub> </em>  =  <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-151"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="4d745-152"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4d745-152"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="4d745-153">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="4d745-153">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4d745-154"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-154"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="4d745-155"><em>) C<sub>f</sub> </em> + <em></em></span><span class="sxs-lookup"><span data-stu-id="4d745-155"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="4d745-156"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="4d745-156"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d745-157"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4d745-157"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4d745-158"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4d745-158"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4d745-159">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4d745-159">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4d745-160"><em>C<sub>v</sub> </em>  =  <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-160"><em>C<sub>v</sub></em> = <em>L?</em></span></span> <span data-ttu-id="4d745-161"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4d745-161"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="4d745-162">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="4d745-162">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4d745-163"><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-163"><em>C<sub>v</sub></em> = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="4d745-164"><em>) C<sub>f</sub> </em> + <em></em></span><span class="sxs-lookup"><span data-stu-id="4d745-164"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="4d745-165"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="4d745-165"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d745-166"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4d745-166"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4d745-167"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4d745-167"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4d745-168">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4d745-168">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4d745-169"><em>C<sub>v</sub> </em>  =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-169"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="4d745-170"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4d745-170"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4d745-171"><em>C<sub>v</sub> </em>  =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-171"><em>C<sub>v</sub></em> = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="4d745-172">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="4d745-172">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d745-173"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="4d745-173"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="4d745-174"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4d745-174"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="4d745-175">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="4d745-175">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="4d745-176"><em>C<sub>v</sub> </em>  =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-176"><em>C<sub>v</sub></em> = <em>C?</em></span></span> <span data-ttu-id="4d745-177"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="4d745-177"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="4d745-178"><em>C<sub>v</sub> </em> = (1- <em>A ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-178"><em>C<sub>v</sub></em> = (1 - <em>A?</em></span></span> <span data-ttu-id="4d745-179"><em>) C<sub>f</sub> </em> + <em>A ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-179"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="4d745-180"><em>Secteur?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-180"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="4d745-181">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="4d745-181">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d745-182"><em>Un<sub>v</sub> </em>  =  <em>R ?</em></span><span class="sxs-lookup"><span data-stu-id="4d745-182"><em>A<sub>v</sub></em> = <em>A?</em></span></span> <span data-ttu-id="4d745-183"><em>Un<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="4d745-183"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="4d745-184"><em>Un<sub>v</sub> </em>  =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="4d745-184"><em>A<sub>v</sub></em> = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="4d745-185">Le \_ mode de la texture GL \_ env \_ est défini par défaut sur le module comptabilité GL \_ .</span><span class="sxs-lookup"><span data-stu-id="4d745-185">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE.</span></span>

<span data-ttu-id="4d745-186">La fonction suivante récupère des informations relatives à **glTexEnvi**:</span><span class="sxs-lookup"><span data-stu-id="4d745-186">The following function retrieves information related to **glTexEnvi**:</span></span>

[<span data-ttu-id="4d745-187">**glTexGetEnviv**</span><span class="sxs-lookup"><span data-stu-id="4d745-187">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="4d745-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d745-188">Requirements</span></span>



| <span data-ttu-id="4d745-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d745-189">Requirement</span></span> | <span data-ttu-id="4d745-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d745-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d745-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d745-191">Minimum supported client</span></span><br/> | <span data-ttu-id="4d745-192">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d745-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4d745-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d745-193">Minimum supported server</span></span><br/> | <span data-ttu-id="4d745-194">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d745-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d745-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d745-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d745-196"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d745-196"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4d745-197">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d745-197">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d745-198"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d745-198"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4d745-199">DLL</span><span class="sxs-lookup"><span data-stu-id="4d745-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d745-200"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d745-200"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d745-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d745-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d745-202">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4d745-202">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4d745-203">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4d745-203">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4d745-204">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="4d745-204">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="4d745-205">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="4d745-205">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="4d745-206">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4d745-206">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





