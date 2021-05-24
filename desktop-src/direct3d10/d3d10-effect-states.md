---
description: Les États d’effet sont des paires nom-valeur sous la forme d’une expression.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Groupes d’états d’effet (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335567"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="375ca-103">Groupes d’états d’effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="375ca-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="375ca-104">Les États d’effet sont des paires nom-valeur sous la forme d’une expression.</span><span class="sxs-lookup"><span data-stu-id="375ca-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="375ca-105">État de fusion</span><span class="sxs-lookup"><span data-stu-id="375ca-105">Blend state</span></span>

| <span data-ttu-id="375ca-106">État de l’effet</span><span class="sxs-lookup"><span data-stu-id="375ca-106">Effect state</span></span> | <span data-ttu-id="375ca-107">Groupe</span><span class="sxs-lookup"><span data-stu-id="375ca-107">Group</span></span> |
|-|-|
| <span data-ttu-id="375ca-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="375ca-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="375ca-109">Membres de [ **D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="375ca-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="375ca-110">État de la profondeur et du stencil</span><span class="sxs-lookup"><span data-stu-id="375ca-110">Depth and stencil state</span></span>

| <span data-ttu-id="375ca-111">État de l’effet</span><span class="sxs-lookup"><span data-stu-id="375ca-111">Effect state</span></span>| <span data-ttu-id="375ca-112">Groupe</span><span class="sxs-lookup"><span data-stu-id="375ca-112">Group</span></span> |
|-|-|
| <span data-ttu-id="375ca-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="375ca-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="375ca-114">Membres de la [ **\_ Description du \_ stencil \_ de profondeur D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="375ca-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="375ca-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="375ca-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="375ca-116">Membre de [ **D3D10 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="375ca-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="375ca-117">État du rastériseur</span><span class="sxs-lookup"><span data-stu-id="375ca-117">Rasterizer state</span></span>

| <span data-ttu-id="375ca-118">État de l’effet</span><span class="sxs-lookup"><span data-stu-id="375ca-118">Effect state</span></span>| <span data-ttu-id="375ca-119">Groupe</span><span class="sxs-lookup"><span data-stu-id="375ca-119">Group</span></span> |
|-|-|
| <span data-ttu-id="375ca-120">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="375ca-120">FILLMODE</span></span> | [<span data-ttu-id="375ca-121">**\_Mode de remplissage D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="375ca-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="375ca-122">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="375ca-122">CULLMODE</span></span> | [<span data-ttu-id="375ca-123">**\_Mode d’élimination D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="375ca-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="375ca-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="375ca-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="375ca-125">Membres de [ **D3D10 \_ rastériseur \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="375ca-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="375ca-126">État de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="375ca-126">Sampler state</span></span>

| <span data-ttu-id="375ca-127">État de l’effet</span><span class="sxs-lookup"><span data-stu-id="375ca-127">Effect state</span></span> | <span data-ttu-id="375ca-128">Groupe</span><span class="sxs-lookup"><span data-stu-id="375ca-128">Group</span></span> |
|-|-|
| <span data-ttu-id="375ca-129">**Filter**,  **adAddressW**, **AddressV**,, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="375ca-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="375ca-130">Membres de l' [ **\_ échantillonneur D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="375ca-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="375ca-131">Pour obtenir des exemples, consultez [type d’échantillonneur (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="375ca-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="375ca-132">État de l’objet d’effet</span><span class="sxs-lookup"><span data-stu-id="375ca-132">Effect object state</span></span>

| <span data-ttu-id="375ca-133">Cet objet Effect</span><span class="sxs-lookup"><span data-stu-id="375ca-133">This effect object</span></span> | <span data-ttu-id="375ca-134">Correspond à</span><span class="sxs-lookup"><span data-stu-id="375ca-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="375ca-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="375ca-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="375ca-136">Objet d’état de l' [État du rastériseur](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="375ca-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="375ca-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="375ca-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="375ca-138">Objet d’état de [profondeur et](#depth-and-stencil-state) d’état de gabarit.</span><span class="sxs-lookup"><span data-stu-id="375ca-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="375ca-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="375ca-139">BLENDSTATE</span></span> | <span data-ttu-id="375ca-140">Objet d’état de l' [État de fusion](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="375ca-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="375ca-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="375ca-141">VERTEXSHADER</span></span> | <span data-ttu-id="375ca-142">Objet de nuanceur de sommets compilé.</span><span class="sxs-lookup"><span data-stu-id="375ca-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="375ca-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="375ca-143">PIXELSHADER</span></span> | <span data-ttu-id="375ca-144">Objet de nuanceur de pixels compilé.</span><span class="sxs-lookup"><span data-stu-id="375ca-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="375ca-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="375ca-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="375ca-146">Objet de nuanceur Geometry compilé.</span><span class="sxs-lookup"><span data-stu-id="375ca-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="375ca-147">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="375ca-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="375ca-148">Membres de [**D3D10 \_ Pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="375ca-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="375ca-149">Définition et utilisation d’objets d’État</span><span class="sxs-lookup"><span data-stu-id="375ca-149">Defining and using state objects</span></span>

<span data-ttu-id="375ca-150">Les objets d’État sont déclarés dans des fichiers FX au format suivant.</span><span class="sxs-lookup"><span data-stu-id="375ca-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="375ca-151">*StateObjectType* est l’un des États indiqués ci-dessus, et *MemberName* est le nom d’un membre qui aura une valeur non définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="375ca-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="375ca-152">Par exemple, pour configurer un objet d’état de fusion avec AlphaToCoverageEnable et BlendEnable \[ 0 ayant \] la valeur **false**, le code suivant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="375ca-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="375ca-153">L’objet d’État est appliqué à une technique Pass à l’aide de l’une des fonctions SetStateGroup décrites dans syntaxe de la [technique Effect (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="375ca-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="375ca-154">Par exemple, pour appliquer l’objet BlendState décrit ci-dessus, vous devez utiliser le code suivant.</span><span class="sxs-lookup"><span data-stu-id="375ca-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="375ca-155">Pour obtenir un didacticiel décrivant l’utilisation des États, consultez Gestion de l' [État](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="375ca-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="375ca-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="375ca-156">Related topics</span></span>

* [<span data-ttu-id="375ca-157">Syntaxe de la technique Effect</span><span class="sxs-lookup"><span data-stu-id="375ca-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="375ca-158">Format d’effet (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="375ca-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
