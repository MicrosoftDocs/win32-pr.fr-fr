---
title: Effets des interfaces système (Direct3D 11)
description: Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671897"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="68ab1-103">Effets des interfaces système (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="68ab1-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="68ab1-104">Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet.</span><span class="sxs-lookup"><span data-stu-id="68ab1-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="68ab1-105">Il existe deux types d’interfaces : ceux utilisés par le runtime pour restituer des interfaces d’effet et de réflexion afin d’obtenir et de définir des variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="68ab1-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="68ab1-106">Interfaces d’exécution Effect</span><span class="sxs-lookup"><span data-stu-id="68ab1-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="68ab1-107">Interfaces d’effet de réflexion</span><span class="sxs-lookup"><span data-stu-id="68ab1-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="68ab1-108">Interfaces d’exécution Effect</span><span class="sxs-lookup"><span data-stu-id="68ab1-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="68ab1-109">Utilisez les interfaces Runtime pour rendre un effet.</span><span class="sxs-lookup"><span data-stu-id="68ab1-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="68ab1-110">Interfaces d’exécution</span><span class="sxs-lookup"><span data-stu-id="68ab1-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="68ab1-111">Description</span><span class="sxs-lookup"><span data-stu-id="68ab1-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="68ab1-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="68ab1-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="68ab1-113">Collection d’un ou plusieurs groupes et techniques pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="68ab1-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="68ab1-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="68ab1-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="68ab1-115">Collection d’assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="68ab1-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="68ab1-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="68ab1-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="68ab1-117">Collection d’une ou de plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="68ab1-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="68ab1-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="68ab1-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="68ab1-119">Collection d’une ou de plusieurs techniques.</span><span class="sxs-lookup"><span data-stu-id="68ab1-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="68ab1-120">Interfaces d’effet de réflexion</span><span class="sxs-lookup"><span data-stu-id="68ab1-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="68ab1-121">La réflexion est implémentée dans le système d’effet pour prendre en charge l’état d’effet de lecture (et d’écriture).</span><span class="sxs-lookup"><span data-stu-id="68ab1-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="68ab1-122">Il existe plusieurs façons d’accéder aux variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="68ab1-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="68ab1-123">Définition de groupes d’état d’effet</span><span class="sxs-lookup"><span data-stu-id="68ab1-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="68ab1-124">Utilisez ces interfaces pour obtenir et définir un groupe d’États.</span><span class="sxs-lookup"><span data-stu-id="68ab1-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="68ab1-125">Interfaces de réflexion</span><span class="sxs-lookup"><span data-stu-id="68ab1-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="68ab1-126">Description</span><span class="sxs-lookup"><span data-stu-id="68ab1-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="68ab1-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="68ab1-128">Obtient et définit l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="68ab1-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="68ab1-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="68ab1-130">Obtient et définit l’état du gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="68ab1-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="68ab1-132">Obtient et définit l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="68ab1-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="68ab1-134">Obtient et définit l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="68ab1-135">Définition des ressources d’effet</span><span class="sxs-lookup"><span data-stu-id="68ab1-135">Setting Effect Resources</span></span>

<span data-ttu-id="68ab1-136">Utilisez ces interfaces pour récupérer et définir des ressources.</span><span class="sxs-lookup"><span data-stu-id="68ab1-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="68ab1-137">Interfaces de réflexion</span><span class="sxs-lookup"><span data-stu-id="68ab1-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="68ab1-138">Description</span><span class="sxs-lookup"><span data-stu-id="68ab1-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="68ab1-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="68ab1-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="68ab1-140">Accéder aux données dans une mémoire tampon de texture ou une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="68ab1-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="68ab1-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="68ab1-142">Accédez aux données dans une ressource de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="68ab1-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="68ab1-144">Accéder aux données dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="68ab1-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="68ab1-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="68ab1-146">Accéder aux données dans une ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="68ab1-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="68ab1-148">Accédez aux données dans une vue d’accès non ordonnée.</span><span class="sxs-lookup"><span data-stu-id="68ab1-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="68ab1-149">Définition d’autres variables d’effet</span><span class="sxs-lookup"><span data-stu-id="68ab1-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="68ab1-150">Utilisez ces interfaces pour récupérer et définir l’État par le type de variable.</span><span class="sxs-lookup"><span data-stu-id="68ab1-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="68ab1-151">Interfaces de réflexion</span><span class="sxs-lookup"><span data-stu-id="68ab1-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="68ab1-152">Description</span><span class="sxs-lookup"><span data-stu-id="68ab1-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="68ab1-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="68ab1-154">Obtient une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="68ab1-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="68ab1-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="68ab1-156">Obtient et définit une interface.</span><span class="sxs-lookup"><span data-stu-id="68ab1-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="68ab1-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="68ab1-158">Obtenir et définir une matrice.</span><span class="sxs-lookup"><span data-stu-id="68ab1-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="68ab1-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="68ab1-160">Obtient et définit une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="68ab1-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="68ab1-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="68ab1-162">Obtenir une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="68ab1-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="68ab1-164">Obtient et définit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="68ab1-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="68ab1-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="68ab1-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="68ab1-166">Obtient un type de variable.</span><span class="sxs-lookup"><span data-stu-id="68ab1-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="68ab1-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="68ab1-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="68ab1-168">Obtient et définit un vecteur.</span><span class="sxs-lookup"><span data-stu-id="68ab1-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="68ab1-169">Toutes les interfaces de réflexion dérivent de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="68ab1-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68ab1-170">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68ab1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ab1-171">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="68ab1-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="68ab1-172">Guide de programmation pour Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="68ab1-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 




