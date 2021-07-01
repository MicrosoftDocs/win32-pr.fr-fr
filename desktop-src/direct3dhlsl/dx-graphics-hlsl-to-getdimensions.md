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
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119835"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="da395-105">GetDimensions, (objet texture HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="da395-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="da395-106">Obtient des informations sur la taille de la texture.</span><span class="sxs-lookup"><span data-stu-id="da395-106">Gets texture size information.</span></span> <span data-ttu-id="da395-107">Le bloc de syntaxe affiche tous les paramètres possibles dans la déclaration de méthode.</span><span class="sxs-lookup"><span data-stu-id="da395-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="da395-108">Le tableau de la section Notes montre quels paramètres sont implémentés pour chaque type d’objet texture.</span><span class="sxs-lookup"><span data-stu-id="da395-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>

<span data-ttu-id="da395-109">void Object. GetDimensions, (UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples);</span><span class="sxs-lookup"><span data-stu-id="da395-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span>



 

<span data-ttu-id="da395-110">typeX indique qu’il existe deux types possibles : **uint** ou **float**.</span><span class="sxs-lookup"><span data-stu-id="da395-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="da395-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da395-111">Parameters</span></span>



| <span data-ttu-id="da395-112">Élément</span><span class="sxs-lookup"><span data-stu-id="da395-112">Item</span></span>                                                                                                                               | <span data-ttu-id="da395-113">Description</span><span class="sxs-lookup"><span data-stu-id="da395-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da395-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Dessin*</span><span class="sxs-lookup"><span data-stu-id="da395-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="da395-115">Tout type d' [objet texture](dx-graphics-hlsl-to-type.md) , à l’exception d’un objet **buffer** .</span><span class="sxs-lookup"><span data-stu-id="da395-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="da395-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="da395-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="da395-117">\[dans \] un index de base zéro qui identifie le niveau de mipmap.</span><span class="sxs-lookup"><span data-stu-id="da395-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="da395-118">Si cet argument n’est pas utilisé, le premier niveau MIP est supposé.</span><span class="sxs-lookup"><span data-stu-id="da395-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="da395-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Largeur*</span><span class="sxs-lookup"><span data-stu-id="da395-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="da395-120">\[\]largeur de la texture, en texels.</span><span class="sxs-lookup"><span data-stu-id="da395-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="da395-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Celle*</span><span class="sxs-lookup"><span data-stu-id="da395-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="da395-122">\[\]hauteur de la texture, en texels.</span><span class="sxs-lookup"><span data-stu-id="da395-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="da395-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Html*</span><span class="sxs-lookup"><span data-stu-id="da395-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="da395-124">\[\]nombre d’éléments dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="da395-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="da395-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondeur*</span><span class="sxs-lookup"><span data-stu-id="da395-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="da395-126">\[\]profondeur de la texture, dans les texels.</span><span class="sxs-lookup"><span data-stu-id="da395-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="da395-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="da395-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="da395-128">\[\]nombre de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="da395-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="da395-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="da395-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="da395-130">\[\]nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="da395-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="da395-131">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="da395-131">Return Value</span></span>

<span data-ttu-id="da395-132">None</span><span class="sxs-lookup"><span data-stu-id="da395-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="da395-133">Méthodes surchargées</span><span class="sxs-lookup"><span data-stu-id="da395-133">Overloaded Methods</span></span>

<span data-ttu-id="da395-134">Ce tableau répertorie toutes les différentes versions de la méthode. les versions diffèrent du nombre de paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="da395-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="da395-135">Notez que pour chaque méthode qui accepte des paramètres entiers, il existe une méthode surchargée qui accepte les paramètres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="da395-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="da395-136">Type de Texture-Object</span><span class="sxs-lookup"><span data-stu-id="da395-136">Texture-Object Type</span></span> | <span data-ttu-id="da395-137">Paramètres d’entrée</span><span class="sxs-lookup"><span data-stu-id="da395-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="da395-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="da395-138">Texture1D</span></span>           | <span data-ttu-id="da395-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="da395-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="da395-140">Texture1D</span></span>           | <span data-ttu-id="da395-141">Largeur UINT</span><span class="sxs-lookup"><span data-stu-id="da395-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="da395-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="da395-142">Texture1D</span></span>           | <span data-ttu-id="da395-143">UINT MipLevel, largeur float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="da395-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="da395-144">Texture1D</span></span>           | <span data-ttu-id="da395-145">Largeur de la virgule flottante</span><span class="sxs-lookup"><span data-stu-id="da395-145">float Width</span></span>                                                                    |
| <span data-ttu-id="da395-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="da395-146">Texture1DArray</span></span>      | <span data-ttu-id="da395-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="da395-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="da395-148">Texture1DArray</span></span>      | <span data-ttu-id="da395-149">UINT Width, UINT, éléments</span><span class="sxs-lookup"><span data-stu-id="da395-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="da395-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="da395-150">Texture1DArray</span></span>      | <span data-ttu-id="da395-151">UINT MipLevel, largeur float, éléments float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="da395-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="da395-152">Texture1DArray</span></span>      | <span data-ttu-id="da395-153">float Width, float, éléments</span><span class="sxs-lookup"><span data-stu-id="da395-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="da395-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="da395-154">Texture2D</span></span>           | <span data-ttu-id="da395-155">UINT MipLevel, largeur UINT, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="da395-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="da395-156">Texture2D</span></span>           | <span data-ttu-id="da395-157">UINT Width, UINT, hauteur</span><span class="sxs-lookup"><span data-stu-id="da395-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="da395-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="da395-158">Texture2D</span></span>           | <span data-ttu-id="da395-159">UINT MipLevel, largeur float, float height, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="da395-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="da395-160">Texture2D</span></span>           | <span data-ttu-id="da395-161">Largeur float, hauteur float</span><span class="sxs-lookup"><span data-stu-id="da395-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="da395-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="da395-162">Texture2DArray</span></span>      | <span data-ttu-id="da395-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="da395-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="da395-164">Texture2DArray</span></span>      | <span data-ttu-id="da395-165">UINT Width, UINT Height, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="da395-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="da395-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="da395-166">Texture2DArray</span></span>      | <span data-ttu-id="da395-167">UINT MipLevel, largeur float, hauteur float, éléments float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="da395-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="da395-168">Texture2DArray</span></span>      | <span data-ttu-id="da395-169">Largeur float, hauteur float, éléments float</span><span class="sxs-lookup"><span data-stu-id="da395-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="da395-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="da395-170">Texture3D</span></span>           | <span data-ttu-id="da395-171">UINT MipLevel, UINT Width, UINT hauteur, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="da395-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="da395-172">Texture3D</span></span>           | <span data-ttu-id="da395-173">UINT Width, hauteur UINT, profondeur UINT</span><span class="sxs-lookup"><span data-stu-id="da395-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="da395-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="da395-174">Texture3D</span></span>           | <span data-ttu-id="da395-175">UINT MipLevel, largeur float, hauteur float, profondeur float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="da395-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="da395-176">Texture3D</span></span>           | <span data-ttu-id="da395-177">Largeur float, hauteur float, profondeur float</span><span class="sxs-lookup"><span data-stu-id="da395-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="da395-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="da395-178">TextureCube</span></span>         | <span data-ttu-id="da395-179">UINT MipLevel, largeur UINT, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="da395-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="da395-180">TextureCube</span></span>         | <span data-ttu-id="da395-181">UINT Width, UINT, hauteur</span><span class="sxs-lookup"><span data-stu-id="da395-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="da395-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="da395-182">TextureCube</span></span>         | <span data-ttu-id="da395-183">UINT MipLevel, largeur float, float height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="da395-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="da395-184">TextureCube</span></span>         | <span data-ttu-id="da395-185">Largeur float, hauteur float</span><span class="sxs-lookup"><span data-stu-id="da395-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="da395-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="da395-186">TextureCubeArray</span></span>    | <span data-ttu-id="da395-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="da395-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="da395-188">TextureCubeArray</span></span>    | <span data-ttu-id="da395-189">UINT Width, UINT Height, UINT Elements</span><span class="sxs-lookup"><span data-stu-id="da395-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="da395-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="da395-190">TextureCubeArray</span></span>    | <span data-ttu-id="da395-191">UINT MipLevel, largeur float, hauteur float, éléments float, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="da395-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="da395-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="da395-192">TextureCubeArray</span></span>    | <span data-ttu-id="da395-193">Largeur float, hauteur float, éléments float</span><span class="sxs-lookup"><span data-stu-id="da395-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="da395-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="da395-194">Texture2DMS</span></span>         | <span data-ttu-id="da395-195">UINT Width, UINT Height, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="da395-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="da395-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="da395-196">Texture2DMS</span></span>         | <span data-ttu-id="da395-197">float Width, float height, float Samples</span><span class="sxs-lookup"><span data-stu-id="da395-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="da395-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="da395-198">Texture2DMSArray</span></span>    | <span data-ttu-id="da395-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span><span class="sxs-lookup"><span data-stu-id="da395-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="da395-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="da395-200">Texture2DMSArray</span></span>    | <span data-ttu-id="da395-201">Floating largeur, float height, float Elements, float Samples</span><span class="sxs-lookup"><span data-stu-id="da395-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="da395-202">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="da395-202">Minimum Shader Model</span></span>

<span data-ttu-id="da395-203">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="da395-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="da395-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da395-204">vs\_4\_0</span></span> | <span data-ttu-id="da395-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="da395-205">vs\_4\_1</span></span>  | <span data-ttu-id="da395-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da395-206">ps\_4\_0</span></span> | <span data-ttu-id="da395-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="da395-207">ps\_4\_1</span></span>  | <span data-ttu-id="da395-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="da395-208">gs\_4\_0</span></span> | <span data-ttu-id="da395-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="da395-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="da395-210">x</span><span class="sxs-lookup"><span data-stu-id="da395-210">x</span></span>        | <span data-ttu-id="da395-211">x</span><span class="sxs-lookup"><span data-stu-id="da395-211">x</span></span>         | <span data-ttu-id="da395-212">x</span><span class="sxs-lookup"><span data-stu-id="da395-212">x</span></span>        | <span data-ttu-id="da395-213">x</span><span class="sxs-lookup"><span data-stu-id="da395-213">x</span></span>         | <span data-ttu-id="da395-214">x</span><span class="sxs-lookup"><span data-stu-id="da395-214">x</span></span>        | <span data-ttu-id="da395-215">x</span><span class="sxs-lookup"><span data-stu-id="da395-215">x</span></span>         |



 

1.  <span data-ttu-id="da395-216">Retourne des dimensions pour le plus grand niveau de mipmap (avant toute chose).</span><span class="sxs-lookup"><span data-stu-id="da395-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="da395-217">TextureCubeArray est disponible dans le nuancier modèle 4,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="da395-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="da395-218">Le modèle de nuanceur 4,1 est disponible dans Direct3D 10,1 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="da395-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da395-219">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da395-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da395-220">Texture-objet</span><span class="sxs-lookup"><span data-stu-id="da395-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





