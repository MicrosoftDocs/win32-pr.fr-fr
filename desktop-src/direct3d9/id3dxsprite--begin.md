---
description: Prépare un appareil pour le dessin des sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite :: Begin, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106541254"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="0bc77-103">ID3DXSprite :: Begin, méthode</span><span class="sxs-lookup"><span data-stu-id="0bc77-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="0bc77-104">Prépare un appareil pour le dessin des sprites.</span><span class="sxs-lookup"><span data-stu-id="0bc77-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bc77-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="0bc77-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bc77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc77-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0bc77-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc77-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0bc77-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0bc77-109">Combinaison de zéro, un ou plusieurs indicateurs qui décrivent les options de rendu Sprite.</span><span class="sxs-lookup"><span data-stu-id="0bc77-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="0bc77-110">Pour cette méthode, les indicateurs valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="0bc77-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="0bc77-111">D3DXSPRITE \_ ALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="0bc77-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="0bc77-112">\_ \_ Panneau D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="0bc77-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="0bc77-113">D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE</span><span class="sxs-lookup"><span data-stu-id="0bc77-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="0bc77-114">D3DXSPRITE \_ DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="0bc77-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="0bc77-115">D3DXSPRITE \_ OBJECTSPACE</span><span class="sxs-lookup"><span data-stu-id="0bc77-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="0bc77-116">D3DXSPRITE \_ \_ profondeur de tri \_ \_ BACKTOFRONT</span><span class="sxs-lookup"><span data-stu-id="0bc77-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="0bc77-117">D3DXSPRITE \_ \_ profondeur de tri \_ \_ FRONTTOBACK</span><span class="sxs-lookup"><span data-stu-id="0bc77-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="0bc77-118">\_ \_ Texture de tri D3DXSPRITE \_</span><span class="sxs-lookup"><span data-stu-id="0bc77-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="0bc77-119">Pour obtenir une description des indicateurs et pour plus d’informations sur la façon de contrôler la capture de l’état des appareils et des transformations d’affichage des appareils, consultez [D3DXSPRITE](d3dxsprite.md).</span><span class="sxs-lookup"><span data-stu-id="0bc77-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc77-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bc77-120">Return value</span></span>

<span data-ttu-id="0bc77-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0bc77-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0bc77-122">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bc77-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0bc77-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0bc77-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc77-124">Notes</span><span class="sxs-lookup"><span data-stu-id="0bc77-124">Remarks</span></span>

<span data-ttu-id="0bc77-125">Cette méthode doit être appelée à partir d’un [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0bc77-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="0bc77-126">.</span><span class="sxs-lookup"><span data-stu-id="0bc77-126">.</span></span> <span data-ttu-id="0bc77-127">.</span><span class="sxs-lookup"><span data-stu-id="0bc77-127">.</span></span> <span data-ttu-id="0bc77-128">Séquence [**IDirect3DDevice9 :: EndScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0bc77-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="0bc77-129">**ID3DXSprite :: Begin** ne peut pas être utilisé comme substitut pour **IDirect3DDevice9 :: BeginScene** ou [**ID3DXRenderToSurface :: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="0bc77-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="0bc77-130">Cette méthode définit les États suivants sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0bc77-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="0bc77-131">États de rendu :</span><span class="sxs-lookup"><span data-stu-id="0bc77-131">Render States:</span></span>



| <span data-ttu-id="0bc77-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="0bc77-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="0bc77-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc77-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc77-134">D3DRS \_ ALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="0bc77-135">TRUE</span><span class="sxs-lookup"><span data-stu-id="0bc77-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="0bc77-136">D3DRS \_ ALPHAFUNC</span><span class="sxs-lookup"><span data-stu-id="0bc77-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="0bc77-137">D3DCMP \_ plus</span><span class="sxs-lookup"><span data-stu-id="0bc77-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="0bc77-138">D3DRS \_ ALPHAREF</span><span class="sxs-lookup"><span data-stu-id="0bc77-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="0bc77-139">0x00</span><span class="sxs-lookup"><span data-stu-id="0bc77-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="0bc77-140">D3DRS \_ ALPHATESTENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="0bc77-141">AlphaCmpCaps</span><span class="sxs-lookup"><span data-stu-id="0bc77-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="0bc77-142">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="0bc77-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="0bc77-143">D3DBLENDOP \_ Ajouter</span><span class="sxs-lookup"><span data-stu-id="0bc77-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="0bc77-144">\_Découpage D3DRS</span><span class="sxs-lookup"><span data-stu-id="0bc77-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="0bc77-145">TRUE</span><span class="sxs-lookup"><span data-stu-id="0bc77-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="0bc77-146">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="0bc77-147">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-148">D3DRS \_ COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="0bc77-149">D3DCOLORWRITEENABLE \_ alpha \| D3DCOLORWRITEENABLE \_ bleu \| D3DCOLORWRITEENABLE \_ vert \| D3DCOLORWRITEENABLE \_ rouge</span><span class="sxs-lookup"><span data-stu-id="0bc77-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="0bc77-150">D3DRS \_ CULLMODE</span><span class="sxs-lookup"><span data-stu-id="0bc77-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="0bc77-151">D3DCULL \_ aucun</span><span class="sxs-lookup"><span data-stu-id="0bc77-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="0bc77-152">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="0bc77-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="0bc77-153">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="0bc77-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="0bc77-154">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="0bc77-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="0bc77-155">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="0bc77-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="0bc77-156">D3DRS \_ ENABLEADAPTIVETESSELLATION</span><span class="sxs-lookup"><span data-stu-id="0bc77-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="0bc77-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-158">D3DRS \_ FillMode</span><span class="sxs-lookup"><span data-stu-id="0bc77-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="0bc77-159">D3DFILL \_ Solid</span><span class="sxs-lookup"><span data-stu-id="0bc77-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="0bc77-160">D3DRS \_ FOGENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="0bc77-161">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-162">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="0bc77-163">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-164">\_Éclairage D3DRS</span><span class="sxs-lookup"><span data-stu-id="0bc77-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="0bc77-165">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-166">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="0bc77-167">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-168">D3DRS \_ SEPARATEALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="0bc77-169">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-170">D3DRS \_ SHADEMODE</span><span class="sxs-lookup"><span data-stu-id="0bc77-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="0bc77-171">D3DSHADE \_ Gouraud</span><span class="sxs-lookup"><span data-stu-id="0bc77-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="0bc77-172">D3DRS \_ SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="0bc77-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="0bc77-173">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-174">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="0bc77-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="0bc77-175">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="0bc77-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="0bc77-176">D3DRS \_ SRGBWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="0bc77-177">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-178">D3DRS \_ STENCILENABLE</span><span class="sxs-lookup"><span data-stu-id="0bc77-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="0bc77-179">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-180">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="0bc77-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="0bc77-181">FALSE</span><span class="sxs-lookup"><span data-stu-id="0bc77-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="0bc77-182">D3DRS \_ WRAP0</span><span class="sxs-lookup"><span data-stu-id="0bc77-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="0bc77-183">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="0bc77-184">États des étapes de texture :</span><span class="sxs-lookup"><span data-stu-id="0bc77-184">Texture Stage States:</span></span>



| <span data-ttu-id="0bc77-185">Identificateur de l’étape</span><span class="sxs-lookup"><span data-stu-id="0bc77-185">Stage Identifier</span></span> | <span data-ttu-id="0bc77-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span><span class="sxs-lookup"><span data-stu-id="0bc77-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="0bc77-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc77-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="0bc77-188">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-188">0</span></span>                | <span data-ttu-id="0bc77-189">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="0bc77-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="0bc77-190">\_Texture D3DTA</span><span class="sxs-lookup"><span data-stu-id="0bc77-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="0bc77-191">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-191">0</span></span>                | <span data-ttu-id="0bc77-192">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="0bc77-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="0bc77-193">\_Diffusion D3DTA</span><span class="sxs-lookup"><span data-stu-id="0bc77-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="0bc77-194">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-194">0</span></span>                | <span data-ttu-id="0bc77-195">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="0bc77-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="0bc77-196">\_Modulation D3DTOP</span><span class="sxs-lookup"><span data-stu-id="0bc77-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="0bc77-197">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-197">0</span></span>                | <span data-ttu-id="0bc77-198">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="0bc77-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="0bc77-199">\_Texture D3DTA</span><span class="sxs-lookup"><span data-stu-id="0bc77-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="0bc77-200">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-200">0</span></span>                | <span data-ttu-id="0bc77-201">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="0bc77-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="0bc77-202">\_Diffusion D3DTA</span><span class="sxs-lookup"><span data-stu-id="0bc77-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="0bc77-203">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-203">0</span></span>                | <span data-ttu-id="0bc77-204">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="0bc77-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="0bc77-205">\_Modulation D3DTOP</span><span class="sxs-lookup"><span data-stu-id="0bc77-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="0bc77-206">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-206">0</span></span>                | <span data-ttu-id="0bc77-207">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="0bc77-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="0bc77-208">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-208">0</span></span>                |
| <span data-ttu-id="0bc77-209">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-209">0</span></span>                | <span data-ttu-id="0bc77-210">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="0bc77-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="0bc77-211">Désactivation de D3DTTFF \_</span><span class="sxs-lookup"><span data-stu-id="0bc77-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="0bc77-212">1</span><span class="sxs-lookup"><span data-stu-id="0bc77-212">1</span></span>                | <span data-ttu-id="0bc77-213">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="0bc77-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="0bc77-214">Désactivation de D3DTOP \_</span><span class="sxs-lookup"><span data-stu-id="0bc77-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="0bc77-215">1</span><span class="sxs-lookup"><span data-stu-id="0bc77-215">1</span></span>                | <span data-ttu-id="0bc77-216">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="0bc77-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="0bc77-217">Désactivation de D3DTOP \_</span><span class="sxs-lookup"><span data-stu-id="0bc77-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="0bc77-218">États de l’échantillonneur :</span><span class="sxs-lookup"><span data-stu-id="0bc77-218">Sampler States:</span></span>



| <span data-ttu-id="0bc77-219">Index d’étape de l’échantillonneur</span><span class="sxs-lookup"><span data-stu-id="0bc77-219">Sampler Stage Index</span></span> | <span data-ttu-id="0bc77-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="0bc77-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="0bc77-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc77-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc77-222">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-222">0</span></span>                   | <span data-ttu-id="0bc77-223">\_Adresse D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="0bc77-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="0bc77-224">D3DTADDRESS \_ clamp</span><span class="sxs-lookup"><span data-stu-id="0bc77-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="0bc77-225">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-225">0</span></span>                   | <span data-ttu-id="0bc77-226">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="0bc77-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="0bc77-227">D3DTADDRESS \_ clamp</span><span class="sxs-lookup"><span data-stu-id="0bc77-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="0bc77-228">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-228">0</span></span>                   | <span data-ttu-id="0bc77-229">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="0bc77-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="0bc77-230">D3DTEXF \_ anisotrope si TextureFilterCaps comprend D3DPTFILTERCAPS \_ MAGFANISOTROPIC ; sinon, D3DTEXF \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="0bc77-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="0bc77-231">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-231">0</span></span>                   | <span data-ttu-id="0bc77-232">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="0bc77-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="0bc77-233">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-233">0</span></span>                                                                                                              |
| <span data-ttu-id="0bc77-234">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-234">0</span></span>                   | <span data-ttu-id="0bc77-235">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="0bc77-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="0bc77-236">MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="0bc77-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="0bc77-237">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-237">0</span></span>                   | <span data-ttu-id="0bc77-238">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="0bc77-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="0bc77-239">D3DTEXF \_ anisotrope si TextureFilterCaps comprend D3DPTFILTERCAPS \_ MINFANISOTROPIC ; sinon, D3DTEXF \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="0bc77-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="0bc77-240">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-240">0</span></span>                   | <span data-ttu-id="0bc77-241">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="0bc77-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="0bc77-242">D3DTEXF \_ Linear si TextureFilterCaps comprend D3DPTFILTERCAPS \_ MIPFLINEAR ; sinon D3DTEXF \_ point</span><span class="sxs-lookup"><span data-stu-id="0bc77-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="0bc77-243">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-243">0</span></span>                   | <span data-ttu-id="0bc77-244">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="0bc77-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="0bc77-245">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-245">0</span></span>                                                                                                              |
| <span data-ttu-id="0bc77-246">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-246">0</span></span>                   | <span data-ttu-id="0bc77-247">D3DSAMP \_ SRGBTEXTURE</span><span class="sxs-lookup"><span data-stu-id="0bc77-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="0bc77-248">0</span><span class="sxs-lookup"><span data-stu-id="0bc77-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="0bc77-249">Cette méthode désactive N-patchs.</span><span class="sxs-lookup"><span data-stu-id="0bc77-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0bc77-250">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bc77-250">Requirements</span></span>



| <span data-ttu-id="0bc77-251">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bc77-251">Requirement</span></span> | <span data-ttu-id="0bc77-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bc77-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc77-253">En-tête</span><span class="sxs-lookup"><span data-stu-id="0bc77-253">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc77-254"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc77-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0bc77-255">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0bc77-255">Library</span></span><br/> | <dl> <span data-ttu-id="0bc77-256"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0bc77-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0bc77-257">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bc77-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc77-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="0bc77-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="0bc77-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="0bc77-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
