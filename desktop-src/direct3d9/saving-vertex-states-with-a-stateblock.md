---
description: Un bloc d’État peut être utilisé pour capturer uniquement l’état du vertex (consultez États d’enregistrement et de restauration des blocs d’État (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Enregistrement des États de vertex avec un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517388"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="0ee8a-103">Enregistrement des États de vertex avec un StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ee8a-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="0ee8a-104">Un bloc d’État peut être utilisé pour capturer uniquement l’état du vertex (consultez États d' [enregistrement et de restauration des blocs d’État (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="0ee8a-105">L’état suivant est état du vertex :</span><span class="sxs-lookup"><span data-stu-id="0ee8a-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="0ee8a-106">État du rendu de vertex (voir [pipeline de vertex : état de rendu](#vertex-pipeline-render-state)).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="0ee8a-107">État de l’échantillonneur de vertex (voir [pipeline de vertex : état de l’échantillonneur](#vertex-pipeline-sampler-state)).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="0ee8a-108">État de la texture de vertex (voir [pipeline de vertex : état](#vertex-pipeline-texture-state)de la texture).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="0ee8a-109">Segments en mode NPatch à partir de [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="0ee8a-110">Chaque lumière de [**IDirect3DDevice9 :: SetLight**](/windows/desktop/api), et si la lumière est activée ou non avec [**IDirect3DDevice9 :: éclaircie**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="0ee8a-111">Le nuanceur de sommets actuel et chacune des constantes de nuanceur vertex.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="0ee8a-112">Pour chaque flux de vertex, stockez la valeur de diviseur à partir de [**IDirect3DDevice9 :: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="0ee8a-113">Déclaration de vertex actuelle.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-113">The current vertex declaration.</span></span>

<span data-ttu-id="0ee8a-114">Pour capturer l’état du vertex avec un bloc d’État, spécifiez D3DSBT \_ VERTEXSTATE lors de l’appel de [**IDirect3DDevice9 :: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="0ee8a-115">Pipeline de vertex : état de rendu</span><span class="sxs-lookup"><span data-stu-id="0ee8a-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="0ee8a-116">Les États de rendu des appareils affectent le comportement de presque toutes les parties du pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="0ee8a-117">Les États de rendu sont définis en appelant [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="0ee8a-118">Le tableau suivant répertorie tous les États de rendu qui définissent l’état du vertex :</span><span class="sxs-lookup"><span data-stu-id="0ee8a-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="0ee8a-119">États de rendu</span><span class="sxs-lookup"><span data-stu-id="0ee8a-119">Render States</span></span>                           | <span data-ttu-id="0ee8a-120">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="0ee8a-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="0ee8a-121">D3DRS \_ CULLMODE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="0ee8a-122">\_CCW D3DCULL</span><span class="sxs-lookup"><span data-stu-id="0ee8a-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="0ee8a-123">D3DRS \_ FOGCOLOR</span><span class="sxs-lookup"><span data-stu-id="0ee8a-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="0ee8a-124">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-124">0</span></span>                      |
| <span data-ttu-id="0ee8a-125">D3DRS \_ FOGTABLEMODE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="0ee8a-126">D3DFOG \_ aucun</span><span class="sxs-lookup"><span data-stu-id="0ee8a-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="0ee8a-127">D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="0ee8a-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="0ee8a-128">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-128">0</span></span>                      |
| <span data-ttu-id="0ee8a-129">D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="0ee8a-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="0ee8a-130">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-130">1</span></span>                      |
| <span data-ttu-id="0ee8a-131">D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="0ee8a-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="0ee8a-132">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-132">1</span></span>                      |
| <span data-ttu-id="0ee8a-133">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="0ee8a-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-134">**FALSE**</span></span>              |
| <span data-ttu-id="0ee8a-135">D3DRS \_ ambiant</span><span class="sxs-lookup"><span data-stu-id="0ee8a-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="0ee8a-136">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-136">0</span></span>                      |
| <span data-ttu-id="0ee8a-137">D3DRS \_ COLORVERTEX</span><span class="sxs-lookup"><span data-stu-id="0ee8a-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="0ee8a-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-138">**TRUE**</span></span>               |
| <span data-ttu-id="0ee8a-139">D3DRS \_ FOGVERTEXMODE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="0ee8a-140">D3DFOG \_ aucun</span><span class="sxs-lookup"><span data-stu-id="0ee8a-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="0ee8a-141">\_Découpage D3DRS</span><span class="sxs-lookup"><span data-stu-id="0ee8a-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="0ee8a-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-142">**TRUE**</span></span>               |
| <span data-ttu-id="0ee8a-143">\_Éclairage D3DRS</span><span class="sxs-lookup"><span data-stu-id="0ee8a-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="0ee8a-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-144">**TRUE**</span></span>               |
| <span data-ttu-id="0ee8a-145">D3DRS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="0ee8a-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="0ee8a-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-146">**TRUE**</span></span>               |
| <span data-ttu-id="0ee8a-147">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="0ee8a-148">\_Matériau D3DMCS</span><span class="sxs-lookup"><span data-stu-id="0ee8a-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="0ee8a-149">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="0ee8a-150">\_Matériau D3DMCS</span><span class="sxs-lookup"><span data-stu-id="0ee8a-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="0ee8a-151">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="0ee8a-152">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="0ee8a-153">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="0ee8a-154">D3DMCS \_ COLOR2</span><span class="sxs-lookup"><span data-stu-id="0ee8a-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="0ee8a-155">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="0ee8a-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="0ee8a-156">Désactivation de D3DVBF \_</span><span class="sxs-lookup"><span data-stu-id="0ee8a-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="0ee8a-157">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="0ee8a-158">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-158">0</span></span>                      |
| <span data-ttu-id="0ee8a-159">D3DRS \_ pointe</span><span class="sxs-lookup"><span data-stu-id="0ee8a-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="0ee8a-160">Dépend du pilote</span><span class="sxs-lookup"><span data-stu-id="0ee8a-160">Driver dependent</span></span>       |
| <span data-ttu-id="0ee8a-161">D3DRS \_ pointe \_ min.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="0ee8a-162">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-162">1</span></span>                      |
| <span data-ttu-id="0ee8a-163">D3DRS \_ POINTSPRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="0ee8a-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-164">**FALSE**</span></span>              |
| <span data-ttu-id="0ee8a-165">D3DRS \_ POINTSCALEENABLE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="0ee8a-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-166">**FALSE**</span></span>              |
| <span data-ttu-id="0ee8a-167">D3DRS \_ POINTSCALE \_ A</span><span class="sxs-lookup"><span data-stu-id="0ee8a-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="0ee8a-168">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-168">1</span></span>                      |
| <span data-ttu-id="0ee8a-169">D3DRS \_ POINTSCALE \_ B</span><span class="sxs-lookup"><span data-stu-id="0ee8a-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="0ee8a-170">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-170">0</span></span>                      |
| <span data-ttu-id="0ee8a-171">D3DRS \_ POINTSCALE \_ C</span><span class="sxs-lookup"><span data-stu-id="0ee8a-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="0ee8a-172">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-172">0</span></span>                      |
| <span data-ttu-id="0ee8a-173">D3DRS \_ MULTISAMPLEANTIALIAS</span><span class="sxs-lookup"><span data-stu-id="0ee8a-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="0ee8a-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-174">**TRUE**</span></span>               |
| <span data-ttu-id="0ee8a-175">D3DRS \_ MULTISAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="0ee8a-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="0ee8a-176">égale</span><span class="sxs-lookup"><span data-stu-id="0ee8a-176">0xffffffff</span></span>             |
| <span data-ttu-id="0ee8a-177">D3DRS \_ PATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="0ee8a-178">D3DPATCHEDGE \_ discret</span><span class="sxs-lookup"><span data-stu-id="0ee8a-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="0ee8a-179">D3DRS \_ pointe \_ Max.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="0ee8a-180">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-180">1</span></span>                      |
| <span data-ttu-id="0ee8a-181">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="0ee8a-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-182">**FALSE**</span></span>              |
| <span data-ttu-id="0ee8a-183">D3DRS \_ TWEENFACTOR</span><span class="sxs-lookup"><span data-stu-id="0ee8a-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="0ee8a-184">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-184">0</span></span>                      |
| <span data-ttu-id="0ee8a-185">D3DRS \_ POSITIONDEGREE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="0ee8a-186">D3DDEGREE \_ cubique</span><span class="sxs-lookup"><span data-stu-id="0ee8a-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="0ee8a-187">D3DRS \_ NORMALDEGREE</span><span class="sxs-lookup"><span data-stu-id="0ee8a-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="0ee8a-188">D3DDEGREE \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="0ee8a-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="0ee8a-189">D3DRS \_ MINTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="0ee8a-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="0ee8a-190">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-190">1</span></span>                      |
| <span data-ttu-id="0ee8a-191">D3DRS \_ MAXTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="0ee8a-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="0ee8a-192">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-192">1</span></span>                      |
| <span data-ttu-id="0ee8a-193">D3DRS \_ ADAPTIVETESS \_ X</span><span class="sxs-lookup"><span data-stu-id="0ee8a-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="0ee8a-194">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-194">0</span></span>                      |
| <span data-ttu-id="0ee8a-195">D3DRS \_ ADAPTIVETESS \_ Y</span><span class="sxs-lookup"><span data-stu-id="0ee8a-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="0ee8a-196">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-196">0</span></span>                      |
| <span data-ttu-id="0ee8a-197">D3DRS \_ ADAPTIVETESS \_ Z</span><span class="sxs-lookup"><span data-stu-id="0ee8a-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="0ee8a-198">1</span><span class="sxs-lookup"><span data-stu-id="0ee8a-198">1</span></span>                      |
| <span data-ttu-id="0ee8a-199">D3DRS \_ ADAPTIVETESS \_ W</span><span class="sxs-lookup"><span data-stu-id="0ee8a-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="0ee8a-200">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-200">0</span></span>                      |
| <span data-ttu-id="0ee8a-201">D3DRS \_ ENABLEADAPTIVETESSELLATION "/></span><span class="sxs-lookup"><span data-stu-id="0ee8a-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="0ee8a-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="0ee8a-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="0ee8a-203">Pipeline de vertex : état de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="0ee8a-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="0ee8a-204">Les États de l’échantillonneur contrôlent les rubriques connexes relatives à l’échantillonnage, telles que le filtrage, la mosaïque et les modes d’adresse des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="0ee8a-205">Utilisez [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) pour configurer l’état de l’échantillonneur (y compris celui utilisé dans l’unité du paveur pour échantillonner les mappages de déplacement).</span><span class="sxs-lookup"><span data-stu-id="0ee8a-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="0ee8a-206">Les États de l’échantillonneur ont été renommés avec un \_ préfixe « D3DSAMP » pour permettre la détection des erreurs au moment de la compilation lors du Portage à partir de DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="0ee8a-207">Le tableau suivant répertorie tous les États de l’échantillonneur qui configurent l’état du vertex :</span><span class="sxs-lookup"><span data-stu-id="0ee8a-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="0ee8a-208">États de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="0ee8a-208">Sampler States</span></span>      | <span data-ttu-id="0ee8a-209">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="0ee8a-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="0ee8a-210">D3DSAMP \_ DMAPOFFSET</span><span class="sxs-lookup"><span data-stu-id="0ee8a-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="0ee8a-211">256</span><span class="sxs-lookup"><span data-stu-id="0ee8a-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="0ee8a-212">Pipeline de vertex : état de la texture</span><span class="sxs-lookup"><span data-stu-id="0ee8a-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="0ee8a-213">Les États de texture contrôlent les opérations de fusion de texture du mélangeur à textures multiples.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="0ee8a-214">Utilisez [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api) pour définir les États de texture.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="0ee8a-215">Utilisez [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) pour associer une texture à une étape d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="0ee8a-216">Le tableau suivant répertorie tous les États de texture qui définissent l’état du vertex :</span><span class="sxs-lookup"><span data-stu-id="0ee8a-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="0ee8a-217">États de la texture</span><span class="sxs-lookup"><span data-stu-id="0ee8a-217">Texture States</span></span>                | <span data-ttu-id="0ee8a-218">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="0ee8a-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="0ee8a-219">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="0ee8a-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="0ee8a-220">0</span><span class="sxs-lookup"><span data-stu-id="0ee8a-220">0</span></span>                |
| <span data-ttu-id="0ee8a-221">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="0ee8a-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="0ee8a-222">Désactivation de D3DTTFF \_</span><span class="sxs-lookup"><span data-stu-id="0ee8a-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="0ee8a-223">D3DTSS \_ TEXCOORDINDEX est un état de traitement de vertex de fonction fixe.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="0ee8a-224">Si un nuanceur de sommet programmable est utilisé, cet État est ignoré.</span><span class="sxs-lookup"><span data-stu-id="0ee8a-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ee8a-225">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ee8a-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ee8a-226">État de l’enregistrement et de la restauration des blocs d’État</span><span class="sxs-lookup"><span data-stu-id="0ee8a-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
