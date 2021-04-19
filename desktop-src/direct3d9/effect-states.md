---
description: Les États d’effet sont utilisés pour initialiser les États de pipeline en préparation du traitement des vertex et des pixels.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: États d’effet (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314762"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="5f378-103">États d’effet (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5f378-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="5f378-104">Les États d’effet sont utilisés pour initialiser les États de pipeline en préparation du traitement des vertex et des pixels.</span><span class="sxs-lookup"><span data-stu-id="5f378-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="5f378-105">Où :</span><span class="sxs-lookup"><span data-stu-id="5f378-105">Where:</span></span>

-   <span data-ttu-id="5f378-106">État d’effet : similaire aux États de pipeline de fonction fixe traditionnels.</span><span class="sxs-lookup"><span data-stu-id="5f378-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="5f378-107">La liste complète des États est fournie ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5f378-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="5f378-108">\[\[ \] index \] -Index entier facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f378-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="5f378-109">L’index identifie un état particulier dans un tableau d’États d’effet.</span><span class="sxs-lookup"><span data-stu-id="5f378-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="5f378-110">Les crochets externes indiquent qu’un index est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f378-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="5f378-111">Si un index est utilisé, veillez à utiliser les crochets intérieurs.</span><span class="sxs-lookup"><span data-stu-id="5f378-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="5f378-112">expression d’assignation d’état d’expression.</span><span class="sxs-lookup"><span data-stu-id="5f378-112">expression - State assignment expression.</span></span> <span data-ttu-id="5f378-113">Consultez [expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="5f378-114">Chaque État a un type de données natif.</span><span class="sxs-lookup"><span data-stu-id="5f378-114">Each state has a native data type.</span></span> <span data-ttu-id="5f378-115">Il s’agit du type de données dans lequel l’État attend des valeurs lorsque l’effet les affecte.</span><span class="sxs-lookup"><span data-stu-id="5f378-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="5f378-116">Les types de données attendus par chaque État sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5f378-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="5f378-117">Notez que l’interface Effect tentera d’effectuer un cast des valeurs vers le type approprié le plus tôt possible.</span><span class="sxs-lookup"><span data-stu-id="5f378-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="5f378-118">Les valeurs littérales peuvent être converties au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="5f378-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="5f378-119">Les non-littéraux (c’est-à-dire les variables régulières) doivent être convertis lorsque les méthodes Set appropriées sont appelées.</span><span class="sxs-lookup"><span data-stu-id="5f378-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="5f378-120">Par exemple, l’interface Effect effectue un cast des valeurs définies à l’aide de [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)et d’autres fonctions similaires, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5f378-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="5f378-121">Pour de meilleures performances, assurez-vous que les valeurs passées à l’interface Effect sont déjà du type correct et n’auront pas besoin d’être castées.</span><span class="sxs-lookup"><span data-stu-id="5f378-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="5f378-122">Si le runtime ne parvient pas à effectuer un cast d’une valeur, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="5f378-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="5f378-123">Les États d’effet peuvent être répartis dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f378-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="5f378-124">États légers</span><span class="sxs-lookup"><span data-stu-id="5f378-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="5f378-125">États du matériau</span><span class="sxs-lookup"><span data-stu-id="5f378-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="5f378-126">États de rendu</span><span class="sxs-lookup"><span data-stu-id="5f378-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="5f378-127">États de rendu de canal de pixels</span><span class="sxs-lookup"><span data-stu-id="5f378-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="5f378-128">États de rendu du canal de vertex</span><span class="sxs-lookup"><span data-stu-id="5f378-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="5f378-129">États de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="5f378-130">États des étapes de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="5f378-131">États du nuanceur</span><span class="sxs-lookup"><span data-stu-id="5f378-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="5f378-132">États constants du nuanceur</span><span class="sxs-lookup"><span data-stu-id="5f378-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="5f378-133">États de la texture</span><span class="sxs-lookup"><span data-stu-id="5f378-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="5f378-134">États des étapes de texture</span><span class="sxs-lookup"><span data-stu-id="5f378-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="5f378-135">États de la transformation</span><span class="sxs-lookup"><span data-stu-id="5f378-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="5f378-136">États légers</span><span class="sxs-lookup"><span data-stu-id="5f378-136">Light States</span></span>

<span data-ttu-id="5f378-137">Pour activer les meilleures performances pour appliquer un effet, tous les composants d’une lumière ou d’un matériau doivent être spécifiés dans le fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="5f378-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="5f378-138">Les États que vous ne pouvez pas déclarer sont définis sur une valeur par défaut, car il n’existe aucun moyen pour Direct3D de définir les États légers individuellement.</span><span class="sxs-lookup"><span data-stu-id="5f378-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f378-139">État clair</span><span class="sxs-lookup"><span data-stu-id="5f378-139">Light State</span></span>            | <span data-ttu-id="5f378-140">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-140">Type</span></span>   | <span data-ttu-id="5f378-141">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="5f378-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="5f378-143">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-143">float4</span></span> | <span data-ttu-id="5f378-144">Consultez le membre ambiant de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="5f378-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="5f378-146">float</span><span class="sxs-lookup"><span data-stu-id="5f378-146">float</span></span>  | <span data-ttu-id="5f378-147">Consultez le membre Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="5f378-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="5f378-149">float</span><span class="sxs-lookup"><span data-stu-id="5f378-149">float</span></span>  | <span data-ttu-id="5f378-150">Consultez le membre Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="5f378-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="5f378-152">float</span><span class="sxs-lookup"><span data-stu-id="5f378-152">float</span></span>  | <span data-ttu-id="5f378-153">Consultez le membre Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="5f378-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="5f378-155">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-155">float4</span></span> | <span data-ttu-id="5f378-156">Consultez le membre diffus de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="5f378-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="5f378-158">float3</span><span class="sxs-lookup"><span data-stu-id="5f378-158">float3</span></span> | <span data-ttu-id="5f378-159">Consultez le membre direction de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="5f378-160">\[N\]</span><span class="sxs-lookup"><span data-stu-id="5f378-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="5f378-161">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-161">bool</span></span>   | <span data-ttu-id="5f378-162">**True** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="5f378-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="5f378-163">Consultez l’argument bEnable dans [**Eclaircir**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="5f378-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="5f378-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="5f378-165">float</span><span class="sxs-lookup"><span data-stu-id="5f378-165">float</span></span>  | <span data-ttu-id="5f378-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="5f378-167">Consultez le membre de retrait de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="5f378-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="5f378-169">float</span><span class="sxs-lookup"><span data-stu-id="5f378-169">float</span></span>  | <span data-ttu-id="5f378-170">Consultez le membre Phi de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="5f378-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="5f378-172">float3</span><span class="sxs-lookup"><span data-stu-id="5f378-172">float3</span></span> | <span data-ttu-id="5f378-173">Consultez le membre position de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="5f378-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-174">LightRange\[n\]</span></span>        | <span data-ttu-id="5f378-175">float</span><span class="sxs-lookup"><span data-stu-id="5f378-175">float</span></span>  | <span data-ttu-id="5f378-176">Consultez le membre de plage de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="5f378-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="5f378-178">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-178">float4</span></span> | <span data-ttu-id="5f378-179">Consultez le membre spéculaire de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="5f378-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="5f378-181">float</span><span class="sxs-lookup"><span data-stu-id="5f378-181">float</span></span>  | <span data-ttu-id="5f378-182">Consultez le membre thêta de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="5f378-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="5f378-183">LightType\[n\]</span></span>         | <span data-ttu-id="5f378-184">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-184">dword</span></span>  | <span data-ttu-id="5f378-185">Même valeur que le tableau de n valeurs jusqu’à n [**D3DLIGHTTYPE**](./d3dlighttype.md) sans le \_ préfixe D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="5f378-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="5f378-186">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5f378-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="5f378-187">Cela permet d’activer l’éclairage, d’éclairer le type, de définir la position de la lumière sur float3<10.0 f, 1.0 f, 23.0 f> et de définir la couleur ambiante sur float4<0,7 f, 0.0 f, 0.0 f, 1.0 f>.</span><span class="sxs-lookup"><span data-stu-id="5f378-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="5f378-188">États du matériau</span><span class="sxs-lookup"><span data-stu-id="5f378-188">Material States</span></span>

<span data-ttu-id="5f378-189">Les États que vous ne pouvez pas déclarer sont définis sur une valeur par défaut, car il n’existe aucun moyen pour Direct3D de définir des États de matériau individuellement.</span><span class="sxs-lookup"><span data-stu-id="5f378-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="5f378-190">État du matériau</span><span class="sxs-lookup"><span data-stu-id="5f378-190">Material State</span></span>   | <span data-ttu-id="5f378-191">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-191">Type</span></span>   | <span data-ttu-id="5f378-192">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-192">Values</span></span>                                         |
| <span data-ttu-id="5f378-193">Propriétés matériau</span><span class="sxs-lookup"><span data-stu-id="5f378-193">MaterialAmbient</span></span>  | <span data-ttu-id="5f378-194">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-194">float4</span></span> | <span data-ttu-id="5f378-195">Même valeur que l' [ **ambiant**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="5f378-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="5f378-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="5f378-196">MaterialDiffuse</span></span>  | <span data-ttu-id="5f378-197">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-197">float4</span></span> | <span data-ttu-id="5f378-198">Valeur identique à la [ **diffusion**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="5f378-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="5f378-199">Matériau émissif</span><span class="sxs-lookup"><span data-stu-id="5f378-199">MaterialEmissive</span></span> | <span data-ttu-id="5f378-200">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-200">float4</span></span> | <span data-ttu-id="5f378-201">Même valeur que [ **émissif**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="5f378-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="5f378-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="5f378-202">MaterialPower</span></span>    | <span data-ttu-id="5f378-203">float</span><span class="sxs-lookup"><span data-stu-id="5f378-203">float</span></span>  | <span data-ttu-id="5f378-204">Même valeur que l' [ **alimentation**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="5f378-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="5f378-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="5f378-205">MaterialSpecular</span></span> | <span data-ttu-id="5f378-206">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-206">float4</span></span> | <span data-ttu-id="5f378-207">Même valeur que [ **spéculaire**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="5f378-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="5f378-208">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5f378-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="5f378-209">Cela permet de définir la couleur diffuse sur float4<0,7 f, 0.0 f, 0.0 f, 1.0 f> et de rendre la puissance de la documentation 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="5f378-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="5f378-210">États de rendu</span><span class="sxs-lookup"><span data-stu-id="5f378-210">Render States</span></span>

<span data-ttu-id="5f378-211">Il existe deux types d’États de rendu :</span><span class="sxs-lookup"><span data-stu-id="5f378-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="5f378-212">États de rendu de canal de pixels</span><span class="sxs-lookup"><span data-stu-id="5f378-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="5f378-213">États de rendu du canal de vertex</span><span class="sxs-lookup"><span data-stu-id="5f378-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="5f378-214">États de rendu de canal de pixels</span><span class="sxs-lookup"><span data-stu-id="5f378-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="5f378-215">Les États de rendu des fichiers Effects ont des noms semblables aux États de pipeline de fonction fixe, souvent avec le préfixe supprimé.</span><span class="sxs-lookup"><span data-stu-id="5f378-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f378-216">État du rendu</span><span class="sxs-lookup"><span data-stu-id="5f378-216">Render State</span></span></td>
<td><span data-ttu-id="5f378-217">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-217">Type</span></span></td>
<td><span data-ttu-id="5f378-218">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="5f378-220">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-220">bool</span></span></td>
<td><span data-ttu-id="5f378-221">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-221">True or False.</span></span> <span data-ttu-id="5f378-222">Mêmes valeurs que D3DRS_ALPHABLENDENABLE dans <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5f378-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="5f378-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="5f378-224">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-224">dword</span></span></td>
<td><span data-ttu-id="5f378-225">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sans le préfixe D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="5f378-226">Consultez D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="5f378-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="5f378-227">AlphaRef</span></span></td>
<td><span data-ttu-id="5f378-228">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-228">dword</span></span></td>
<td><span data-ttu-id="5f378-229">Mêmes valeurs que D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="5f378-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="5f378-231">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-231">dword</span></span></td>
<td><span data-ttu-id="5f378-232">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-232">True or False.</span></span> <span data-ttu-id="5f378-233">Consultez D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="5f378-234">BlendOp</span></span></td>
<td><span data-ttu-id="5f378-235">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-235">dword</span></span></td>
<td><span data-ttu-id="5f378-236">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sans le préfixe D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="5f378-238">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-238">dword</span></span></td>
<td><span data-ttu-id="5f378-239">Combinaison d’opérations de bits de RED | VERT | BLEU | Lettres.</span><span class="sxs-lookup"><span data-stu-id="5f378-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="5f378-240">Consultez D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="5f378-241">DepthBias</span></span></td>
<td><span data-ttu-id="5f378-242">float</span><span class="sxs-lookup"><span data-stu-id="5f378-242">float</span></span></td>
<td><span data-ttu-id="5f378-243">Mêmes valeurs que D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="5f378-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="5f378-244">DestBlend</span></span></td>
<td><span data-ttu-id="5f378-245">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-245">dword</span></span></td>
<td><span data-ttu-id="5f378-246">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sans le préfixe D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="5f378-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-247">DitherEnable</span></span></td>
<td><span data-ttu-id="5f378-248">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-248">bool</span></span></td>
<td><span data-ttu-id="5f378-249">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-249">True or False.</span></span> <span data-ttu-id="5f378-250">Mêmes valeurs que D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="5f378-251">FillMode</span></span></td>
<td><span data-ttu-id="5f378-252">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-252">dword</span></span></td>
<td><span data-ttu-id="5f378-253">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sans le préfixe D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="5f378-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="5f378-254">LastPixel</span></span></td>
<td><span data-ttu-id="5f378-255">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-255">dword</span></span></td>
<td><span data-ttu-id="5f378-256">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-256">True or False.</span></span> <span data-ttu-id="5f378-257">Consultez D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="5f378-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-258">ShadeMode</span><span class="sxs-lookup"><span data-stu-id="5f378-258">ShadeMode</span></span></td>
<td><span data-ttu-id="5f378-259">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-259">dword</span></span></td>
<td><span data-ttu-id="5f378-260">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sans le préfixe D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="5f378-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="5f378-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="5f378-262">float</span><span class="sxs-lookup"><span data-stu-id="5f378-262">float</span></span></td>
<td><span data-ttu-id="5f378-263">Mêmes valeurs que D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="5f378-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="5f378-264">SrcBlend</span></span></td>
<td><span data-ttu-id="5f378-265">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-265">dword</span></span></td>
<td><span data-ttu-id="5f378-266">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sans le préfixe D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="5f378-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="5f378-268">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-268">bool</span></span></td>
<td><span data-ttu-id="5f378-269">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-269">True or False.</span></span> <span data-ttu-id="5f378-270">Mêmes valeurs que D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-271">StencilEnable</span></span></td>
<td><span data-ttu-id="5f378-272">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-272">bool</span></span></td>
<td><span data-ttu-id="5f378-273">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-273">True or False.</span></span> <span data-ttu-id="5f378-274">Mêmes valeurs que D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="5f378-275">StencilFail</span></span></td>
<td><span data-ttu-id="5f378-276">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-276">dword</span></span></td>
<td><span data-ttu-id="5f378-277">Mêmes valeurs que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sans le préfixe D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="5f378-278">Consultez D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="5f378-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="5f378-279">StencilFunc</span></span></td>
<td><span data-ttu-id="5f378-280">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-280">dword</span></span></td>
<td><span data-ttu-id="5f378-281">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sans le préfixe D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="5f378-282">Consultez D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="5f378-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="5f378-283">StencilMask</span></span></td>
<td><span data-ttu-id="5f378-284">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-284">dword</span></span></td>
<td><span data-ttu-id="5f378-285">Mêmes valeurs que D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="5f378-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="5f378-286">StencilPass</span></span></td>
<td><span data-ttu-id="5f378-287">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-287">dword</span></span></td>
<td><span data-ttu-id="5f378-288">Mêmes valeurs que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sans le préfixe D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="5f378-289">Consultez D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="5f378-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="5f378-290">StencilRef</span></span></td>
<td><span data-ttu-id="5f378-291">int</span><span class="sxs-lookup"><span data-stu-id="5f378-291">int</span></span></td>
<td><span data-ttu-id="5f378-292">Mêmes valeurs que D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="5f378-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="5f378-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="5f378-294">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-294">dword</span></span></td>
<td><span data-ttu-id="5f378-295">Mêmes valeurs que D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="5f378-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="5f378-296">StencilZFail</span></span></td>
<td><span data-ttu-id="5f378-297">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-297">dword</span></span></td>
<td><span data-ttu-id="5f378-298">Mêmes valeurs que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sans le préfixe D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="5f378-299">Consultez D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="5f378-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="5f378-300">TextureFactor</span></span></td>
<td><span data-ttu-id="5f378-301">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-301">dword</span></span></td>
<td><span data-ttu-id="5f378-302">Mêmes valeurs que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5f378-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="5f378-303">Mêmes valeurs que D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="5f378-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="5f378-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="5f378-305">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-305">dword</span></span></td>
<td><span data-ttu-id="5f378-306">Les valeurs sont les mêmes que les valeurs utilisées par D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="5f378-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="5f378-307">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="5f378-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="5f378-308">COORD0 (qui correspond à D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="5f378-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="5f378-309">COORD1 (qui correspond à D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="5f378-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="5f378-310">COORD2 (qui correspond à D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="5f378-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="5f378-311">COORD3 (qui correspond à D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="5f378-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="5f378-312">U (qui correspond à D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="5f378-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="5f378-313">V (qui correspond à D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="5f378-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="5f378-314">W (qui correspond à D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="5f378-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-315">ZEnable</span></span></td>
<td><span data-ttu-id="5f378-316">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-316">dword</span></span></td>
<td><span data-ttu-id="5f378-317">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sans le préfixe D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="5f378-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f378-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="5f378-318">ZFunc</span></span></td>
<td><span data-ttu-id="5f378-319">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-319">dword</span></span></td>
<td><span data-ttu-id="5f378-320">Mêmes valeurs que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sans le préfixe D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="5f378-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="5f378-321">Consultez D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="5f378-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f378-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="5f378-323">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-323">bool</span></span></td>
<td><span data-ttu-id="5f378-324">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-324">True or False.</span></span> <span data-ttu-id="5f378-325">Consultez D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5f378-326">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5f378-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="5f378-327">Cela active la fusion alpha et rend toutes les géométries affichées en filaire.</span><span class="sxs-lookup"><span data-stu-id="5f378-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="5f378-328">États de rendu du canal de vertex</span><span class="sxs-lookup"><span data-stu-id="5f378-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="5f378-329">Les États de rendu des fichiers Effects ont des noms semblables aux États de pipeline de fonction fixe, souvent avec le préfixe supprimé.</span><span class="sxs-lookup"><span data-stu-id="5f378-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f378-330">État du rendu</span><span class="sxs-lookup"><span data-stu-id="5f378-330">Render State</span></span>             | <span data-ttu-id="5f378-331">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-331">Type</span></span>   | <span data-ttu-id="5f378-332">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-332">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="5f378-333">Ambiant</span><span class="sxs-lookup"><span data-stu-id="5f378-333">Ambient</span></span>                  | <span data-ttu-id="5f378-334">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-334">float4</span></span> | <span data-ttu-id="5f378-335">Mêmes valeurs que D3DRS \_ ambiant.</span><span class="sxs-lookup"><span data-stu-id="5f378-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="5f378-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="5f378-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="5f378-337">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-337">dword</span></span>  | <span data-ttu-id="5f378-338">Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="5f378-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="5f378-339">Consultez D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="5f378-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="5f378-340">Portion</span><span class="sxs-lookup"><span data-stu-id="5f378-340">Clipping</span></span>                 | <span data-ttu-id="5f378-341">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-341">bool</span></span>   | <span data-ttu-id="5f378-342">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-342">True or False.</span></span> <span data-ttu-id="5f378-343">Mêmes valeurs que le \_ découpage D3DRS.</span><span class="sxs-lookup"><span data-stu-id="5f378-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="5f378-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="5f378-345">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-345">dword</span></span>  | <span data-ttu-id="5f378-346">Combinaison d’opérations de bits de macros D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="5f378-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="5f378-347">Consultez [**D3DCLIPPLANEn**](d3dclipplanen.md) et D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="5f378-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="5f378-348">ColorVertex</span></span>              | <span data-ttu-id="5f378-349">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-349">bool</span></span>   | <span data-ttu-id="5f378-350">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-350">True or False.</span></span> <span data-ttu-id="5f378-351">Mêmes valeurs que D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="5f378-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="5f378-352">CullMode</span><span class="sxs-lookup"><span data-stu-id="5f378-352">CullMode</span></span>                 | <span data-ttu-id="5f378-353">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-353">dword</span></span>  | <span data-ttu-id="5f378-354">Mêmes valeurs que [**D3DCULL**](./d3dcull.md) sans le \_ préfixe D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="5f378-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="5f378-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="5f378-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="5f378-356">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-356">dword</span></span>  | <span data-ttu-id="5f378-357">Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="5f378-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="5f378-358">Consultez D3DRS \_ DIFFUSEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="5f378-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="5f378-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="5f378-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="5f378-360">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-360">dword</span></span>  | <span data-ttu-id="5f378-361">Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="5f378-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="5f378-362">Consultez D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="5f378-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="5f378-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="5f378-363">FogColor</span></span>                 | <span data-ttu-id="5f378-364">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-364">dword</span></span>  | <span data-ttu-id="5f378-365">Mêmes valeurs que [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="5f378-366">Consultez D3DRS \_ FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="5f378-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="5f378-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="5f378-367">FogDensity</span></span>               | <span data-ttu-id="5f378-368">float</span><span class="sxs-lookup"><span data-stu-id="5f378-368">float</span></span>  | <span data-ttu-id="5f378-369">Mêmes valeurs que D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="5f378-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="5f378-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-370">FogEnable</span></span>                | <span data-ttu-id="5f378-371">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-371">bool</span></span>   | <span data-ttu-id="5f378-372">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-372">True or False.</span></span> <span data-ttu-id="5f378-373">Mêmes valeurs que D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="5f378-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="5f378-374">FogEnd</span></span>                   | <span data-ttu-id="5f378-375">float</span><span class="sxs-lookup"><span data-stu-id="5f378-375">float</span></span>  | <span data-ttu-id="5f378-376">Mêmes valeurs que D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="5f378-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="5f378-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="5f378-377">FogStart</span></span>                 | <span data-ttu-id="5f378-378">float</span><span class="sxs-lookup"><span data-stu-id="5f378-378">float</span></span>  | <span data-ttu-id="5f378-379">Mêmes valeurs que D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="5f378-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="5f378-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="5f378-380">FogTableMode</span></span>             | <span data-ttu-id="5f378-381">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-381">dword</span></span>  | <span data-ttu-id="5f378-382">Mêmes valeurs que [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="5f378-383">Consultez D3DRS \_ FOGTABLEMODE dans [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="5f378-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="5f378-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="5f378-384">FogVertexMode</span></span>            | <span data-ttu-id="5f378-385">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-385">dword</span></span>  | <span data-ttu-id="5f378-386">Mêmes valeurs que [**D3DFOGMODE**](./d3dfogmode.md) sans le \_ préfixe D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="5f378-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="5f378-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="5f378-388">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-388">bool</span></span>   | <span data-ttu-id="5f378-389">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-389">True or False.</span></span> <span data-ttu-id="5f378-390">Mêmes valeurs que D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="5f378-391">Éclairage</span><span class="sxs-lookup"><span data-stu-id="5f378-391">Lighting</span></span>                 | <span data-ttu-id="5f378-392">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-392">bool</span></span>   | <span data-ttu-id="5f378-393">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-393">True or False.</span></span> <span data-ttu-id="5f378-394">Mêmes valeurs que l' \_ éclairage D3DRS.</span><span class="sxs-lookup"><span data-stu-id="5f378-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="5f378-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="5f378-395">LocalViewer</span></span>              | <span data-ttu-id="5f378-396">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-396">bool</span></span>   | <span data-ttu-id="5f378-397">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-397">True or False.</span></span> <span data-ttu-id="5f378-398">Mêmes valeurs que D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="5f378-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="5f378-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="5f378-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="5f378-400">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-400">bool</span></span>   | <span data-ttu-id="5f378-401">Mêmes valeurs que D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="5f378-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="5f378-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="5f378-402">MultiSampleMask</span></span>          | <span data-ttu-id="5f378-403">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-403">dword</span></span>  | <span data-ttu-id="5f378-404">Mêmes valeurs que D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="5f378-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="5f378-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="5f378-405">NormalizeNormals</span></span>         | <span data-ttu-id="5f378-406">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-406">bool</span></span>   | <span data-ttu-id="5f378-407">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-407">True or False.</span></span> <span data-ttu-id="5f378-408">Mêmes valeurs que D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="5f378-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="5f378-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="5f378-409">PatchSegments</span></span>            | <span data-ttu-id="5f378-410">float</span><span class="sxs-lookup"><span data-stu-id="5f378-410">float</span></span>  | <span data-ttu-id="5f378-411">Mêmes valeurs que nSegments dans [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="5f378-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="5f378-412">PointScale \_ A</span><span class="sxs-lookup"><span data-stu-id="5f378-412">PointScale\_A</span></span>            | <span data-ttu-id="5f378-413">float</span><span class="sxs-lookup"><span data-stu-id="5f378-413">float</span></span>  | <span data-ttu-id="5f378-414">Mêmes valeurs que D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="5f378-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="5f378-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="5f378-415">PointScale\_B</span></span>            | <span data-ttu-id="5f378-416">float</span><span class="sxs-lookup"><span data-stu-id="5f378-416">float</span></span>  | <span data-ttu-id="5f378-417">Mêmes valeurs que D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="5f378-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="5f378-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="5f378-418">PointScale\_C</span></span>            | <span data-ttu-id="5f378-419">float</span><span class="sxs-lookup"><span data-stu-id="5f378-419">float</span></span>  | <span data-ttu-id="5f378-420">Mêmes valeurs que D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="5f378-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="5f378-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-421">PointScaleEnable</span></span>         | <span data-ttu-id="5f378-422">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-422">bool</span></span>   | <span data-ttu-id="5f378-423">Mêmes valeurs que D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="5f378-424">PointSize</span><span class="sxs-lookup"><span data-stu-id="5f378-424">PointSize</span></span>                | <span data-ttu-id="5f378-425">float</span><span class="sxs-lookup"><span data-stu-id="5f378-425">float</span></span>  | <span data-ttu-id="5f378-426">Les mêmes valeurs que D3DRS sont \_ désignables.</span><span class="sxs-lookup"><span data-stu-id="5f378-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="5f378-427">Repointer \_ min.</span><span class="sxs-lookup"><span data-stu-id="5f378-427">PointSize\_Min</span></span>           | <span data-ttu-id="5f378-428">float</span><span class="sxs-lookup"><span data-stu-id="5f378-428">float</span></span>  | <span data-ttu-id="5f378-429">Les mêmes valeurs que D3DRS \_ redirigent \_ min.</span><span class="sxs-lookup"><span data-stu-id="5f378-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="5f378-430">Délimiter \_ Max.</span><span class="sxs-lookup"><span data-stu-id="5f378-430">PointSize\_Max</span></span>           | <span data-ttu-id="5f378-431">float</span><span class="sxs-lookup"><span data-stu-id="5f378-431">float</span></span>  | <span data-ttu-id="5f378-432">Les mêmes valeurs que D3DRS \_ redirigent \_ Max sans le \_ préfixe D3DRS.</span><span class="sxs-lookup"><span data-stu-id="5f378-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="5f378-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-433">PointSpriteEnable</span></span>        | <span data-ttu-id="5f378-434">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-434">bool</span></span>   | <span data-ttu-id="5f378-435">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-435">True or False.</span></span> <span data-ttu-id="5f378-436">Mêmes valeurs que D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="5f378-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-437">RangeFogEnable</span></span>           | <span data-ttu-id="5f378-438">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-438">bool</span></span>   | <span data-ttu-id="5f378-439">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-439">True or False.</span></span> <span data-ttu-id="5f378-440">Mêmes valeurs que D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="5f378-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="5f378-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="5f378-441">SpecularEnable</span></span>           | <span data-ttu-id="5f378-442">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-442">bool</span></span>   | <span data-ttu-id="5f378-443">True ou False.</span><span class="sxs-lookup"><span data-stu-id="5f378-443">True or False.</span></span> <span data-ttu-id="5f378-444">Mêmes valeurs que D3DRS \_ SpecularEnable.</span><span class="sxs-lookup"><span data-stu-id="5f378-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="5f378-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="5f378-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="5f378-446">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-446">dword</span></span>  | <span data-ttu-id="5f378-447">Mêmes valeurs que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sans le \_ préfixe D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="5f378-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="5f378-448">Consultez D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="5f378-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="5f378-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="5f378-449">TweenFactor</span></span>              | <span data-ttu-id="5f378-450">float</span><span class="sxs-lookup"><span data-stu-id="5f378-450">float</span></span>  | <span data-ttu-id="5f378-451">Mêmes valeurs que D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="5f378-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="5f378-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="5f378-452">VertexBlend</span></span>              | <span data-ttu-id="5f378-453">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-453">dword</span></span>  | <span data-ttu-id="5f378-454">Mêmes valeurs que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sans le \_ préfixe D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="5f378-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="5f378-455">Consultez D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="5f378-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="5f378-456">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5f378-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="5f378-457">Cela rend la couleur ambiante float4<0,7 f, 0.0 f, 0.0 f, 1.0 f>, définir le mode d’élimination des faces arrière pour qu’il s’affiche dans le sens inverse des aiguilles d’une montre et définir la couleur de brouillard sur rouge.</span><span class="sxs-lookup"><span data-stu-id="5f378-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="5f378-458">États de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-458">Sampler States</span></span>

<span data-ttu-id="5f378-459">Un état de l’échantillonneur représente un objet d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="5f378-459">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="5f378-460">State</span><span class="sxs-lookup"><span data-stu-id="5f378-460">State</span></span>   | <span data-ttu-id="5f378-461">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-461">Type</span></span>    | <span data-ttu-id="5f378-462">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-462">Values</span></span>                              |
| <span data-ttu-id="5f378-463">Échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-463">Sampler</span></span> | <span data-ttu-id="5f378-464">échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-464">sampler</span></span> | <span data-ttu-id="5f378-465">**Null**, ou un bloc d’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="5f378-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="5f378-466">États des étapes de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-466">Sampler Stage States</span></span>

<span data-ttu-id="5f378-467">Les États des étapes de l’échantillonneur sont utilisés pour échantillonner les textures.</span><span class="sxs-lookup"><span data-stu-id="5f378-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="5f378-468">L’état de l’échantillonneur détermine les types de filtrage et les modes d’adressage des textures.</span><span class="sxs-lookup"><span data-stu-id="5f378-468">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f378-469">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="5f378-469">Sampler State</span></span>       | <span data-ttu-id="5f378-470">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-470">Type</span></span>                         | <span data-ttu-id="5f378-471">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-471">Values</span></span>                                                                                                                            |
| <span data-ttu-id="5f378-472">Adressed \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-472">AddressU\[16\]</span></span>      | <span data-ttu-id="5f378-473">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-473">dword</span></span>                        | <span data-ttu-id="5f378-474">Mêmes valeurs que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sans le \_ préfixe D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="5f378-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="5f378-475">Consultez D3DSAMP \_ .</span><span class="sxs-lookup"><span data-stu-id="5f378-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="5f378-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-476">AddressV\[16\]</span></span>      | <span data-ttu-id="5f378-477">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-477">dword</span></span>                        | <span data-ttu-id="5f378-478">Mêmes valeurs que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sans le \_ préfixe D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="5f378-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="5f378-479">Consultez D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="5f378-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="5f378-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-480">AddressW\[16\]</span></span>      | <span data-ttu-id="5f378-481">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-481">dword</span></span>                        | <span data-ttu-id="5f378-482">Mêmes valeurs que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sans le \_ préfixe D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="5f378-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="5f378-483">Consultez D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="5f378-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="5f378-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="5f378-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="5f378-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="5f378-486">Mêmes valeurs que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sans le \_ préfixe D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="5f378-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="5f378-487">Consultez D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="5f378-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="5f378-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="5f378-489">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-489">dword</span></span>                        | <span data-ttu-id="5f378-490">Mêmes valeurs que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sans le \_ préfixe D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="5f378-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="5f378-491">Consultez D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="5f378-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="5f378-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="5f378-493">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-493">dword</span></span>                        | <span data-ttu-id="5f378-494">Mêmes valeurs que D3DSAMP \_ MAXANISOTROPY sans le \_ préfixe D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="5f378-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="5f378-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="5f378-496">int</span><span class="sxs-lookup"><span data-stu-id="5f378-496">int</span></span>                          | <span data-ttu-id="5f378-497">Mêmes valeurs que D3DSAMP \_ MAXMIPLEVEL sans le \_ préfixe D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="5f378-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="5f378-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="5f378-499">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-499">dword</span></span>                        | <span data-ttu-id="5f378-500">Mêmes valeurs que D3DSAMP \_ MINFILTER sans le \_ préfixe D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="5f378-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="5f378-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="5f378-502">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-502">dword</span></span>                        | <span data-ttu-id="5f378-503">Mêmes valeurs que D3DSAMP \_ MIPFILTER sans le \_ préfixe D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="5f378-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="5f378-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="5f378-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="5f378-505">float</span><span class="sxs-lookup"><span data-stu-id="5f378-505">float</span></span>                        | <span data-ttu-id="5f378-506">Mêmes valeurs que D3DSAMP \_ MIPMAPLODBIAS sans le \_ préfixe D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="5f378-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="5f378-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="5f378-507">SRGBTexture</span></span>         | <span data-ttu-id="5f378-508">bool</span><span class="sxs-lookup"><span data-stu-id="5f378-508">bool</span></span>                         | <span data-ttu-id="5f378-509">Même valeur que D3DSAMP \_ SRGBTEXTURE sans le \_ préfixe D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="5f378-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="5f378-510">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5f378-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="5f378-511">Les valeurs UVW doivent être comprises entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="5f378-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="5f378-512">États du nuanceur</span><span class="sxs-lookup"><span data-stu-id="5f378-512">Shader States</span></span>

<span data-ttu-id="5f378-513">Il n’y a que deux États de nuanceur d’effet : l’un associé à un objet nuanceur vertex et l’autre à un objet nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5f378-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5f378-514">État du nuanceur</span><span class="sxs-lookup"><span data-stu-id="5f378-514">Shader State</span></span> | <span data-ttu-id="5f378-515">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-515">Type</span></span>         | <span data-ttu-id="5f378-516">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-516">Values</span></span>                                                                      |
| <span data-ttu-id="5f378-517">PixelShader</span><span class="sxs-lookup"><span data-stu-id="5f378-517">PixelShader</span></span>  | <span data-ttu-id="5f378-518">PixelShader</span><span class="sxs-lookup"><span data-stu-id="5f378-518">pixelshader</span></span>  | <span data-ttu-id="5f378-519">**Null**, un bloc d’assembly, une cible de compilation ou un paramètre de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5f378-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="5f378-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="5f378-520">VertexShader</span></span> | <span data-ttu-id="5f378-521">VertexShader</span><span class="sxs-lookup"><span data-stu-id="5f378-521">vertexshader</span></span> | <span data-ttu-id="5f378-522">**Null**, un bloc d’assembly, une cible de compilation ou un paramètre de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="5f378-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="5f378-523">Exemple :</span><span class="sxs-lookup"><span data-stu-id="5f378-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="5f378-524">Cela compilera VSTexture, un nuanceur de sommets défini plus tôt dans le fichier. FX, à la version 1,1 du nuanceur de sommets, puis définira ce nuanceur compilé comme nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="5f378-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="5f378-525">Le nuanceur de pixels est assigné à la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5f378-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="5f378-526">États constants du nuanceur</span><span class="sxs-lookup"><span data-stu-id="5f378-526">Shader Constant States</span></span>

<span data-ttu-id="5f378-527">Les États de constante de nuanceur sont utilisés pour accéder aux paramètres de constante de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="5f378-527">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="5f378-528">État constant du nuanceur</span><span class="sxs-lookup"><span data-stu-id="5f378-528">Shader Constant State</span></span> | <span data-ttu-id="5f378-529">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-529">Type</span></span>            | <span data-ttu-id="5f378-530">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-530">Values</span></span>                                       |
| <span data-ttu-id="5f378-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="5f378-531">PixelShaderConstant</span></span>   | <span data-ttu-id="5f378-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="5f378-533">Tableau de valeurs float de m x n ; m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="5f378-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="5f378-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="5f378-535">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-535">float4</span></span>          | <span data-ttu-id="5f378-536">Un flottant 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-536">One 4D float.</span></span>                                |
| <span data-ttu-id="5f378-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="5f378-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="5f378-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="5f378-538">float4x2</span></span>        | <span data-ttu-id="5f378-539">Deux valeurs en virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="5f378-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="5f378-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="5f378-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="5f378-541">float4x3</span></span>        | <span data-ttu-id="5f378-542">Trois valeurs en virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="5f378-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="5f378-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="5f378-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="5f378-544">float4x4</span></span>        | <span data-ttu-id="5f378-545">Quatre valeurs en virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="5f378-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="5f378-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="5f378-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="5f378-548">Tableau de bool m x n ; m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="5f378-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="5f378-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="5f378-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="5f378-551">Tableau d’entiers m x n.</span><span class="sxs-lookup"><span data-stu-id="5f378-551">m x n array of ints.</span></span> <span data-ttu-id="5f378-552">m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-552">m and n are optional.</span></span>   |
| <span data-ttu-id="5f378-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="5f378-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="5f378-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="5f378-555">Tableau de valeurs à virgule flottante m x n.</span><span class="sxs-lookup"><span data-stu-id="5f378-555">m x n array of floats.</span></span> <span data-ttu-id="5f378-556">m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-556">m and n are optional.</span></span> |
| <span data-ttu-id="5f378-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="5f378-557">VertexShaderConstant</span></span>  | <span data-ttu-id="5f378-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="5f378-559">Tableau de valeurs à virgule flottante m x n.</span><span class="sxs-lookup"><span data-stu-id="5f378-559">m x n array of floats.</span></span> <span data-ttu-id="5f378-560">m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-560">m and n are optional.</span></span> |
| <span data-ttu-id="5f378-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="5f378-561">VertexShaderConstant1</span></span> | <span data-ttu-id="5f378-562">float4</span><span class="sxs-lookup"><span data-stu-id="5f378-562">float4</span></span>          | <span data-ttu-id="5f378-563">Un flottant 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-563">One 4D float.</span></span>                                |
| <span data-ttu-id="5f378-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="5f378-564">VertexShaderConstant2</span></span> | <span data-ttu-id="5f378-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="5f378-565">float4x2</span></span>        | <span data-ttu-id="5f378-566">Deux valeurs en virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="5f378-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="5f378-567">VertexShaderConstant3</span></span> | <span data-ttu-id="5f378-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="5f378-568">float4x3</span></span>        | <span data-ttu-id="5f378-569">Trois valeurs en virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="5f378-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="5f378-570">VertexShaderConstant4</span></span> | <span data-ttu-id="5f378-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="5f378-571">float4x4</span></span>        | <span data-ttu-id="5f378-572">Quatre valeurs en virgule flottante 4D.</span><span class="sxs-lookup"><span data-stu-id="5f378-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="5f378-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="5f378-573">VertexShaderConstantB</span></span> | <span data-ttu-id="5f378-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="5f378-575">Tableau de bool m x n.</span><span class="sxs-lookup"><span data-stu-id="5f378-575">m x n array of bools.</span></span> <span data-ttu-id="5f378-576">m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-576">m and n are optional.</span></span>  |
| <span data-ttu-id="5f378-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="5f378-577">VertexShaderConstantI</span></span> | <span data-ttu-id="5f378-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="5f378-579">Tableau d’entiers m x n.</span><span class="sxs-lookup"><span data-stu-id="5f378-579">m x n array of ints.</span></span> <span data-ttu-id="5f378-580">m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-580">m and n are optional.</span></span>   |
| <span data-ttu-id="5f378-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="5f378-581">VertexShaderConstantF</span></span> | <span data-ttu-id="5f378-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="5f378-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="5f378-583">Tableau de valeurs à virgule flottante m x n.</span><span class="sxs-lookup"><span data-stu-id="5f378-583">m x n array of floats.</span></span> <span data-ttu-id="5f378-584">m et n sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5f378-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="5f378-585">États de la texture</span><span class="sxs-lookup"><span data-stu-id="5f378-585">Texture States</span></span>

<span data-ttu-id="5f378-586">Les États de texture initialisent les textures utilisées par le mélangeur de multitexture.</span><span class="sxs-lookup"><span data-stu-id="5f378-586">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="5f378-587">État de la texture</span><span class="sxs-lookup"><span data-stu-id="5f378-587">Texture State</span></span> | <span data-ttu-id="5f378-588">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-588">Type</span></span>    | <span data-ttu-id="5f378-589">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-589">Values</span></span>                            |
| <span data-ttu-id="5f378-590">Texture \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-590">Texture\[8\]</span></span>  | <span data-ttu-id="5f378-591">texture</span><span class="sxs-lookup"><span data-stu-id="5f378-591">texture</span></span> | <span data-ttu-id="5f378-592">**Null**, ou un paramètre de texture.</span><span class="sxs-lookup"><span data-stu-id="5f378-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="5f378-593">États des étapes de texture</span><span class="sxs-lookup"><span data-stu-id="5f378-593">Texture Stage States</span></span>

<span data-ttu-id="5f378-594">Les États de l’étape de texture définissent les textures et les étapes de texture dans le mélangeur de textures multiples.</span><span class="sxs-lookup"><span data-stu-id="5f378-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f378-595">État de l’étape de texture</span><span class="sxs-lookup"><span data-stu-id="5f378-595">Texture Stage State</span></span>        | <span data-ttu-id="5f378-596">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-596">Type</span></span>  | <span data-ttu-id="5f378-597">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-597">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="5f378-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="5f378-599">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-599">dword</span></span> | <span data-ttu-id="5f378-600">Identique à [**D3DTEXTUREOP**](./d3dtextureop.md) sans le \_ préfixe D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="5f378-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="5f378-601">Consultez D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="5f378-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="5f378-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="5f378-603">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-603">dword</span></span> | <span data-ttu-id="5f378-604">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-605">Consultez D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="5f378-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="5f378-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="5f378-607">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-607">dword</span></span> | <span data-ttu-id="5f378-608">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-609">Consultez D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="5f378-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="5f378-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="5f378-611">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-611">dword</span></span> | <span data-ttu-id="5f378-612">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-613">Consultez D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="5f378-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="5f378-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="5f378-615">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-615">dword</span></span> | <span data-ttu-id="5f378-616">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-617">Consultez D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="5f378-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="5f378-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="5f378-619">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-619">dword</span></span> | <span data-ttu-id="5f378-620">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-621">Consultez D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="5f378-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="5f378-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="5f378-623">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-623">dword</span></span> | <span data-ttu-id="5f378-624">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-625">Consultez D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="5f378-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="5f378-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="5f378-627">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-627">dword</span></span> | <span data-ttu-id="5f378-628">Identique à [**D3DTEXTUREOP**](./d3dtextureop.md) sans le \_ préfixe D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="5f378-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="5f378-629">Consultez D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="5f378-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="5f378-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="5f378-631">float</span><span class="sxs-lookup"><span data-stu-id="5f378-631">float</span></span> | <span data-ttu-id="5f378-632">Mêmes valeurs que D3DTSS \_ BUMPENVLSCALE sans le \_ préfixe D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="5f378-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="5f378-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="5f378-634">float</span><span class="sxs-lookup"><span data-stu-id="5f378-634">float</span></span> | <span data-ttu-id="5f378-635">Mêmes valeurs que D3DTSS \_ BUMPENVLOFFSET sans le \_ préfixe D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="5f378-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="5f378-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="5f378-637">float</span><span class="sxs-lookup"><span data-stu-id="5f378-637">float</span></span> | <span data-ttu-id="5f378-638">Mêmes valeurs que D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="5f378-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="5f378-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="5f378-640">float</span><span class="sxs-lookup"><span data-stu-id="5f378-640">float</span></span> | <span data-ttu-id="5f378-641">Mêmes valeurs que D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="5f378-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="5f378-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="5f378-643">float</span><span class="sxs-lookup"><span data-stu-id="5f378-643">float</span></span> | <span data-ttu-id="5f378-644">Mêmes valeurs que D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="5f378-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="5f378-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="5f378-646">float</span><span class="sxs-lookup"><span data-stu-id="5f378-646">float</span></span> | <span data-ttu-id="5f378-647">Mêmes valeurs que D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="5f378-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="5f378-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="5f378-649">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-649">dword</span></span> | <span data-ttu-id="5f378-650">Identique à [D3DTA](d3dta.md) sans le \_ préfixe D3DTA.</span><span class="sxs-lookup"><span data-stu-id="5f378-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="5f378-651">Consultez D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="5f378-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="5f378-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="5f378-653">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-653">dword</span></span> | <span data-ttu-id="5f378-654">Mêmes valeurs que D3DTSS \_ TEXCOORDINDEX sans le \_ préfixe D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="5f378-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="5f378-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="5f378-656">dword</span><span class="sxs-lookup"><span data-stu-id="5f378-656">dword</span></span> | <span data-ttu-id="5f378-657">Mêmes valeurs que les valeurs [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) sans le \_ préfixe D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="5f378-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="5f378-658">Consultez D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="5f378-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="5f378-659">États de la transformation</span><span class="sxs-lookup"><span data-stu-id="5f378-659">Transform States</span></span>

<span data-ttu-id="5f378-660">Définissez les États de transformation pour initialiser les matrices de transformation.</span><span class="sxs-lookup"><span data-stu-id="5f378-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="5f378-661">Les effets utilisent des matrices transposées pour des performances optimales.</span><span class="sxs-lookup"><span data-stu-id="5f378-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="5f378-662">Vous pouvez fournir des matrices transposées à un effet, ou un effet transposera automatiquement les matrices avant de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="5f378-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f378-663">Transformer l’État</span><span class="sxs-lookup"><span data-stu-id="5f378-663">Transform State</span></span>       | <span data-ttu-id="5f378-664">Type</span><span class="sxs-lookup"><span data-stu-id="5f378-664">Type</span></span>     | <span data-ttu-id="5f378-665">Valeurs</span><span class="sxs-lookup"><span data-stu-id="5f378-665">Values</span></span>                                                                                                                          |
| <span data-ttu-id="5f378-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="5f378-666">ProjectionTransform</span></span>   | <span data-ttu-id="5f378-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="5f378-667">float4x4</span></span> | <span data-ttu-id="5f378-668">Matrice 4x4 de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f378-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="5f378-669">Mêmes valeurs que \_ la projection D3DTS sans le \_ préfixe D3DTS.</span><span class="sxs-lookup"><span data-stu-id="5f378-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="5f378-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="5f378-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="5f378-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="5f378-671">float4x4</span></span> | <span data-ttu-id="5f378-672">Matrice 4x4 de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f378-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="5f378-673">Mêmes valeurs que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sans le \_ préfixe D3DTS.</span><span class="sxs-lookup"><span data-stu-id="5f378-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="5f378-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="5f378-674">ViewTransform</span></span>         | <span data-ttu-id="5f378-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="5f378-675">float4x4</span></span> | <span data-ttu-id="5f378-676">Matrice 4x4 de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f378-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="5f378-677">Mêmes valeurs que \_ la vue D3DTS sans le \_ préfixe D3DTS.</span><span class="sxs-lookup"><span data-stu-id="5f378-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="5f378-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="5f378-678">WorldTransform</span></span>        | <span data-ttu-id="5f378-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="5f378-679">float4x4</span></span> | <span data-ttu-id="5f378-680">Matrice 4x4 de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="5f378-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="5f378-681">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f378-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f378-682">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="5f378-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
