---
description: Cette section spécifie les formats ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans le matériel 10,0 de niveau de fonctionnalité Direct3D.
ms.assetid: 3C1CCA7D-9F2F-4B1B-8424-BA9C6DED4974
title: Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 10.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f298460330feb2143b20da37ae82c3a6d63790
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200694"
---
# <a name="format-support-for-direct3d-feature-level-100-hardware"></a><span data-ttu-id="2b66d-103">Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 10.0</span><span class="sxs-lookup"><span data-stu-id="2b66d-103">Format support for Direct3D Feature Level 10.0 hardware</span></span>

<span data-ttu-id="2b66d-104">Cette section spécifie les formats ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans le matériel 10,0 de niveau de fonctionnalité Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2b66d-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.0 hardware.</span></span>

<span data-ttu-id="2b66d-105">Le tableau récapitule la prise en charge des fonctionnalités à l’aide de la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="2b66d-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="2b66d-106">Symbole</span><span class="sxs-lookup"><span data-stu-id="2b66d-106">Symbol</span></span>                            | <span data-ttu-id="2b66d-107">Description</span><span class="sxs-lookup"><span data-stu-id="2b66d-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="2b66d-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="2b66d-108">_ *-*\*</span></span>                             | <span data-ttu-id="2b66d-109">Non autorisé ou non disponible.</span><span class="sxs-lookup"><span data-stu-id="2b66d-109">Disallowed or not available.</span></span>                                                  |
| ![obligatoire](images/letter-r.jpg)  | <span data-ttu-id="2b66d-111">Un support matériel est requis.</span><span class="sxs-lookup"><span data-stu-id="2b66d-111">Hardware support is required.</span></span>                                                 |
| ![facultatif](images/letter-o.jpg)  | <span data-ttu-id="2b66d-113">Prise en charge du matériel facultative, le format peut ou non être accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="2b66d-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dépendants](images/letter-d.jpg) | <span data-ttu-id="2b66d-115">Obligatoire si la fonctionnalité facultative associée est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2b66d-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="2b66d-116">Cette rubrique contient une section par format.</span><span class="sxs-lookup"><span data-stu-id="2b66d-116">This topic contains a section per format.</span></span> <span data-ttu-id="2b66d-117">Une *cible* de format (tables contenant une ligne par cible) peut être un type de ressource, une fonction intrinsèque HLSL ou une fonctionnalité particulière qui est dépendante d’un format particulier.</span><span class="sxs-lookup"><span data-stu-id="2b66d-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="2b66d-118">Pour vérifier par programmation la prise en charge du format dans D3D11 et D3D12, consultez vérification de la [prise en charge des fonctionnalités matérielles](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="2b66d-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="2b66d-119">Les nombres des formats sont principalement, mais pas tous, dans l’ordre numérique croissant, &mdash; certains ne sont pas triés par ordre numérique et sont répertoriés avec d’autres formats pertinents.</span><span class="sxs-lookup"><span data-stu-id="2b66d-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="2b66d-120">Notez également que les *types* sans type dans un nom de format peuvent signifier un type *partiellement* typé, et non strictement typés (reportez-vous à la section Remarques sur le [format](#format-notes) à la fin de la rubrique).</span><span class="sxs-lookup"><span data-stu-id="2b66d-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>
 
## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="2b66d-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="2b66d-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="2b66d-122">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-122">Target</span></span> | <span data-ttu-id="2b66d-123">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-123">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-124">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-125">0</span><span class="sxs-lookup"><span data-stu-id="2b66d-125">0</span></span> |
| <span data-ttu-id="2b66d-126">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-126">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-128">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-130">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-131">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-132">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-133">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-134">Texture2D</span></span> | \- |
| <span data-ttu-id="2b66d-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-135">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-136">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-137">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-137">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-138">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-139">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-140">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-141">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-142">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-143">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-143">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-144">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-146">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-147">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-148">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-149">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-150">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-151">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-152">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-153">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-155">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-157">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-158">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-159">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-160">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-160">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-162">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-163">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-164">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-165">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-166">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-167">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-168">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-169">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-170">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-171">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-172">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-173">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="2b66d-174">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32A32 type (1)</span><span class="sxs-lookup"><span data-stu-id="2b66d-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="2b66d-175">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-175">Target</span></span> | <span data-ttu-id="2b66d-176">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-176">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-177">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-178">128</span><span class="sxs-lookup"><span data-stu-id="2b66d-178">128</span></span> |
| <span data-ttu-id="2b66d-179">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-179">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-181">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-182">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-183">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-184">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-185">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-187">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-189">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-191">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-193">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-193">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-194">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-195">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-196">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-197">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-198">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-199">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-199">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-201">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-203">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-204">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-205">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-206">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-207">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-208">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-209">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-210">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-211">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-212">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-214">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-215">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-216">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-217">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-217">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-219">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-220">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-221">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-222">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-223">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-224">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-225">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-225">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-227">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-228">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-229">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-230">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-230">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-232">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="2b66d-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="2b66d-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="2b66d-234">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-234">Target</span></span> | <span data-ttu-id="2b66d-235">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-235">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-236">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-237">128</span><span class="sxs-lookup"><span data-stu-id="2b66d-237">128</span></span> |
| <span data-ttu-id="2b66d-238">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-238">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-240">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-242">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-242">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-244">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-245">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-245">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-247">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-249">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-251">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-253">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-255">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-255">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-257">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-257">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-259">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-260">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-261">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-262">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-263">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-263">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-265">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-265">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-267">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-269">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-269">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-271">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-272">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-273">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-274">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-275">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-276">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-277">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-278">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-279">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-281">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-282">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-283">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-284">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-284">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-286">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-286">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-288">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-288">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-290">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-290">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-292">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-292">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-294">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-294">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-296">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-297">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-297">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-299">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-300">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-301">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-302">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-302">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-304">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="2b66d-305">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="2b66d-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="2b66d-306">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-306">Target</span></span> | <span data-ttu-id="2b66d-307">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-307">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-308">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-309">128</span><span class="sxs-lookup"><span data-stu-id="2b66d-309">128</span></span> |
| <span data-ttu-id="2b66d-310">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-310">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-312">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-314">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-314">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-316">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-317">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-317">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-319">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-321">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-323">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-325">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-327">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-327">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-329">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-330">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-331">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-332">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-333">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-334">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-334">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-336">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-337">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-339">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-340">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-340">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-342">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-343">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-344">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-345">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-346">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-347">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-348">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-349">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-351">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-352">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-353">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-354">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-354">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-356">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-356">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-358">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-358">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-360">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-360">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-362">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-363">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-363">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-365">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-366">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-366">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-368">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-369">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-370">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-371">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-371">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-373">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="2b66d-374">DXGI_FORMAT_R32G32B32A32 \_ Saint-<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="2b66d-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="2b66d-375">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-375">Target</span></span> | <span data-ttu-id="2b66d-376">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-376">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-377">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-378">128</span><span class="sxs-lookup"><span data-stu-id="2b66d-378">128</span></span> |
| <span data-ttu-id="2b66d-379">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-379">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-381">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-383">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-383">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-385">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-386">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-386">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-388">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-390">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-392">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-394">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-396">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-396">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-398">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-399">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-400">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-401">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-402">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-403">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-403">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-405">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-406">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-408">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-409">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-410">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-411">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-412">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-413">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-414">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-415">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-417">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-419">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-420">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-421">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-422">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-422">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-424">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-424">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-426">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-426">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-428">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-428">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-430">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-431">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-431">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-433">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-434">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-434">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-436">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-437">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-438">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-439">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-439">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-441">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="2b66d-442">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32 type (5)</span><span class="sxs-lookup"><span data-stu-id="2b66d-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="2b66d-443">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-443">Target</span></span> | <span data-ttu-id="2b66d-444">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-444">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-445">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-446">96</span><span class="sxs-lookup"><span data-stu-id="2b66d-446">96</span></span> |
| <span data-ttu-id="2b66d-447">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-447">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-449">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-450">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-451">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-452">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-453">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-455">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-457">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-459">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-461">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-461">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-462">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-463">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-464">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-465">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-466">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-467">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-467">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-469">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-471">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-472">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-473">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-474">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-475">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-476">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-477">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-478">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-480">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-482">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-483">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-484">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-485">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-485">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-487">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-488">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-489">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-490">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-491">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-492">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-493">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-493">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-495">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-496">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-497">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-498">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-499">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="2b66d-500">DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="2b66d-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="2b66d-501">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-501">Target</span></span> | <span data-ttu-id="2b66d-502">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-502">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-503">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-504">96</span><span class="sxs-lookup"><span data-stu-id="2b66d-504">96</span></span> |
| <span data-ttu-id="2b66d-505">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-505">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-507">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-509">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-509">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-511">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-512">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-512">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-514">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-516">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-518">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-520">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-522">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-522">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-524">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-524">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-526">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-527">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-528">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-529">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-530">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-530">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-532">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-532">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-534">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-536">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-536">Blendable RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-538">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-539">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-540">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-541">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-542">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-543">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-544">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-545">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-546">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-548">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-549">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-550">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-551">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-551">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-553">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-553">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-555">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-555">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-557">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-557">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-559">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-559">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-561">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-561">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-563">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-564">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-564">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-566">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-567">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-568">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-569">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-570">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="2b66d-571">DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="2b66d-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="2b66d-572">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-572">Target</span></span> | <span data-ttu-id="2b66d-573">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-573">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-574">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-575">96</span><span class="sxs-lookup"><span data-stu-id="2b66d-575">96</span></span> |
| <span data-ttu-id="2b66d-576">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-576">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-578">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-580">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-580">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-582">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-583">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-583">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-585">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-587">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-589">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-591">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-593">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-593">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-595">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-596">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-597">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-598">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-599">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-600">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-600">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-602">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-603">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-605">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-606">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-606">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-608">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-609">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-610">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-611">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-612">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-613">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-614">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-615">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-617">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-618">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-619">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-620">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-620">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-622">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-622">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-624">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-624">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-626">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-626">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-628">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-629">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-629">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-631">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-632">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-632">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-634">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-635">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-636">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-637">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-638">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="2b66d-639">DXGI_FORMAT_R32G32B32 \_ Saint-<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="2b66d-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="2b66d-640">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-640">Target</span></span> | <span data-ttu-id="2b66d-641">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-641">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-642">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-643">96</span><span class="sxs-lookup"><span data-stu-id="2b66d-643">96</span></span> |
| <span data-ttu-id="2b66d-644">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-644">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-646">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-648">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-648">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-650">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-651">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-651">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-653">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-655">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-657">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-659">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-661">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-661">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-663">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-664">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-665">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-666">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-667">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-668">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-668">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-670">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-671">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-673">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-674">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-675">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-676">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-677">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-678">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-679">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-680">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-682">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-684">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-685">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-686">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-687">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-687">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-689">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-689">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-691">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-691">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="2b66d-693">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-693">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-695">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-696">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-696">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-698">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-699">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-699">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-701">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-702">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-703">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-704">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-705">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="2b66d-706">\_<sup>PC</sup> DXGI_FORMAT_R16G16B16A16 type (9)</span><span class="sxs-lookup"><span data-stu-id="2b66d-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="2b66d-707">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-707">Target</span></span> | <span data-ttu-id="2b66d-708">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-708">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-709">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-710">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-710">64</span></span> |
| <span data-ttu-id="2b66d-711">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-711">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-713">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-714">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-715">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-716">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-717">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-719">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-721">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-723">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-725">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-725">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-726">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-727">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-728">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-729">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-730">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-731">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-731">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-733">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-735">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-736">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-737">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-738">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-739">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-740">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-741">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-742">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-743">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-744">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-746">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-747">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-748">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-749">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-749">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-751">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-752">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-753">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-754">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-755">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-756">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-757">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-757">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-759">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-760">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-761">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-762">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-762">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-764">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="2b66d-765">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="2b66d-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="2b66d-766">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-766">Target</span></span> | <span data-ttu-id="2b66d-767">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-767">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-768">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-769">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-769">64</span></span> |
| <span data-ttu-id="2b66d-770">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-770">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-772">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-774">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-774">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-776">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-777">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-778">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-780">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-782">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-784">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-786">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-786">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-788">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-788">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-790">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-791">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-792">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-793">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-794">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-794">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-796">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-796">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-798">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-800">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-800">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-802">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-803">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-804">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-805">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-806">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-807">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-808">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-809">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-810">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-812">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-813">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-814">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-815">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-815">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-817">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-817">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-819">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-819">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-821">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-821">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-823">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-823">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-825">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-825">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-827">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-827">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-829">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-829">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-831">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-832">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-832">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-834">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-834">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-836">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-836">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-838">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="2b66d-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="2b66d-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="2b66d-840">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-840">Target</span></span> | <span data-ttu-id="2b66d-841">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-841">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-842">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-843">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-843">64</span></span> |
| <span data-ttu-id="2b66d-844">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-844">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-846">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-848">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-848">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-850">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-851">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-852">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-854">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-856">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-858">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-860">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-860">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-862">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-862">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-864">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-865">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-866">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-867">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-868">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-868">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-870">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-870">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-872">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-874">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-874">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-876">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-877">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-878">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-879">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-880">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-881">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-882">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-884">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-886">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-887">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-888">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-889">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-889">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-891">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-891">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-893">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-893">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-895">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-895">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-897">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-897">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-899">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-899">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-901">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-902">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-902">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-904">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-905">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-906">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-907">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-907">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-909">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="2b66d-910">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="2b66d-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="2b66d-911">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-911">Target</span></span> | <span data-ttu-id="2b66d-912">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-912">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-913">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-914">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-914">64</span></span> |
| <span data-ttu-id="2b66d-915">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-915">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-917">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-919">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-919">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-921">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-922">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-923">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-925">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-927">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-929">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-931">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-931">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-933">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-934">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-935">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-936">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-937">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-938">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-938">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-940">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-941">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-943">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-944">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-944">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-946">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-947">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-948">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-949">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-950">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-951">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-952">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-953">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-955">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-956">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-957">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-958">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-958">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-960">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-960">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-962">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-962">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-964">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-964">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-966">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-967">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-967">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-969">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-970">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-970">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-972">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-973">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-974">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-975">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-975">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-977">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="2b66d-978">DXGI_FORMAT_R16G16B16A16 \_ ronfler<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="2b66d-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="2b66d-979">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-979">Target</span></span> | <span data-ttu-id="2b66d-980">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-980">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-981">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-982">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-982">64</span></span> |
| <span data-ttu-id="2b66d-983">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-983">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-985">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-987">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-987">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-989">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-990">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-991">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-993">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-995">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-997">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-999">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-999">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1001">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1001">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1003">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1004">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1005">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1006">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1007">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1007">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1009">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1009">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1011">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1013">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1013">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1014">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1014">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1015">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1015">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1016">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1016">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1017">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1017">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1018">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1018">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1019">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1019">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1020">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1020">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1021">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1021">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1022">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1022">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1023">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1023">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1024">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1024">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1025">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1025">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1026">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1026">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1027">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1027">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1029">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1029">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1031">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1031">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1033">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1033">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1035">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1035">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1037">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1037">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1039">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1039">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1040">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1040">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1042">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1042">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1043">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1043">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1044">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1044">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1045">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1045">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1047">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1047">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="2b66d-1048">DXGI_FORMAT_R16G16B16A16 \_ Saint-<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1048">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="2b66d-1049">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1049">Target</span></span> | <span data-ttu-id="2b66d-1050">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1050">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1051">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1051">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1052">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1052">64</span></span> |
| <span data-ttu-id="2b66d-1053">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1053">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1055">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1055">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1057">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1057">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1059">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1059">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1060">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1060">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1061">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1061">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1063">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1063">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1065">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1065">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1067">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1067">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1069">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1069">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1071">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1071">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1072">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1072">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1073">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1073">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1074">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1074">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1075">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1075">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1076">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1076">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1078">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1078">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1079">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1079">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1081">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1081">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1082">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1082">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1083">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1083">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1084">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1084">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1085">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1085">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1086">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1086">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1087">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1087">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1088">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1088">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1089">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1089">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1090">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1090">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1091">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1091">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1092">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1092">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1093">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1093">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1094">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1094">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1095">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1095">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1097">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1097">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1099">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1099">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1101">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1101">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1103">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1103">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1104">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1104">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1106">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1106">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1107">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1107">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1109">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1109">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1110">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1110">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1111">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1111">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1112">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1112">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1114">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="2b66d-1115">\_<sup>PC</sup> DXGI_FORMAT_R32G32 type (15)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1115">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="2b66d-1116">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1116">Target</span></span> | <span data-ttu-id="2b66d-1117">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1117">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1118">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1119">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1119">64</span></span> |
| <span data-ttu-id="2b66d-1120">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1120">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1122">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1122">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1123">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1124">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1125">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1126">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1128">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1130">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1132">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1134">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1134">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-1135">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1135">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1136">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1136">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1137">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1137">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1138">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1138">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1139">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1139">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1140">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1140">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1142">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1143">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1144">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1145">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1146">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1147">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1148">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1149">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1149">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1150">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1151">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1153">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1154">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1155">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1156">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1157">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1158">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1158">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1160">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1160">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1161">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1161">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1162">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1162">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1163">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1163">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1164">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1164">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1165">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1165">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1166">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1166">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1168">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1168">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1169">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1169">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1170">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1170">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1171">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1171">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1172">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1172">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="2b66d-1173">DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1173">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="2b66d-1174">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1174">Target</span></span> | <span data-ttu-id="2b66d-1175">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1175">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1176">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1176">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1177">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1177">64</span></span> |
| <span data-ttu-id="2b66d-1178">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1178">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1180">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1180">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1182">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1182">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1184">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1184">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1185">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1185">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1187">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1189">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1189">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1191">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1191">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1193">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1193">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1195">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1195">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1197">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1197">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1199">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1199">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1200">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1200">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1201">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1201">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1202">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1202">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1203">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1203">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1205">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1205">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1207">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1207">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1209">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1209">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1211">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1211">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1212">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1212">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1213">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1213">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1214">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1214">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1215">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1215">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1216">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1216">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1217">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1217">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1218">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1218">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1219">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1219">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1220">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1220">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1221">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1221">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1222">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1222">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1223">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1223">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1224">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1224">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1226">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1226">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1228">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1228">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1230">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1230">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1232">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1232">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1234">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1234">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1236">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1236">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1237">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1237">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1239">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1239">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1240">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1240">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1241">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1241">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1242">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1242">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1243">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1243">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="2b66d-1244">DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1244">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="2b66d-1245">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1245">Target</span></span> | <span data-ttu-id="2b66d-1246">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1246">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1247">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1247">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1248">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1248">64</span></span> |
| <span data-ttu-id="2b66d-1249">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1249">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1251">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1251">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1253">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1253">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1255">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1255">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1256">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1256">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1258">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1258">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1260">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1260">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1262">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1262">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1264">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1264">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1266">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1266">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1268">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1268">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1269">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1269">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1270">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1270">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1271">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1271">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1272">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1272">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1273">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1273">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1275">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1275">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1276">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1276">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1278">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1278">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1279">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1279">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1281">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1281">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1282">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1282">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1283">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1283">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1284">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1284">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1285">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1285">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1286">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1286">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1287">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1287">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1288">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1288">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1289">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1289">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1290">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1290">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1291">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1291">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1292">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1292">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1293">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1293">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1295">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1295">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1297">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1297">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1299">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1299">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1301">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1302">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1302">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1304">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1304">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1305">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1305">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1307">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1307">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1308">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1308">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1309">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1309">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1310">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1310">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1311">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="2b66d-1312">DXGI_FORMAT_R32G32 \_ Saint-<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1312">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="2b66d-1313">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1313">Target</span></span> | <span data-ttu-id="2b66d-1314">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1314">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1315">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1316">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1316">64</span></span> |
| <span data-ttu-id="2b66d-1317">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1317">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1319">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1319">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1321">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1321">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1323">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1323">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1324">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1324">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1326">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1326">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1328">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1328">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1330">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1330">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1332">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1332">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1334">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1334">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1336">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1336">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1337">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1337">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1338">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1338">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1339">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1339">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1340">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1340">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1341">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1341">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1343">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1343">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1344">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1344">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1346">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1346">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1347">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1347">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1348">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1348">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1349">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1349">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1350">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1350">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1351">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1351">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1352">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1352">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1353">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1353">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1354">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1354">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1355">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1355">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1356">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1356">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1357">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1357">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1358">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1358">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1359">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1359">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1360">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1360">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1362">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1362">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1364">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1364">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1366">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1366">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1368">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1368">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1369">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1369">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1371">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1372">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1372">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1374">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1375">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1376">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1377">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1377">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1378">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="2b66d-1379">\_<sup>PC</sup> DXGI_FORMAT_R32G8X24 type (19)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1379">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="2b66d-1380">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1380">Target</span></span> | <span data-ttu-id="2b66d-1381">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1381">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1382">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1383">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1383">64</span></span> |
| <span data-ttu-id="2b66d-1384">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1384">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1386">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1386">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1387">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1387">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1388">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1388">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1389">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1389">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1390">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1390">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1392">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1394">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-1395">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1395">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1397">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1397">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-1398">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1399">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1400">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1401">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1401">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1402">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1403">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1403">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1405">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1406">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1407">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1407">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1408">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1408">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1409">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1409">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1410">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1410">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1411">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1411">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1412">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1412">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1413">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1413">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1414">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1414">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1415">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1415">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1416">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1416">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1417">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1417">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1418">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1418">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1419">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1419">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1420">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1420">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1421">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1421">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1423">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1424">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1425">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1426">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1427">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1427">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1428">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1429">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1429">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1431">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1431">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1432">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1432">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1433">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1433">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1434">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1434">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1435">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1435">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="2b66d-1436">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1436">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="2b66d-1437">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1437">Target</span></span> | <span data-ttu-id="2b66d-1438">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1438">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1439">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1439">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1440">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1440">64</span></span> |
| <span data-ttu-id="2b66d-1441">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1441">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1443">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1443">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1444">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1444">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1445">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1446">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1447">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1449">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1449">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1451">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1451">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-1452">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1452">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1454">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1454">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-1455">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1455">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1456">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1456">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1457">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1457">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1458">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1458">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1459">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1459">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1460">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1460">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1462">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1462">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1463">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1463">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1464">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1464">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1465">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1465">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1466">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1466">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1468">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1469">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1470">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1471">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1472">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1473">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1474">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1475">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1476">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1477">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1478">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1479">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1479">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1481">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1481">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1483">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1483">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1485">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1485">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1487">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1487">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1488">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1488">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1489">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1489">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1490">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1490">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1492">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1492">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1493">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1493">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1494">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1494">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1495">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1495">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1496">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1496">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="2b66d-1497">DXGI_FORMAT_R32 \_ \_ FCS X8X24 float \_ (<sup></sup> 21)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1497">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="2b66d-1498">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1498">Target</span></span> | <span data-ttu-id="2b66d-1499">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1499">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1500">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1500">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1501">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1501">64</span></span> |
| <span data-ttu-id="2b66d-1502">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1502">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1504">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1504">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1505">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1505">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1506">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1506">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1507">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1507">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1508">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1508">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1510">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1510">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1512">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-1513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1513">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1515">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1515">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1517">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1517">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1519">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1519">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1521">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1521">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1522">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1522">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1523">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1523">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1524">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1524">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1526">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1526">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1527">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1527">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1528">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1528">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1529">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1529">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1530">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1530">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1531">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1531">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1532">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1532">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1533">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1533">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1534">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1534">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1535">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1535">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1536">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1536">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1537">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1537">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1538">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1538">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1539">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1539">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1540">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1540">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1541">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1541">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1542">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1542">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1544">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1544">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1545">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1545">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1546">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1546">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1547">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1547">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1548">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1548">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1549">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1549">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1550">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1550">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1552">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1552">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1553">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1553">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1554">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1554">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1555">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1555">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1556">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1556">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="2b66d-1557">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FCS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1557">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="2b66d-1558">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1558">Target</span></span> | <span data-ttu-id="2b66d-1559">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1559">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1560">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1560">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1561">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-1561">64</span></span> |
| <span data-ttu-id="2b66d-1562">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1562">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1564">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1564">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1565">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1565">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1566">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1566">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1567">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1567">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1568">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1568">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1570">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1570">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1572">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1572">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-1573">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1573">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1575">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1575">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1577">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1577">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1578">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1578">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1579">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1579">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1580">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1580">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1581">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1581">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1582">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1582">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1584">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1584">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1585">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1585">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1586">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1586">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1587">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1587">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1588">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1588">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1589">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1589">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1590">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1590">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1591">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1591">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1592">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1592">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1593">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1593">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1594">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1594">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1595">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1595">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1596">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1596">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1597">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1597">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1598">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1598">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1599">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1599">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1600">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1600">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1602">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1602">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1603">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1603">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1604">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1604">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1605">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1605">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1606">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1606">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1607">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1607">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1608">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1608">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1610">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1610">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1611">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1611">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1612">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1612">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1613">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1613">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1614">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1614">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="2b66d-1615">\_<sup>PC</sup> DXGI_FORMAT_R10G10B10A2 type (23)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1615">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="2b66d-1616">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1616">Target</span></span> | <span data-ttu-id="2b66d-1617">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1617">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1618">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1618">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1619">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-1619">32</span></span> |
| <span data-ttu-id="2b66d-1620">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1620">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1622">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1622">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1623">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1623">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1624">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1624">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1625">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1625">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1626">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1626">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1628">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1628">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1630">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1630">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1632">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1632">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1634">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1634">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-1635">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1635">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1636">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1636">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1637">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1637">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1638">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1638">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1639">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1639">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1640">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1640">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1642">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1642">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1643">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1643">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1644">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1644">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1645">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1645">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1646">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1646">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1647">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1647">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1648">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1648">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1649">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1649">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1650">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1650">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1651">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1651">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1652">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1652">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1653">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1653">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1654">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1654">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1655">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1655">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1656">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1656">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1657">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1657">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1658">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1658">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1660">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1660">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1661">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1661">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1662">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1662">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1663">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1663">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1664">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1664">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1665">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1665">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1666">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1666">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1668">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1669">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1670">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1671">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1671">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1673">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1673">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="2b66d-1674">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1674">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="2b66d-1675">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1675">Target</span></span> | <span data-ttu-id="2b66d-1676">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1676">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1677">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1677">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1678">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-1678">32</span></span> |
| <span data-ttu-id="2b66d-1679">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1679">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1681">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1681">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1683">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1683">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1685">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1685">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1686">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1686">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1687">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1687">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1689">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1689">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1691">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1691">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1693">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1693">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1695">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1695">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1697">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1697">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1699">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1699">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1700">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1700">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1701">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1701">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1702">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1702">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1703">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1703">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1705">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1705">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1707">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1707">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1709">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1709">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1711">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1711">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1712">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1712">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1713">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1713">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1714">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1714">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1715">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1715">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1716">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1716">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1717">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1717">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1718">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1718">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1719">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1719">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1720">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1720">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1721">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1721">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1722">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1722">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1723">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1723">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1724">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1724">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1726">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1726">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1728">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1728">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1730">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1730">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1732">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1732">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1734">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1734">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1736">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1736">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1738">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1738">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1740">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1740">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1741">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1741">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1743">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1743">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1745">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1745">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1747">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1747">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="2b66d-1748">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1748">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="2b66d-1749">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1749">Target</span></span> | <span data-ttu-id="2b66d-1750">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1750">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1751">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1751">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1752">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-1752">32</span></span> |
| <span data-ttu-id="2b66d-1753">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1753">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1755">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1755">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1757">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1757">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1759">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1760">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1761">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1763">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1765">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1765">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1767">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1767">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1769">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1769">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1771">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1771">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1772">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1772">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1773">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1773">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1774">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1774">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1775">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1775">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1776">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1776">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1778">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1778">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1779">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1779">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1781">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1781">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1782">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1782">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1784">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1785">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1786">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1787">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1787">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1788">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1789">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1790">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1791">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1793">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1794">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1795">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1796">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1796">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1798">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1798">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1800">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1800">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1802">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1802">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1804">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1805">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1805">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1807">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1807">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1808">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1808">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1810">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1810">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1811">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1811">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1812">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1812">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1813">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1813">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1815">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1815">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="2b66d-1816">DXGI_FORMAT_R10G10B10 \_ XR de \_ décalage \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1816">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="2b66d-1817">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1817">Target</span></span> | <span data-ttu-id="2b66d-1818">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1818">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1819">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1819">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1820">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-1820">32</span></span> |
| <span data-ttu-id="2b66d-1821">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1821">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1823">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1823">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1824">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1824">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1825">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1825">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1826">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1826">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1827">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1827">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-1828">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1828">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1830">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1830">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-1831">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1831">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-1832">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1832">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-1833">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1833">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1834">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1834">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1835">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1835">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1836">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1836">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1837">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1837">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1838">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1838">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-1839">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1839">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1840">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1840">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1841">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1841">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1842">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1842">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1843">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1843">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1844">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1845">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1846">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1846">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1847">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1848">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1849">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1850">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1852">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1853">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1854">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1855">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1855">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1857">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1857">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1858">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1858">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1859">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1859">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1860">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1860">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1861">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1861">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1862">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1862">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1864">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1864">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1866">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1866">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1867">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1867">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1869">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1869">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1871">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1871">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1873">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="2b66d-1874">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1874">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="2b66d-1875">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1875">Target</span></span> | <span data-ttu-id="2b66d-1876">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1876">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1877">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1878">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-1878">32</span></span> |
| <span data-ttu-id="2b66d-1879">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1879">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1881">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1881">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1883">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1883">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1885">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1886">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1886">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1887">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1887">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1889">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1889">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1891">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1893">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1893">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1895">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1895">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1897">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1897">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1899">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1899">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1900">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1900">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1901">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1901">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1902">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1902">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1903">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1903">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1905">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1905">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1907">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1909">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1909">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1911">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1911">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1912">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1912">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1913">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1913">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1914">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1914">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1915">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1915">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1916">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1916">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1917">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1917">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1918">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1918">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1919">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1919">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1920">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1920">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1921">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1921">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1922">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1922">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1923">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1923">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1924">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1924">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1926">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1926">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1928">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1928">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1930">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1930">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1932">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1932">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1934">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1934">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-1936">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1936">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1937">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1937">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-1938">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1938">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1939">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1939">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1940">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1940">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1941">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1941">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-1942">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-1942">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="2b66d-1943">\_<sup>PC</sup> DXGI_FORMAT_R8G8B8A8 type (27)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1943">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="2b66d-1944">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-1944">Target</span></span> | <span data-ttu-id="2b66d-1945">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-1945">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-1946">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1946">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-1947">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-1947">32</span></span> |
| <span data-ttu-id="2b66d-1948">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-1948">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1950">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-1950">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1951">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1951">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1952">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1952">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1953">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-1953">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-1954">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1954">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1956">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1956">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1958">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-1958">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1960">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-1960">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1962">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-1962">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-1963">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1963">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1964">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1964">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1965">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-1965">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-1966">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-1966">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-1967">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-1967">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-1968">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-1968">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1970">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-1970">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-1971">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1971">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1972">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1972">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1973">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-1973">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-1974">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-1974">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-1975">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-1975">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1976">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-1976">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-1977">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-1977">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-1978">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1978">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-1979">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1979">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-1980">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-1980">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-1981">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1981">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-1982">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-1982">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-1983">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1983">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-1984">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-1984">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1985">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-1985">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-1986">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-1986">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1988">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-1988">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1989">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-1989">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-1990">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-1990">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-1991">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-1991">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-1992">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-1992">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-1993">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-1993">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-1994">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-1994">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-1996">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1996">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-1997">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1997">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-1998">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-1998">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-1999">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-1999">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2001">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2001">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="2b66d-2002">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2002">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="2b66d-2003">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2003">Target</span></span> | <span data-ttu-id="2b66d-2004">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2004">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2005">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2005">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2006">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2006">32</span></span> |
| <span data-ttu-id="2b66d-2007">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2007">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2009">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2009">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2011">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2011">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2013">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2013">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2014">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2014">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2015">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2015">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2017">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2017">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2019">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2019">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2021">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2021">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2023">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2023">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2025">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2025">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2027">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2027">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2028">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2028">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2029">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2029">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2030">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2030">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2031">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2031">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2033">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2033">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2035">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2035">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2037">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2037">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2039">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2040">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2041">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2042">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2043">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2043">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2044">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2045">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2046">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2047">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2048">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2049">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2050">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2051">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2052">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2052">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2054">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2054">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2056">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2056">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2058">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2058">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2060">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2060">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2062">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2062">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2064">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2064">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2066">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2066">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2068">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2068">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2069">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2069">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2071">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2071">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2073">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2073">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2075">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="2b66d-2076">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRVB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2076">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="2b66d-2077">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2077">Target</span></span> | <span data-ttu-id="2b66d-2078">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2078">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2079">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2080">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2080">32</span></span> |
| <span data-ttu-id="2b66d-2081">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2081">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2083">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2083">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2084">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2085">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2086">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2087">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2089">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2091">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2093">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2095">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2095">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2097">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2097">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2099">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2100">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2101">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2101">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2102">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2103">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2103">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2105">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2105">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2107">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2109">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2109">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2111">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2112">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2113">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2114">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2115">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2115">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2116">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2117">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2118">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2119">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2120">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2121">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2122">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2123">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2124">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2124">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2126">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2126">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2128">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2128">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2130">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2130">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2132">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2132">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2134">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2134">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2136">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2136">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2138">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2138">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2140">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2140">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2141">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2141">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2143">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2143">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2145">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2145">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2147">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="2b66d-2148">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2148">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="2b66d-2149">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2149">Target</span></span> | <span data-ttu-id="2b66d-2150">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2150">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2151">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2152">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2152">32</span></span> |
| <span data-ttu-id="2b66d-2153">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2153">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2155">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2155">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2157">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2157">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2159">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2159">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2160">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2160">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2161">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2161">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2163">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2163">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2165">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2165">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2167">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2167">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2169">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2169">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2171">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2171">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2172">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2172">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2173">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2173">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2174">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2174">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2175">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2175">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2176">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2176">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2178">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2178">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2179">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2179">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2181">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2181">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2182">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2182">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2184">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2184">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2185">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2185">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2186">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2186">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2187">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2187">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2188">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2188">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2189">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2189">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2190">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2190">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2191">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2191">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2192">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2192">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2193">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2193">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2194">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2194">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2195">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2195">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2196">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2196">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2198">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2198">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2200">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2200">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2202">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2202">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2204">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2204">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2205">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2205">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2207">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2207">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2208">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2208">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2210">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2210">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2211">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2211">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2212">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2212">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2213">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2213">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2215">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2215">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="2b66d-2216">DXGI_FORMAT_R8G8B8A8 \_ ronfler<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2216">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="2b66d-2217">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2217">Target</span></span> | <span data-ttu-id="2b66d-2218">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2218">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2219">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2219">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2220">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2220">32</span></span> |
| <span data-ttu-id="2b66d-2221">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2221">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2223">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2223">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2225">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2225">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2227">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2227">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2228">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2228">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2229">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2229">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2231">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2231">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2233">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2233">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2235">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2235">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2237">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2237">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2239">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2239">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2241">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2241">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2242">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2242">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2243">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2243">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2244">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2244">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2245">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2245">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2247">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2247">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2249">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2249">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2251">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2251">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2252">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2252">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2253">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2253">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2254">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2254">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2255">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2255">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2256">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2256">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2257">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2257">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2258">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2258">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2259">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2259">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2260">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2260">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2261">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2261">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2262">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2262">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2263">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2263">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2264">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2264">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2265">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2265">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2267">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2267">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2269">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2269">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2271">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2271">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2273">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2273">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2275">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2275">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2277">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2277">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2278">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2278">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2280">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2281">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2282">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2283">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2283">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2285">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2285">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="2b66d-2286">DXGI_FORMAT_R8G8B8A8 \_ Saint-<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2286">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="2b66d-2287">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2287">Target</span></span> | <span data-ttu-id="2b66d-2288">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2288">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2289">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2289">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2290">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2290">32</span></span> |
| <span data-ttu-id="2b66d-2291">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2291">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2293">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2293">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2295">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2295">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2297">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2297">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2298">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2298">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2299">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2299">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2301">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2301">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2303">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2305">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2305">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2307">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2307">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2309">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2309">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2310">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2310">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2311">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2311">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2312">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2312">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2313">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2313">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2314">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2314">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2316">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2316">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2317">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2317">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2319">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2319">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2320">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2320">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2321">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2321">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2322">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2322">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2323">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2323">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2324">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2324">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2325">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2325">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2326">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2326">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2327">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2327">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2328">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2328">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2329">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2329">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2330">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2330">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2331">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2331">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2332">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2332">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2333">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2333">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2335">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2335">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2337">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2337">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2339">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2339">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2341">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2341">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2342">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2342">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2344">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2345">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2345">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2347">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2348">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2349">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2350">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2350">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2352">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2352">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="2b66d-2353">\_<sup>PC</sup> DXGI_FORMAT_R16G16 type (33)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2353">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="2b66d-2354">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2354">Target</span></span> | <span data-ttu-id="2b66d-2355">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2355">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2356">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2356">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2357">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2357">32</span></span> |
| <span data-ttu-id="2b66d-2358">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2358">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2360">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2360">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2361">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2361">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2362">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2362">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2363">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2363">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2364">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2364">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2366">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2366">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2368">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2368">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2370">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2370">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2372">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2372">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-2373">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2373">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2374">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2375">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2376">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2376">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2377">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2378">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2378">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2380">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2381">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2382">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2383">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2384">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2385">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2386">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2387">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2387">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2388">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2389">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2390">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2391">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2393">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2394">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2395">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2396">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2396">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2398">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2399">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2400">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-2401">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2402">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2402">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-2403">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2404">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2404">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2406">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2407">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2408">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2409">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2409">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-2410">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="2b66d-2411">DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2411">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="2b66d-2412">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2412">Target</span></span> | <span data-ttu-id="2b66d-2413">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2413">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2414">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2415">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2415">32</span></span> |
| <span data-ttu-id="2b66d-2416">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2416">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2418">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2418">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2420">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2420">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2422">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2422">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2423">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2423">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2424">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2424">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2426">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2426">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2428">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2428">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2430">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2430">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2432">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2432">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2434">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2434">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2436">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2436">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2437">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2437">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2438">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2438">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2439">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2439">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2440">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2440">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2442">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2442">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2444">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2444">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2446">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2446">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2448">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2448">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2449">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2449">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2450">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2450">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2451">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2451">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2452">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2452">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2453">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2453">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2454">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2454">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2455">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2455">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2456">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2456">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2457">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2457">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2458">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2458">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2459">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2459">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2460">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2460">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2461">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2461">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2463">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2463">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2465">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2465">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2467">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2467">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2469">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2469">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2471">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2471">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2473">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2473">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2474">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2474">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2476">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2476">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2477">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2477">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2478">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2478">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2479">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2479">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-2480">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2480">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="2b66d-2481">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2481">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="2b66d-2482">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2482">Target</span></span> | <span data-ttu-id="2b66d-2483">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2483">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2484">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2484">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2485">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2485">32</span></span> |
| <span data-ttu-id="2b66d-2486">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2486">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2488">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2488">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2490">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2490">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2492">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2492">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2493">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2493">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2494">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2494">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2496">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2496">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2498">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2498">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2500">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2500">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2502">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2502">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2504">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2504">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2506">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2507">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2508">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2508">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2509">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2510">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2510">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2512">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2512">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2514">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2516">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2516">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2518">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2518">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2519">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2519">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2520">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2520">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2521">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2521">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2522">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2522">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2523">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2523">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2524">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2524">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2525">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2525">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2526">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2526">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2527">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2527">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2528">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2528">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2529">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2529">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2530">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2530">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2531">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2531">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2533">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2533">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2535">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2535">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2537">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2537">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2539">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2539">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2541">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2541">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2543">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2544">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2544">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2546">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2546">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2547">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2547">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2548">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2548">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2549">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2549">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-2550">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="2b66d-2551">DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2551">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="2b66d-2552">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2552">Target</span></span> | <span data-ttu-id="2b66d-2553">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2553">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2554">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2555">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2555">32</span></span> |
| <span data-ttu-id="2b66d-2556">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2556">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2558">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2558">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2560">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2560">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2562">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2562">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2563">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2563">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2564">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2564">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2566">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2566">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2568">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2568">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2570">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2570">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2572">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2572">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2574">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2574">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2575">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2575">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2576">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2576">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2577">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2577">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2578">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2578">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2579">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2579">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2581">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2581">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2582">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2582">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2584">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2584">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2585">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2585">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2587">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2587">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2588">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2588">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2589">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2589">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2590">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2590">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2591">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2591">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2592">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2592">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2593">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2593">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2594">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2594">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2595">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2595">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2596">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2596">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2597">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2597">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2598">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2598">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2599">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2599">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2601">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2601">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2603">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2603">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2605">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2605">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2607">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2607">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2608">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2608">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2610">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2610">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2611">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2611">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2613">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2613">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2614">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2614">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2615">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2615">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2616">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2616">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-2617">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2617">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="2b66d-2618">DXGI_FORMAT_R16G16 \_ ronfler<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2618">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="2b66d-2619">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2619">Target</span></span> | <span data-ttu-id="2b66d-2620">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2620">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2621">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2621">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2622">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2622">32</span></span> |
| <span data-ttu-id="2b66d-2623">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2623">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2625">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2625">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2627">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2627">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2629">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2629">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2630">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2630">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2631">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2631">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2633">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2633">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2635">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2635">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2637">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2637">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2639">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2639">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2641">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2641">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2643">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2643">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2644">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2644">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2645">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2645">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2646">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2646">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2647">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2647">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2649">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2649">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2651">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2651">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2653">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2653">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2654">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2654">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2655">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2655">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2656">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2656">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2657">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2657">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2658">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2658">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2659">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2659">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2660">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2660">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2661">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2661">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2662">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2662">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2663">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2663">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2664">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2664">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2665">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2665">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2666">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2666">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2667">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2667">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2669">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2669">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2671">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2671">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2673">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2673">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2675">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2675">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2677">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2677">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2679">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2679">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2680">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2680">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2682">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2682">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2683">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2683">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2684">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2684">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2685">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2685">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-2686">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2686">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="2b66d-2687">DXGI_FORMAT_R16G16 \_ Saint-<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2687">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="2b66d-2688">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2688">Target</span></span> | <span data-ttu-id="2b66d-2689">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2689">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2690">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2690">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2691">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2691">32</span></span> |
| <span data-ttu-id="2b66d-2692">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2692">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2694">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2694">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2696">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2696">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2698">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2698">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2699">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2699">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2700">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2700">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2702">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2702">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2704">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2704">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2706">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2706">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2708">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2708">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2710">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2710">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2711">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2711">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2712">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2712">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2713">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2713">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2714">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2714">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2715">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2715">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2717">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2717">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2718">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2718">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2720">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2720">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2721">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2721">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2722">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2722">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2723">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2723">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2724">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2724">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2725">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2725">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2726">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2726">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2727">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2727">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2728">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2728">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2729">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2729">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2730">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2730">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2731">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2731">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2732">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2732">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2733">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2733">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2734">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2734">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2736">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2736">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2738">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2738">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2740">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2740">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2742">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2743">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2743">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2745">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2746">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2746">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2748">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2748">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2749">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2749">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2750">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2750">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2751">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2751">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-2752">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2752">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="2b66d-2753">\_<sup>PC</sup> DXGI_FORMAT_R32 type (39)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2753">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="2b66d-2754">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2754">Target</span></span> | <span data-ttu-id="2b66d-2755">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2755">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2756">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2756">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2757">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2757">32</span></span> |
| <span data-ttu-id="2b66d-2758">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2758">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2760">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2760">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2761">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2761">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2762">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2762">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2763">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2763">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2764">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2764">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2766">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2766">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2768">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2768">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2770">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2772">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2772">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-2773">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2773">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2774">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2774">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2775">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2775">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2776">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2776">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2777">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2777">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2778">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2778">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2780">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2780">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2781">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2781">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2782">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2782">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2783">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2783">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2784">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2784">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2785">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2785">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2786">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2786">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2787">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2787">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2788">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2788">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2789">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2789">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2790">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2790">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2791">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2791">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2792">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2792">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2793">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2793">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2794">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2794">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2795">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2795">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2796">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2796">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2798">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2798">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2799">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2799">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2800">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2800">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-2801">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2801">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2802">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2802">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-2803">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2803">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2804">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2804">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2806">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2807">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2807">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2808">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2808">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2809">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2809">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2811">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="2b66d-2812">DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2812">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="2b66d-2813">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2813">Target</span></span> | <span data-ttu-id="2b66d-2814">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2814">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2815">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2816">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2816">32</span></span> |
| <span data-ttu-id="2b66d-2817">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2817">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2819">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2819">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2820">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2821">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2822">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2823">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2825">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2825">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2827">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2827">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-2828">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2828">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2830">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2830">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-2831">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2831">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2832">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2832">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2833">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2833">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2834">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2834">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2835">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2835">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2836">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2836">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2838">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2838">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2839">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2839">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2840">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2840">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2841">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2841">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2842">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2842">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2844">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2844">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2845">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2845">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2846">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2846">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2847">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2847">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2848">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2848">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2849">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2849">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2850">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2850">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2851">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2851">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2852">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2852">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2853">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2853">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2854">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2854">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2855">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2855">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2857">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2857">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2859">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2859">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2861">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2861">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2863">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2863">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-2864">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2864">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-2865">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2865">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2866">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2866">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2868">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2868">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2869">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2869">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2870">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2870">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2871">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2871">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2873">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2873">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="2b66d-2874">DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2874">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="2b66d-2875">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2875">Target</span></span> | <span data-ttu-id="2b66d-2876">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2876">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2877">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2877">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2878">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2878">32</span></span> |
| <span data-ttu-id="2b66d-2879">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2879">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2881">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2881">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2883">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2883">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2885">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2885">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-2886">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2886">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2888">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2888">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2890">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2892">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2892">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2894">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2894">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2896">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2896">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2898">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2898">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2900">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2900">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2902">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2902">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2903">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2903">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2904">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2904">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2905">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2905">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2907">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2907">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2909">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2909">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2911">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2911">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2913">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2913">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-2914">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2914">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2915">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2915">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2916">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2916">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2917">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2917">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2918">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2918">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2919">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2919">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2920">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2920">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2921">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2921">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2922">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2922">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2923">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2923">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2924">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2924">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2925">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2925">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2926">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2926">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2928">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2928">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2930">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2930">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2932">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-2932">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2934">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-2934">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2936">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-2936">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2938">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-2938">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-2939">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-2939">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2941">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2941">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-2942">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2942">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-2943">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-2943">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-2944">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2944">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2946">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-2946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="2b66d-2947">DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2947">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="2b66d-2948">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-2948">Target</span></span> | <span data-ttu-id="2b66d-2949">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-2949">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-2950">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-2951">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-2951">32</span></span> |
| <span data-ttu-id="2b66d-2952">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-2952">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2954">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-2954">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2956">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2956">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2958">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-2958">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2960">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-2960">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2962">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2964">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2964">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2966">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-2966">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2968">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-2968">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2970">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-2970">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2972">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2972">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2973">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2973">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2974">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-2974">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-2975">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-2975">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-2976">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-2976">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-2977">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-2977">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2979">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-2979">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-2980">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-2980">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2982">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-2983">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-2983">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-2985">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-2985">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-2986">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-2986">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2987">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-2987">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-2988">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-2988">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-2989">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2989">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-2990">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2990">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-2991">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-2991">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-2992">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2992">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-2993">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-2993">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-2994">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2994">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-2995">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-2995">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2996">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-2996">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-2997">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-2997">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-2999">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-2999">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3001">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3001">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3003">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3003">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3005">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3006">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3006">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3008">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3009">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3009">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3011">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3011">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3012">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3012">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3013">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3013">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3014">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3014">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3016">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3016">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="2b66d-3017">DXGI_FORMAT_R32 \_ Saint-<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3017">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="2b66d-3018">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3018">Target</span></span> | <span data-ttu-id="2b66d-3019">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3019">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3020">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3020">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3021">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-3021">32</span></span> |
| <span data-ttu-id="2b66d-3022">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3022">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3024">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3024">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3026">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3026">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3028">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3028">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3029">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3029">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3031">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3031">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3033">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3033">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3035">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3035">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3037">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3037">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3039">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3039">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3041">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3041">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3042">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3042">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3043">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3043">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3044">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3044">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3045">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3045">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3046">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3046">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3048">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3048">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3049">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3049">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3051">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3051">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3052">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3052">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3053">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3053">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3054">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3054">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3055">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3055">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3056">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3056">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3057">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3057">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3058">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3058">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3059">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3059">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3060">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3060">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3061">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3061">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3062">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3062">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3063">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3063">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3064">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3064">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3065">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3065">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3067">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3067">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3069">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3069">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3071">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3071">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3073">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3073">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3074">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3074">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3076">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3076">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3077">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3077">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3079">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3079">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3080">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3080">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3081">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3081">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3082">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3082">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3084">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3084">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="2b66d-3085">\_<sup>PC</sup> DXGI_FORMAT_R24G8 type (44)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3085">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="2b66d-3086">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3086">Target</span></span> | <span data-ttu-id="2b66d-3087">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3087">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3088">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3088">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3089">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-3089">32</span></span> |
| <span data-ttu-id="2b66d-3090">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3090">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3092">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3092">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3093">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3093">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3094">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3094">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3095">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3095">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3096">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3096">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3098">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3098">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3100">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3100">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-3101">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3101">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3103">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3103">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-3104">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3104">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3105">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3105">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3106">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3106">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3107">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3107">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3108">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3108">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3109">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3109">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3111">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3111">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3112">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3112">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3113">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3113">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3114">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3115">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3116">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3117">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3118">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3118">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3119">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3120">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3121">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3122">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3124">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3125">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3126">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3127">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3127">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3129">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3130">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3131">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-3132">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3133">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3133">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3134">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3135">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3135">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3137">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3138">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3139">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3140">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3140">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3141">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3141">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="2b66d-3142">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3142">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="2b66d-3143">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3143">Target</span></span> | <span data-ttu-id="2b66d-3144">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3144">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3145">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3145">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3146">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-3146">32</span></span> |
| <span data-ttu-id="2b66d-3147">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3147">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3149">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3149">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3150">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3150">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3151">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3151">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3152">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3152">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3153">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3153">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3155">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3157">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-3158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3158">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3160">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3160">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-3161">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3161">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3162">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3162">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3163">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3163">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3164">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3164">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3165">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3165">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3166">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3166">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3168">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3168">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3169">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3169">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3170">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3170">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3171">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3171">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3172">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3172">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3174">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3174">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3175">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3175">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3176">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3176">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3177">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3177">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3178">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3178">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3179">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3179">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3180">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3180">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3181">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3181">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3182">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3182">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3183">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3183">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3184">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3184">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3185">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3185">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3187">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3187">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3189">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3189">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3191">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3191">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3193">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3193">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3194">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3194">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3195">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3195">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3196">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3196">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3198">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3198">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3199">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3199">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3200">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3200">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3201">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3201">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3202">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3202">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="2b66d-3203">DXGI_FORMAT_R24 \_ \_ FCS UNORM x8 non \_ typé (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="2b66d-3203">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="2b66d-3204">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3204">Target</span></span> | <span data-ttu-id="2b66d-3205">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3205">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3206">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3206">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3207">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-3207">32</span></span> |
| <span data-ttu-id="2b66d-3208">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3208">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3210">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3210">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3211">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3211">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3212">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3212">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3213">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3213">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3214">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3214">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3216">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3216">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3218">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3218">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-3219">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3219">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3221">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3221">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3223">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3223">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3225">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3225">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3227">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3227">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3228">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3228">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3229">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3229">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3230">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3230">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3232">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3232">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3233">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3233">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3234">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3234">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3235">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3235">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3236">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3236">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3237">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3237">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3238">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3238">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3239">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3239">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3240">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3240">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3241">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3241">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3242">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3242">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3243">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3243">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3244">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3244">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3245">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3245">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3246">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3246">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3247">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3247">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3248">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3248">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3250">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3250">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3251">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3251">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3252">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3252">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-3253">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3253">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3254">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3254">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3255">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3255">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3256">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3256">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3258">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3258">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3259">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3259">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3260">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3260">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3261">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3261">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3262">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3262">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="2b66d-3263">DXGI_FORMAT_X24 \_ \_ G8 \_ UINT<sup>FCS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3263">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="2b66d-3264">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3264">Target</span></span> | <span data-ttu-id="2b66d-3265">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3265">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3266">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3266">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3267">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-3267">32</span></span> |
| <span data-ttu-id="2b66d-3268">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3268">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3270">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3270">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3271">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3271">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3272">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3272">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3273">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3273">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3274">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3274">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3276">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3276">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3278">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3278">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-3279">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3279">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3281">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3281">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3283">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3283">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3284">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3284">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3285">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3285">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3286">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3286">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3287">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3287">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3288">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3288">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3290">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3290">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3291">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3291">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3292">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3292">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3293">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3293">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3294">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3294">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3295">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3295">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3296">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3296">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3297">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3297">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3298">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3298">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3299">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3299">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3300">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3300">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3301">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3301">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3302">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3302">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3303">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3303">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3304">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3304">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3305">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3305">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3306">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3306">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3308">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3308">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3309">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3309">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3310">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3310">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-3311">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3311">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3312">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3312">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3313">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3313">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3314">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3314">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3316">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3316">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3317">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3317">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3318">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3318">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3319">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3319">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3320">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3320">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="2b66d-3321">\_<sup>PC</sup> DXGI_FORMAT_R8G8 type (48)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3321">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="2b66d-3322">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3322">Target</span></span> | <span data-ttu-id="2b66d-3323">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3323">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3324">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3324">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3325">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3325">16</span></span> |
| <span data-ttu-id="2b66d-3326">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3326">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3328">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3328">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3329">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3329">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3330">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3330">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3331">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3331">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3332">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3332">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3334">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3334">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3336">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3336">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3338">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3338">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3340">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3340">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-3341">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3341">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3342">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3342">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3343">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3343">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3344">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3344">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3345">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3345">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3346">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3346">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3348">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3348">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3349">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3349">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3350">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3350">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3351">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3351">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3352">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3352">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3353">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3353">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3354">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3354">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3355">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3355">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3356">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3356">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3357">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3357">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3358">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3358">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3359">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3359">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3360">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3360">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3361">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3361">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3362">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3362">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3363">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3363">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3364">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3364">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3366">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3366">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3367">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3367">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3368">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3368">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-3369">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3370">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3370">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3371">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3371">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3372">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3372">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3374">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3375">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3376">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3377">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3377">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3378">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="2b66d-3379">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3379">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="2b66d-3380">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3380">Target</span></span> | <span data-ttu-id="2b66d-3381">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3381">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3382">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3383">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3383">16</span></span> |
| <span data-ttu-id="2b66d-3384">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3384">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3386">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3386">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3388">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3388">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3390">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3390">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3391">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3391">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3392">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3392">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3394">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3394">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3396">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3396">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3398">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3400">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3400">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3402">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3402">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3404">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3404">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3405">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3405">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3406">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3406">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3407">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3407">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3408">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3408">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3410">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3410">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3412">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3412">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3414">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3414">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3416">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3416">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3417">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3417">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3418">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3418">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3419">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3419">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3420">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3420">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3421">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3421">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3422">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3422">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3423">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3423">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3424">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3424">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3425">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3425">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3426">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3426">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3427">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3427">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3428">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3428">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3429">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3429">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3431">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3431">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3433">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3433">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3435">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3435">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3437">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3437">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3439">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3439">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3441">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3441">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3442">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3442">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3444">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3444">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3445">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3445">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3446">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3446">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3447">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3447">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3449">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="2b66d-3450">DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3450">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="2b66d-3451">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3451">Target</span></span> | <span data-ttu-id="2b66d-3452">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3452">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3453">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3454">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3454">16</span></span> |
| <span data-ttu-id="2b66d-3455">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3455">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3457">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3457">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3459">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3459">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3461">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3461">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3462">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3462">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3463">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3463">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3465">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3465">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3467">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3467">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3469">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3469">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3471">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3471">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3473">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3473">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3474">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3474">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3475">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3475">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3476">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3476">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3477">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3477">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3478">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3478">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3480">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3480">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3481">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3481">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3483">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3483">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3484">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3484">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3486">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3486">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3487">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3487">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3488">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3488">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3489">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3489">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3490">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3490">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3491">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3491">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3492">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3492">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3493">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3493">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3494">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3494">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3495">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3495">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3496">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3496">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3497">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3497">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3498">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3498">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3500">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3500">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3502">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3502">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3504">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3504">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3506">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3507">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3507">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3509">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3509">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3510">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3510">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3512">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3512">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3513">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3513">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3514">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3514">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3515">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3515">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3516">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3516">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="2b66d-3517">DXGI_FORMAT_R8G8 \_ ronfler<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3517">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="2b66d-3518">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3518">Target</span></span> | <span data-ttu-id="2b66d-3519">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3519">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3520">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3520">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3521">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3521">16</span></span> |
| <span data-ttu-id="2b66d-3522">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3522">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3524">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3524">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3526">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3526">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3528">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3529">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3530">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3532">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3532">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3534">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3534">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3536">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3536">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3538">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3538">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3540">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3540">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3542">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3542">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3543">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3543">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3544">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3544">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3545">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3545">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3546">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3546">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3548">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3548">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3550">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3550">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3552">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3552">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3553">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3553">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3554">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3554">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3555">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3555">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3556">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3556">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3557">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3557">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3558">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3558">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3559">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3559">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3560">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3560">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3561">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3561">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3562">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3562">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3563">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3563">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3564">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3564">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3565">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3565">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3566">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3566">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3568">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3568">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3570">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3570">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3572">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3572">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3574">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3574">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3576">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3576">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3578">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3579">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3579">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3581">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3582">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3583">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3584">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3584">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3585">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="2b66d-3586">DXGI_FORMAT_R8G8 \_ Saint-<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3586">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="2b66d-3587">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3587">Target</span></span> | <span data-ttu-id="2b66d-3588">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3588">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3589">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3590">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3590">16</span></span> |
| <span data-ttu-id="2b66d-3591">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3591">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3593">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3593">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3595">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3595">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3597">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3598">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3599">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3601">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3603">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3605">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3607">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3607">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3609">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3610">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3611">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3612">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3612">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3613">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3614">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3614">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3616">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3616">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3617">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3617">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3619">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3619">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3620">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3620">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3621">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3621">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3622">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3622">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3623">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3623">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3624">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3624">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3625">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3625">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3626">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3626">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3627">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3627">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3628">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3628">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3629">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3629">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3630">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3630">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3631">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3631">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3632">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3632">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3633">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3633">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3635">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3635">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3637">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3637">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3639">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3639">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3641">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3642">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3642">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3644">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3645">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3645">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3647">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3647">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3648">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3648">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3649">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3649">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3650">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3650">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-3651">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3651">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="2b66d-3652">\_<sup>PC</sup> DXGI_FORMAT_R16 type (53)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3652">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="2b66d-3653">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3653">Target</span></span> | <span data-ttu-id="2b66d-3654">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3654">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3655">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3655">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3656">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3656">16</span></span> |
| <span data-ttu-id="2b66d-3657">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3657">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3659">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3659">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3660">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3660">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3661">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3661">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3662">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3662">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3663">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3663">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3665">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3665">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3667">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3667">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3669">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3669">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3671">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3671">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-3672">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3672">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3673">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3673">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3674">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3674">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3675">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3675">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3676">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3676">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3677">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3677">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3679">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3679">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3680">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3680">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3681">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3681">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3682">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3682">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3683">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3683">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3684">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3684">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3685">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3685">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3686">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3686">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3687">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3687">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3688">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3688">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3689">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3689">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3690">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3690">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3691">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3691">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3692">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3692">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3693">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3693">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3694">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3694">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3695">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3695">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3697">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3697">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3698">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3698">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3699">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3699">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-3700">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3700">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3701">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3701">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3702">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3702">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3703">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3703">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3705">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3706">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3707">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3708">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3708">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3710">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="2b66d-3711">DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3711">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="2b66d-3712">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3712">Target</span></span> | <span data-ttu-id="2b66d-3713">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3713">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3714">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3715">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3715">16</span></span> |
| <span data-ttu-id="2b66d-3716">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3716">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3718">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3718">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3720">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3720">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3722">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3722">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3723">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3723">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3724">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3724">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3726">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3728">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3730">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3730">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3732">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3732">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3734">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3734">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3736">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3736">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3737">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3737">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3738">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3738">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3739">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3739">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3740">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3740">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3742">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3742">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3744">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3744">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3746">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3746">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3748">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3748">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3749">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3749">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3750">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3750">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3751">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3751">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3752">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3752">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3753">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3753">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3754">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3754">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3755">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3755">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3756">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3756">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3757">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3757">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3758">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3758">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3759">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3759">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3760">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3760">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3761">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3761">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3763">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3763">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3765">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3765">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3767">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3767">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3769">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3769">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3771">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3771">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3773">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3773">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3774">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3774">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3776">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3776">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3777">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3777">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3778">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3778">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3779">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3779">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3781">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3781">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="2b66d-3782">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3782">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="2b66d-3783">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3783">Target</span></span> | <span data-ttu-id="2b66d-3784">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3784">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3785">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3785">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3786">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3786">16</span></span> |
| <span data-ttu-id="2b66d-3787">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3787">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3789">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3789">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3790">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3790">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3791">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3792">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3793">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3795">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3795">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3797">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3797">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-3798">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3798">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3800">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3800">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-3801">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3801">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3802">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3802">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3803">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3803">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3804">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3804">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3805">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3805">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3806">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3806">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3808">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3808">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3809">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3809">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3810">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3810">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3811">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3811">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3812">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3812">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3814">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3814">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3815">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3815">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3816">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3816">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3817">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3817">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3818">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3818">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3819">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3819">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3820">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3820">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3821">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3821">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3822">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3822">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3823">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3823">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3824">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3824">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3825">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3825">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3827">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3827">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3829">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3829">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3831">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3831">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3833">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3834">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3834">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-3835">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3836">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3836">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3838">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3838">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3839">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3839">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3840">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3841">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3841">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3843">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3843">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="2b66d-3844">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3844">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="2b66d-3845">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3845">Target</span></span> | <span data-ttu-id="2b66d-3846">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3846">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3847">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3847">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3848">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3848">16</span></span> |
| <span data-ttu-id="2b66d-3849">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3849">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3851">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3851">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3853">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3853">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3855">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3855">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3856">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3856">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3857">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3857">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3859">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3859">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3861">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3861">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3863">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3863">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3865">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3865">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3867">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3867">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3869">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3869">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3871">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3871">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3872">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3872">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3873">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3873">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3874">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3874">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3876">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3876">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3878">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3878">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3880">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3880">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3882">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3882">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-3883">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3883">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3884">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3884">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3885">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3885">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3886">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3886">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3887">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3887">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3888">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3888">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3889">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3889">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3890">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3890">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3891">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3891">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3892">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3892">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3893">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3893">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3894">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3894">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3895">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3895">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3897">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3897">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3899">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3899">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3901">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3901">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3903">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3903">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3905">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3905">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3907">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3907">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3908">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3908">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3910">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3910">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3911">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3911">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3912">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3912">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3913">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3913">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3915">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3915">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="2b66d-3916">DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3916">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="2b66d-3917">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3917">Target</span></span> | <span data-ttu-id="2b66d-3918">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3918">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3919">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3919">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3920">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3920">16</span></span> |
| <span data-ttu-id="2b66d-3921">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3921">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3923">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3923">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3925">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3925">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3927">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3927">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3929">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3929">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3930">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3930">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3932">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3934">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3936">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-3936">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3938">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-3938">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3940">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3940">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3941">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3941">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3942">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3942">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-3943">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-3943">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-3944">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-3944">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-3945">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-3945">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3947">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-3947">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-3948">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3948">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3950">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-3951">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-3951">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3953">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-3953">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-3954">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-3954">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3955">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-3955">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-3956">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-3956">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-3957">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3957">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-3958">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3958">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-3959">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-3959">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-3960">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3960">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-3961">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-3961">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-3962">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3962">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-3963">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-3963">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3964">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-3964">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-3965">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-3965">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3967">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-3967">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3969">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-3969">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3971">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-3971">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3973">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-3973">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-3974">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-3974">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-3976">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-3976">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-3977">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-3977">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3979">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3979">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-3980">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3980">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-3981">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-3981">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-3982">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3982">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3984">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-3984">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="2b66d-3985">DXGI_FORMAT_R16 \_ ronfler<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3985">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="2b66d-3986">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-3986">Target</span></span> | <span data-ttu-id="2b66d-3987">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-3987">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-3988">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-3988">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-3989">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-3989">16</span></span> |
| <span data-ttu-id="2b66d-3990">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-3990">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3992">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-3992">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3994">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3994">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-3996">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-3996">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3997">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-3997">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-3998">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-3998">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4000">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4000">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4002">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4002">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4004">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4004">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4006">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4006">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4008">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4008">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4010">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4010">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4011">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4011">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4012">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4012">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4013">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4013">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4014">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4014">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4016">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4016">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4018">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4018">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4020">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4020">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4021">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4021">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4022">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4022">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4023">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4023">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4024">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4024">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4025">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4025">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4026">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4026">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4027">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4027">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4028">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4028">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4029">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4029">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4030">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4030">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4031">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4031">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4032">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4032">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4033">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4033">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4034">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4034">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4036">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4036">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4038">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4038">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4040">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4040">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4042">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4042">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4044">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4044">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4046">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4046">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4047">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4047">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4049">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4050">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4051">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4052">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4052">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4054">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4054">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="2b66d-4055">DXGI_FORMAT_R16 \_ Saint-<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4055">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="2b66d-4056">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4056">Target</span></span> | <span data-ttu-id="2b66d-4057">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4057">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4058">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4058">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4059">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-4059">16</span></span> |
| <span data-ttu-id="2b66d-4060">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4060">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4062">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4062">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4064">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4064">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4066">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4066">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4067">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4067">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4068">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4068">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4070">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4072">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4074">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4076">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4076">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4078">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4078">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4079">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4079">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4080">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4080">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4081">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4081">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4082">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4082">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4083">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4083">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4085">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4085">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4086">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4086">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4088">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4089">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4090">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4091">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4092">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4093">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4093">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4094">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4095">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4096">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4097">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4098">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4099">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4100">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4101">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4102">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4102">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4104">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4104">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4106">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4106">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4108">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4108">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4110">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4110">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4111">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4111">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4113">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4113">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4114">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4114">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4116">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4116">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4117">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4117">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4118">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4118">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4119">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4119">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4121">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4121">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="2b66d-4122">\_<sup>PC</sup> DXGI_FORMAT_R8 type (60)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4122">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="2b66d-4123">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4123">Target</span></span> | <span data-ttu-id="2b66d-4124">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4124">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4125">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4125">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4126">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4126">8</span></span> |
| <span data-ttu-id="2b66d-4127">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4127">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4129">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4129">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4130">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4131">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4132">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4133">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4135">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4135">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4137">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4137">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4139">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4139">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4141">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4141">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-4142">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4142">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4143">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4143">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4144">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4144">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4145">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4145">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4146">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4146">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4147">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4147">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4149">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4149">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4150">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4150">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4151">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4151">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4152">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4152">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4153">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4153">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4154">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4154">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4155">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4155">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4156">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4156">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4157">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4157">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4158">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4158">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4159">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4159">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4160">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4160">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4161">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4161">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4162">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4162">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4163">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4163">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4164">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4164">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4165">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4165">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4167">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4167">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4168">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4168">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4169">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4169">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4170">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4170">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4171">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4171">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4172">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4172">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4173">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4173">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4175">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4175">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4176">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4176">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4177">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4177">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4178">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4178">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4180">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4180">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="2b66d-4181">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4181">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="2b66d-4182">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4182">Target</span></span> | <span data-ttu-id="2b66d-4183">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4183">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4184">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4184">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4185">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4185">8</span></span> |
| <span data-ttu-id="2b66d-4186">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4186">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4188">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4188">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4190">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4190">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4192">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4193">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4194">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4196">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4196">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4198">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4198">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4200">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4200">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4202">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4202">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4204">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4204">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4206">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4206">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4207">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4207">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4208">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4208">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4209">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4209">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4210">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4210">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4212">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4212">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4214">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4214">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4216">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4216">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4218">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4218">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4219">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4219">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4220">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4220">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4221">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4221">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4222">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4222">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4223">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4223">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4224">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4224">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4225">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4225">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4226">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4226">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4227">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4227">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4228">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4228">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4229">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4229">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4230">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4230">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4231">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4231">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4233">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4233">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4235">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4235">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4237">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4237">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4239">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4239">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4241">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4241">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4243">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4243">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4244">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4244">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4246">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4246">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4247">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4247">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4248">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4248">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4249">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4249">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4251">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="2b66d-4252">DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4252">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="2b66d-4253">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4253">Target</span></span> | <span data-ttu-id="2b66d-4254">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4254">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4255">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4256">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4256">8</span></span> |
| <span data-ttu-id="2b66d-4257">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4257">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4259">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4259">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4261">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4261">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4263">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4264">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4265">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4267">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4269">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4271">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4271">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4273">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4273">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4275">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4275">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4276">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4276">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4277">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4277">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4278">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4278">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4279">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4279">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4280">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4280">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4282">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4282">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4283">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4283">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4285">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4285">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4286">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4286">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4288">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4288">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4289">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4289">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4290">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4290">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4291">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4291">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4292">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4292">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4293">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4293">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4294">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4294">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4295">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4295">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4296">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4296">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4297">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4297">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4298">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4298">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4299">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4299">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4300">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4300">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4302">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4302">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4304">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4304">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4306">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4306">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4308">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4308">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4309">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4309">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4311">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4311">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4312">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4312">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4314">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4314">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4315">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4315">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4316">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4316">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4317">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4317">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4319">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4319">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="2b66d-4320">DXGI_FORMAT_R8 \_ ronfler<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4320">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="2b66d-4321">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4321">Target</span></span> | <span data-ttu-id="2b66d-4322">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4322">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4323">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4323">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4324">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4324">8</span></span> |
| <span data-ttu-id="2b66d-4325">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4325">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4327">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4327">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4329">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4329">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4331">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4331">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4332">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4332">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4333">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4333">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4335">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4335">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4337">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4337">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4339">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4339">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4341">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4341">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4343">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4343">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4345">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4346">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4347">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4347">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4348">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4349">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4349">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4351">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4351">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4353">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4355">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4355">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4356">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4356">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4357">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4357">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4358">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4358">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4359">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4359">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4360">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4360">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4361">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4361">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4362">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4362">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4363">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4363">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4364">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4364">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4365">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4365">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4366">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4366">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4367">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4367">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4368">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4368">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4369">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4369">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4371">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4371">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4373">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4373">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4375">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4375">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4377">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4377">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4379">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4379">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4381">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4382">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4382">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4384">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4385">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4386">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4387">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4387">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4389">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4389">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="2b66d-4390">DXGI_FORMAT_R8 \_ Saint-<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4390">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="2b66d-4391">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4391">Target</span></span> | <span data-ttu-id="2b66d-4392">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4392">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4393">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4393">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4394">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4394">8</span></span> |
| <span data-ttu-id="2b66d-4395">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4395">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4397">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4397">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4399">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4399">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4401">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4401">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4402">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4402">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4403">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4403">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4405">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4405">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4407">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4407">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4409">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4409">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4411">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4411">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4413">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4413">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4414">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4415">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4416">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4416">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4417">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4418">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4418">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4420">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4420">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4421">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4421">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4423">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4424">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4425">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4426">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4427">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4428">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4429">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4430">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4431">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4432">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4433">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4434">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4435">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4436">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4437">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4437">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4439">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4439">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4441">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4441">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4443">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4443">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4445">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4445">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4446">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4446">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4448">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4448">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4449">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4449">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4451">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4451">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4452">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4452">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4453">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4453">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4454">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4454">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4456">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="2b66d-4457">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4457">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="2b66d-4458">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4458">Target</span></span> | <span data-ttu-id="2b66d-4459">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4459">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4460">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4461">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4461">8</span></span> |
| <span data-ttu-id="2b66d-4462">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4462">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4464">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4464">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4465">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4466">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4467">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4468">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4470">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4470">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4472">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4472">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4474">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4474">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4476">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4476">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4478">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4478">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4480">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4480">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4481">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4481">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4482">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4482">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4483">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4483">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4484">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4484">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4486">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4486">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4488">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4488">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4490">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4490">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4492">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4492">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4493">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4493">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4494">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4494">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4495">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4495">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4496">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4496">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4497">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4497">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4498">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4498">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4499">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4499">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4500">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4500">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4501">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4501">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4502">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4502">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4503">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4503">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4504">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4504">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4505">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4505">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4507">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4507">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4509">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4509">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4511">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4511">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4513">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4513">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4515">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4515">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-4517">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4517">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4518">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4518">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-4519">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4519">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4520">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4520">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4521">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4521">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4522">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4522">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4524">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4524">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="2b66d-4525">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4525">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="2b66d-4526">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4526">Target</span></span> | <span data-ttu-id="2b66d-4527">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4527">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4528">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4528">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4529">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-4529">32</span></span> |
| <span data-ttu-id="2b66d-4530">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4530">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4532">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4532">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4533">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4533">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4534">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4534">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4535">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4535">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4536">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4536">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4538">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4538">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4540">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4540">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4542">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4542">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4544">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4544">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4546">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4546">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4548">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4548">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4549">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4549">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4550">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4550">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4551">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4551">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4552">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4552">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4554">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4554">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4555">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4555">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4556">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4556">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4557">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4557">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4558">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4558">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4559">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4559">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4560">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4560">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4561">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4561">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4562">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4562">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4563">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4563">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4564">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4564">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4565">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4565">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4566">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4566">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4567">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4567">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4568">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4568">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4569">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4569">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4570">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4570">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4572">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4572">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4573">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4573">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4574">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4574">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4575">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4575">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4576">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4576">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4577">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4577">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4578">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4578">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-4579">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4579">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4580">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4580">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4581">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4581">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4582">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4582">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-4583">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4583">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="2b66d-4584">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4584">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="2b66d-4585">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4585">Target</span></span> | <span data-ttu-id="2b66d-4586">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4586">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4587">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4587">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4588">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-4588">16</span></span> |
| <span data-ttu-id="2b66d-4589">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4589">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4591">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4591">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4592">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4592">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4593">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4593">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4594">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4594">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4595">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4595">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4597">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4597">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4599">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4599">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4601">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4601">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4603">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4603">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4605">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4605">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4607">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4607">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4608">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4608">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4609">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4609">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4610">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4610">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4611">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4611">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4613">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4614">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4615">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4616">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4617">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4618">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4619">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4620">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4620">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4621">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4622">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4624">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4625">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4626">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4627">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4628">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4629">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4629">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4631">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4632">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4633">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4634">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4635">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4635">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4636">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4637">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-4638">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4638">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4639">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4639">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4640">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4640">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4641">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4641">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-4642">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4642">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="2b66d-4643">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4643">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="2b66d-4644">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4644">Target</span></span> | <span data-ttu-id="2b66d-4645">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4645">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4646">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4646">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4647">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-4647">16</span></span> |
| <span data-ttu-id="2b66d-4648">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4648">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4650">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4650">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4651">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4651">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4652">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4653">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4654">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4656">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4656">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4658">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4658">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4660">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4660">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4662">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4662">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4664">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4664">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4666">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4666">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4667">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4667">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4668">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4668">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4669">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4669">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4670">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4670">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4672">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4673">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4674">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4675">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4676">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4677">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4678">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4679">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4679">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4680">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4681">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4682">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4683">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4684">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4685">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4686">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4687">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4688">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4688">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4690">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4690">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4691">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4691">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4692">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4692">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4693">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4693">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4694">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4694">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4695">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4695">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4696">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4696">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-4697">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4697">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4698">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4698">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4699">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4699">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4700">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4700">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-4701">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="2b66d-4702">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non typé (70)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4702">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="2b66d-4703">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4703">Target</span></span> | <span data-ttu-id="2b66d-4704">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4704">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4705">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4706">4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4706">4</span></span> |
| <span data-ttu-id="2b66d-4707">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4707">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4709">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4709">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4710">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4711">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4712">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4713">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-4714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4714">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4716">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4718">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4718">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4720">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4720">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-4721">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4721">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4722">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4722">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4723">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4723">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4724">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4724">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4725">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4725">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4726">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4726">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4728">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4728">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4729">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4729">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4730">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4730">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4731">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4731">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4732">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4732">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4733">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4733">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4734">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4734">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4735">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4735">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4736">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4736">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4737">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4737">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4738">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4738">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4739">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4739">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4740">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4740">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4741">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4741">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4742">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4742">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4743">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4743">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4744">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4744">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4746">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4746">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4747">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4747">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4748">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4748">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4749">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4749">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4750">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4750">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4751">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4752">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4752">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4754">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4755">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4756">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4757">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4757">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4759">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4759">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="2b66d-4760">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4760">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="2b66d-4761">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4761">Target</span></span> | <span data-ttu-id="2b66d-4762">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4762">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4763">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4763">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4764">4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4764">4</span></span> |
| <span data-ttu-id="2b66d-4765">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4765">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4767">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4767">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4768">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4768">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4769">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4769">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4770">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4770">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4771">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4771">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-4772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4772">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4774">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4776">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4778">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4778">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4780">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4780">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4782">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4782">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4783">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4783">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4784">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4784">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4785">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4785">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4786">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4786">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4788">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4788">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4789">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4789">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4790">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4790">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4791">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4791">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4792">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4792">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4793">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4793">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4794">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4794">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4795">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4795">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4796">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4796">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4797">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4797">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4798">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4798">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4799">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4799">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4800">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4800">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4801">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4801">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4802">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4802">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4803">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4803">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4804">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4804">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4806">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4806">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4807">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4807">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4808">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4808">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4809">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4809">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4810">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4810">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4811">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4812">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4812">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4814">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4815">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4816">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4817">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4817">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4819">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="2b66d-4820">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4820">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="2b66d-4821">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4821">Target</span></span> | <span data-ttu-id="2b66d-4822">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4822">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4823">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4824">4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4824">4</span></span> |
| <span data-ttu-id="2b66d-4825">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4825">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4827">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4827">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4828">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4829">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4830">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4831">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-4832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4832">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4834">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4836">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4836">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4838">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4838">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4840">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4840">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4842">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4842">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4843">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4843">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4844">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4844">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4845">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4845">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4846">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4846">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4848">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4849">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4850">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4851">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4852">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4853">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4854">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4855">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4855">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4856">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4857">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4858">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4859">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4860">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4861">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4862">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4863">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4864">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4864">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4866">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4866">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4867">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4867">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4868">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4868">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4869">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4870">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4870">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4871">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4872">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4872">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4874">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4875">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4876">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4877">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4877">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4879">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="2b66d-4880">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non typé (73)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4880">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="2b66d-4881">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4881">Target</span></span> | <span data-ttu-id="2b66d-4882">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4882">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4883">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4884">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4884">8</span></span> |
| <span data-ttu-id="2b66d-4885">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4885">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4887">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4887">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4888">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4888">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4889">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4890">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4891">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-4892">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4892">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4894">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4894">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4896">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4896">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4898">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4898">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-4899">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4899">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4900">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4900">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4901">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4901">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4902">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4902">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4903">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4903">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4904">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4904">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4906">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4906">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4907">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4907">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4908">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4908">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4909">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4909">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4910">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4910">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4911">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4911">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4912">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4912">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4913">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4913">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4914">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4914">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4915">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4915">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4916">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4916">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4917">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4917">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4918">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4918">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4919">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4919">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4920">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4920">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4921">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4921">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4922">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4922">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4924">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4924">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4925">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4925">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4926">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4926">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4927">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4927">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4928">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4928">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4929">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4929">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4930">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4930">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4932">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4932">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4933">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4933">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4934">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4934">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4935">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4935">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4937">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4937">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="2b66d-4938">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4938">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="2b66d-4939">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4939">Target</span></span> | <span data-ttu-id="2b66d-4940">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-4940">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-4941">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4941">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-4942">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-4942">8</span></span> |
| <span data-ttu-id="2b66d-4943">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-4943">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4945">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-4945">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4946">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4946">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4947">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4947">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4948">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-4948">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-4949">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4949">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-4950">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4950">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-4952">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4954">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-4954">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4956">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-4956">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4958">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4958">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4960">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4960">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4961">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4961">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-4962">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-4962">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-4963">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-4963">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-4964">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-4964">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4966">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-4966">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-4967">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4967">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4968">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4968">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4969">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-4969">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-4970">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-4970">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-4971">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-4971">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4972">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-4972">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-4973">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-4973">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-4974">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4974">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-4975">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4975">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-4976">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-4976">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-4977">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4977">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-4978">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-4978">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-4979">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4979">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-4980">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-4980">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4981">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-4981">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-4982">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-4982">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4984">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-4984">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4985">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-4985">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-4986">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-4986">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-4987">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-4987">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-4988">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-4988">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-4989">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-4989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-4990">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-4990">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4992">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-4993">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-4994">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-4994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-4995">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-4995">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-4997">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-4997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="2b66d-4998">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="2b66d-4998">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="2b66d-4999">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-4999">Target</span></span> | <span data-ttu-id="2b66d-5000">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5000">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5001">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5002">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5002">8</span></span> |
| <span data-ttu-id="2b66d-5003">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5003">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5005">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5005">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5006">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5006">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5007">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5007">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5008">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5008">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5009">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5009">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5010">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5010">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5012">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5012">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5014">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5014">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5016">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5016">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5018">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5018">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5020">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5020">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5021">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5021">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5022">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5022">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5023">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5023">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5024">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5024">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5026">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5026">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5027">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5027">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5028">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5028">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5029">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5029">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5030">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5030">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5031">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5031">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5032">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5032">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5033">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5033">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5034">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5034">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5035">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5035">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5036">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5036">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5037">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5037">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5038">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5038">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5039">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5039">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5040">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5040">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5041">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5041">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5042">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5042">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5044">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5044">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5045">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5045">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5046">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5046">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5047">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5047">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5048">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5048">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5049">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5049">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5050">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5050">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5052">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5052">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5053">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5053">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5054">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5054">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5055">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5055">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5057">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5057">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="2b66d-5058">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non typé (76)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5058">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="2b66d-5059">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5059">Target</span></span> | <span data-ttu-id="2b66d-5060">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5060">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5061">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5061">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5062">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5062">8</span></span> |
| <span data-ttu-id="2b66d-5063">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5063">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5065">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5065">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5066">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5066">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5067">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5067">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5068">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5068">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5069">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5069">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5070">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5070">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5072">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5072">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5074">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5074">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5076">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5076">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-5077">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5077">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5078">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5078">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5079">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5079">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5080">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5080">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5081">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5081">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5082">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5082">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5084">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5084">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5085">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5085">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5086">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5087">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5088">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5089">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5090">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5091">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5091">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5092">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5093">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5094">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5095">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5096">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5097">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5098">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5099">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5100">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5100">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5102">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5102">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5103">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5103">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5104">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5104">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5105">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5105">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5106">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5106">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5107">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5108">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5108">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5110">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5111">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5112">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5113">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5113">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5115">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="2b66d-5116">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5116">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="2b66d-5117">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5117">Target</span></span> | <span data-ttu-id="2b66d-5118">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5118">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5119">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5120">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5120">8</span></span> |
| <span data-ttu-id="2b66d-5121">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5121">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5123">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5123">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5124">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5125">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5126">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5127">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5128">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5130">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5132">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5132">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5134">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5134">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5136">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5136">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5138">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5138">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5139">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5139">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5140">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5140">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5141">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5141">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5142">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5142">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5144">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5145">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5146">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5147">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5148">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5149">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5150">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5151">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5151">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5152">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5153">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5155">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5157">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5158">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5159">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5160">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5160">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5162">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5163">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5164">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5165">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5166">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5166">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5167">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5168">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5168">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5170">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5170">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5171">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5171">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5172">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5172">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5173">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5173">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5175">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5175">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="2b66d-5176">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5176">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="2b66d-5177">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5177">Target</span></span> | <span data-ttu-id="2b66d-5178">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5178">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5179">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5179">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5180">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5180">8</span></span> |
| <span data-ttu-id="2b66d-5181">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5181">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5183">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5183">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5184">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5184">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5185">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5186">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5186">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5187">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5187">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5188">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5188">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5190">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5190">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5192">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5192">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5194">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5194">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5196">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5196">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5198">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5198">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5199">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5199">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5200">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5200">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5201">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5201">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5202">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5202">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5204">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5204">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5205">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5205">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5206">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5206">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5207">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5207">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5208">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5208">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5209">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5209">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5210">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5210">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5211">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5211">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5212">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5212">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5213">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5213">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5214">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5214">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5215">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5215">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5216">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5216">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5217">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5217">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5218">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5218">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5219">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5219">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5220">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5220">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5222">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5223">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5224">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5225">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5226">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5226">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5227">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5228">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5228">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5230">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5230">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5231">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5231">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5232">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5232">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5233">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5233">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5235">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5235">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="2b66d-5236">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non typé (79)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5236">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="2b66d-5237">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5237">Target</span></span> | <span data-ttu-id="2b66d-5238">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5238">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5239">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5239">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5240">4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5240">4</span></span> |
| <span data-ttu-id="2b66d-5241">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5241">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5243">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5243">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5244">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5244">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5245">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5245">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5246">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5246">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5247">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5248">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5248">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5250">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5250">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5252">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5252">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5254">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5254">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-5255">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5255">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5256">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5256">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5257">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5257">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5258">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5258">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5259">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5259">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5260">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5260">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5262">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5263">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5264">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5265">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5266">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5267">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5268">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5269">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5269">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5270">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5271">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5272">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5273">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5274">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5275">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5276">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5277">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5278">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5278">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5280">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5280">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5281">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5281">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5282">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5282">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5283">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5283">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5284">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5284">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5285">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5285">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5286">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5286">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5288">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5288">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5289">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5289">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5290">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5290">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5291">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5291">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5292">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5292">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="2b66d-5293">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5293">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="2b66d-5294">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5294">Target</span></span> | <span data-ttu-id="2b66d-5295">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5295">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5296">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5296">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5297">4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5297">4</span></span> |
| <span data-ttu-id="2b66d-5298">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5298">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5300">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5300">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5301">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5301">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5302">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5303">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5304">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5305">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5305">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5307">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5307">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5309">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5309">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5311">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5311">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5313">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5313">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5315">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5316">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5317">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5317">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5318">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5319">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5319">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5321">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5322">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5323">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5323">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5324">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5324">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5325">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5325">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5326">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5326">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5327">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5327">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5328">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5328">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5329">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5329">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5330">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5330">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5331">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5331">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5332">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5332">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5333">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5333">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5334">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5334">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5335">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5335">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5336">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5336">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5337">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5337">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5339">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5339">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5340">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5340">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5341">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5341">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5342">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5342">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5343">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5343">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5344">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5344">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5345">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5345">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5347">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5347">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5348">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5348">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5349">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5349">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5350">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5350">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5351">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5351">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="2b66d-5352">DXGI_FORMAT_BC4 \_ ronfler<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5352">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="2b66d-5353">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5353">Target</span></span> | <span data-ttu-id="2b66d-5354">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5354">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5355">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5355">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5356">4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5356">4</span></span> |
| <span data-ttu-id="2b66d-5357">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5357">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5359">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5359">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5360">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5360">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5361">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5361">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5362">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5362">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5363">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5363">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5364">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5364">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5366">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5366">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5368">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5368">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5370">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5370">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5372">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5372">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5374">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5374">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5375">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5375">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5376">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5376">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5377">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5377">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5378">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5378">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5380">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5380">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5381">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5381">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5382">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5382">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5383">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5383">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5384">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5384">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5385">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5385">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5386">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5386">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5387">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5387">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5388">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5388">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5389">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5389">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5390">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5390">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5391">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5391">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5392">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5392">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5393">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5393">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5394">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5394">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5395">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5395">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5396">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5396">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5398">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5398">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5399">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5399">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5400">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5400">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5401">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5401">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5402">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5402">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5403">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5403">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5404">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5404">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5406">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5406">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5407">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5407">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5408">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5408">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5409">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5409">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5410">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5410">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="2b66d-5411">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non typé (82)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5411">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="2b66d-5412">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5412">Target</span></span> | <span data-ttu-id="2b66d-5413">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5413">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5414">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5414">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5415">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5415">8</span></span> |
| <span data-ttu-id="2b66d-5416">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5416">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5418">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5418">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5419">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5419">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5420">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5420">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5421">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5421">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5422">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5422">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5423">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5425">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5427">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5429">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5429">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-5430">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5430">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5431">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5431">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5432">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5432">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5433">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5433">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5434">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5434">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5435">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5435">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5437">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5437">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5438">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5438">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5439">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5439">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5440">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5440">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5441">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5441">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5442">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5442">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5443">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5443">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5444">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5444">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5445">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5445">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5446">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5446">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5447">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5447">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5448">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5448">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5449">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5449">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5450">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5450">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5451">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5451">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5452">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5452">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5453">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5453">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5455">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5455">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5456">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5456">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5457">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5457">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5458">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5458">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5459">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5459">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5460">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5460">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5461">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5461">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5463">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5463">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5464">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5464">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5465">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5465">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5466">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5466">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5467">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5467">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="2b66d-5468">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5468">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="2b66d-5469">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5469">Target</span></span> | <span data-ttu-id="2b66d-5470">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5470">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5471">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5471">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5472">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5472">8</span></span> |
| <span data-ttu-id="2b66d-5473">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5473">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5475">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5475">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5476">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5476">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5477">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5477">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5478">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5478">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5479">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5479">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5480">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5480">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5482">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5482">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5484">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5484">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5486">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5486">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5488">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5488">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5490">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5490">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5491">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5491">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5492">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5492">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5493">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5493">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5494">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5494">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5496">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5496">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5497">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5497">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5498">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5498">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5499">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5499">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5500">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5500">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5501">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5501">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5502">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5502">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5503">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5503">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5504">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5504">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5505">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5505">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5506">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5506">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5507">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5507">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5508">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5508">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5509">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5509">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5510">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5510">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5511">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5511">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5512">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5512">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5514">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5514">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5515">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5515">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5516">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5516">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5517">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5517">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5518">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5518">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5519">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5520">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5520">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5522">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5523">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5524">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5525">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5525">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5526">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="2b66d-5527">DXGI_FORMAT_BC5 \_ ronfler<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5527">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="2b66d-5528">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5528">Target</span></span> | <span data-ttu-id="2b66d-5529">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5529">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5530">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5531">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-5531">8</span></span> |
| <span data-ttu-id="2b66d-5532">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5532">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5534">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5534">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5535">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5535">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5536">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5536">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5537">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5537">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5538">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5538">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-5539">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5539">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5541">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5541">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5543">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5543">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5545">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5545">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5547">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5547">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5549">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5549">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5550">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5550">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5551">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5551">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5552">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5552">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5553">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5553">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5555">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5555">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5556">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5556">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5557">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5557">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5558">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5558">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5559">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5559">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5560">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5560">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5561">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5561">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5562">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5562">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5563">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5563">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5564">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5564">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5565">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5565">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5566">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5566">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5567">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5567">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5568">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5568">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5569">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5569">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5570">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5570">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5571">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5571">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5573">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5573">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5574">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5574">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5575">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5575">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5576">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5576">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5577">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5577">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5578">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5578">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5579">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5579">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5581">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5581">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5582">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5582">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5583">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5583">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5584">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5584">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5585">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5585">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="2b66d-5586">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5586">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="2b66d-5587">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5587">Target</span></span> | <span data-ttu-id="2b66d-5588">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5588">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5589">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5589">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5590">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-5590">16</span></span> |
| <span data-ttu-id="2b66d-5591">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5591">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5593">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5593">Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5595">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5595">Input Assembler Vertex Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5597">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5597">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5598">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5598">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5599">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5599">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5601">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5601">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5603">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5603">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5605">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5607">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5607">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5609">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5609">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5611">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5611">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5612">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5612">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5613">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5613">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5614">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5614">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5615">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5615">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5617">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5617">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5619">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5621">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5621">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5623">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5623">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5624">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5624">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5625">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5625">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5626">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5626">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5627">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5627">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5628">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5628">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5629">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5629">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5630">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5630">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5631">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5631">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5632">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5632">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5633">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5633">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5634">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5634">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5635">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5635">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5636">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5636">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5638">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5638">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5640">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5640">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5642">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5642">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5644">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5644">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5646">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5646">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5648">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5648">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5649">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5649">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-5650">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5650">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5651">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5651">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5652">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5652">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5653">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5653">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5654">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5654">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="2b66d-5655">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5655">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="2b66d-5656">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5656">Target</span></span> | <span data-ttu-id="2b66d-5657">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5657">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5658">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5658">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5659">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-5659">16</span></span> |
| <span data-ttu-id="2b66d-5660">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5660">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5662">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5662">Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5664">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5664">Input Assembler Vertex Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5666">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5666">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5667">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5667">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5668">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5668">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5670">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5670">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5672">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5672">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5674">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5674">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5676">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5676">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5678">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5678">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5680">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5680">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5681">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5681">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5682">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5682">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5683">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5683">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5684">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5684">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5686">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5686">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5688">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5688">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5690">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5690">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5692">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5692">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5693">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5693">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5694">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5694">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5695">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5695">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5696">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5696">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5697">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5697">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5698">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5698">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5699">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5699">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5700">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5700">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5701">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5701">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5702">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5702">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5703">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5703">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5704">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5704">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5705">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5705">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5707">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5707">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5709">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5709">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5711">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5711">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5713">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5713">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5715">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5715">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5717">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5718">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-5719">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5719">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5720">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5720">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5721">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5721">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5722">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5722">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-5723">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5723">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="2b66d-5724">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8A8 type (90)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5724">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="2b66d-5725">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5725">Target</span></span> | <span data-ttu-id="2b66d-5726">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5726">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5727">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5727">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5728">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-5728">32</span></span> |
| <span data-ttu-id="2b66d-5729">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5729">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5731">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5731">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5732">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5732">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5733">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5734">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5735">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5737">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5739">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5741">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5743">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5743">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-5744">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5744">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5745">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5745">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5746">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5746">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5747">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5747">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5748">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5748">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5749">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5749">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5751">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5751">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5752">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5752">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5753">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5753">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5754">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5754">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5755">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5755">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5756">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5756">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5757">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5757">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5758">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5758">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5759">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5759">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5760">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5760">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5761">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5761">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5762">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5762">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5763">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5763">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5764">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5764">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5765">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5765">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5766">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5766">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5767">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5767">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5769">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5769">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5770">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5770">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5771">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5771">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5772">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5772">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5773">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5773">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5774">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5774">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5775">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5775">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5777">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5777">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5778">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5778">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5779">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5779">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5780">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5780">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5782">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5782">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="2b66d-5783">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5783">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="2b66d-5784">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5784">Target</span></span> | <span data-ttu-id="2b66d-5785">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5785">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5786">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5786">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5787">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-5787">32</span></span> |
| <span data-ttu-id="2b66d-5788">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5788">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5790">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5790">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5792">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5792">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5794">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5794">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5795">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5795">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5796">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5796">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5798">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5798">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5800">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5800">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5802">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5802">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5804">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5804">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5806">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5806">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5808">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5808">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5809">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5809">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5810">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5810">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5811">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5811">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5812">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5812">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5814">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5814">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5816">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5816">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5818">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5818">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5820">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5820">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5821">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5821">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5822">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5822">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5823">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5823">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5824">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5824">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5825">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5825">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5826">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5826">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5827">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5827">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5828">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5828">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5829">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5829">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5830">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5830">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5831">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5831">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5832">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5832">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5833">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5833">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5835">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5835">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5837">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5837">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5839">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5839">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5841">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5841">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5843">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5843">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5845">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5845">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5847">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5847">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5849">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5849">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5850">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5850">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5852">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5852">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5854">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5854">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5856">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5856">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="2b66d-5857">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRVB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5857">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="2b66d-5858">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5858">Target</span></span> | <span data-ttu-id="2b66d-5859">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5859">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5860">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5860">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5861">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-5861">32</span></span> |
| <span data-ttu-id="2b66d-5862">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5862">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5864">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5864">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5865">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5865">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5866">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5866">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5867">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5867">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5868">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5868">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5870">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5872">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5872">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5874">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5874">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5876">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5876">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5878">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5878">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5880">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5880">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5881">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5881">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5882">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5882">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5883">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5883">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5884">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5884">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5886">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5886">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5888">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5888">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5890">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5890">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5892">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5893">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5894">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5895">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5896">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5897">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5898">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5900">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5901">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5902">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5903">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5904">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5905">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5905">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5907">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5907">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5909">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5909">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5911">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5911">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5913">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5913">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5915">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5915">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5917">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5917">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5919">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5919">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5921">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5921">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5922">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5922">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5924">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5924">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-5926">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5926">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5928">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="2b66d-5929">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8X8 type (92)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5929">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="2b66d-5930">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5930">Target</span></span> | <span data-ttu-id="2b66d-5931">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5931">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5932">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5933">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-5933">32</span></span> |
| <span data-ttu-id="2b66d-5934">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5934">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5936">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5936">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5937">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5937">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5938">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5938">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5939">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-5939">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-5940">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5940">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5942">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5942">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5944">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-5944">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5946">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-5946">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5948">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-5948">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-5949">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5949">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5950">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5950">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5951">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5951">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-5952">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-5952">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-5953">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-5953">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-5954">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-5954">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5956">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-5956">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-5957">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5957">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5958">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5958">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5959">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-5959">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-5960">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-5960">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-5961">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-5961">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5962">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-5962">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-5963">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-5963">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-5964">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5964">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-5965">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5965">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-5966">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-5966">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-5967">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5967">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-5968">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-5968">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-5969">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5969">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-5970">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-5970">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5971">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-5971">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-5972">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-5972">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5974">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-5974">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5975">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-5975">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-5976">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-5976">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-5977">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-5977">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-5978">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-5978">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-5979">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-5979">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-5980">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-5980">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5982">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5982">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-5983">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5983">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-5984">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-5984">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-5985">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5985">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5987">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-5987">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="2b66d-5988">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5988">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="2b66d-5989">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-5989">Target</span></span> | <span data-ttu-id="2b66d-5990">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-5990">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-5991">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-5991">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-5992">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-5992">32</span></span> |
| <span data-ttu-id="2b66d-5993">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-5993">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5995">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-5995">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5997">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5997">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-5999">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-5999">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6000">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6000">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6001">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6001">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6003">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6005">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6007">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6009">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6009">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6011">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6011">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6013">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6013">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6014">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6014">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6015">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6015">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6016">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6016">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6017">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6017">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6019">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6019">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6021">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6021">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6023">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6023">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6025">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6025">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6026">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6026">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6027">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6027">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6028">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6028">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6029">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6029">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6030">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6030">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6031">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6031">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6032">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6032">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6033">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6033">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6034">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6034">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6035">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6035">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6036">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6036">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6037">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6037">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6038">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6038">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6040">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6040">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6042">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6042">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6044">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6044">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6046">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6046">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6048">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6048">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6050">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6050">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6051">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6051">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6053">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6053">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-6054">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6054">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6056">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6056">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6058">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6058">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6060">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6060">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="2b66d-6061">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRVB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6061">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="2b66d-6062">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6062">Target</span></span> | <span data-ttu-id="2b66d-6063">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6063">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6064">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6064">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6065">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-6065">32</span></span> |
| <span data-ttu-id="2b66d-6066">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6066">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6068">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6068">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6069">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6069">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6070">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6070">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6071">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6071">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6072">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6072">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6074">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6074">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6076">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6076">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6078">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6080">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6080">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6082">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6082">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6084">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6084">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6085">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6085">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6086">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6086">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6087">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6087">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6088">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6088">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6090">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6090">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6092">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6092">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6094">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6094">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6096">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6096">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6097">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6097">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6098">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6098">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6099">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6099">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6100">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6100">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6101">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6101">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6102">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6102">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6103">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6103">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6104">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6104">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6105">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6105">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6106">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6106">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6107">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6107">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6108">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6108">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6109">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6109">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6111">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6111">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6113">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6113">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6115">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6115">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6117">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6117">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6119">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6119">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6121">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6121">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6122">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6122">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6124">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6124">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-6125">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6125">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-6126">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6126">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-6127">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6127">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6129">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6129">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="2b66d-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6130">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="2b66d-6131">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6131">Target</span></span> | <span data-ttu-id="2b66d-6132">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6132">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6133">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6133">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6134">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-6134">32</span></span> |
| <span data-ttu-id="2b66d-6135">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6135">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6137">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6137">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6138">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6138">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6139">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6139">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6140">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6140">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6141">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6141">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6142">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6142">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6144">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6144">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6145">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6145">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6146">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6146">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6148">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6148">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6150">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6150">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6151">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6151">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6152">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6152">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6153">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6153">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6154">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6154">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6156">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6156">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6158">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6158">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6160">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6160">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6162">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6162">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6163">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6163">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6164">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6164">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6165">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6165">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6166">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6166">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6167">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6167">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6168">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6168">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6169">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6169">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6170">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6170">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6171">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6171">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6172">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6172">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6173">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6173">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6174">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6174">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6175">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6175">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6177">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6177">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6178">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6178">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6179">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6179">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6180">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6180">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6181">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6181">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6182">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6182">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6183">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6183">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6184">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6184">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6186">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6186">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6188">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6188">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6190">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6190">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6192">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6192">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="2b66d-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6193">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="2b66d-6194">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6194">Target</span></span> | <span data-ttu-id="2b66d-6195">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6195">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6196">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6196">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6197">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-6197">32</span></span> |
| <span data-ttu-id="2b66d-6198">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6198">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6200">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6200">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6201">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6201">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6202">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6202">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6203">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6203">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6204">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6204">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6205">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6205">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6207">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6207">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6208">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6208">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6209">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6209">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6211">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6211">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6213">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6213">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6214">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6214">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6215">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6215">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6216">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6216">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6217">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6217">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6218">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6218">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6219">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6219">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6220">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6220">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6221">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6221">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6222">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6222">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6223">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6223">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6224">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6224">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6225">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6225">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6226">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6226">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6227">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6227">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6228">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6228">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6229">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6229">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6230">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6230">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6231">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6231">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6232">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6232">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6233">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6233">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6234">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6234">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6236">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6236">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6237">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6237">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6238">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6238">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6239">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6239">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6240">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6240">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6241">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6241">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6242">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6242">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6243">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6243">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6245">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6245">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6247">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6247">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6249">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6249">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6251">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6251">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="2b66d-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6252">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="2b66d-6253">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6253">Target</span></span> | <span data-ttu-id="2b66d-6254">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6254">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6255">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6255">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6256">64</span><span class="sxs-lookup"><span data-stu-id="2b66d-6256">64</span></span> |
| <span data-ttu-id="2b66d-6257">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6257">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6259">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6259">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6260">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6260">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6261">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6261">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6262">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6262">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6263">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6263">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6264">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6264">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6266">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6266">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6267">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6267">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6268">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6268">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6270">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6270">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6272">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6272">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6273">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6273">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6274">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6274">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6275">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6275">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6276">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6276">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6278">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6279">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6280">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6281">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6282">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6283">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6284">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6285">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6285">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6286">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6287">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6289">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6291">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6292">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6293">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6294">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6294">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6296">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6297">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6298">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6299">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6300">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6300">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6301">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6302">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6303">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6303">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6305">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6305">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6307">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6307">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6309">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6309">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6311">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6311">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="2b66d-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6312">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="2b66d-6313">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6313">Target</span></span> | <span data-ttu-id="2b66d-6314">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6314">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6315">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6315">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6316">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-6316">8</span></span> |
| <span data-ttu-id="2b66d-6317">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6317">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6319">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6319">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6320">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6320">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6321">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6321">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6322">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6322">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6323">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6323">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6324">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6324">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6326">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6326">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6327">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6328">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6328">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6330">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6330">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6332">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6332">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6333">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6333">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6334">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6334">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6335">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6335">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6336">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6336">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6337">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6337">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6338">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6338">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6340">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6340">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6342">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6343">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6344">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6345">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6346">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6346">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6347">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6348">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6350">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6352">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6353">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6354">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6355">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6355">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6357">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6358">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6359">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6360">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6361">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6361">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6362">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6363">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6363">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6364">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6364">Video Decoder Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6366">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6366">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6368">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6368">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6370">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6370">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6372">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6372">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="2b66d-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6373">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="2b66d-6374">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6374">Target</span></span> | <span data-ttu-id="2b66d-6375">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6375">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6376">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6376">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6377">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-6377">16</span></span> |
| <span data-ttu-id="2b66d-6378">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6378">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6380">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6380">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6381">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6381">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6382">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6382">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6383">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6383">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6384">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6384">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6385">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6385">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6387">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6387">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6388">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6388">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6389">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6389">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6391">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6391">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6393">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6393">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6394">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6394">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6395">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6395">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6396">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6396">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6397">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6397">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6398">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6399">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6401">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6401">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6403">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6403">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6404">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6404">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6405">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6405">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6406">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6406">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6407">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6407">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6408">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6408">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6409">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6409">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6410">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6410">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6411">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6411">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6412">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6412">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6413">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6413">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6414">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6414">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6415">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6415">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6416">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6416">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6418">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6418">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6419">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6419">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6420">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6420">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6421">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6421">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6422">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6422">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6423">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6423">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6424">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6424">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6425">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6425">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6427">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6427">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6429">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6429">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6431">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6431">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6433">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6433">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="2b66d-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6434">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="2b66d-6435">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6435">Target</span></span> | <span data-ttu-id="2b66d-6436">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6436">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6437">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6437">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6438">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-6438">16</span></span> |
| <span data-ttu-id="2b66d-6439">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6439">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6441">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6441">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6442">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6442">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6443">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6443">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6444">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6444">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6445">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6445">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6446">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6446">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6448">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6448">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6449">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6449">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6450">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6450">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6452">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6452">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6454">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6454">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6455">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6455">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6456">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6456">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6457">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6457">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6458">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6458">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6459">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6460">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6462">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6462">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6464">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6465">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6466">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6467">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6468">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6468">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6469">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6470">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6472">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6473">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6474">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6475">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6476">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6477">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6477">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6479">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6480">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6481">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6482">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6483">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6483">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6484">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6485">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6486">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6486">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6488">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6488">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6490">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6490">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6492">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6492">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6494">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="2b66d-6495">DXGI_FORMAT_420 \_ <sup>V</sup> opaque (106)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6495">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="2b66d-6496">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6496">Target</span></span> | <span data-ttu-id="2b66d-6497">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6497">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6498">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6499">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-6499">8</span></span> |
| <span data-ttu-id="2b66d-6500">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6500">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6502">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6502">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6503">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6503">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6504">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6504">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6505">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6505">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6506">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6506">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6507">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6507">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6509">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6509">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6510">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6510">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6511">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6511">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-6512">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6512">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6513">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6513">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6514">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6514">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6515">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6515">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6516">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6516">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6517">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6517">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6518">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6518">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6519">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6520">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6520">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6521">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6521">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6522">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6522">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6523">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6523">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6524">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6524">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6525">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6525">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6526">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6526">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6527">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6527">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6528">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6528">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6529">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6529">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6530">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6530">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6531">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6531">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6532">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6532">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6533">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6533">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6534">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6534">CPU Lockable</span></span> | \- |
| <span data-ttu-id="2b66d-6535">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6535">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6536">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6536">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6537">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6537">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6538">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6538">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6539">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6539">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6540">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6540">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6541">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6541">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6542">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6542">Video Decoder Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6544">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6544">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6546">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6546">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6548">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6548">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6550">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6550">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="2b66d-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6551">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="2b66d-6552">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6552">Target</span></span> | <span data-ttu-id="2b66d-6553">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6553">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6554">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6554">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6555">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-6555">16</span></span> |
| <span data-ttu-id="2b66d-6556">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6556">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6558">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6558">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6559">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6559">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6560">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6560">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6561">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6561">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6562">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6562">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6563">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6563">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6565">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6565">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6566">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6566">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6567">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6567">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6569">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6569">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6571">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6571">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6572">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6572">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6573">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6573">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6574">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6574">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6575">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6575">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6576">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6576">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6577">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6577">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6578">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6578">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6579">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6579">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6580">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6580">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6581">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6581">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6582">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6582">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6583">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6583">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6584">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6584">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6585">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6585">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6586">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6586">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6587">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6587">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6588">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6588">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6589">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6589">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6590">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6590">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6591">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6591">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6592">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6592">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6594">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6594">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6595">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6595">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6596">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6596">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6597">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6597">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6598">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6598">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6599">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6599">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6600">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6600">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6601">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6601">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6603">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6603">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6605">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6605">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6607">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6607">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6609">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6609">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="2b66d-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6610">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="2b66d-6611">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6611">Target</span></span> | <span data-ttu-id="2b66d-6612">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6612">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6613">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6613">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6614">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-6614">32</span></span> |
| <span data-ttu-id="2b66d-6615">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6615">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6617">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6617">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6618">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6618">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6619">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6619">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6620">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6620">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6621">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6621">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6622">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6622">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6624">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6624">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6625">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6625">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6626">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6626">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6628">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6628">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6630">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6630">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6631">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6631">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6632">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6632">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6633">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6633">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6634">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6634">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6635">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6635">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6636">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6636">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6637">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6637">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6638">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6638">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6639">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6639">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6640">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6640">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6641">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6641">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6642">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6642">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6643">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6643">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6644">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6644">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6645">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6645">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6646">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6646">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6647">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6647">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6648">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6648">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6649">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6649">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6650">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6650">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6651">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6651">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6653">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6653">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6654">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6654">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6655">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6655">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6656">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6656">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6657">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6657">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6658">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6658">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6659">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6659">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6660">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6660">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6662">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6662">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6664">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6664">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6666">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6666">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6668">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6668">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="2b66d-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6669">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="2b66d-6670">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6670">Target</span></span> | <span data-ttu-id="2b66d-6671">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6671">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6672">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6672">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6673">32</span><span class="sxs-lookup"><span data-stu-id="2b66d-6673">32</span></span> |
| <span data-ttu-id="2b66d-6674">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6674">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6676">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6676">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6677">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6677">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6678">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6678">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6679">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6679">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6680">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6680">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6681">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6681">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6683">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6683">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6684">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6684">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6685">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6685">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6687">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6687">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6689">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6689">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6690">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6690">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6691">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6691">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6692">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6692">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6693">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6693">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6694">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6694">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6695">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6695">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6696">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6696">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6697">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6697">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6698">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6698">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6699">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6699">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6700">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6700">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6701">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6701">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6702">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6702">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6703">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6703">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6704">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6704">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6705">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6705">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6706">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6706">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6707">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6707">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6708">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6708">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6709">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6709">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6710">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6710">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6712">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6712">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6713">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6713">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6714">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6714">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6715">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6715">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6716">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6716">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6717">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6717">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6718">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6718">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6719">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6719">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6721">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6721">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6723">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6723">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6725">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6725">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6727">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6727">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="2b66d-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6728">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="2b66d-6729">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6729">Target</span></span> | <span data-ttu-id="2b66d-6730">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6730">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6731">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6731">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6732">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-6732">8</span></span> |
| <span data-ttu-id="2b66d-6733">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6733">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6735">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6735">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6736">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6736">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6737">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6737">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6738">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6738">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6739">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6739">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6740">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6740">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6742">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6742">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6743">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6743">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6744">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6744">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6746">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6746">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6748">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6748">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6749">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6749">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6750">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6750">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6751">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6752">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6752">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6753">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6753">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6754">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6754">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6756">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6756">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6758">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6758">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6759">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6759">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6760">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6760">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6761">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6761">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6762">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6762">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6763">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6763">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6764">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6764">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6765">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6765">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6766">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6766">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6767">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6767">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6768">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6768">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6769">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6769">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6770">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6770">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6771">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6771">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6773">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6773">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6774">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6774">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6775">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6775">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6776">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6776">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6777">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6777">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6778">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6778">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6779">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6779">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6780">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6780">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6782">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6782">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6784">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6784">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6786">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6786">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6788">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6788">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="2b66d-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6789">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="2b66d-6790">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6790">Target</span></span> | <span data-ttu-id="2b66d-6791">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6791">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6792">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6792">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6793">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-6793">8</span></span> |
| <span data-ttu-id="2b66d-6794">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6794">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6796">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6796">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6797">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6797">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6798">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6798">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6799">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6799">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6800">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6800">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6801">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6801">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6803">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6803">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6804">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6804">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6805">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6805">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-6806">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6806">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6807">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6807">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6808">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6808">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6809">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6809">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6810">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6810">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6811">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6811">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6812">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6812">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6813">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6813">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6814">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6814">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6815">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6815">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6816">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6816">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6817">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6817">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6818">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6818">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6819">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6819">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6820">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6820">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6821">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6821">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6822">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6822">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6823">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6823">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6824">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6824">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6825">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6825">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6826">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6826">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6827">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6827">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6828">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6828">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6830">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6830">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6831">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6831">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6832">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6832">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6833">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6833">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6834">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6834">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6835">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6835">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6836">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6836">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6837">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6837">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-6838">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6838">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6840">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6840">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-6841">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6841">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-6842">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6842">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="2b66d-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6843">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="2b66d-6844">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6844">Target</span></span> | <span data-ttu-id="2b66d-6845">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6845">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6846">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6846">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6847">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-6847">8</span></span> |
| <span data-ttu-id="2b66d-6848">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6848">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6850">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6850">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6851">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6851">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6852">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6852">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6853">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6853">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6854">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6854">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6855">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6855">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6857">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6857">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6858">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6859">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6859">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-6860">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6860">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6861">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6861">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6862">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6862">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6863">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6863">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6864">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6864">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6865">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6865">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6866">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6867">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6868">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6869">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6870">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6871">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6872">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6873">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6873">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6874">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6875">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6876">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6877">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6879">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6880">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6881">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6882">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6882">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6884">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6885">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6886">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6887">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6888">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6888">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6889">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6890">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6890">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6891">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6891">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-6892">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6892">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6894">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-6895">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6895">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-6896">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6896">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="2b66d-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6897">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="2b66d-6898">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6898">Target</span></span> | <span data-ttu-id="2b66d-6899">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6899">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6900">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6900">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6901">8</span><span class="sxs-lookup"><span data-stu-id="2b66d-6901">8</span></span> |
| <span data-ttu-id="2b66d-6902">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6902">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6904">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6904">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6905">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6905">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6906">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6906">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6907">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6907">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6908">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6908">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6909">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6909">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6911">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6911">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6912">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6912">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6913">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6913">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-6914">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6914">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6915">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6915">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6916">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6916">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6917">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6917">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6918">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6918">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6919">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6919">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6920">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6920">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6921">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6921">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6922">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6922">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6923">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6923">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6924">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6924">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6925">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6925">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6926">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6926">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6927">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6927">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6928">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6928">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6929">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6929">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6930">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6930">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6931">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6931">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6932">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6932">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6933">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6933">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6934">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6934">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6935">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6935">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6936">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6936">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6938">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6938">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6939">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6939">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6940">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6940">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6941">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6941">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6942">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6942">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6943">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6943">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6944">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6944">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6945">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6945">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-6946">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6946">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6948">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6948">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-6949">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6949">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-6950">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-6950">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="2b66d-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6951">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="2b66d-6952">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-6952">Target</span></span> | <span data-ttu-id="2b66d-6953">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-6953">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-6954">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6954">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-6955">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-6955">16</span></span> |
| <span data-ttu-id="2b66d-6956">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-6956">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-6958">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-6958">Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6959">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6959">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6960">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-6960">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6961">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-6961">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-6962">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6962">Texture1D</span></span> | \- |
| <span data-ttu-id="2b66d-6963">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6963">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6965">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-6965">Texture3D</span></span> | \- |
| <span data-ttu-id="2b66d-6966">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-6966">TextureCube</span></span> | \- |
| <span data-ttu-id="2b66d-6967">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-6967">Shader ld</span></span> | \- |
| <span data-ttu-id="2b66d-6968">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6968">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6969">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6969">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6970">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-6970">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-6971">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-6971">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-6972">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-6972">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-6973">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-6973">Mipmap</span></span> | \- |
| <span data-ttu-id="2b66d-6974">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-6974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="2b66d-6975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6975">RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6976">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6977">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-6977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-6978">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-6978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-6979">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-6979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6980">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-6980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-6981">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-6981">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-6982">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-6983">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-6984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-6984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-6985">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-6986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-6986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-6987">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-6988">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-6988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6989">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-6989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-6990">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-6990">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-6992">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-6992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6993">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-6993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="2b66d-6994">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-6994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="2b66d-6995">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-6995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="2b66d-6996">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-6996">Multisample Load</span></span> | \- |
| <span data-ttu-id="2b66d-6997">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-6997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-6998">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-6998">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-6999">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-6999">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-7000">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-7000">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7002">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-7002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-7003">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-7003">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-7004">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-7004">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="2b66d-7005">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="2b66d-7005">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="2b66d-7006">Cible</span><span class="sxs-lookup"><span data-stu-id="2b66d-7006">Target</span></span> | <span data-ttu-id="2b66d-7007">Support</span><span class="sxs-lookup"><span data-stu-id="2b66d-7007">Support</span></span> |
| - | - |
| <span data-ttu-id="2b66d-7008">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="2b66d-7008">Bits Per Element (BPE)</span></span> | <span data-ttu-id="2b66d-7009">16</span><span class="sxs-lookup"><span data-stu-id="2b66d-7009">16</span></span> |
| <span data-ttu-id="2b66d-7010">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="2b66d-7010">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7012">Buffer</span><span class="sxs-lookup"><span data-stu-id="2b66d-7012">Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7014">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-7014">Input Assembler Vertex Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7016">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="2b66d-7016">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-7017">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="2b66d-7017">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="2b66d-7018">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2b66d-7018">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7020">Texture2D</span><span class="sxs-lookup"><span data-stu-id="2b66d-7020">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7022">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2b66d-7022">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7024">TextureCube</span><span class="sxs-lookup"><span data-stu-id="2b66d-7024">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7026">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="2b66d-7026">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7028">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="2b66d-7028">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7030">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="2b66d-7030">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="2b66d-7031">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="2b66d-7031">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="2b66d-7032">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="2b66d-7032">Shader gather4</span></span> | \- |
| <span data-ttu-id="2b66d-7033">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="2b66d-7033">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="2b66d-7034">MIP</span><span class="sxs-lookup"><span data-stu-id="2b66d-7034">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7036">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="2b66d-7036">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7038">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-7038">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7040">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="2b66d-7040">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7042">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="2b66d-7042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="2b66d-7043">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="2b66d-7043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="2b66d-7044">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="2b66d-7044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-7045">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="2b66d-7045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="2b66d-7046">UAV typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-7046">Typed UAV</span></span> | \- |
| <span data-ttu-id="2b66d-7047">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-7047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="2b66d-7048">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-7048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="2b66d-7049">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="2b66d-7049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="2b66d-7050">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-7050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="2b66d-7051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="2b66d-7051">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="2b66d-7052">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-7052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="2b66d-7053">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="2b66d-7053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-7054">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="2b66d-7054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="2b66d-7055">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="2b66d-7055">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7057">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="2b66d-7057">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7059">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="2b66d-7059">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7061">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="2b66d-7061">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7063">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="2b66d-7063">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="2b66d-7065">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="2b66d-7065">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="2b66d-7067">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="2b66d-7067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="2b66d-7068">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="2b66d-7068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="2b66d-7069">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-7069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="2b66d-7070">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-7070">Video Processor Input</span></span> | \- |
| <span data-ttu-id="2b66d-7071">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-7071">Video Processor Output</span></span> | \- |
| <span data-ttu-id="2b66d-7072">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="2b66d-7072">Shared Resource</span></span> | \- |
| <span data-ttu-id="2b66d-7073">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="2b66d-7073">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="2b66d-7074">Mettre en forme les notes</span><span class="sxs-lookup"><span data-stu-id="2b66d-7074">Format notes</span></span>

<span data-ttu-id="2b66d-7075">L’objectif du format peut passer d’un niveau de fonctionnalité matériel à l’autre.</span><span class="sxs-lookup"><span data-stu-id="2b66d-7075">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="2b66d-7076"><sup>L</sup> : format non typé</span><span class="sxs-lookup"><span data-stu-id="2b66d-7076"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="2b66d-7077"><sup>PC</sup> : disposition partiellement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="2b66d-7077"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="2b66d-7078"><sup>FCS</sup> : mise en page entièrement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="2b66d-7078"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="2b66d-7079"><sup>FNS</sup> : mise en page entièrement typée, non stable et simple</span><span class="sxs-lookup"><span data-stu-id="2b66d-7079"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="2b66d-7080"><sup>PCC</sup> : disposition partiellement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="2b66d-7080"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="2b66d-7081"><sup>FCC</sup> : mise en page entièrement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="2b66d-7081"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="2b66d-7082"><sup>FNC</sup> : mise en page entièrement typée, non stable et complexe</span><span class="sxs-lookup"><span data-stu-id="2b66d-7082"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="2b66d-7083"><sup>V</sup> : format vidéo</span><span class="sxs-lookup"><span data-stu-id="2b66d-7083"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="2b66d-7084">Les mémoires tampons d’arrière-plan et les analyses avec le format [**dxgi \_ \_ \_ float R16G16B16A16**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contiennent des données de gamma linéaires.</span><span class="sxs-lookup"><span data-stu-id="2b66d-7084">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b66d-7085">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b66d-7085">Related topics</span></span>

[<span data-ttu-id="2b66d-7086">Niveaux de fonctionnalité matérielle D3D12</span><span class="sxs-lookup"><span data-stu-id="2b66d-7086">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="2b66d-7087">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="2b66d-7087">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="2b66d-7088">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="2b66d-7088">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
