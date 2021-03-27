---
title: GetDimensions, (objet texture HLSL DirectX)
description: Obtient des informations sur la taille de la texture. Le bloc de syntaxe affiche tous les paramètres possibles dans la déclaration de méthode. Le tableau de la section Notes montre quels paramètres sont implémentés pour chaque type d’objet texture.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841649"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="5ebe8-105">GetDimensions, (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="5ebe8-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="5ebe8-106">Obtient des informations sur la taille de la texture.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-106">Gets texture size information.</span></span> <span data-ttu-id="5ebe8-107">Le bloc de syntaxe affiche tous les paramètres possibles dans la déclaration de méthode.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="5ebe8-108">Le tableau de la section Notes montre quels paramètres sont implémentés pour chaque type d’objet texture.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebe8-109">void Object. GetDimensions, (UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples);</span><span class="sxs-lookup"><span data-stu-id="5ebe8-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="5ebe8-110">typeX indique qu’il existe deux types possibles : **uint** ou **float**.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ebe8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ebe8-111">Parameters</span></span>



| <span data-ttu-id="5ebe8-112">Élément</span><span class="sxs-lookup"><span data-stu-id="5ebe8-112">Item</span></span>                                                                                                                               | <span data-ttu-id="5ebe8-113">Description</span><span class="sxs-lookup"><span data-stu-id="5ebe8-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebe8-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="5ebe8-115">Tout type d' [objet texture](dx-graphics-hlsl-to-type.md) , à l’exception d’un objet **buffer** .</span><span class="sxs-lookup"><span data-stu-id="5ebe8-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="5ebe8-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="5ebe8-117">\[dans \] un index de base zéro qui identifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="5ebe8-118">Si cet argument n’est pas utilisé, le premier niveau MIP est supposé.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="5ebe8-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Largeur*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="5ebe8-120">\[\]largeur de la texture, en texels.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="5ebe8-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Celle*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="5ebe8-122">\[\]hauteur de la texture, en texels.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="5ebe8-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Html*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="5ebe8-124">\[\]nombre d’éléments dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="5ebe8-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondeur*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="5ebe8-126">\[\]profondeur de la texture, dans les texels.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="5ebe8-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="5ebe8-128">\[\]nombre de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="5ebe8-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="5ebe8-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="5ebe8-130">\[\]nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="5ebe8-131">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5ebe8-131">Return Value</span></span>

<span data-ttu-id="5ebe8-132">None</span><span class="sxs-lookup"><span data-stu-id="5ebe8-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="5ebe8-133">Méthodes surchargées</span><span class="sxs-lookup"><span data-stu-id="5ebe8-133">Overloaded Methods</span></span>

<span data-ttu-id="5ebe8-134">Ce tableau répertorie toutes les différentes versions de la méthode. les versions diffèrent du nombre de paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="5ebe8-135">Notez que pour chaque méthode qui accepte des paramètres entiers, il existe une méthode surchargée qui accepte les paramètres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="5ebe8-136">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="5ebe8-136">Texture-Object Type</span></span> | <span data-ttu-id="5ebe8-137">Paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="5ebe8-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5ebe8-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-138">Texture1D</span></span>           | <span data-ttu-id="5ebe8-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="5ebe8-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-140">Texture1D</span></span>           | <span data-ttu-id="5ebe8-141">Largeur UINT</span><span class="sxs-lookup"><span data-stu-id="5ebe8-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="5ebe8-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-142">Texture1D</span></span>           | <span data-ttu-id="5ebe8-143">UINT MipLevel, largeur float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="5ebe8-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-144">Texture1D</span></span>           | <span data-ttu-id="5ebe8-145">Largeur de la virgule flottante</span><span class="sxs-lookup"><span data-stu-id="5ebe8-145">float Width</span></span>                                                                    |
| <span data-ttu-id="5ebe8-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-146">Texture1DArray</span></span>      | <span data-ttu-id="5ebe8-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="5ebe8-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-148">Texture1DArray</span></span>      | <span data-ttu-id="5ebe8-149">UINT Width, UINT, éléments</span><span class="sxs-lookup"><span data-stu-id="5ebe8-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="5ebe8-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-150">Texture1DArray</span></span>      | <span data-ttu-id="5ebe8-151">UINT MipLevel, largeur float, éléments float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="5ebe8-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-152">Texture1DArray</span></span>      | <span data-ttu-id="5ebe8-153">float Width, float, éléments</span><span class="sxs-lookup"><span data-stu-id="5ebe8-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="5ebe8-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-154">Texture2D</span></span>           | <span data-ttu-id="5ebe8-155">UINT MipLevel, largeur UINT, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="5ebe8-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-156">Texture2D</span></span>           | <span data-ttu-id="5ebe8-157">UINT Width, UINT, hauteur</span><span class="sxs-lookup"><span data-stu-id="5ebe8-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="5ebe8-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-158">Texture2D</span></span>           | <span data-ttu-id="5ebe8-159">UINT MipLevel, largeur float, float height, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="5ebe8-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-160">Texture2D</span></span>           | <span data-ttu-id="5ebe8-161">Largeur float, hauteur float</span><span class="sxs-lookup"><span data-stu-id="5ebe8-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="5ebe8-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-162">Texture2DArray</span></span>      | <span data-ttu-id="5ebe8-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="5ebe8-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-164">Texture2DArray</span></span>      | <span data-ttu-id="5ebe8-165">UINT Width, UINT Height, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="5ebe8-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="5ebe8-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-166">Texture2DArray</span></span>      | <span data-ttu-id="5ebe8-167">UINT MipLevel, largeur float, hauteur float, éléments float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="5ebe8-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-168">Texture2DArray</span></span>      | <span data-ttu-id="5ebe8-169">Largeur float, hauteur float, éléments float</span><span class="sxs-lookup"><span data-stu-id="5ebe8-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="5ebe8-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-170">Texture3D</span></span>           | <span data-ttu-id="5ebe8-171">UINT MipLevel, UINT Width, UINT hauteur, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="5ebe8-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-172">Texture3D</span></span>           | <span data-ttu-id="5ebe8-173">UINT Width, hauteur UINT, profondeur UINT</span><span class="sxs-lookup"><span data-stu-id="5ebe8-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="5ebe8-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-174">Texture3D</span></span>           | <span data-ttu-id="5ebe8-175">UINT MipLevel, largeur float, hauteur float, profondeur float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="5ebe8-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="5ebe8-176">Texture3D</span></span>           | <span data-ttu-id="5ebe8-177">Largeur float, hauteur float, profondeur float</span><span class="sxs-lookup"><span data-stu-id="5ebe8-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="5ebe8-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5ebe8-178">TextureCube</span></span>         | <span data-ttu-id="5ebe8-179">UINT MipLevel, largeur UINT, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="5ebe8-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5ebe8-180">TextureCube</span></span>         | <span data-ttu-id="5ebe8-181">UINT Width, UINT, hauteur</span><span class="sxs-lookup"><span data-stu-id="5ebe8-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="5ebe8-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5ebe8-182">TextureCube</span></span>         | <span data-ttu-id="5ebe8-183">UINT MipLevel, largeur float, float height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="5ebe8-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="5ebe8-184">TextureCube</span></span>         | <span data-ttu-id="5ebe8-185">Largeur float, hauteur float</span><span class="sxs-lookup"><span data-stu-id="5ebe8-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="5ebe8-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-186">TextureCubeArray</span></span>    | <span data-ttu-id="5ebe8-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="5ebe8-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-188">TextureCubeArray</span></span>    | <span data-ttu-id="5ebe8-189">UINT Width, UINT Height, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="5ebe8-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="5ebe8-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-190">TextureCubeArray</span></span>    | <span data-ttu-id="5ebe8-191">UINT MipLevel, largeur float, hauteur float, éléments float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="5ebe8-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="5ebe8-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-192">TextureCubeArray</span></span>    | <span data-ttu-id="5ebe8-193">Largeur float, hauteur float, éléments float</span><span class="sxs-lookup"><span data-stu-id="5ebe8-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="5ebe8-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="5ebe8-194">Texture2DMS</span></span>         | <span data-ttu-id="5ebe8-195">UINT Width, UINT Height, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="5ebe8-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="5ebe8-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="5ebe8-196">Texture2DMS</span></span>         | <span data-ttu-id="5ebe8-197">float Width, float height, float Samples</span><span class="sxs-lookup"><span data-stu-id="5ebe8-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="5ebe8-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-198">Texture2DMSArray</span></span>    | <span data-ttu-id="5ebe8-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="5ebe8-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="5ebe8-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="5ebe8-200">Texture2DMSArray</span></span>    | <span data-ttu-id="5ebe8-201">Floating largeur, float height, float Elements, float Samples</span><span class="sxs-lookup"><span data-stu-id="5ebe8-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ebe8-202">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5ebe8-202">Minimum Shader Model</span></span>

<span data-ttu-id="5ebe8-203">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5ebe8-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ebe8-204">vs\_4\_0</span></span> | <span data-ttu-id="5ebe8-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5ebe8-205">vs\_4\_1</span></span>  | <span data-ttu-id="5ebe8-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ebe8-206">ps\_4\_0</span></span> | <span data-ttu-id="5ebe8-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5ebe8-207">ps\_4\_1</span></span>  | <span data-ttu-id="5ebe8-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ebe8-208">gs\_4\_0</span></span> | <span data-ttu-id="5ebe8-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="5ebe8-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="5ebe8-210">x</span><span class="sxs-lookup"><span data-stu-id="5ebe8-210">x</span></span>        | <span data-ttu-id="5ebe8-211">x</span><span class="sxs-lookup"><span data-stu-id="5ebe8-211">x</span></span>         | <span data-ttu-id="5ebe8-212">x</span><span class="sxs-lookup"><span data-stu-id="5ebe8-212">x</span></span>        | <span data-ttu-id="5ebe8-213">x</span><span class="sxs-lookup"><span data-stu-id="5ebe8-213">x</span></span>         | <span data-ttu-id="5ebe8-214">x</span><span class="sxs-lookup"><span data-stu-id="5ebe8-214">x</span></span>        | <span data-ttu-id="5ebe8-215">x</span><span class="sxs-lookup"><span data-stu-id="5ebe8-215">x</span></span>         |



 

1.  <span data-ttu-id="5ebe8-216">Retourne des dimensions pour le plus grand niveau de mipmap (avant toute chose).</span><span class="sxs-lookup"><span data-stu-id="5ebe8-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="5ebe8-217">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="5ebe8-218">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5ebe8-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ebe8-219">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ebe8-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ebe8-220">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="5ebe8-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





