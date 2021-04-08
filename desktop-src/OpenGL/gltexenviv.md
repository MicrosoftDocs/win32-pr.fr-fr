---
title: fonction glTexEnviv (GL. h)
description: La fonction glTexEnviv définit un paramètre d’environnement de texture.
ms.assetid: e98ce736-cc68-4687-8c1b-6b0fef7a677a
keywords:
- glTexEnviv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexEnviv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ec232f559e8d4af10369ebe98dd0aea71e36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844389"
---
# <a name="gltexenviv-function"></a><span data-ttu-id="3f341-104">glTexEnviv fonction)</span><span class="sxs-lookup"><span data-stu-id="3f341-104">glTexEnviv function</span></span>

<span data-ttu-id="3f341-105">La fonction **glTexEnviv** définit un paramètre d’environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="3f341-105">The **glTexEnviv** function sets a texture environment parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f341-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f341-106">Syntax</span></span>


```C++
void WINAPI glTexEnviv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="3f341-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f341-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f341-108">*cible*</span><span class="sxs-lookup"><span data-stu-id="3f341-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="3f341-109">Environnement de texture.</span><span class="sxs-lookup"><span data-stu-id="3f341-109">A texture environment.</span></span> <span data-ttu-id="3f341-110">Doit être une \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="3f341-110">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="3f341-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="3f341-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3f341-112">Nom symbolique d’un paramètre d’environnement de texture à valeur unique.</span><span class="sxs-lookup"><span data-stu-id="3f341-112">The symbolic name of a single-valued texture environment parameter.</span></span> <span data-ttu-id="3f341-113">Les valeurs acceptées sont \_ le \_ mode env de la texture du GL \_ et la couleur de la \_ texture GL \_ env \_ .</span><span class="sxs-lookup"><span data-stu-id="3f341-113">Accepted values are GL\_TEXTURE\_ENV\_MODE and GL\_TEXTURE\_ENV\_COLOR.</span></span>

</dd> <dt>

<span data-ttu-id="3f341-114">*params*</span><span class="sxs-lookup"><span data-stu-id="3f341-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3f341-115">Pointeur vers un tableau de paramètres : une constante symbolique unique ou une couleur RVBA.</span><span class="sxs-lookup"><span data-stu-id="3f341-115">A pointer to an array of parameters: either a single symbolic constant or an RGBA color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f341-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3f341-116">Return value</span></span>

<span data-ttu-id="3f341-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3f341-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3f341-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3f341-118">Error codes</span></span>

<span data-ttu-id="3f341-119">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3f341-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3f341-120">Nom</span><span class="sxs-lookup"><span data-stu-id="3f341-120">Name</span></span>                                                                                                  | <span data-ttu-id="3f341-121">Signification</span><span class="sxs-lookup"><span data-stu-id="3f341-121">Meaning</span></span>                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f341-122"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f341-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3f341-123">*target* ou *pname* ne faisait pas partie des valeurs définies acceptées, ou lorsque les *paramètres* devaient avoir une valeur de constante définie (basée sur la valeur de *pname*) et ne l’a pas fait.</span><span class="sxs-lookup"><span data-stu-id="3f341-123">*target* or *pname* was not one of the accepted defined values, or when *params* should have had a defined constant value (based on the value of *pname*) and did not.</span></span><br/> |
| <dl> <span data-ttu-id="3f341-124"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3f341-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3f341-125">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3f341-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="3f341-126">Notes</span><span class="sxs-lookup"><span data-stu-id="3f341-126">Remarks</span></span>

<span data-ttu-id="3f341-127">Un environnement de texture spécifie la manière dont les valeurs de texture sont interprétées lorsqu’un fragment est texturé.</span><span class="sxs-lookup"><span data-stu-id="3f341-127">A texture environment specifies how texture values are interpreted when a fragment is textured.</span></span> <span data-ttu-id="3f341-128">Le paramètre *cible* doit être de la \_ texture GL \_ env.</span><span class="sxs-lookup"><span data-stu-id="3f341-128">The *target* parameter must be GL\_TEXTURE\_ENV.</span></span> <span data-ttu-id="3f341-129">Le paramètre *pname* peut être le \_ mode env de la texture GL ou la \_ \_ couleur de la texture du GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="3f341-129">The *pname* parameter can be either GL\_TEXTURE\_ENV\_MODE or GL\_TEXTURE\_ENV\_COLOR.</span></span>

<span data-ttu-id="3f341-130">Si *pname* est \_ \_ \_ le mode de texture GL env, alors *params* est (ou pointe vers) le nom symbolique d’une fonction de texture.</span><span class="sxs-lookup"><span data-stu-id="3f341-130">If *pname* is GL\_TEXTURE\_ENV\_MODE, then *params* is (or points to) the symbolic name of a texture function.</span></span> <span data-ttu-id="3f341-131">Trois fonctions de texture sont définies : \_ module de comptabilité GL, \_ décalque GL et fusion du GL \_ .</span><span class="sxs-lookup"><span data-stu-id="3f341-131">Three texture functions are defined: GL\_MODULATE, GL\_DECAL, and GL\_BLEND.</span></span>

<span data-ttu-id="3f341-132">Une fonction de texture agit sur le fragment pour être texturée à l’aide de la valeur d’image de texture qui s’applique au fragment (voir [**glTexParameter**](gltexparameter-functions.md)) et produit une couleur RVBA pour ce fragment.</span><span class="sxs-lookup"><span data-stu-id="3f341-132">A texture function acts on the fragment to be textured using the texture image value that applies to the fragment (see [**glTexParameter**](gltexparameter-functions.md)) and produces an RGBA color for that fragment.</span></span> <span data-ttu-id="3f341-133">Le tableau suivant montre comment la couleur RVBA est produite pour chacune des trois fonctions de texture qui peuvent être choisies.</span><span class="sxs-lookup"><span data-stu-id="3f341-133">The following table shows how the RGBA color is produced for each of the three texture functions that can be chosen.</span></span> <span data-ttu-id="3f341-134">*C* est une triple des valeurs de couleur (RGB) et *a* est la valeur alpha associée.</span><span class="sxs-lookup"><span data-stu-id="3f341-134">*C* is a triple of color values (RGB) and *A* is the associated alpha value.</span></span> <span data-ttu-id="3f341-135">Les valeurs RVBA extraites d’une image de texture sont comprises dans la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="3f341-135">RGBA values extracted from a texture image are in the range \[0, 1\].</span></span> <span data-ttu-id="3f341-136">L’indice *f* fait référence au fragment entrant, l’indice *t* à l’image de texture, l’indice *c* à la couleur de l’environnement de texture et l’indice *v* indique une valeur produite par la fonction de texture.</span><span class="sxs-lookup"><span data-stu-id="3f341-136">The subscript *f* refers to the incoming fragment, the subscript *t* to the texture image, the subscript *c* to the texture environment color, and subscript *v* indicates a value produced by the texture function.</span></span>

<span data-ttu-id="3f341-137">Une image de texture peut avoir jusqu’à quatre composants par élément de texture (consultez [**glTexImage1D**](glteximage1d.md) et [**glTexImage2D**](glteximage2d.md)).</span><span class="sxs-lookup"><span data-stu-id="3f341-137">A texture image can have up to four components per texture element (see [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md)).</span></span> <span data-ttu-id="3f341-138">Dans une image à un composant, lt indique que seul un composant.</span><span class="sxs-lookup"><span data-stu-id="3f341-138">In a one-component image, Lt indicates that single component.</span></span> <span data-ttu-id="3f341-139">Une image à deux composants utilise *L ?*</span><span class="sxs-lookup"><span data-stu-id="3f341-139">A two-component image uses *L?*</span></span>  <span data-ttu-id="3f341-140">et *un ?*</span><span class="sxs-lookup"><span data-stu-id="3f341-140">and *A?*</span></span> <span data-ttu-id="3f341-141">.</span><span class="sxs-lookup"><span data-stu-id="3f341-141">.</span></span> <span data-ttu-id="3f341-142">Une image à trois composants a uniquement une valeur de couleur, *C ?*</span><span class="sxs-lookup"><span data-stu-id="3f341-142">A three-component image has only a color value, *C?*</span></span> <span data-ttu-id="3f341-143">.</span><span class="sxs-lookup"><span data-stu-id="3f341-143">.</span></span> <span data-ttu-id="3f341-144">Une image à quatre composants a-t-elle une valeur de couleur *C ?*</span><span class="sxs-lookup"><span data-stu-id="3f341-144">A four-component image has both a color value *C?*</span></span>  <span data-ttu-id="3f341-145">et une valeur alpha *A ?*</span><span class="sxs-lookup"><span data-stu-id="3f341-145">and an alpha value *A?*</span></span> <span data-ttu-id="3f341-146">.</span><span class="sxs-lookup"><span data-stu-id="3f341-146">.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3f341-147">Nombre de composants</span><span class="sxs-lookup"><span data-stu-id="3f341-147">Number of components</span></span></th>
<th><span data-ttu-id="3f341-148">GL_MODULATE</span><span class="sxs-lookup"><span data-stu-id="3f341-148">GL_MODULATE</span></span></th>
<th><span data-ttu-id="3f341-149">GL_DECAL</span><span class="sxs-lookup"><span data-stu-id="3f341-149">GL_DECAL</span></span></th>
<th><span data-ttu-id="3f341-150">GL_BLEND</span><span class="sxs-lookup"><span data-stu-id="3f341-150">GL_BLEND</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="3f341-151">1 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="3f341-151">1${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3f341-152"><em>C<sub>v</sub> </em>   =  <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-152"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="3f341-153"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="3f341-153"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="3f341-154">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="3f341-154">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3f341-155"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-155"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="3f341-156"><em>) C<sub>f</sub> </em> + <em></em></span><span class="sxs-lookup"><span data-stu-id="3f341-156"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="3f341-157"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="3f341-157"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f341-158"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="3f341-158"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="3f341-159"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="3f341-159"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="3f341-160">2 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="3f341-160">2${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3f341-161"><em>C<sub>v</sub> </em>   =  <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-161"><em>C<sub>v</sub></em>  = <em>L?</em></span></span> <span data-ttu-id="3f341-162"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="3f341-162"><em>C<sub>f</sub></em></span></span></td>
<td rowspan="2"><span data-ttu-id="3f341-163">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="3f341-163">undefined${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3f341-164"><em>C<sub>v</sub> </em>   =  <em>(1</em> - <em>L ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-164"><em>C<sub>v</sub></em>  = <em>(1</em> - <em>L?</em></span></span> <span data-ttu-id="3f341-165"><em>) C<sub>f</sub> </em> + <em></em></span><span class="sxs-lookup"><span data-stu-id="3f341-165"><em>)C<sub>f</sub></em> + <em>L?</em></span></span> <span data-ttu-id="3f341-166"><em>C<sub>c</sub></em></span><span class="sxs-lookup"><span data-stu-id="3f341-166"><em>C<sub>c</sub></em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f341-167"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="3f341-167"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="3f341-168"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="3f341-168"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="3f341-169">3 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="3f341-169">3${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3f341-170"><em>C<sub>v</sub> </em>   =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-170"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="3f341-171"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="3f341-171"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="3f341-172"><em>C<sub>v</sub> </em>   =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-172"><em>C<sub>v</sub></em>  = <em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="3f341-173">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="3f341-173">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f341-174"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em> </span><span class="sxs-lookup"><span data-stu-id="3f341-174"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="3f341-175"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="3f341-175"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="3f341-176">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="3f341-176">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="3f341-177"><em>C<sub>v</sub> </em>   =  <em>C ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-177"><em>C<sub>v</sub></em>  = <em>C?</em></span></span> <span data-ttu-id="3f341-178"><em>C<sub>f</sub></em></span><span class="sxs-lookup"><span data-stu-id="3f341-178"><em>C<sub>f</sub></em></span></span></td>
<td><span data-ttu-id="3f341-179"><em>C<sub>v</sub> </em> = (1- <em>A ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-179"><em>C<sub>v</sub></em>  = (1 - <em>A?</em></span></span> <span data-ttu-id="3f341-180"><em>) C<sub>f</sub> </em> + <em>A ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-180"><em>)C<sub>f</sub></em> + <em>A?</em></span></span> <span data-ttu-id="3f341-181"><em>Secteur?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-181"><em>C?</em></span></span></td>
<td rowspan="2"><span data-ttu-id="3f341-182">$ {REMOVE} $ non défini</span><span class="sxs-lookup"><span data-stu-id="3f341-182">undefined${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f341-183"><em>Un<sub>v</sub> </em>   =  <em>R ?</em></span><span class="sxs-lookup"><span data-stu-id="3f341-183"><em>A<sub>v</sub></em>  = <em>A?</em></span></span> <span data-ttu-id="3f341-184"><em>Un<sub>f</sub></em> </span><span class="sxs-lookup"><span data-stu-id="3f341-184"><em>A<sub>f</sub></em> </span></span></td>
<td><span data-ttu-id="3f341-185"><em>Un<sub>v</sub> </em>   =  <em>Un<sub>f</sub> </em></span><span class="sxs-lookup"><span data-stu-id="3f341-185"><em>A<sub>v</sub></em>  = <em>A<sub>f</sub></em></span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="3f341-186">Si pname correspond \_ \_ \_ à la couleur de la texture du GL, *params* est un pointeur vers un tableau qui contient une couleur RVBA composée de quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="3f341-186">If pname is GL\_TEXTURE\_ENV\_COLOR, *params* is a pointer to an array that holds an RGBA color consisting of four values.</span></span> <span data-ttu-id="3f341-187">Les composants de couleur entier sont interprétés de manière linéaire de telle sorte que l’entier le plus positif est mappé à 1,0, et l’entier le plus négatif est mappé à-1,0.</span><span class="sxs-lookup"><span data-stu-id="3f341-187">Integer color components are interpreted linearly such that the most positive integer maps to 1.0, and the most negative integer maps to -1.0.</span></span> <span data-ttu-id="3f341-188">Les valeurs sont ancrées à la plage \[ 0, 1 \] quand elles sont spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3f341-188">The values are clamped to the range \[0, 1\] when they are specified.</span></span> <span data-ttu-id="3f341-189">*C <sub>c</sub>* accepte ces quatre valeurs.</span><span class="sxs-lookup"><span data-stu-id="3f341-189">*C<sub>c</sub>* takes these four values.</span></span>

<span data-ttu-id="3f341-190">Le \_ \_ mode env de la texture GL \_ est défini par défaut sur la valeur par défaut du module comptabilité GL \_ et la \_ couleur de la texture de la comptabilité \_ env \_ est (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="3f341-190">GL\_TEXTURE\_ENV\_MODE defaults to GL\_MODULATE and GL\_TEXTURE\_ENV\_COLOR defaults to (0, 0, 0, 0).</span></span>

<span data-ttu-id="3f341-191">La fonction suivante récupère des informations relatives à **glTexEnviv**:</span><span class="sxs-lookup"><span data-stu-id="3f341-191">The following function retrieves information related to **glTexEnviv**:</span></span>

[<span data-ttu-id="3f341-192">**glTexGetEnviv**</span><span class="sxs-lookup"><span data-stu-id="3f341-192">**glTexGetEnviv**</span></span>](glgettexenviv.md)

## <a name="requirements"></a><span data-ttu-id="3f341-193">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f341-193">Requirements</span></span>



| <span data-ttu-id="3f341-194">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f341-194">Requirement</span></span> | <span data-ttu-id="3f341-195">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f341-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f341-196">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f341-196">Minimum supported client</span></span><br/> | <span data-ttu-id="3f341-197">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f341-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3f341-198">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f341-198">Minimum supported server</span></span><br/> | <span data-ttu-id="3f341-199">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f341-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f341-200">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f341-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f341-201"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f341-201"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3f341-202">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3f341-202">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f341-203"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f341-203"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3f341-204">DLL</span><span class="sxs-lookup"><span data-stu-id="3f341-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f341-205"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f341-205"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f341-206">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f341-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f341-207">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3f341-207">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3f341-208">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3f341-208">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3f341-209">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="3f341-209">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="3f341-210">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="3f341-210">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="3f341-211">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3f341-211">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





