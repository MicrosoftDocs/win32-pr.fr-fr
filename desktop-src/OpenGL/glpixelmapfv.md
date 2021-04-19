---
title: fonction glPixelMapfv (GL. h)
description: La fonction glPixelMapfv définit les mappages de transfert de pixels.
ms.assetid: 13403243-1ec4-4b1d-a9da-9a6693b6f9b8
keywords:
- glPixelMapfv fonction OpenGL
topic_type:
- apiref
api_name:
- glPixelMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97124eeca8051ec23d9a4fea03a98468d320af8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512616"
---
# <a name="glpixelmapfv-function"></a><span data-ttu-id="0df0e-104">glPixelMapfv fonction)</span><span class="sxs-lookup"><span data-stu-id="0df0e-104">glPixelMapfv function</span></span>

<span data-ttu-id="0df0e-105">La fonction **glPixelMapfv** définit les mappages de transfert de pixels.</span><span class="sxs-lookup"><span data-stu-id="0df0e-105">The **glPixelMapfv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df0e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0df0e-106">Syntax</span></span>


```C++
void WINAPI glPixelMapfv(
         GLenum  map,
         GLsizei mapsize,
   const GLfloat *values
);
```



## <a name="parameters"></a><span data-ttu-id="0df0e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0df0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df0e-108">*map*</span><span class="sxs-lookup"><span data-stu-id="0df0e-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="0df0e-109">Nom de mappage symbolique.</span><span class="sxs-lookup"><span data-stu-id="0df0e-109">A symbolic map name.</span></span> <span data-ttu-id="0df0e-110">Les dix cartes sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0df0e-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="0df0e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="0df0e-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="0df0e-112">Signification</span><span class="sxs-lookup"><span data-stu-id="0df0e-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="0df0e-113"><dt>**\_ \_ carte de pixels \_ GL \_ i \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="0df0e-114">Mappe les index de couleurs aux index de couleurs.</span><span class="sxs-lookup"><span data-stu-id="0df0e-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="0df0e-115"><dt>**\_ \_ cartes de pixels \_ GL \_ sur \_ s**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="0df0e-116">Mappe des index de stencil à des index de stencil.</span><span class="sxs-lookup"><span data-stu-id="0df0e-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="0df0e-117"><dt>**\_ \_ carte de pixels GL \_ I \_ à \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="0df0e-118">Mappe les index de couleurs aux composants Red.</span><span class="sxs-lookup"><span data-stu-id="0df0e-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="0df0e-119"><dt>**\_ \_ carte de pixels GL \_ I \_ à \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="0df0e-120">Mappe les index de couleurs aux composants verts.</span><span class="sxs-lookup"><span data-stu-id="0df0e-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="0df0e-121"><dt>**\_ \_ carte de pixels GL \_ I \_ à \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="0df0e-122">Mappe les index de couleurs aux composants bleus.</span><span class="sxs-lookup"><span data-stu-id="0df0e-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="0df0e-123"><dt>**\_ \_ carte de pixels GL \_ I \_ à \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="0df0e-124">Mappe les index de couleurs aux composants alpha.</span><span class="sxs-lookup"><span data-stu-id="0df0e-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="0df0e-125"><dt>**\_ \_ carte de pixels GL \_ r \_ vers \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="0df0e-126">Mappe les composants Red aux composants Red.</span><span class="sxs-lookup"><span data-stu-id="0df0e-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="0df0e-127"><dt>**\_ \_ carte de pixels GL \_ g \_ à \_ g**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="0df0e-128">Mappe les composants verts aux composants verts.</span><span class="sxs-lookup"><span data-stu-id="0df0e-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="0df0e-129"><dt>**\_ \_ carte de pixels GL \_ b \_ à \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="0df0e-130">Mappe les composants bleus aux composants bleus.</span><span class="sxs-lookup"><span data-stu-id="0df0e-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="0df0e-131"><dt>**\_mappage de pixel GL \_ \_ a \_ à \_ un**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="0df0e-132">Mappe les composants alpha aux composants alpha.</span><span class="sxs-lookup"><span data-stu-id="0df0e-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0df0e-133">*mapper*</span><span class="sxs-lookup"><span data-stu-id="0df0e-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="0df0e-134">Taille de la carte en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="0df0e-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="0df0e-135">*valeurs*</span><span class="sxs-lookup"><span data-stu-id="0df0e-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="0df0e-136">Tableau de valeurs de la valeur de *Mapping* .</span><span class="sxs-lookup"><span data-stu-id="0df0e-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df0e-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0df0e-137">Return value</span></span>

<span data-ttu-id="0df0e-138">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0df0e-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0df0e-139">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0df0e-139">Error codes</span></span>

<span data-ttu-id="0df0e-140">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0df0e-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0df0e-141">Nom</span><span class="sxs-lookup"><span data-stu-id="0df0e-141">Name</span></span>                                                                                                  | <span data-ttu-id="0df0e-142">Signification</span><span class="sxs-lookup"><span data-stu-id="0df0e-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0df0e-143"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0df0e-144">le *mappage* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="0df0e-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="0df0e-145"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="0df0e-146">la valeur de la taille de *mappage* était négative ou supérieure à celle de la \_ table de mappage de pixels GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0df0e-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="0df0e-147"><dt>**\_valeur non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="0df0e-148">*Map* était la \_ \_ carte de pixels GL \_ i \_ à \_ i \_ , \_ les cartes de pixels GL \_ s \_ à \_ s, les \_ mappages de pixel GL \_ \_ i \_ à \_ R, \_ les cartes de pixel GL \_ \_ i \_ à \_ G, \_ \_ la carte de pixels GL \_ i \_ à \_ B, ou \_ \_ la carte de pixels GL \_ i \_ à \_ a, et la *correspondance* n’était pas une puissance de deux.</span><span class="sxs-lookup"><span data-stu-id="0df0e-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="0df0e-149"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0df0e-150">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0df0e-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="0df0e-151">Notes</span><span class="sxs-lookup"><span data-stu-id="0df0e-151">Remarks</span></span>

<span data-ttu-id="0df0e-152">La fonction **glPixelMap** définit les tables de traduction, ou *Maps*, utilisées [**par glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)et [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="0df0e-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="0df0e-153">L’utilisation de ces mappages est décrite entièrement dans la rubrique [**glPixelTransfer**](glpixeltransfer.md) , et en partie dans les rubriques relatives aux commandes de pixels et d’images de texture.</span><span class="sxs-lookup"><span data-stu-id="0df0e-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="0df0e-154">Seule la spécification des mappages est décrite dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0df0e-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="0df0e-155">Le paramètre *Map* est un nom de mappage symbolique, indiquant l’un des dix mappages à définir.</span><span class="sxs-lookup"><span data-stu-id="0df0e-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="0df0e-156">Le paramètre *Mapping* spécifie le nombre d’entrées dans le mappage, et les *valeurs* sont un pointeur vers un tableau de valeurs de mappage *de mappage.*</span><span class="sxs-lookup"><span data-stu-id="0df0e-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="0df0e-157">Les entrées d’un mappage peuvent être spécifiées sous la forme de nombres à virgule flottante simple précision, d’entiers courts non signés ou d’entiers longs non signés.</span><span class="sxs-lookup"><span data-stu-id="0df0e-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="0df0e-158">Les mappages qui stockent les valeurs de composant de couleur (toutes les cartes de \_ pixels GL \_ \_ i \_ à \_ i et les \_ \_ cartes de pixels GL \_ \_ en \_ s) conservent leurs valeurs dans un format à virgule flottante, avec la mantisse et les tailles d’exposant non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0df0e-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="0df0e-159">Les valeurs à virgule flottante spécifiées par [**glPixelMapfv**](glpixelmap.md) sont converties directement au format à virgule flottante interne de ces mappages, puis ancrées à la plage \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="0df0e-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="0df0e-160">Les valeurs entières non signées spécifiées par **glPixelMapusv** et **glPixelMapuiv** sont converties de manière linéaire de telle sorte que le plus grand entier pouvant être représenté est mappé à 1,0, et zéro est mappé à 0,0.</span><span class="sxs-lookup"><span data-stu-id="0df0e-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="0df0e-161">Les mappages qui stockent les index, les cartes de \_ pixels GL \_ \_ i \_ à \_ i et les \_ \_ mappages de pixel GL \_ s \_ à \_ s, conservent leurs valeurs dans un format à virgule fixe, avec un nombre non spécifié de bits à droite du point binaire.</span><span class="sxs-lookup"><span data-stu-id="0df0e-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="0df0e-162">Les valeurs à virgule flottante spécifiées par [**glPixelMapfv**](glpixelmap.md) sont converties directement au format à virgule fixe interne de ces mappages.</span><span class="sxs-lookup"><span data-stu-id="0df0e-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="0df0e-163">Les valeurs entières non signées spécifiées par **glPixelMapusv** et **glPixelMapuiv** spécifient des valeurs entières, avec des zéros à droite du point binaire.</span><span class="sxs-lookup"><span data-stu-id="0df0e-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="0df0e-164">Le tableau suivant indique les tailles et les valeurs initiales de chaque mappage.</span><span class="sxs-lookup"><span data-stu-id="0df0e-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="0df0e-165">Les mappages qui sont indexés par des index de couleur ou de stencil doivent avoir la valeur *Mapping* = 2 ^ *n* pour un nombre *n* ou les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="0df0e-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="0df0e-166">La taille maximale autorisée pour chaque mappage dépend de l’implémentation et peut être déterminée en appelant **glGet** à l’aide de la \_ table de correspondance de pixels max. de l’argument GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0df0e-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="0df0e-167">La valeur maximale unique s’applique à tous les mappages et est au moins égale à 32.</span><span class="sxs-lookup"><span data-stu-id="0df0e-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="0df0e-168">Mappage</span><span class="sxs-lookup"><span data-stu-id="0df0e-168">Map</span></span>                      | <span data-ttu-id="0df0e-169">Index de recherche</span><span class="sxs-lookup"><span data-stu-id="0df0e-169">Lookup Index</span></span>  | <span data-ttu-id="0df0e-170">Valeur de recherche</span><span class="sxs-lookup"><span data-stu-id="0df0e-170">Lookup Value</span></span>  | <span data-ttu-id="0df0e-171">Taille initiale</span><span class="sxs-lookup"><span data-stu-id="0df0e-171">Initial Size</span></span> | <span data-ttu-id="0df0e-172">Valeur initiale</span><span class="sxs-lookup"><span data-stu-id="0df0e-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="0df0e-173">\_ \_ carte de pixels \_ GL \_ i \_</span><span class="sxs-lookup"><span data-stu-id="0df0e-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="0df0e-174">index des couleurs</span><span class="sxs-lookup"><span data-stu-id="0df0e-174">color index</span></span>   | <span data-ttu-id="0df0e-175">index des couleurs</span><span class="sxs-lookup"><span data-stu-id="0df0e-175">color index</span></span>   | <span data-ttu-id="0df0e-176">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-176">1</span></span>            | <span data-ttu-id="0df0e-177">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-177">0.0</span></span>           |
| <span data-ttu-id="0df0e-178">\_ \_ cartes de pixels \_ GL \_ sur \_ s</span><span class="sxs-lookup"><span data-stu-id="0df0e-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="0df0e-179">index de stencil</span><span class="sxs-lookup"><span data-stu-id="0df0e-179">stencil index</span></span> | <span data-ttu-id="0df0e-180">index de stencil</span><span class="sxs-lookup"><span data-stu-id="0df0e-180">stencil index</span></span> | <span data-ttu-id="0df0e-181">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-181">1</span></span>            | <span data-ttu-id="0df0e-182">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-182">0.0</span></span>           |
| <span data-ttu-id="0df0e-183">\_ \_ carte de pixels GL \_ I \_ à \_ R</span><span class="sxs-lookup"><span data-stu-id="0df0e-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="0df0e-184">index des couleurs</span><span class="sxs-lookup"><span data-stu-id="0df0e-184">color index</span></span>   | <span data-ttu-id="0df0e-185">R</span><span class="sxs-lookup"><span data-stu-id="0df0e-185">R</span></span>             | <span data-ttu-id="0df0e-186">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-186">1</span></span>            | <span data-ttu-id="0df0e-187">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-187">0.0</span></span>           |
| <span data-ttu-id="0df0e-188">\_ \_ carte de pixels GL \_ I \_ à \_ G</span><span class="sxs-lookup"><span data-stu-id="0df0e-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="0df0e-189">index des couleurs</span><span class="sxs-lookup"><span data-stu-id="0df0e-189">color index</span></span>   | <span data-ttu-id="0df0e-190">G</span><span class="sxs-lookup"><span data-stu-id="0df0e-190">G</span></span>             | <span data-ttu-id="0df0e-191">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-191">1</span></span>            | <span data-ttu-id="0df0e-192">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-192">0.0</span></span>           |
| <span data-ttu-id="0df0e-193">\_ \_ carte de pixels GL \_ I \_ à \_ B</span><span class="sxs-lookup"><span data-stu-id="0df0e-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="0df0e-194">index des couleurs</span><span class="sxs-lookup"><span data-stu-id="0df0e-194">color index</span></span>   | <span data-ttu-id="0df0e-195">B</span><span class="sxs-lookup"><span data-stu-id="0df0e-195">B</span></span>             | <span data-ttu-id="0df0e-196">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-196">1</span></span>            | <span data-ttu-id="0df0e-197">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-197">0.0</span></span>           |
| <span data-ttu-id="0df0e-198">\_ \_ carte de pixels GL \_ I \_ à \_ A</span><span class="sxs-lookup"><span data-stu-id="0df0e-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="0df0e-199">index des couleurs</span><span class="sxs-lookup"><span data-stu-id="0df0e-199">color index</span></span>   | <span data-ttu-id="0df0e-200">Un</span><span class="sxs-lookup"><span data-stu-id="0df0e-200">A</span></span>             | <span data-ttu-id="0df0e-201">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-201">1</span></span>            | <span data-ttu-id="0df0e-202">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-202">0.0</span></span>           |
| <span data-ttu-id="0df0e-203">\_ \_ carte de pixels GL \_ r \_ vers \_ r</span><span class="sxs-lookup"><span data-stu-id="0df0e-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="0df0e-204">R</span><span class="sxs-lookup"><span data-stu-id="0df0e-204">R</span></span>             | <span data-ttu-id="0df0e-205">R</span><span class="sxs-lookup"><span data-stu-id="0df0e-205">R</span></span>             | <span data-ttu-id="0df0e-206">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-206">1</span></span>            | <span data-ttu-id="0df0e-207">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-207">0.0</span></span>           |
| <span data-ttu-id="0df0e-208">\_ \_ carte de pixels GL \_ g \_ à \_ g</span><span class="sxs-lookup"><span data-stu-id="0df0e-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="0df0e-209">G</span><span class="sxs-lookup"><span data-stu-id="0df0e-209">G</span></span>             | <span data-ttu-id="0df0e-210">G</span><span class="sxs-lookup"><span data-stu-id="0df0e-210">G</span></span>             | <span data-ttu-id="0df0e-211">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-211">1</span></span>            | <span data-ttu-id="0df0e-212">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-212">0.0</span></span>           |
| <span data-ttu-id="0df0e-213">\_ \_ carte de pixels GL \_ b \_ à \_ b</span><span class="sxs-lookup"><span data-stu-id="0df0e-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="0df0e-214">B</span><span class="sxs-lookup"><span data-stu-id="0df0e-214">B</span></span>             | <span data-ttu-id="0df0e-215">B</span><span class="sxs-lookup"><span data-stu-id="0df0e-215">B</span></span>             | <span data-ttu-id="0df0e-216">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-216">1</span></span>            | <span data-ttu-id="0df0e-217">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-217">0.0</span></span>           |
| <span data-ttu-id="0df0e-218">\_mappage de pixel GL \_ \_ a \_ à \_ un</span><span class="sxs-lookup"><span data-stu-id="0df0e-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="0df0e-219">A</span><span class="sxs-lookup"><span data-stu-id="0df0e-219">A</span></span>             | <span data-ttu-id="0df0e-220">A</span><span class="sxs-lookup"><span data-stu-id="0df0e-220">A</span></span>             | <span data-ttu-id="0df0e-221">1</span><span class="sxs-lookup"><span data-stu-id="0df0e-221">1</span></span>            | <span data-ttu-id="0df0e-222">0.0</span><span class="sxs-lookup"><span data-stu-id="0df0e-222">0.0</span></span>           |



 

<span data-ttu-id="0df0e-223">Les fonctions suivantes récupèrent les informations relatives à **glPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="0df0e-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="0df0e-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec arguments GL \_ pixel \_ Map \_ i \_ à \_ i \_ Size</span><span class="sxs-lookup"><span data-stu-id="0df0e-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="0df0e-225">**glGet** avec argument GL de \_ correspondance des pixels \_ \_ \_ en \_ s \_</span><span class="sxs-lookup"><span data-stu-id="0df0e-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="0df0e-226">**glGet** avec argument GL de \_ mappage de pixel \_ \_ I \_ à \_ R \_ taille</span><span class="sxs-lookup"><span data-stu-id="0df0e-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="0df0e-227">**glGet** avec argument GL de \_ cartes de pixels \_ \_ I \_ à \_ G \_ taille</span><span class="sxs-lookup"><span data-stu-id="0df0e-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="0df0e-228">**glGet** avec argument GL \_ pixel \_ Map \_ I \_ à \_ B \_ Size</span><span class="sxs-lookup"><span data-stu-id="0df0e-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="0df0e-229">**glGet** avec argument GL \_ pixel \_ Map \_ I \_ en \_ \_ taille</span><span class="sxs-lookup"><span data-stu-id="0df0e-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="0df0e-230">**glGet** avec argument GL de \_ mappage de pixel \_ \_ r \_ à \_ \_ taille r</span><span class="sxs-lookup"><span data-stu-id="0df0e-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="0df0e-231">**glGet** avec argument GL de \_ mappage de pixel \_ \_ g \_ à \_ g \_ taille</span><span class="sxs-lookup"><span data-stu-id="0df0e-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="0df0e-232">**glGet** avec argument GL \_ pixel \_ carte \_ b \_ à \_ b \_ taille</span><span class="sxs-lookup"><span data-stu-id="0df0e-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="0df0e-233">**glGet** avec argument GL \_ pixel \_ mapper \_ a \_ à \_ une \_ taille</span><span class="sxs-lookup"><span data-stu-id="0df0e-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="0df0e-234">**glGet** avec argument table de la \_ carte de pixels max. GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="0df0e-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="0df0e-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0df0e-235">Requirements</span></span>



| <span data-ttu-id="0df0e-236">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0df0e-236">Requirement</span></span> | <span data-ttu-id="0df0e-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="0df0e-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0df0e-238">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0df0e-238">Minimum supported client</span></span><br/> | <span data-ttu-id="0df0e-239">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0df0e-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0df0e-240">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0df0e-240">Minimum supported server</span></span><br/> | <span data-ttu-id="0df0e-241">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0df0e-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0df0e-242">En-tête</span><span class="sxs-lookup"><span data-stu-id="0df0e-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df0e-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0df0e-244">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0df0e-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="0df0e-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0df0e-246">DLL</span><span class="sxs-lookup"><span data-stu-id="0df0e-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df0e-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df0e-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df0e-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0df0e-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df0e-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0df0e-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0df0e-250">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="0df0e-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="0df0e-251">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="0df0e-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="0df0e-252">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0df0e-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0df0e-253">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="0df0e-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="0df0e-254">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="0df0e-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="0df0e-255">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="0df0e-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="0df0e-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="0df0e-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="0df0e-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="0df0e-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





