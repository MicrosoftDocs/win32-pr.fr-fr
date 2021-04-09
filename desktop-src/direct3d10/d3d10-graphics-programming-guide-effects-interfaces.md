---
description: 'Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet. Il existe deux types d’interfaces : ceux utilisés par le runtime pour restituer des interfaces d’effet et de réflexion afin d’obtenir et de définir des variables d’effet.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Effets des interfaces système (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110383"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="3576a-104">Effets des interfaces système (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="3576a-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="3576a-105">Le système d’effet définit plusieurs interfaces pour gérer l’état de l’effet.</span><span class="sxs-lookup"><span data-stu-id="3576a-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="3576a-106">Il existe deux types d’interfaces : ceux utilisés par le runtime pour restituer des interfaces d’effet et de réflexion afin d’obtenir et de définir des variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="3576a-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="3576a-107">Interfaces d’exécution Effect</span><span class="sxs-lookup"><span data-stu-id="3576a-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="3576a-108">Interfaces d’effet de réflexion</span><span class="sxs-lookup"><span data-stu-id="3576a-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="3576a-109">Interfaces d’exécution Effect</span><span class="sxs-lookup"><span data-stu-id="3576a-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="3576a-110">Utilisez les interfaces Runtime pour rendre un effet.</span><span class="sxs-lookup"><span data-stu-id="3576a-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="3576a-111">Interfaces d’exécution</span><span class="sxs-lookup"><span data-stu-id="3576a-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="3576a-112">Description</span><span class="sxs-lookup"><span data-stu-id="3576a-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3576a-113">**Interface ID3D10Effect**</span><span class="sxs-lookup"><span data-stu-id="3576a-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="3576a-114">Collection d’une ou de plusieurs techniques de rendu.</span><span class="sxs-lookup"><span data-stu-id="3576a-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="3576a-115">[**Interface ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3576a-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="3576a-116">Interface pour l’ajout de comportements personnalisés lors de la lecture de fichiers include.</span><span class="sxs-lookup"><span data-stu-id="3576a-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="3576a-117">**Interface ID3D10EffectPass**</span><span class="sxs-lookup"><span data-stu-id="3576a-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="3576a-118">Collection d’assignations d’État.</span><span class="sxs-lookup"><span data-stu-id="3576a-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="3576a-119">**Interface ID3D10EffectPool**</span><span class="sxs-lookup"><span data-stu-id="3576a-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="3576a-120">Créez un emplacement de mémoire pour les variables à partager entre les effets.</span><span class="sxs-lookup"><span data-stu-id="3576a-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="3576a-121">**Interface ID3D10EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="3576a-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="3576a-122">Collection d’une ou de plusieurs passes.</span><span class="sxs-lookup"><span data-stu-id="3576a-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="3576a-123">Interfaces d’effet de réflexion</span><span class="sxs-lookup"><span data-stu-id="3576a-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="3576a-124">La réflexion est implémentée dans le système d’effet pour prendre en charge l’état d’effet de lecture (et d’écriture).</span><span class="sxs-lookup"><span data-stu-id="3576a-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="3576a-125">Il existe plusieurs façons d’accéder aux variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="3576a-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="3576a-126">Définition de groupes d’état d’effet</span><span class="sxs-lookup"><span data-stu-id="3576a-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="3576a-127">Utilisez ces interfaces pour obtenir et définir un groupe d’États.</span><span class="sxs-lookup"><span data-stu-id="3576a-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="3576a-128">Interfaces de réflexion</span><span class="sxs-lookup"><span data-stu-id="3576a-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="3576a-129">Description</span><span class="sxs-lookup"><span data-stu-id="3576a-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="3576a-130">**Interface ID3D10EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="3576a-131">Obtient et définit l’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="3576a-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="3576a-132">**Interface ID3D10EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="3576a-133">Obtient et définit l’état du gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3576a-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="3576a-134">**Interface ID3D10EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="3576a-135">Obtient et définit l’état du rastériseur.</span><span class="sxs-lookup"><span data-stu-id="3576a-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="3576a-136">**Interface ID3D10EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="3576a-137">Obtient et définit l’état de l’échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="3576a-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="3576a-138">Définition des ressources d’effet</span><span class="sxs-lookup"><span data-stu-id="3576a-138">Setting Effect Resources</span></span>

<span data-ttu-id="3576a-139">Utilisez ces interfaces pour récupérer et définir des ressources.</span><span class="sxs-lookup"><span data-stu-id="3576a-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="3576a-140">Interfaces de réflexion</span><span class="sxs-lookup"><span data-stu-id="3576a-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="3576a-141">Description</span><span class="sxs-lookup"><span data-stu-id="3576a-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="3576a-142">**Interface ID3D10EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="3576a-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="3576a-143">Accéder aux données dans une mémoire tampon de texture ou une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="3576a-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="3576a-144">**Interface ID3D10EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="3576a-145">Accédez aux données dans une ressource de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="3576a-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="3576a-146">**Interface ID3D10EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="3576a-147">Accéder aux données dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="3576a-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="3576a-148">**Interface ID3D10EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="3576a-149">Accéder aux données dans une ressource de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3576a-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="3576a-150">Définition d’autres variables d’effet</span><span class="sxs-lookup"><span data-stu-id="3576a-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="3576a-151">Utilisez ces interfaces pour récupérer et définir l’État par le type de variable.</span><span class="sxs-lookup"><span data-stu-id="3576a-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="3576a-152">Interfaces de réflexion</span><span class="sxs-lookup"><span data-stu-id="3576a-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="3576a-153">Description</span><span class="sxs-lookup"><span data-stu-id="3576a-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="3576a-154">**Interface ID3D10EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="3576a-155">Obtenir et définir une matrice.</span><span class="sxs-lookup"><span data-stu-id="3576a-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="3576a-156">**Interface ID3D10EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="3576a-157">Obtient et définit une valeur scalaire.</span><span class="sxs-lookup"><span data-stu-id="3576a-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="3576a-158">**Interface ID3D10EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="3576a-159">Obtient et définit une variable de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="3576a-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="3576a-160">**Interface ID3D10EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="3576a-161">Obtient et définit une chaîne.</span><span class="sxs-lookup"><span data-stu-id="3576a-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="3576a-162">**Interface ID3D10EffectType**</span><span class="sxs-lookup"><span data-stu-id="3576a-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="3576a-163">Obtient un type de variable.</span><span class="sxs-lookup"><span data-stu-id="3576a-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="3576a-164">**Interface ID3D10EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="3576a-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="3576a-165">Obtient et définit un vecteur.</span><span class="sxs-lookup"><span data-stu-id="3576a-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="3576a-166">Toutes les interfaces de réflexion dérivent de l' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span><span class="sxs-lookup"><span data-stu-id="3576a-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3576a-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3576a-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3576a-168">Effets</span><span class="sxs-lookup"><span data-stu-id="3576a-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="3576a-169">Guide de programmation pour Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="3576a-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
