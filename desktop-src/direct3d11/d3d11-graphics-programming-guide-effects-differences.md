---
title: Différences entre les effets 10 et les effets 11
description: Cette rubrique présente les différences entre les effets 10 et 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728229"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="4bdf9-103">Différences entre les effets 10 et les effets 11</span><span class="sxs-lookup"><span data-stu-id="4bdf9-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="4bdf9-104">Cette rubrique présente les différences entre les effets 10 et 11.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="4bdf9-105">Contextes de périphérique, Threading et clonage</span><span class="sxs-lookup"><span data-stu-id="4bdf9-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="4bdf9-106">L’interface ID3D10Device a été divisée en deux interfaces dans Direct3D 11 : ID3D11Device et ID3D11DeviceContext.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="4bdf9-107">Vous pouvez créer plusieurs ID3D11DeviceContexts pour faciliter l’exécution simultanée sur plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="4bdf9-108">Effects 11 étend ce concept à l’infrastructure Effects.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="4bdf9-109">Le runtime Effects 11 est monothread.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="4bdf9-110">Pour cette raison, vous ne devez pas utiliser une seule instance ID3DX11Effect avec plusieurs threads simultanément.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="4bdf9-111">Pour utiliser le runtime Effects 11 sur plusieurs instances, vous devez créer des instances ID3DX11Effect distinctes.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="4bdf9-112">Étant donné que le ID3D11DeviceContext est également à thread unique, vous devez passer différentes instances ID3D11DeviceContext à chaque instance Effect à l’application.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="4bdf9-113">Vous pouvez utiliser ces contextes de périphérique distincts pour créer des listes de commandes afin que le thread de rendu puisse les appliquer dans le contexte de périphérique immédiat.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="4bdf9-114">Le moyen le plus simple de créer plusieurs effets qui encapsulent la même fonctionnalité, pour une utilisation sur plusieurs threads, est de créer un effet, puis de créer des copies clonées.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="4bdf9-115">Le clonage présente les avantages suivants par rapport à la création de plusieurs copies à partir de zéro :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="4bdf9-116">La routine de clonage est plus rapide que la routine de création.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="4bdf9-117">Les effets clonés partagent les nuanceurs, les blocs d’État et les instances de classe créés (ils n’ont donc pas besoin d’être recréés).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="4bdf9-118">Les effets clonés peuvent partager des mémoires tampons constantes.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="4bdf9-119">Les effets clonés commencent par l’État qui correspond à l’effet actuel (valeurs des variables, qu’elles aient été optimisées ou non).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="4bdf9-120">Pour plus d’informations, consultez [clonage d’un effet](d3d11-graphics-programming-guide-effects-cloning.md) .</span><span class="sxs-lookup"><span data-stu-id="4bdf9-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="4bdf9-121">Pools et groupes d’effets</span><span class="sxs-lookup"><span data-stu-id="4bdf9-121">Effect Pools and Groups</span></span>

<span data-ttu-id="4bdf9-122">De loin, l’utilisation la plus répandue des pools d’effets dans Direct3D 10 consistait à regrouper les matériaux.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="4bdf9-123">Les pools d’effets ont été supprimés des effets 11 et les groupes ont été ajoutés, ce qui constitue une méthode plus efficace de regroupement de matériaux.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="4bdf9-124">Un groupe d’effets est simplement un ensemble de techniques.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="4bdf9-125">Pour plus d’informations [, consultez Syntaxe du groupe Effect (Direct3D 11)](d3d11-effect-group-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="4bdf9-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="4bdf9-126">Considérez la hiérarchie d’effets suivante avec quatre effets enfants et un pool d’effets :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="4bdf9-127">Vous pouvez obtenir la même fonctionnalité dans Effects 11 à l’aide de groupes :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="4bdf9-128">Nouvelles étapes de nuanceur</span><span class="sxs-lookup"><span data-stu-id="4bdf9-128">New Shader Stages</span></span>

<span data-ttu-id="4bdf9-129">Il existe trois nouvelles étapes de nuanceur dans Direct3D 11 : le nuanceur de coque, le nuanceur de domaine et le nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="4bdf9-130">Les effets 11 les traitent de la même façon que les nuanceurs de vertex, les nuanceurs de géométrie et les nuanceurs de pixels.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="4bdf9-131">Trois nouveaux types de variables ont été ajoutés aux effets 11 :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="4bdf9-132">HullShader</span><span class="sxs-lookup"><span data-stu-id="4bdf9-132">HullShader</span></span>
-   <span data-ttu-id="4bdf9-133">DomainShader</span><span class="sxs-lookup"><span data-stu-id="4bdf9-133">DomainShader</span></span>
-   <span data-ttu-id="4bdf9-134">ComputeShader</span><span class="sxs-lookup"><span data-stu-id="4bdf9-134">ComputeShader</span></span>

<span data-ttu-id="4bdf9-135">Si vous utilisez ces nuanceurs dans une technique, vous devez étiqueter cette technique « technique11 », et non pas « technique10 ».</span><span class="sxs-lookup"><span data-stu-id="4bdf9-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="4bdf9-136">Le nuanceur de calcul ne peut pas être défini dans le même test que les autres États graphiques (autres nuanceurs, blocs d’État ou cibles de rendu).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="4bdf9-137">Nouveaux types de texture</span><span class="sxs-lookup"><span data-stu-id="4bdf9-137">New Texture Types</span></span>

<span data-ttu-id="4bdf9-138">Direct3D 11 prend en charge les types de textures suivants :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="4bdf9-139">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="4bdf9-140">ByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="4bdf9-141">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="4bdf9-142">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="4bdf9-143">Vues d’accès non ordonnées</span><span class="sxs-lookup"><span data-stu-id="4bdf9-143">Unordered Access Views</span></span>

<span data-ttu-id="4bdf9-144">Effects 11 prend en charge l’obtention et la définition des nouveaux types de vues d’accès non ordonnés.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="4bdf9-145">Cela fonctionne de la même façon que les textures.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="4bdf9-146">Considérez cet exemple HLSL :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="4bdf9-147">Vous pouvez définir cette variable en C++ comme suit :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="4bdf9-148">Direct3D 11 prend en charge les types de vues d’accès non triés suivants :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="4bdf9-149">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-149">RWBuffer</span></span>
-   <span data-ttu-id="4bdf9-150">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="4bdf9-151">RWStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="4bdf9-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="4bdf9-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="4bdf9-152">RWTexture1D</span></span>
-   <span data-ttu-id="4bdf9-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="4bdf9-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="4bdf9-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="4bdf9-154">RWTexture2D</span></span>
-   <span data-ttu-id="4bdf9-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="4bdf9-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="4bdf9-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="4bdf9-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="4bdf9-157">Interfaces et instances de classe</span><span class="sxs-lookup"><span data-stu-id="4bdf9-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="4bdf9-158">Pour connaître la syntaxe de la classe et de l’interface, consultez [interfaces et classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="4bdf9-159">Pour utiliser des interfaces et des classes dans Effects, consultez [interfaces et classes dans Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="4bdf9-160">Flux adressable</span><span class="sxs-lookup"><span data-stu-id="4bdf9-160">Addressable Stream Out</span></span>

<span data-ttu-id="4bdf9-161">Dans Direct3D 10, les nuanceurs de géométrie peuvent générer un flux de données vers l’unité de sortie de flux et l’unité de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="4bdf9-162">Dans Direct3D11, les nuanceurs de géométrie peuvent générer jusqu’à quatre flux de données vers l’unité de sortie de flux, et au plus l’un de ces flux vers l’unité de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="4bdf9-163">L’intrinsèque **ConstructGSWithSO** a été mis à jour pour refléter cette nouvelle fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="4bdf9-164">Pour plus d’informations, consultez [syntaxe de flux sortant](d3d11-graphics-reference-effect-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="4bdf9-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="4bdf9-165">Définition et désactivation de l’état de l’appareil</span><span class="sxs-lookup"><span data-stu-id="4bdf9-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="4bdf9-166">Dans Effects 10, vous pouviez rendre des mémoires tampons constantes et des mémoires tampons de texture gérées par l’utilisateur à l’aide des fonctions [**ID3D10EffectConstantBuffer :: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) et [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4bdf9-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="4bdf9-167">Une fois que vous avez appelé ces fonctions, les effets 10 Runtime ne gèrent plus la mémoire tampon constante ou la mémoire tampon de texture et l’utilisateur doit remplir les données à l’aide de l’interface ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="4bdf9-168">Dans Effects 11, vous pouvez également faire en sorte que les blocs d’État (état de fusion, état du rastériseur, état du gabarit de profondeur et état de l’échantillonneur) soient gérés par l’utilisateur à l’aide des appels suivants :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="4bdf9-169">**ID3DX11EffectBlendVariable::SetBlendState**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="4bdf9-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="4bdf9-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="4bdf9-172">**ID3DX11EffectSamplerVariable::SetSampler**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="4bdf9-173">Une fois que vous avez appelé ces fonctions, le runtime Effects 11 ne gère plus les variables de bloc d’État, et les valeurs resteront inchangées.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="4bdf9-174">Notez que dans la mesure où les blocs d’État sont immuables, l’utilisateur doit définir un nouveau bloc d’État pour modifier les valeurs.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="4bdf9-175">Vous pouvez également rétablir les mémoires tampons constantes, les mémoires tampons de texture et les blocs d’État à l’état non géré par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="4bdf9-176">Si vous annulez ces variables, le runtime Effects 11 continuera à les mettre à jour si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="4bdf9-177">Vous pouvez utiliser les appels suivants pour annuler les variables gérées par l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="4bdf9-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="4bdf9-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="4bdf9-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="4bdf9-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="4bdf9-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="4bdf9-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span><span class="sxs-lookup"><span data-stu-id="4bdf9-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="4bdf9-184">Ordinateur virtuel Effects</span><span class="sxs-lookup"><span data-stu-id="4bdf9-184">Effects Virtual Machine</span></span>

<span data-ttu-id="4bdf9-185">La machine virtuelle Effects, qui a évalué des expressions complexes en dehors des fonctions, a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="4bdf9-186">Les exemples suivants d’expressions complexes ne sont pas pris en charge :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="4bdf9-187">SetPixelShader (myPSArray (i \* 3 + j));</span><span class="sxs-lookup"><span data-stu-id="4bdf9-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="4bdf9-188">SetPixelShader (myPSArray ((float) i);</span><span class="sxs-lookup"><span data-stu-id="4bdf9-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="4bdf9-189">FILTRE = i + 2 ;</span><span class="sxs-lookup"><span data-stu-id="4bdf9-189">FILTER = i + 2;</span></span>

<span data-ttu-id="4bdf9-190">Les exemples suivants d’expressions non complexes sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="4bdf9-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="4bdf9-191">SetPixelShader( myPS );</span><span class="sxs-lookup"><span data-stu-id="4bdf9-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="4bdf9-192">SetPixelShader (myPS \[ i \] );</span><span class="sxs-lookup"><span data-stu-id="4bdf9-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="4bdf9-193">SetPixelShader (myPS \[ uIndex \] );//uIndex est une variable uint</span><span class="sxs-lookup"><span data-stu-id="4bdf9-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="4bdf9-194">FILTRE = i ;</span><span class="sxs-lookup"><span data-stu-id="4bdf9-194">FILTER = i;</span></span>
5.  <span data-ttu-id="4bdf9-195">FILTRE = ANISOTROPE ;</span><span class="sxs-lookup"><span data-stu-id="4bdf9-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="4bdf9-196">Ces expressions peuvent apparaître dans des expressions de bloc d’État (par exemple, filtre) et des expressions de passe (par exemple, SetPixelShader).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="4bdf9-197">Disponibilité et emplacement de la source</span><span class="sxs-lookup"><span data-stu-id="4bdf9-197">Source Availability and Location</span></span>

<span data-ttu-id="4bdf9-198">Effects 10 a été distribué dans D3D10.dll.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="4bdf9-199">Effects 11 est distribué en tant que source, avec les solutions Visual Studio correspondantes pour le compiler.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="4bdf9-200">Lorsque vous créez des applications de type Effects, nous vous recommandons d’inclure la source Effects 11 directement dans ces applications.</span><span class="sxs-lookup"><span data-stu-id="4bdf9-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="4bdf9-201">Vous pouvez obtenir les effets 11 des [effets de la mise à jour de Direct3D 11](https://github.com/Microsoft/FX11).</span><span class="sxs-lookup"><span data-stu-id="4bdf9-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bdf9-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4bdf9-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bdf9-203">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4bdf9-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 