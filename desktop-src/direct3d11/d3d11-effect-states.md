---
title: Groupes d’état des effets (Direct3D 11)
description: Les États d’effet sont des paires nom-valeur sous la forme d’une expression.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- effet, groupes d’États (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941018"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="a0904-104">Groupes d’état des effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a0904-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="a0904-105">Les États d’effet sont des paires nom-valeur sous la forme d’une expression.</span><span class="sxs-lookup"><span data-stu-id="a0904-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="a0904-106">État de fusion</span><span class="sxs-lookup"><span data-stu-id="a0904-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="a0904-107">État de la profondeur et du stencil</span><span class="sxs-lookup"><span data-stu-id="a0904-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="a0904-108">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="a0904-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="a0904-109">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="a0904-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="a0904-110">État de l’objet d’effet</span><span class="sxs-lookup"><span data-stu-id="a0904-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="a0904-111">Définition et utilisation d’objets d’État</span><span class="sxs-lookup"><span data-stu-id="a0904-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="a0904-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0904-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="a0904-113">État de fusion</span><span class="sxs-lookup"><span data-stu-id="a0904-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a0904-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="a0904-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="a0904-115">Membres de [ **d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="a0904-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="a0904-116">État de la profondeur et du stencil</span><span class="sxs-lookup"><span data-stu-id="a0904-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a0904-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span><span class="sxs-lookup"><span data-stu-id="a0904-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="a0904-118">Membres de la [ **\_ Description du \_ stencil \_ de profondeur d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="a0904-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="a0904-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="a0904-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="a0904-120">Membre de [ **d3d11 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="a0904-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="a0904-121">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="a0904-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a0904-122">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="a0904-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="a0904-123">**\_Mode de remplissage d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="a0904-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="a0904-124">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="a0904-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="a0904-125">**\_Mode d’élimination d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="a0904-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="a0904-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span><span class="sxs-lookup"><span data-stu-id="a0904-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="a0904-127">Membres de [ **d3d11 \_ rastériseur \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="a0904-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="a0904-128">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="a0904-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a0904-129">Filtre d’adresse AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span><span class="sxs-lookup"><span data-stu-id="a0904-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="a0904-130">Membres de l' [ **\_ échantillonneur d3d11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="a0904-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="a0904-131">Pour obtenir des exemples, consultez [type d’échantillonneur (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .</span><span class="sxs-lookup"><span data-stu-id="a0904-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="a0904-132">État de l’objet d’effet</span><span class="sxs-lookup"><span data-stu-id="a0904-132">Effect Object State</span></span>



| <span data-ttu-id="a0904-133">Cet objet Effect</span><span class="sxs-lookup"><span data-stu-id="a0904-133">This Effect Object</span></span>                          | <span data-ttu-id="a0904-134">Correspond à</span><span class="sxs-lookup"><span data-stu-id="a0904-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a0904-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="a0904-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="a0904-136">Objet d’état de l' [État du rastériseur](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="a0904-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="a0904-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="a0904-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="a0904-138">Objet d’état de [profondeur et](#depth-and-stencil-state) d’état de gabarit.</span><span class="sxs-lookup"><span data-stu-id="a0904-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="a0904-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="a0904-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="a0904-140">Objet d’état de l' [État de fusion](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="a0904-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="a0904-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="a0904-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="a0904-142">Objet de nuanceur de sommets compilé.</span><span class="sxs-lookup"><span data-stu-id="a0904-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="a0904-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="a0904-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="a0904-144">Objet de nuanceur de pixels compilé.</span><span class="sxs-lookup"><span data-stu-id="a0904-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="a0904-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="a0904-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="a0904-146">Objet de nuanceur Geometry compilé.</span><span class="sxs-lookup"><span data-stu-id="a0904-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="a0904-147">DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="a0904-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="a0904-148">Membres de [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="a0904-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="a0904-149">Définition et utilisation d’objets d’État</span><span class="sxs-lookup"><span data-stu-id="a0904-149">Defining and using state objects</span></span>

<span data-ttu-id="a0904-150">Les objets d’État sont déclarés dans des fichiers FX au format suivant.</span><span class="sxs-lookup"><span data-stu-id="a0904-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="a0904-151">StateObjectType est l’un des États listés ci-dessus et MemberName est le nom d’un membre qui aura une valeur non définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="a0904-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="a0904-152">Par exemple, pour configurer un objet d’état de fusion avec AlphaToCoverageEnable et BlendEnable \[ 0 ayant \] la valeur **false** , le code suivant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0904-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="a0904-153">L’objet d’État est appliqué à une technique Pass à l’aide de l’une des fonctions SetStateGroup décrites dans syntaxe de la [technique Effect (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a0904-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="a0904-154">Par exemple, pour appliquer l’objet BlendState décrit ci-dessus, vous devez utiliser le code suivant.</span><span class="sxs-lookup"><span data-stu-id="a0904-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="a0904-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0904-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0904-156">Syntaxe de la technique Effect</span><span class="sxs-lookup"><span data-stu-id="a0904-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="a0904-157">Format d’effet (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="a0904-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 