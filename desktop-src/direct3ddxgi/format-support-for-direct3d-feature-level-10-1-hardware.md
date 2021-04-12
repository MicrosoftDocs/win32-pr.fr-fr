---
description: Cette section spécifie les formats ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans le matériel 10,1 de niveau de fonctionnalité Direct3D.
ms.assetid: 2C7E16D7-EEF0-4EA7-A819-5274C9105F68
title: Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 10.1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edb5c81ef0a99bc14031a9a7a505736e91e13d8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481296"
---
# <a name="format-support-for-direct3d-feature-level-101-hardware"></a><span data-ttu-id="04ce8-103">Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 10.1</span><span class="sxs-lookup"><span data-stu-id="04ce8-103">Format support for Direct3D Feature Level 10.1 hardware</span></span>

<span data-ttu-id="04ce8-104">Cette section spécifie les formats ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans le matériel 10,1 de niveau de fonctionnalité Direct3D.</span><span class="sxs-lookup"><span data-stu-id="04ce8-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature Level 10.1 hardware.</span></span>

<span data-ttu-id="04ce8-105">Le tableau récapitule la prise en charge des fonctionnalités à l’aide de la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="04ce8-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="04ce8-106">Symbole</span><span class="sxs-lookup"><span data-stu-id="04ce8-106">Symbol</span></span>                            | <span data-ttu-id="04ce8-107">Description</span><span class="sxs-lookup"><span data-stu-id="04ce8-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="04ce8-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="04ce8-108">_ *-*\*</span></span>                             | <span data-ttu-id="04ce8-109">Non autorisé ou non disponible.</span><span class="sxs-lookup"><span data-stu-id="04ce8-109">Disallowed or not available.</span></span>                                                  |
| ![obligatoire](images/letter-r.jpg)  | <span data-ttu-id="04ce8-111">Un support matériel est requis.</span><span class="sxs-lookup"><span data-stu-id="04ce8-111">Hardware support is required.</span></span>                                                 |
| ![facultatif](images/letter-o.jpg)  | <span data-ttu-id="04ce8-113">Prise en charge du matériel facultative, le format peut ou non être accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="04ce8-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dépendants](images/letter-d.jpg) | <span data-ttu-id="04ce8-115">Obligatoire si la fonctionnalité facultative associée est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="04ce8-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="04ce8-116">Cette rubrique contient une section par format.</span><span class="sxs-lookup"><span data-stu-id="04ce8-116">This topic contains a section per format.</span></span> <span data-ttu-id="04ce8-117">Une *cible* de format (tables contenant une ligne par cible) peut être un type de ressource, une fonction intrinsèque HLSL ou une fonctionnalité particulière qui est dépendante d’un format particulier.</span><span class="sxs-lookup"><span data-stu-id="04ce8-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="04ce8-118">Pour vérifier par programmation la prise en charge du format dans D3D11 et D3D12, consultez vérification de la [prise en charge des fonctionnalités matérielles](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="04ce8-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="04ce8-119">Les nombres des formats sont principalement, mais pas tous, dans l’ordre numérique croissant, &mdash; certains ne sont pas triés par ordre numérique et sont répertoriés avec d’autres formats pertinents.</span><span class="sxs-lookup"><span data-stu-id="04ce8-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="04ce8-120">Notez également que les *types* sans type dans un nom de format peuvent signifier un type *partiellement* typé, et non strictement typés (reportez-vous à la section Remarques sur le [format](#format-notes) à la fin de la rubrique).</span><span class="sxs-lookup"><span data-stu-id="04ce8-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="04ce8-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="04ce8-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="04ce8-122">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-122">Target</span></span> | <span data-ttu-id="04ce8-123">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-123">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-124">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-125">0</span><span class="sxs-lookup"><span data-stu-id="04ce8-125">0</span></span> |
| <span data-ttu-id="04ce8-126">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-126">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-128">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-128">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-130">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-130">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-131">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-131">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-132">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-132">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-133">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-133">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-134">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-134">Texture2D</span></span> | \- |
| <span data-ttu-id="04ce8-135">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-135">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-136">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-137">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-137">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-138">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-138">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-139">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-139">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-140">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-140">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-141">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-141">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-142">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-142">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-143">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-143">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-144">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-144">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-145">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-145">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-146">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-146">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-147">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-147">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-148">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-148">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-149">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-149">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-150">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-150">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-151">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-151">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-152">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-152">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-153">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-153">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-154">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-154">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-155">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-155">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-156">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-156">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-157">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-157">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-158">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-158">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-159">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-159">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-160">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-160">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-162">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-162">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-163">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-163">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-164">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-164">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-165">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-165">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-166">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-166">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-167">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-167">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-168">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-168">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-169">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-170">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-171">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-172">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-172">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-173">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="04ce8-174">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32A32 type (1)</span><span class="sxs-lookup"><span data-stu-id="04ce8-174">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="04ce8-175">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-175">Target</span></span> | <span data-ttu-id="04ce8-176">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-176">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-177">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-178">128</span><span class="sxs-lookup"><span data-stu-id="04ce8-178">128</span></span> |
| <span data-ttu-id="04ce8-179">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-179">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-181">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-181">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-182">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-182">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-183">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-183">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-184">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-184">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-185">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-185">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-187">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-187">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-189">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-189">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-191">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-191">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-193">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-193">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-194">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-194">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-195">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-195">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-196">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-196">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-197">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-197">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-198">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-198">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-199">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-199">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-201">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-201">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-202">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-202">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-203">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-203">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-204">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-204">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-205">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-205">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-206">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-206">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-207">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-207">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-208">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-208">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-209">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-209">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-210">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-210">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-211">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-211">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-212">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-212">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-213">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-213">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-214">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-214">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-215">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-215">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-216">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-216">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-217">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-217">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-219">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-219">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-220">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-220">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-221">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-221">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-222">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-222">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-223">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-223">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-224">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-224">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-225">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-225">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-227">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-227">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-228">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-228">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-229">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-229">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-230">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-230">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-232">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-232">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a><span data-ttu-id="04ce8-233">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FCS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="04ce8-233">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FCS</sup> (2)</span></span>
| <span data-ttu-id="04ce8-234">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-234">Target</span></span> | <span data-ttu-id="04ce8-235">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-235">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-236">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-236">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-237">128</span><span class="sxs-lookup"><span data-stu-id="04ce8-237">128</span></span> |
| <span data-ttu-id="04ce8-238">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-238">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-240">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-240">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-242">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-242">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-244">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-244">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-245">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-245">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-247">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-247">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-249">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-249">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-251">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-251">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-253">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-253">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-255">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-255">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-257">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-257">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-259">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-259">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-260">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-260">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-261">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-261">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-262">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-262">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-263">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-263">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-265">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-265">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-267">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-267">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-269">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-269">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-271">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-271">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-272">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-272">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-273">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-273">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-274">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-274">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-275">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-275">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-276">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-276">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-277">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-277">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-278">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-278">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-279">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-279">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-280">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-280">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-281">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-281">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-282">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-282">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-283">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-283">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-284">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-284">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-286">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-286">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-288">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-288">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-290">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-290">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-292">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-292">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-294">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-294">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-296">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-296">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-297">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-297">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-299">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-299">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-300">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-300">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-301">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-301">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-302">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-302">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-304">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-304">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a><span data-ttu-id="04ce8-305">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FCS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="04ce8-305">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FCS</sup> (3)</span></span>
| <span data-ttu-id="04ce8-306">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-306">Target</span></span> | <span data-ttu-id="04ce8-307">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-307">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-308">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-308">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-309">128</span><span class="sxs-lookup"><span data-stu-id="04ce8-309">128</span></span> |
| <span data-ttu-id="04ce8-310">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-310">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-312">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-312">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-314">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-314">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-316">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-316">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-317">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-317">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-319">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-319">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-321">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-321">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-323">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-323">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-325">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-325">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-327">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-327">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-329">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-329">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-330">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-330">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-331">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-331">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-332">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-332">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-333">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-333">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-334">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-334">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-336">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-336">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-337">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-337">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-339">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-339">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-340">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-340">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-342">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-342">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-343">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-343">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-344">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-344">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-345">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-345">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-346">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-346">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-347">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-347">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-348">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-348">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-349">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-349">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-350">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-350">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-351">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-351">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-352">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-352">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-353">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-353">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-354">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-354">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-356">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-356">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-358">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-358">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-360">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-360">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-362">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-362">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-363">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-363">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-365">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-365">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-366">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-366">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-368">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-368">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-369">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-369">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-370">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-370">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-371">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-371">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-373">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-373">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a><span data-ttu-id="04ce8-374">DXGI_FORMAT_R32G32B32A32 \_ Saint-<sup>FCS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="04ce8-374">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FCS</sup> (4)</span></span>
| <span data-ttu-id="04ce8-375">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-375">Target</span></span> | <span data-ttu-id="04ce8-376">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-376">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-377">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-377">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-378">128</span><span class="sxs-lookup"><span data-stu-id="04ce8-378">128</span></span> |
| <span data-ttu-id="04ce8-379">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-379">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-381">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-381">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-383">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-383">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-385">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-385">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-386">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-386">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-388">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-388">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-390">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-390">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-392">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-392">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-394">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-396">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-396">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-398">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-398">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-399">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-399">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-400">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-400">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-401">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-401">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-402">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-402">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-403">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-403">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-405">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-405">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-406">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-406">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-408">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-409">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-410">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-411">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-412">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-413">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-414">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-415">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-417">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-419">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-420">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-421">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-422">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-422">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-424">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-424">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-426">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-426">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-428">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-428">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-430">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-430">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-431">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-431">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-433">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-433">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-434">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-434">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-436">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-437">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-438">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-439">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-439">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-441">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="04ce8-442">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32 type (5)</span><span class="sxs-lookup"><span data-stu-id="04ce8-442">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="04ce8-443">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-443">Target</span></span> | <span data-ttu-id="04ce8-444">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-444">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-445">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-446">96</span><span class="sxs-lookup"><span data-stu-id="04ce8-446">96</span></span> |
| <span data-ttu-id="04ce8-447">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-447">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-449">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-449">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-450">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-450">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-451">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-451">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-452">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-452">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-453">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-453">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-455">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-455">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-457">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-459">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-459">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-461">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-461">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-462">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-462">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-463">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-463">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-464">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-464">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-465">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-465">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-466">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-466">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-467">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-467">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-469">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-469">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-470">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-470">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-471">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-471">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-472">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-472">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-473">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-473">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-474">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-474">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-475">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-475">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-476">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-476">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-477">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-477">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-478">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-478">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-479">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-479">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-480">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-480">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-481">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-481">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-482">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-482">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-483">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-483">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-484">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-484">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-485">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-485">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-487">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-487">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-488">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-488">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-489">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-489">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-490">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-490">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-491">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-491">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-492">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-492">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-493">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-493">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-495">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-496">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-497">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-498">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-498">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-499">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a><span data-ttu-id="04ce8-500">DXGI_FORMAT_R32G32B32 \_ float<sup>FCS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="04ce8-500">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FCS</sup> (6)</span></span>
| <span data-ttu-id="04ce8-501">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-501">Target</span></span> | <span data-ttu-id="04ce8-502">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-502">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-503">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-504">96</span><span class="sxs-lookup"><span data-stu-id="04ce8-504">96</span></span> |
| <span data-ttu-id="04ce8-505">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-505">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-507">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-507">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-509">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-509">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-511">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-511">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-512">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-512">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-514">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-514">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-516">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-516">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-518">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-518">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-520">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-520">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-522">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-522">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-524">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-524">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-526">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-526">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-527">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-527">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-528">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-528">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-529">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-529">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-530">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-530">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-532">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-532">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-534">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-534">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-536">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-536">Blendable RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-538">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-538">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-539">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-539">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-540">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-540">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-541">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-541">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-542">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-542">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-543">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-543">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-544">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-544">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-545">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-545">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-546">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-546">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-547">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-547">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-548">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-548">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-549">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-549">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-550">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-550">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-551">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-551">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-553">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-553">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-555">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-555">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-557">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-557">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-559">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-559">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-561">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-561">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-563">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-563">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-564">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-564">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-566">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-566">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-567">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-567">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-568">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-568">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-569">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-569">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-570">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-570">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a><span data-ttu-id="04ce8-571">DXGI_FORMAT_R32G32B32 \_ uint<sup>FCS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="04ce8-571">DXGI_FORMAT_R32G32B32\_UINT<sup>FCS</sup> (7)</span></span>
| <span data-ttu-id="04ce8-572">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-572">Target</span></span> | <span data-ttu-id="04ce8-573">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-573">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-574">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-574">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-575">96</span><span class="sxs-lookup"><span data-stu-id="04ce8-575">96</span></span> |
| <span data-ttu-id="04ce8-576">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-576">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-578">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-578">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-580">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-580">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-582">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-582">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-583">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-583">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-585">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-585">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-587">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-589">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-591">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-591">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-593">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-593">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-595">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-595">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-596">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-596">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-597">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-597">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-598">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-598">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-599">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-600">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-600">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-602">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-602">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-603">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-603">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-605">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-605">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-606">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-606">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-608">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-608">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-609">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-609">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-610">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-610">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-611">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-611">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-612">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-612">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-613">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-613">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-614">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-614">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-615">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-615">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-616">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-616">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-617">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-617">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-618">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-618">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-619">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-619">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-620">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-620">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-622">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-622">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-624">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-624">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-626">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-626">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-628">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-628">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-629">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-629">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-631">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-631">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-632">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-632">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-634">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-634">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-635">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-635">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-636">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-636">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-637">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-637">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-638">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-638">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a><span data-ttu-id="04ce8-639">DXGI_FORMAT_R32G32B32 \_ Saint-<sup>FCS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="04ce8-639">DXGI_FORMAT_R32G32B32\_SINT<sup>FCS</sup> (8)</span></span>
| <span data-ttu-id="04ce8-640">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-640">Target</span></span> | <span data-ttu-id="04ce8-641">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-641">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-642">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-642">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-643">96</span><span class="sxs-lookup"><span data-stu-id="04ce8-643">96</span></span> |
| <span data-ttu-id="04ce8-644">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-644">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-646">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-646">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-648">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-648">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-650">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-650">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-651">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-651">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-653">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-655">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-657">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-659">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-661">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-661">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-663">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-664">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-665">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-666">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-666">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-667">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-668">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-668">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-670">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-670">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-671">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-671">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-673">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-673">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-674">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-675">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-676">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-677">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-678">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-678">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-679">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-680">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-682">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-683">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-684">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-685">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-686">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-687">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-687">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-689">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-689">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-691">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-691">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="04ce8-693">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-693">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-695">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-695">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-696">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-696">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-698">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-698">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-699">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-699">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-701">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-701">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-702">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-702">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-703">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-703">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-704">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-704">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-705">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-705">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="04ce8-706">\_<sup>PC</sup> DXGI_FORMAT_R16G16B16A16 type (9)</span><span class="sxs-lookup"><span data-stu-id="04ce8-706">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="04ce8-707">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-707">Target</span></span> | <span data-ttu-id="04ce8-708">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-708">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-709">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-709">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-710">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-710">64</span></span> |
| <span data-ttu-id="04ce8-711">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-711">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-713">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-713">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-714">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-714">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-715">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-715">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-716">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-716">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-717">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-717">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-719">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-719">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-721">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-721">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-723">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-723">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-725">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-725">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-726">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-726">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-727">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-727">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-728">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-728">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-729">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-729">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-730">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-730">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-731">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-731">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-733">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-733">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-734">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-734">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-735">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-735">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-736">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-736">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-737">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-737">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-738">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-738">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-739">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-739">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-740">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-740">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-741">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-741">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-742">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-742">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-743">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-743">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-744">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-744">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-745">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-745">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-746">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-746">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-747">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-747">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-748">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-748">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-749">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-749">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-751">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-751">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-752">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-752">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-753">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-753">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-754">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-754">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-755">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-755">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-756">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-756">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-757">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-757">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-759">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-759">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-760">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-760">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-761">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-761">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-762">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-762">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-764">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-764">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a><span data-ttu-id="04ce8-765">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FCS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="04ce8-765">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FCS</sup> (10)</span></span>
| <span data-ttu-id="04ce8-766">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-766">Target</span></span> | <span data-ttu-id="04ce8-767">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-767">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-768">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-768">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-769">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-769">64</span></span> |
| <span data-ttu-id="04ce8-770">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-770">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-772">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-772">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-774">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-774">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-776">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-776">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-777">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-777">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-778">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-778">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-780">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-780">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-782">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-782">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-784">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-786">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-786">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-788">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-788">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-790">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-790">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-791">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-791">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-792">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-792">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-793">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-793">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-794">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-794">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-796">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-796">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-798">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-798">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-800">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-800">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-802">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-802">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-803">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-803">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-804">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-804">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-805">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-805">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-806">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-806">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-807">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-807">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-808">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-808">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-809">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-809">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-810">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-810">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-811">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-811">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-812">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-812">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-813">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-813">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-814">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-814">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-815">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-815">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-817">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-817">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-819">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-819">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-821">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-821">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-823">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-823">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-825">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-825">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-827">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-827">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-829">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-829">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-831">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-831">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-832">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-832">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-834">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-834">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-836">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-836">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-838">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-838">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a><span data-ttu-id="04ce8-839">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FCS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="04ce8-839">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FCS</sup> (11)</span></span>
| <span data-ttu-id="04ce8-840">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-840">Target</span></span> | <span data-ttu-id="04ce8-841">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-841">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-842">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-842">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-843">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-843">64</span></span> |
| <span data-ttu-id="04ce8-844">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-844">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-846">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-846">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-848">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-848">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-850">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-850">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-851">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-851">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-852">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-852">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-854">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-854">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-856">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-856">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-858">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-858">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-860">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-860">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-862">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-862">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-864">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-864">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-865">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-865">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-866">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-866">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-867">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-867">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-868">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-868">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-870">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-870">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-872">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-872">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-874">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-874">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-876">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-877">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-878">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-879">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-880">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-880">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-881">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-882">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-884">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-885">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-886">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-887">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-888">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-889">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-889">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-891">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-891">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-893">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-893">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-895">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-895">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-897">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-897">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-899">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-899">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-901">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-901">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-902">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-902">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-904">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-905">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-906">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-907">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-907">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-909">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-909">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a><span data-ttu-id="04ce8-910">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FCS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="04ce8-910">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FCS</sup> (12)</span></span>
| <span data-ttu-id="04ce8-911">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-911">Target</span></span> | <span data-ttu-id="04ce8-912">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-912">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-913">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-913">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-914">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-914">64</span></span> |
| <span data-ttu-id="04ce8-915">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-915">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-917">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-917">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-919">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-919">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-921">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-921">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-922">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-922">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-923">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-923">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-925">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-925">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-927">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-927">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-929">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-929">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-931">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-931">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-933">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-933">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-934">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-934">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-935">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-935">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-936">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-936">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-937">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-937">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-938">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-938">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-940">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-940">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-941">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-941">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-943">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-943">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-944">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-944">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-946">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-946">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-947">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-947">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-948">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-948">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-949">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-949">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-950">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-950">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-951">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-951">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-952">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-952">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-953">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-953">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-954">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-954">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-955">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-955">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-956">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-956">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-957">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-957">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-958">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-958">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-960">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-960">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-962">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-962">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-964">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-964">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-966">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-966">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-967">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-967">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-969">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-969">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-970">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-970">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-972">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-972">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-973">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-973">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-974">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-974">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-975">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-975">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-977">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-977">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a><span data-ttu-id="04ce8-978">DXGI_FORMAT_R16G16B16A16 \_ ronfler<sup>FCS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="04ce8-978">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FCS</sup> (13)</span></span>
| <span data-ttu-id="04ce8-979">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-979">Target</span></span> | <span data-ttu-id="04ce8-980">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-980">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-981">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-981">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-982">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-982">64</span></span> |
| <span data-ttu-id="04ce8-983">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-983">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-985">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-985">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-987">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-987">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-989">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-990">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-991">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-993">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-993">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-995">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-995">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-997">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-997">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-999">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-999">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1001">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1001">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1003">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1003">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1004">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1004">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1005">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1005">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1006">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1006">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1007">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1007">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1009">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1009">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1011">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1011">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1013">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1013">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1015">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1015">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1016">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1016">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1017">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1017">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1018">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1018">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1019">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1019">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1020">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1020">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1021">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1021">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1022">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1022">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1023">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1023">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1024">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1024">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1025">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1025">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1026">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1026">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1027">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1027">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1028">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1028">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1030">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1030">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1032">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1032">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1034">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1034">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1036">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1036">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1038">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1038">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1040">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1040">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1041">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1041">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1043">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1043">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1044">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1044">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1045">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1045">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1046">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1046">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1048">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1048">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a><span data-ttu-id="04ce8-1049">DXGI_FORMAT_R16G16B16A16 \_ Saint-<sup>FCS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1049">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FCS</sup> (14)</span></span>
| <span data-ttu-id="04ce8-1050">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1050">Target</span></span> | <span data-ttu-id="04ce8-1051">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1051">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1052">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1052">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1053">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1053">64</span></span> |
| <span data-ttu-id="04ce8-1054">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1054">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1056">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1056">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1058">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1058">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1060">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1060">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1061">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1061">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1062">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1062">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1064">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1064">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1066">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1066">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1068">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1068">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1070">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1070">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1072">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1072">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1073">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1073">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1074">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1074">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1075">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1075">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1076">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1076">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1077">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1077">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1079">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1079">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1080">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1080">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1082">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1082">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1083">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1083">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1084">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1084">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1085">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1085">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1086">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1086">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1087">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1087">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1088">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1088">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1089">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1089">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1090">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1090">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1091">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1091">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1092">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1092">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1093">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1093">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1094">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1094">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1095">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1095">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1096">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1096">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1098">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1098">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1100">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1100">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1102">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1102">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1104">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1104">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1105">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1105">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1107">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1107">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1108">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1108">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1110">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1111">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1112">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1113">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1113">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1115">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1115">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="04ce8-1116">\_<sup>PC</sup> DXGI_FORMAT_R32G32 type (15)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1116">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="04ce8-1117">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1117">Target</span></span> | <span data-ttu-id="04ce8-1118">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1118">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1119">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1119">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1120">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1120">64</span></span> |
| <span data-ttu-id="04ce8-1121">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1121">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1123">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1123">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1124">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1124">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1125">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1125">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1126">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1126">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1127">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1127">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1129">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1131">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1131">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1133">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1133">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1135">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1135">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-1136">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1137">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1138">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1139">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1139">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1140">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1141">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1141">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1143">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1143">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1144">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1144">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1145">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1145">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1146">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1146">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1147">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1147">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1148">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1148">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1149">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1149">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1150">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1150">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1151">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1151">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1152">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1152">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1153">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1153">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1154">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1154">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1155">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1155">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1156">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1156">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1157">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1157">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1158">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1158">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1159">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1159">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1161">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1161">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1162">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1162">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1163">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1163">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1164">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1164">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1165">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1165">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-1166">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1166">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1167">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1167">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1169">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1169">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1170">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1170">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1171">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1171">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1172">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1172">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1173">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1173">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a><span data-ttu-id="04ce8-1174">DXGI_FORMAT_R32G32 \_ float<sup>FCS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1174">DXGI_FORMAT_R32G32\_FLOAT<sup>FCS</sup> (16)</span></span>
| <span data-ttu-id="04ce8-1175">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1175">Target</span></span> | <span data-ttu-id="04ce8-1176">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1176">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1177">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1177">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1178">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1178">64</span></span> |
| <span data-ttu-id="04ce8-1179">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1179">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1181">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1181">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1183">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1183">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1185">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1185">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1186">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1186">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1188">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1188">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1190">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1190">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1192">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1192">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1194">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1194">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1196">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1196">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1198">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1198">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1200">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1201">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1202">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1202">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1203">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1204">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1204">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1206">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1206">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1208">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1208">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1210">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1210">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1212">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1212">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1213">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1213">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1214">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1214">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1215">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1215">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1216">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1216">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1217">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1217">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1218">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1218">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1219">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1219">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1220">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1220">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1221">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1221">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1222">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1222">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1223">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1223">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1224">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1224">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1225">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1225">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1227">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1227">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1229">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1229">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1231">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1231">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1233">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1233">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1235">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1235">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1237">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1237">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1238">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1238">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1240">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1240">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1241">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1241">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1242">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1242">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1243">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1243">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1244">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1244">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a><span data-ttu-id="04ce8-1245">DXGI_FORMAT_R32G32 \_ uint<sup>FCS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1245">DXGI_FORMAT_R32G32\_UINT<sup>FCS</sup> (17)</span></span>
| <span data-ttu-id="04ce8-1246">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1246">Target</span></span> | <span data-ttu-id="04ce8-1247">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1247">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1248">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1248">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1249">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1249">64</span></span> |
| <span data-ttu-id="04ce8-1250">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1250">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1252">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1252">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1254">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1254">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1256">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1256">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1257">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1257">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1259">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1259">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1261">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1261">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1263">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1263">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1265">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1265">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1267">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1267">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1269">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1269">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1270">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1270">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1271">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1271">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1272">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1272">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1273">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1273">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1274">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1274">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1276">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1276">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1277">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1277">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1279">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1279">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1280">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1280">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1282">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1283">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1284">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1285">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1285">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1286">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1287">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1289">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1290">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1291">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1292">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1293">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1294">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1294">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1296">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1296">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1298">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1298">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1300">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1300">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1302">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1302">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1303">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1303">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1305">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1305">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1306">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1306">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1308">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1308">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1309">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1309">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1310">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1310">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1311">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1311">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1312">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1312">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a><span data-ttu-id="04ce8-1313">DXGI_FORMAT_R32G32 \_ Saint-<sup>FCS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1313">DXGI_FORMAT_R32G32\_SINT<sup>FCS</sup> (18)</span></span>
| <span data-ttu-id="04ce8-1314">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1314">Target</span></span> | <span data-ttu-id="04ce8-1315">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1315">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1316">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1316">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1317">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1317">64</span></span> |
| <span data-ttu-id="04ce8-1318">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1318">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1320">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1320">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1322">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1322">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1324">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1324">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1325">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1325">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1327">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1327">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1329">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1329">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1331">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1331">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1333">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1333">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1335">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1335">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1337">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1337">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1338">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1338">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1339">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1339">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1340">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1340">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1341">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1341">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1342">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1342">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1344">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1344">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1345">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1345">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1347">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1347">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1348">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1348">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1349">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1349">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1350">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1350">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1351">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1351">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1352">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1352">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1353">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1353">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1354">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1354">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1355">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1355">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1356">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1356">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1357">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1357">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1358">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1358">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1359">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1359">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1360">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1360">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1361">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1361">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1363">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1363">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1365">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1365">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1367">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1367">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1369">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1369">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1370">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1370">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1372">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1373">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1373">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1375">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1375">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1376">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1376">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1377">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1377">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1378">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1378">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1379">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1379">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="04ce8-1380">\_<sup>PC</sup> DXGI_FORMAT_R32G8X24 type (19)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1380">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="04ce8-1381">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1381">Target</span></span> | <span data-ttu-id="04ce8-1382">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1382">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1383">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1383">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1384">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1384">64</span></span> |
| <span data-ttu-id="04ce8-1385">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1385">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1387">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1387">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1388">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1389">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1390">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1391">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1393">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1393">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1395">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1395">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-1396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1396">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1398">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1398">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-1399">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1399">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1400">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1400">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1401">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1401">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1402">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1402">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1403">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1403">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1404">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1404">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1406">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1407">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1408">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1409">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1410">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1411">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1412">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1413">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1413">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1414">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1415">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1417">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1418">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1419">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1420">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1421">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1422">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1422">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1424">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1424">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1425">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1425">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1426">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1426">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1427">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1427">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1428">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1428">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-1429">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1429">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1430">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1430">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1432">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1432">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1433">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1433">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1434">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1434">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1435">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1435">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1436">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1436">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a><span data-ttu-id="04ce8-1437">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FCS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1437">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FCS</sup> (20)</span></span>
| <span data-ttu-id="04ce8-1438">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1438">Target</span></span> | <span data-ttu-id="04ce8-1439">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1439">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1440">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1440">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1441">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1441">64</span></span> |
| <span data-ttu-id="04ce8-1442">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1442">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1444">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1444">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1445">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1445">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1446">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1446">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1447">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1447">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1448">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1448">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1450">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1450">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1452">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1452">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-1453">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1453">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1455">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1455">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-1456">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1456">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1457">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1457">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1458">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1458">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1459">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1459">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1460">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1460">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1461">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1461">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1463">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1465">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1466">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1467">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1467">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1469">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1469">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1470">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1470">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1471">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1471">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1472">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1472">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1473">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1473">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1474">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1474">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1475">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1475">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1476">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1476">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1477">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1477">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1478">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1478">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1479">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1479">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1480">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1480">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1482">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1482">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1484">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1484">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1486">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1486">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1488">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1488">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1489">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1489">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-1490">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1490">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1491">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1491">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1493">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1493">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1494">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1494">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1495">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1495">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1496">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1496">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1497">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1497">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a><span data-ttu-id="04ce8-1498">DXGI_FORMAT_R32 \_ \_ FCS X8X24 float \_ (<sup></sup> 21)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1498">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FCS</sup> (21)</span></span>
| <span data-ttu-id="04ce8-1499">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1499">Target</span></span> | <span data-ttu-id="04ce8-1500">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1500">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1501">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1501">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1502">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1502">64</span></span> |
| <span data-ttu-id="04ce8-1503">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1503">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1505">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1505">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1506">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1506">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1507">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1507">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1508">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1508">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1509">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1509">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1511">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1513">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1513">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-1514">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1514">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1516">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1516">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1518">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1518">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1520">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1520">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1522">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1522">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1523">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1523">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1525">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1525">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1526">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1526">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1528">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1528">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1529">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1529">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1530">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1530">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1531">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1531">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1532">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1532">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1533">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1533">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1534">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1534">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1535">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1535">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1536">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1536">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1537">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1537">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1538">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1538">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1539">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1539">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1540">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1540">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1541">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1541">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1542">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1542">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1543">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1543">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1544">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1544">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1546">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1546">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1547">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1547">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1548">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1548">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1549">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1549">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1550">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1550">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1552">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1552">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1553">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1553">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1555">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1555">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1556">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1556">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1557">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1557">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1558">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1558">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1559">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1559">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a><span data-ttu-id="04ce8-1560">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FCS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1560">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FCS</sup> (22)</span></span>
| <span data-ttu-id="04ce8-1561">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1561">Target</span></span> | <span data-ttu-id="04ce8-1562">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1562">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1563">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1563">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1564">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-1564">64</span></span> |
| <span data-ttu-id="04ce8-1565">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1565">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1567">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1567">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1568">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1568">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1569">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1569">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1570">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1570">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1571">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1571">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1573">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1573">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1575">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1575">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-1576">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1576">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1578">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1578">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1580">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1580">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1581">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1581">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1582">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1582">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1583">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1583">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1584">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1584">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1585">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1585">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1587">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1587">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1588">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1588">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1589">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1590">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1590">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1591">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1591">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1592">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1592">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1593">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1593">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1594">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1594">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1595">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1595">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1596">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1596">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1597">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1597">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1598">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1598">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1599">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1599">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1600">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1600">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1601">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1601">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1602">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1602">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1603">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1603">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1605">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1605">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1606">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1606">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1607">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1607">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1608">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1608">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1609">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1609">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1611">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1611">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1612">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1612">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1614">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1614">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1615">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1615">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1616">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1616">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1617">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1617">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1618">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1618">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="04ce8-1619">\_<sup>PC</sup> DXGI_FORMAT_R10G10B10A2 type (23)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1619">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="04ce8-1620">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1620">Target</span></span> | <span data-ttu-id="04ce8-1621">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1621">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1622">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1622">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1623">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-1623">32</span></span> |
| <span data-ttu-id="04ce8-1624">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1624">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1626">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1626">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1627">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1627">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1628">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1628">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1629">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1629">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1630">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1630">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1632">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1632">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1634">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1634">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1636">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1636">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1638">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1638">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-1639">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1639">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1640">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1640">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1641">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1641">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1642">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1642">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1643">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1643">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1644">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1644">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1646">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1646">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1647">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1647">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1648">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1648">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1649">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1649">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1650">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1650">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1651">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1651">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1652">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1652">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1653">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1653">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1654">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1654">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1655">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1655">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1656">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1656">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1657">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1657">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1658">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1658">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1659">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1659">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1660">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1660">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1661">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1661">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1662">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1662">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1664">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1664">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1665">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1665">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1666">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1666">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1667">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1667">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1668">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1668">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-1669">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1669">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1670">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1670">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1672">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1672">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1673">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1673">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1674">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1674">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1675">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1675">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1677">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1677">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a><span data-ttu-id="04ce8-1678">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FCS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1678">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FCS</sup> (24)</span></span>
| <span data-ttu-id="04ce8-1679">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1679">Target</span></span> | <span data-ttu-id="04ce8-1680">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1680">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1681">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1681">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1682">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-1682">32</span></span> |
| <span data-ttu-id="04ce8-1683">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1683">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1685">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1685">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1687">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1687">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1689">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1689">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1690">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1690">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1691">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1691">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1693">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1693">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1695">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1695">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1697">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1697">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1699">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1699">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1701">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1701">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1703">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1703">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1704">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1704">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1705">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1705">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1706">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1706">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1707">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1707">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1709">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1709">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1711">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1711">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1713">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1713">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1715">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1715">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1716">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1716">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1717">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1717">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1718">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1718">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1719">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1719">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1720">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1720">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1721">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1721">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1722">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1722">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1723">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1723">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1724">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1724">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1725">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1725">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1726">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1726">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1727">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1727">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1728">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1728">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1730">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1730">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1732">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1732">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1734">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1734">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1736">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1736">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1738">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1738">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1740">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1740">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1742">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1742">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1744">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1744">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1745">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1745">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1747">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1747">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1749">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1749">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1751">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a><span data-ttu-id="04ce8-1752">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FCS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1752">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FCS</sup> (25)</span></span>
| <span data-ttu-id="04ce8-1753">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1753">Target</span></span> | <span data-ttu-id="04ce8-1754">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1754">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1755">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1756">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-1756">32</span></span> |
| <span data-ttu-id="04ce8-1757">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1757">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1759">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1759">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1761">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1761">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1763">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1763">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1764">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1764">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1765">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1765">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1767">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1769">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1771">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1771">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1773">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1773">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1775">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1776">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1777">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1778">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1778">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1779">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1780">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1780">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1782">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1782">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1783">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1783">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1785">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1785">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1786">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1786">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1788">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1788">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1789">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1789">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1790">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1790">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1791">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1791">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1792">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1792">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1793">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1793">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1794">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1794">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1795">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1795">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1796">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1796">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1797">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1797">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1798">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1798">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1799">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1799">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1800">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1800">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1802">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1802">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1804">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1804">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1806">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1806">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1808">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1808">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1809">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1809">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1811">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1811">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1812">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1812">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1814">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1814">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1815">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1815">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1816">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1816">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1817">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1817">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1819">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1819">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a><span data-ttu-id="04ce8-1820">DXGI_FORMAT_R10G10B10 \_ XR de \_ décalage \_ a2 \_ UNORM<sup>FCS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1820">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FCS</sup> (89)</span></span>
| <span data-ttu-id="04ce8-1821">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1821">Target</span></span> | <span data-ttu-id="04ce8-1822">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1822">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1823">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1823">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1824">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-1824">32</span></span> |
| <span data-ttu-id="04ce8-1825">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1825">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1827">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1827">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1828">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1828">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1829">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1829">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1830">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1830">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1831">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1831">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-1832">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1832">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1834">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1834">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-1835">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1835">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-1836">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1836">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-1837">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1838">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1839">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1840">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1840">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1841">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1842">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1842">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-1843">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1843">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1844">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1844">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1845">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1845">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1846">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1846">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1847">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1847">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1848">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1848">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1849">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1849">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1850">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1850">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1851">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1851">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1852">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1852">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1853">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1853">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1854">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1854">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1855">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1855">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1856">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1856">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1857">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1857">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1858">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1858">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1859">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1859">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1861">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1861">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1862">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1862">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1863">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1863">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1864">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1864">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1865">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1865">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-1866">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1866">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1868">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1868">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1870">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1870">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1871">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1871">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1873">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1873">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1875">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1875">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1877">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1877">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="04ce8-1878">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1878">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="04ce8-1879">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1879">Target</span></span> | <span data-ttu-id="04ce8-1880">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1880">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1881">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1881">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1882">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-1882">32</span></span> |
| <span data-ttu-id="04ce8-1883">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1883">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1885">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1885">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1887">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1887">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1889">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1889">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1890">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1890">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1891">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1891">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1893">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1893">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1895">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1895">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1897">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1897">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1899">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1899">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1901">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1901">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1903">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1903">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1904">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1904">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1905">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1905">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1906">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1906">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1907">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1907">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1909">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1909">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1911">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1911">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1913">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1913">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1915">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1915">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1916">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1916">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1917">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1917">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1918">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1918">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1919">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1919">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1920">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1920">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1921">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1921">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1922">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1922">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1923">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1923">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1924">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1924">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1925">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1925">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1926">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1926">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1927">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1927">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1928">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1928">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1930">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1930">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1932">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1932">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1934">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1934">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-1936">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1936">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1938">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1938">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1940">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1940">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1941">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1941">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-1942">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1942">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-1943">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1943">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-1944">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-1944">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-1945">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1945">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-1946">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-1946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="04ce8-1947">\_<sup>PC</sup> DXGI_FORMAT_R8G8B8A8 type (27)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1947">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="04ce8-1948">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-1948">Target</span></span> | <span data-ttu-id="04ce8-1949">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-1949">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-1950">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-1951">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-1951">32</span></span> |
| <span data-ttu-id="04ce8-1952">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-1952">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1954">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-1954">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1955">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1956">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-1956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1957">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-1957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-1958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1958">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1960">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-1962">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-1964">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1966">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-1966">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-1967">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1968">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1969">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-1969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-1970">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-1970">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-1971">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-1971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-1972">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-1972">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1974">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-1974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-1975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1975">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1976">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1977">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-1977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-1978">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-1978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-1979">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-1979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1980">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-1980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-1981">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-1981">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-1982">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-1983">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-1984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-1984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-1985">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-1986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-1986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-1987">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-1988">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-1988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1989">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-1989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-1990">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-1990">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-1992">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-1992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1993">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-1993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-1994">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-1994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-1995">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-1995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-1996">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-1996">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-1997">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-1997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-1998">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-1998">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2000">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2001">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2002">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2003">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2003">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2005">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a><span data-ttu-id="04ce8-2006">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FCS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2006">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FCS</sup> (28)</span></span>
| <span data-ttu-id="04ce8-2007">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2007">Target</span></span> | <span data-ttu-id="04ce8-2008">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2008">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2009">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2010">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2010">32</span></span> |
| <span data-ttu-id="04ce8-2011">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2011">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2013">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2013">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2015">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2015">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2017">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2018">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2019">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2021">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2023">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2025">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2027">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2027">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2029">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2029">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2031">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2032">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2033">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2033">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2034">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2035">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2035">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2037">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2037">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2039">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2041">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2041">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2043">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2044">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2045">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2046">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2047">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2047">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2048">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2049">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2051">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2053">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2054">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2055">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2056">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2056">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2058">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2058">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2060">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2060">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2062">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2062">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2064">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2064">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2066">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2066">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2068">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2068">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2070">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2070">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2072">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2072">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2073">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2073">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2075">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2075">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2077">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2077">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2079">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2079">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a><span data-ttu-id="04ce8-2080">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRVB<sup>FCS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2080">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FCS</sup> (29)</span></span>
| <span data-ttu-id="04ce8-2081">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2081">Target</span></span> | <span data-ttu-id="04ce8-2082">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2082">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2083">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2083">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2084">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2084">32</span></span> |
| <span data-ttu-id="04ce8-2085">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2085">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2087">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2087">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2088">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2088">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2089">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2089">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2090">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2090">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2091">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2091">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2093">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2093">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2095">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2095">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2097">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2097">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2099">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2099">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2101">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2101">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2103">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2103">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2104">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2104">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2105">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2105">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2106">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2106">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2107">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2107">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2109">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2109">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2111">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2111">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2113">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2113">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2115">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2116">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2117">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2118">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2119">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2119">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2120">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2121">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2122">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2123">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2124">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2125">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2126">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2127">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2128">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2128">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2130">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2130">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2132">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2132">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2134">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2134">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2136">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2136">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2138">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2138">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2140">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2140">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2142">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2142">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2144">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2145">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2145">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2147">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2147">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2149">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2149">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2151">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2151">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a><span data-ttu-id="04ce8-2152">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FCS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2152">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FCS</sup> (30)</span></span>
| <span data-ttu-id="04ce8-2153">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2153">Target</span></span> | <span data-ttu-id="04ce8-2154">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2154">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2155">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2155">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2156">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2156">32</span></span> |
| <span data-ttu-id="04ce8-2157">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2157">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2159">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2159">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2161">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2161">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2163">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2163">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2164">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2164">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2165">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2165">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2167">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2167">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2169">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2169">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2171">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2171">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2173">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2173">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2175">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2175">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2176">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2176">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2177">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2177">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2178">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2178">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2179">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2179">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2180">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2180">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2182">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2182">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2183">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2183">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2185">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2185">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2186">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2186">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2188">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2188">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2189">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2189">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2190">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2190">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2191">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2191">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2192">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2192">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2193">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2193">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2194">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2194">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2195">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2195">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2196">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2196">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2197">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2197">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2198">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2198">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2199">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2199">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2200">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2200">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2202">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2202">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2204">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2204">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2206">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2206">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2208">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2208">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2209">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2209">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2211">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2211">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2212">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2212">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2214">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2214">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2215">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2215">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2216">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2216">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2217">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2217">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2219">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2219">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a><span data-ttu-id="04ce8-2220">DXGI_FORMAT_R8G8B8A8 \_ ronfler<sup>FCS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2220">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FCS</sup> (31)</span></span>
| <span data-ttu-id="04ce8-2221">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2221">Target</span></span> | <span data-ttu-id="04ce8-2222">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2222">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2223">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2223">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2224">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2224">32</span></span> |
| <span data-ttu-id="04ce8-2225">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2225">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2227">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2227">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2229">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2229">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2231">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2232">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2233">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2235">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2235">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2237">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2237">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2239">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2239">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2241">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2241">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2243">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2243">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2245">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2246">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2247">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2248">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2249">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2249">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2251">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2251">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2253">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2255">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2255">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2257">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2257">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2258">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2258">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2259">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2259">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2260">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2260">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2261">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2261">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2262">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2262">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2263">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2263">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2264">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2264">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2265">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2265">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2266">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2266">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2267">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2267">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2268">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2268">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2269">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2269">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2270">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2270">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2272">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2272">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2274">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2274">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2276">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2276">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2278">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2278">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2280">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2280">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2282">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2282">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2283">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2283">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2285">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2285">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2286">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2286">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2287">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2287">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2288">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2288">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2290">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a><span data-ttu-id="04ce8-2291">DXGI_FORMAT_R8G8B8A8 \_ Saint-<sup>FCS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2291">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FCS</sup> (32)</span></span>
| <span data-ttu-id="04ce8-2292">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2292">Target</span></span> | <span data-ttu-id="04ce8-2293">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2293">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2294">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2295">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2295">32</span></span> |
| <span data-ttu-id="04ce8-2296">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2296">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2298">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2298">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2300">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2300">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2302">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2302">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2303">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2303">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2304">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2304">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2306">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2306">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2308">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2308">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2310">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2310">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2312">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2312">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2314">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2314">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2315">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2315">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2316">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2316">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2317">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2317">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2318">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2318">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2319">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2319">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2321">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2321">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2322">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2322">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2324">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2324">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2325">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2325">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2326">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2326">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2327">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2327">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2328">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2328">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2329">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2329">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2330">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2330">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2331">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2331">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2332">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2332">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2333">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2333">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2334">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2334">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2335">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2335">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2336">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2336">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2337">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2337">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2338">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2338">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2340">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2340">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2342">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2342">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2344">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2344">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2346">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2346">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2347">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2347">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2349">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2349">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2350">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2350">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2352">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2352">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2353">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2353">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2354">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2354">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2355">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2355">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2357">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2357">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="04ce8-2358">\_<sup>PC</sup> DXGI_FORMAT_R16G16 type (33)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2358">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="04ce8-2359">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2359">Target</span></span> | <span data-ttu-id="04ce8-2360">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2360">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2361">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2361">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2362">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2362">32</span></span> |
| <span data-ttu-id="04ce8-2363">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2363">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2365">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2365">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2366">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2366">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2367">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2367">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2368">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2368">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2369">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2369">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2371">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2371">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2373">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2373">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2375">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2375">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2377">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2377">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-2378">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2378">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2379">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2379">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2380">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2380">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2381">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2381">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2382">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2382">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2383">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2383">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2385">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2385">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2386">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2386">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2387">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2387">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2388">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2388">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2389">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2389">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2390">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2390">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2391">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2391">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2392">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2392">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2393">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2393">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2394">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2394">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2395">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2395">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2396">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2396">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2397">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2397">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2398">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2398">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2399">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2399">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2400">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2400">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2401">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2401">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2403">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2403">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2404">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2404">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2405">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2405">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-2406">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2406">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2407">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2407">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-2408">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2408">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2409">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2409">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2411">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2411">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2412">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2412">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2413">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2413">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2414">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2414">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-2415">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2415">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a><span data-ttu-id="04ce8-2416">DXGI_FORMAT_R16G16 \_ float<sup>FCS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2416">DXGI_FORMAT_R16G16\_FLOAT<sup>FCS</sup> (34)</span></span>
| <span data-ttu-id="04ce8-2417">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2417">Target</span></span> | <span data-ttu-id="04ce8-2418">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2418">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2419">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2419">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2420">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2420">32</span></span> |
| <span data-ttu-id="04ce8-2421">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2421">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2423">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2423">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2425">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2425">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2427">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2427">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2428">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2428">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2429">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2429">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2431">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2431">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2433">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2433">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2435">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2435">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2437">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2437">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2439">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2439">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2441">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2442">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2443">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2443">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2444">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2445">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2445">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2447">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2447">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2449">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2449">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2451">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2451">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2453">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2453">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2454">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2454">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2455">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2455">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2456">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2456">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2457">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2457">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2458">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2458">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2459">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2459">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2460">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2460">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2461">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2461">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2462">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2462">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2463">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2463">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2464">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2464">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2465">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2465">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2466">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2466">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2468">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2468">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2470">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2470">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2472">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2472">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2474">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2474">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2476">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2476">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2478">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2479">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2479">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2481">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2482">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2483">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2484">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2484">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-2485">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a><span data-ttu-id="04ce8-2486">DXGI_FORMAT_R16G16 \_ UNORM<sup>FCS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2486">DXGI_FORMAT_R16G16\_UNORM<sup>FCS</sup> (35)</span></span>
| <span data-ttu-id="04ce8-2487">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2487">Target</span></span> | <span data-ttu-id="04ce8-2488">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2488">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2489">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2490">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2490">32</span></span> |
| <span data-ttu-id="04ce8-2491">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2491">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2493">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2493">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2495">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2495">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2497">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2497">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2498">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2498">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2499">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2499">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2501">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2503">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2503">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2505">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2507">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2507">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2509">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2509">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2511">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2512">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2513">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2514">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2515">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2515">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2517">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2517">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2519">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2519">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2521">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2521">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2523">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2523">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2524">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2524">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2525">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2525">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2526">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2526">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2527">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2527">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2528">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2528">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2529">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2529">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2530">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2530">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2531">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2531">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2532">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2532">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2533">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2533">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2534">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2534">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2535">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2535">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2536">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2536">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2538">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2538">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2540">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2540">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2542">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2542">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2544">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2544">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2546">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2546">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2548">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2548">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2549">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2549">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2551">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2551">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2552">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2552">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2553">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2553">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2554">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2554">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-2555">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2555">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a><span data-ttu-id="04ce8-2556">DXGI_FORMAT_R16G16 \_ uint<sup>FCS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2556">DXGI_FORMAT_R16G16\_UINT<sup>FCS</sup> (36)</span></span>
| <span data-ttu-id="04ce8-2557">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2557">Target</span></span> | <span data-ttu-id="04ce8-2558">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2558">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2559">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2559">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2560">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2560">32</span></span> |
| <span data-ttu-id="04ce8-2561">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2561">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2563">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2563">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2565">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2565">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2567">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2567">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2568">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2568">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2569">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2569">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2571">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2571">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2573">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2573">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2575">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2575">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2577">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2577">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2579">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2579">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2580">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2580">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2581">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2581">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2582">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2582">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2583">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2583">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2584">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2584">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2586">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2586">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2587">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2587">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2589">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2589">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2590">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2590">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2592">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2592">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2593">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2593">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2594">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2594">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2595">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2595">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2596">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2596">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2597">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2597">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2598">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2598">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2599">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2599">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2600">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2600">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2601">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2601">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2602">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2602">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2603">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2603">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2604">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2604">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2606">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2606">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2608">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2608">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2610">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2610">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2612">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2612">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2613">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2613">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2615">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2615">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2616">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2616">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2618">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2618">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2619">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2619">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2620">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2620">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2621">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2621">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-2622">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2622">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a><span data-ttu-id="04ce8-2623">DXGI_FORMAT_R16G16 \_ ronfler<sup>FCS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2623">DXGI_FORMAT_R16G16\_SNORM<sup>FCS</sup> (37)</span></span>
| <span data-ttu-id="04ce8-2624">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2624">Target</span></span> | <span data-ttu-id="04ce8-2625">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2625">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2626">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2626">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2627">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2627">32</span></span> |
| <span data-ttu-id="04ce8-2628">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2628">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2630">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2630">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2632">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2632">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2634">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2634">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2635">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2635">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2636">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2636">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2638">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2638">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2640">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2640">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2642">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2642">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2644">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2644">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2646">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2646">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2648">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2648">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2649">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2649">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2650">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2650">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2651">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2651">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2652">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2652">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2654">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2654">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2656">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2656">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2658">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2658">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2660">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2660">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2661">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2661">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2662">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2662">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2663">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2663">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2664">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2664">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2665">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2665">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2666">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2666">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2667">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2667">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2668">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2668">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2669">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2669">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2670">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2670">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2671">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2671">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2672">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2672">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2673">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2673">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2675">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2675">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2677">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2677">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2679">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2679">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2681">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2681">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2683">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2683">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2685">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2685">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2686">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2686">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2688">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2688">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2689">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2689">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2690">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2690">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2691">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2691">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-2692">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2692">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a><span data-ttu-id="04ce8-2693">DXGI_FORMAT_R16G16 \_ Saint-<sup>FCS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2693">DXGI_FORMAT_R16G16\_SINT<sup>FCS</sup> (38)</span></span>
| <span data-ttu-id="04ce8-2694">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2694">Target</span></span> | <span data-ttu-id="04ce8-2695">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2695">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2696">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2696">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2697">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2697">32</span></span> |
| <span data-ttu-id="04ce8-2698">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2698">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2700">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2700">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2702">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2702">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2704">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2705">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2706">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2708">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2708">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2710">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2710">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2712">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2712">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2714">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2714">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2716">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2717">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2718">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2719">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2720">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2721">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2721">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2723">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2724">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2726">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2726">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2727">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2727">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2728">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2728">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2729">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2729">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2730">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2730">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2731">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2731">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2732">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2732">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2733">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2733">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2734">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2734">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2735">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2735">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2736">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2736">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2737">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2737">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2738">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2738">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2739">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2739">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2740">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2740">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2742">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2742">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2744">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2744">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2746">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2746">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2748">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2748">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2749">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2749">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2751">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2751">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2752">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2752">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2754">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2754">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2755">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2755">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2756">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2756">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2757">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2757">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-2758">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2758">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="04ce8-2759">\_<sup>PC</sup> DXGI_FORMAT_R32 type (39)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2759">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="04ce8-2760">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2760">Target</span></span> | <span data-ttu-id="04ce8-2761">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2761">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2762">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2762">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2763">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2763">32</span></span> |
| <span data-ttu-id="04ce8-2764">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2764">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2766">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2766">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2767">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2767">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2768">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2768">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2769">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2769">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2770">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2770">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2772">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2772">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2774">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2774">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2776">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2776">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2778">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2778">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-2779">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2779">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2780">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2780">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2781">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2781">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2782">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2782">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2783">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2783">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2784">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2784">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2786">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2786">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2787">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2787">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2788">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2788">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2789">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2789">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2790">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2790">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2791">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2791">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2792">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2792">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2793">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2793">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2794">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2794">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2795">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2795">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2796">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2796">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2797">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2797">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2798">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2798">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2799">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2799">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2800">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2800">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2801">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2801">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2802">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2802">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2804">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2804">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2805">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2805">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2806">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2806">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-2807">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2807">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2808">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2808">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-2809">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2809">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2810">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2810">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2812">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2812">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2813">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2813">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2814">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2814">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2815">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2815">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2817">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2817">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a><span data-ttu-id="04ce8-2818">DXGI_FORMAT_D32 \_ float<sup>FCS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2818">DXGI_FORMAT_D32\_FLOAT<sup>FCS</sup> (40)</span></span>
| <span data-ttu-id="04ce8-2819">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2819">Target</span></span> | <span data-ttu-id="04ce8-2820">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2820">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2821">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2821">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2822">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2822">32</span></span> |
| <span data-ttu-id="04ce8-2823">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2823">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2825">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2825">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2826">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2826">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2827">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2827">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2828">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2828">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2829">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2829">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2831">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2831">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2833">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2833">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-2834">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2834">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2836">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2836">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-2837">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2837">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2838">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2838">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2839">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2839">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2840">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2840">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2841">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2841">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2842">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2842">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2844">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2844">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2845">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2845">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2846">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2846">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2847">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2847">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2848">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2848">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2850">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2850">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2851">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2851">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2852">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2852">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2853">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2853">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2854">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2854">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2855">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2855">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2856">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2856">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2857">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2857">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2858">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2858">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2859">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2859">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2860">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2860">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2861">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2861">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2863">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2863">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2865">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2865">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2867">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2867">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2869">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2869">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-2870">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2870">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-2871">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2871">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2872">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2872">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2874">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2874">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2875">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2875">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2876">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2876">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2877">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2877">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2879">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2879">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a><span data-ttu-id="04ce8-2880">DXGI_FORMAT_R32 \_ float<sup>FCS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2880">DXGI_FORMAT_R32\_FLOAT<sup>FCS</sup> (41)</span></span>
| <span data-ttu-id="04ce8-2881">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2881">Target</span></span> | <span data-ttu-id="04ce8-2882">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2882">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2883">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2883">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2884">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2884">32</span></span> |
| <span data-ttu-id="04ce8-2885">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2885">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2887">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2887">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2889">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2889">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2891">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2891">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-2892">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2892">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2894">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2894">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2896">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2896">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2898">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2898">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2900">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2900">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2902">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2902">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2904">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2904">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2906">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2906">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2908">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2908">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2909">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2909">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2911">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2911">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2912">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2912">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2914">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2914">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2916">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2916">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2918">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2918">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2920">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2920">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-2921">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2921">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2922">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2922">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2923">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2923">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2924">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2924">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2925">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2925">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2926">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2926">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2927">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2927">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2928">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2928">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-2929">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-2929">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-2930">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2930">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-2931">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2931">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2932">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-2932">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-2933">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2933">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2935">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-2935">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2937">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2937">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2939">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-2939">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2941">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-2941">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2943">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-2943">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2945">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-2945">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-2946">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-2946">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2948">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2948">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-2949">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2949">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-2950">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-2950">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-2951">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2951">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2953">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-2953">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a><span data-ttu-id="04ce8-2954">DXGI_FORMAT_R32 \_ uint<sup>FCS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2954">DXGI_FORMAT_R32\_UINT<sup>FCS</sup> (42)</span></span>
| <span data-ttu-id="04ce8-2955">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-2955">Target</span></span> | <span data-ttu-id="04ce8-2956">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-2956">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-2957">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2957">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-2958">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-2958">32</span></span> |
| <span data-ttu-id="04ce8-2959">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-2959">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2961">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-2961">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2963">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2963">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2965">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-2965">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2967">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-2967">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2969">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2971">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2971">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2973">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-2973">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-2975">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2977">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-2977">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2979">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2979">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2980">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2980">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2981">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-2981">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-2982">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-2982">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-2983">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-2983">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-2984">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-2984">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2986">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-2987">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-2989">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-2989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-2990">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-2990">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-2992">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-2992">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-2993">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-2993">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2994">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-2994">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-2995">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-2995">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-2996">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2996">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-2997">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2997">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-2998">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-2998">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-2999">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-2999">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3000">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3000">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3001">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3001">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3002">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3002">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3003">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3003">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3004">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3004">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3006">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3006">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3008">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3008">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3010">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3010">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3012">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3012">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3013">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3013">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3015">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3015">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3016">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3016">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3018">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3018">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3019">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3019">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3020">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3020">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3021">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3021">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3023">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3023">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a><span data-ttu-id="04ce8-3024">DXGI_FORMAT_R32 \_ Saint-<sup>FCS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3024">DXGI_FORMAT_R32\_SINT<sup>FCS</sup> (43)</span></span>
| <span data-ttu-id="04ce8-3025">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3025">Target</span></span> | <span data-ttu-id="04ce8-3026">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3026">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3027">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3027">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3028">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-3028">32</span></span> |
| <span data-ttu-id="04ce8-3029">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3029">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3031">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3031">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3033">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3033">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3035">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3035">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3036">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3036">Stream Output Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3038">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3038">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3040">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3040">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3042">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3042">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3044">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3044">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3046">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3046">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3048">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3048">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3049">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3049">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3050">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3050">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3051">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3051">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3052">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3052">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3053">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3053">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3055">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3055">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3056">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3056">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3058">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3058">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3059">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3059">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3060">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3060">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3061">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3061">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3062">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3062">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3063">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3063">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3064">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3064">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3065">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3065">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3066">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3066">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3067">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3067">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3068">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3068">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3069">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3069">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3070">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3070">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3071">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3071">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3072">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3072">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3074">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3074">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3076">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3076">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3078">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3078">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3080">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3080">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3081">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3081">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3083">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3083">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3084">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3084">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3086">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3087">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3088">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3089">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3089">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3091">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3091">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="04ce8-3092">\_<sup>PC</sup> DXGI_FORMAT_R24G8 type (44)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3092">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="04ce8-3093">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3093">Target</span></span> | <span data-ttu-id="04ce8-3094">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3094">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3095">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3095">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3096">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-3096">32</span></span> |
| <span data-ttu-id="04ce8-3097">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3097">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3099">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3099">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3100">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3100">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3101">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3101">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3102">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3102">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3103">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3103">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3105">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3105">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3107">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3107">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-3108">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3108">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3110">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3110">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-3111">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3111">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3112">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3112">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3113">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3113">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3114">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3114">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3115">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3115">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3116">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3116">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3118">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3118">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3119">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3119">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3120">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3120">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3121">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3121">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3122">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3122">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3123">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3123">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3124">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3124">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3125">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3125">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3126">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3126">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3127">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3127">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3128">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3128">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3129">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3129">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3130">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3130">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3131">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3131">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3132">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3132">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3133">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3133">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3134">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3134">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3136">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3136">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3137">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3137">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3138">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3138">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-3139">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3139">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3140">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3140">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-3141">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3141">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3142">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3142">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3144">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3144">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3145">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3145">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3146">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3146">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3147">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3147">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3148">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3148">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a><span data-ttu-id="04ce8-3149">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FCS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3149">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FCS</sup> (45)</span></span>
| <span data-ttu-id="04ce8-3150">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3150">Target</span></span> | <span data-ttu-id="04ce8-3151">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3151">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3152">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3152">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3153">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-3153">32</span></span> |
| <span data-ttu-id="04ce8-3154">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3154">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3156">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3156">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3157">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3157">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3158">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3158">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3159">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3159">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3160">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3160">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3162">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3162">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3164">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3164">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-3165">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3165">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3167">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3167">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-3168">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3168">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3169">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3169">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3170">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3170">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3171">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3171">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3172">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3173">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3173">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3175">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3175">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3176">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3176">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3177">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3177">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3178">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3178">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3179">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3179">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3181">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3181">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3182">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3182">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3183">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3183">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3184">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3184">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3185">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3185">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3186">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3186">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3187">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3187">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3188">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3189">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3189">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3190">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3190">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3191">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3191">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3192">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3192">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3194">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3194">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3196">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3196">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3198">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3198">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3200">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3200">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3201">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3201">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-3202">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3202">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3203">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3203">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3205">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3205">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3206">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3206">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3207">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3207">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3208">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3208">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3209">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3209">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a><span data-ttu-id="04ce8-3210">DXGI_FORMAT_R24 \_ \_ FCS UNORM x8 non \_ typé (46)<sup></sup></span><span class="sxs-lookup"><span data-stu-id="04ce8-3210">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FCS</sup> (46)</span></span>
| <span data-ttu-id="04ce8-3211">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3211">Target</span></span> | <span data-ttu-id="04ce8-3212">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3212">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3213">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3213">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3214">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-3214">32</span></span> |
| <span data-ttu-id="04ce8-3215">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3215">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3217">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3217">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3218">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3218">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3219">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3219">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3220">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3220">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3221">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3221">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3223">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3223">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3225">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3225">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-3226">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3226">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3228">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3228">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3230">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3230">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3232">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3232">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3234">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3234">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3235">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3235">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3237">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3237">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3238">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3238">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3240">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3240">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3241">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3241">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3242">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3242">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3243">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3243">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3244">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3244">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3245">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3245">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3246">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3246">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3247">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3247">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3248">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3248">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3249">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3249">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3250">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3250">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3251">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3251">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3252">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3252">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3253">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3253">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3254">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3254">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3255">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3255">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3256">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3256">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3258">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3258">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3259">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3259">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3260">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3260">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-3261">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3261">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3262">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3262">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3264">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3264">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3265">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3265">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3267">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3267">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3268">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3268">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3269">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3269">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3270">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3270">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3271">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a><span data-ttu-id="04ce8-3272">DXGI_FORMAT_X24 \_ \_ G8 \_ UINT<sup>FCS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3272">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FCS</sup> (47)</span></span>
| <span data-ttu-id="04ce8-3273">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3273">Target</span></span> | <span data-ttu-id="04ce8-3274">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3274">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3275">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3276">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-3276">32</span></span> |
| <span data-ttu-id="04ce8-3277">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3277">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3279">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3279">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3280">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3281">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3282">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3283">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3285">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3285">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3287">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3287">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-3288">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3288">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3290">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3290">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3292">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3292">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3293">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3293">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3294">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3294">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3295">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3295">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3296">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3297">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3297">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3299">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3300">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3301">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3302">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3303">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3304">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3305">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3306">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3306">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3307">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3308">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3309">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3310">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3312">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3313">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3314">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3315">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3315">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3317">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3318">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3319">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-3320">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3321">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3321">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3323">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3323">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3324">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3324">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3326">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3327">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3328">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3329">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3330">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="04ce8-3331">\_<sup>PC</sup> DXGI_FORMAT_R8G8 type (48)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3331">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="04ce8-3332">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3332">Target</span></span> | <span data-ttu-id="04ce8-3333">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3334">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3335">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3335">16</span></span> |
| <span data-ttu-id="04ce8-3336">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3336">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3338">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3338">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3339">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3339">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3340">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3340">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3341">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3341">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3342">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3342">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3344">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3344">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3346">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3346">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3348">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3350">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3350">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-3351">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3351">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3352">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3352">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3353">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3353">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3354">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3354">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3355">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3355">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3356">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3356">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3358">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3358">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3359">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3359">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3360">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3360">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3361">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3361">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3362">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3362">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3363">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3363">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3364">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3364">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3365">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3365">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3366">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3366">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3367">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3367">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3368">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3368">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3369">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3369">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3370">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3370">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3371">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3371">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3372">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3372">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3373">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3373">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3374">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3374">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3376">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3376">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3377">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3377">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3378">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3378">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-3379">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3379">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3380">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3380">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-3381">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3381">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3382">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3382">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3384">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3384">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3385">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3385">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3386">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3386">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3387">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3387">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3388">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3388">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a><span data-ttu-id="04ce8-3389">DXGI_FORMAT_R8G8 \_ UNORM<sup>FCS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3389">DXGI_FORMAT_R8G8\_UNORM<sup>FCS</sup> (49)</span></span>
| <span data-ttu-id="04ce8-3390">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3390">Target</span></span> | <span data-ttu-id="04ce8-3391">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3391">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3392">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3392">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3393">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3393">16</span></span> |
| <span data-ttu-id="04ce8-3394">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3394">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3396">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3396">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3398">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3398">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3400">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3400">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3401">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3401">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3402">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3402">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3404">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3404">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3406">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3406">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3408">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3408">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3410">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3410">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3412">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3412">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3414">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3414">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3415">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3415">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3416">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3416">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3417">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3417">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3418">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3418">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3420">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3420">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3422">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3424">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3424">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3426">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3427">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3428">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3429">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3430">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3430">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3431">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3432">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3433">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3434">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3436">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3437">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3438">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3439">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3439">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3441">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3441">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3443">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3443">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3445">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3445">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3447">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3447">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3449">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3449">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3451">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3451">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3452">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3452">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3454">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3454">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3455">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3455">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3456">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3456">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3457">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3457">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3459">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3459">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a><span data-ttu-id="04ce8-3460">DXGI_FORMAT_R8G8 \_ uint<sup>FCS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3460">DXGI_FORMAT_R8G8\_UINT<sup>FCS</sup> (50)</span></span>
| <span data-ttu-id="04ce8-3461">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3461">Target</span></span> | <span data-ttu-id="04ce8-3462">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3462">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3463">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3463">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3464">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3464">16</span></span> |
| <span data-ttu-id="04ce8-3465">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3465">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3467">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3467">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3469">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3469">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3471">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3471">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3472">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3472">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3473">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3473">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3475">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3475">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3477">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3477">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3479">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3479">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3481">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3481">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3483">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3483">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3484">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3484">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3485">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3485">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3486">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3486">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3487">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3487">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3488">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3488">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3490">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3490">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3491">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3491">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3493">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3493">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3494">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3494">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3496">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3496">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3497">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3497">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3498">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3498">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3499">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3499">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3500">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3500">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3501">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3501">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3502">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3502">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3503">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3503">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3504">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3504">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3505">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3505">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3506">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3506">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3507">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3507">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3508">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3508">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3510">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3510">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3512">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3512">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3514">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3514">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3516">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3516">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3517">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3517">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3519">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3519">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3520">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3520">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3522">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3522">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3523">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3523">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3524">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3524">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3525">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3525">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3526">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3526">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a><span data-ttu-id="04ce8-3527">DXGI_FORMAT_R8G8 \_ ronfler<sup>FCS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3527">DXGI_FORMAT_R8G8\_SNORM<sup>FCS</sup> (51)</span></span>
| <span data-ttu-id="04ce8-3528">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3528">Target</span></span> | <span data-ttu-id="04ce8-3529">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3529">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3530">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3530">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3531">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3531">16</span></span> |
| <span data-ttu-id="04ce8-3532">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3532">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3534">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3534">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3536">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3536">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3538">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3538">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3539">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3539">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3540">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3540">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3542">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3542">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3544">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3544">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3546">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3546">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3548">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3548">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3550">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3550">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3552">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3553">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3554">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3554">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3555">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3556">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3556">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3558">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3558">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3560">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3560">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3562">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3562">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3564">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3564">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3565">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3565">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3566">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3566">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3567">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3567">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3568">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3568">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3569">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3569">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3570">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3570">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3571">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3571">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3572">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3572">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3573">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3573">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3574">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3574">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3575">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3575">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3576">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3576">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3577">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3577">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3579">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3579">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3581">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3581">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3583">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3583">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3585">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3585">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3587">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3587">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3589">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3589">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3590">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3590">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3592">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3592">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3593">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3593">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3594">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3594">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3595">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3595">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3596">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3596">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a><span data-ttu-id="04ce8-3597">DXGI_FORMAT_R8G8 \_ Saint-<sup>FCS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3597">DXGI_FORMAT_R8G8\_SINT<sup>FCS</sup> (52)</span></span>
| <span data-ttu-id="04ce8-3598">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3598">Target</span></span> | <span data-ttu-id="04ce8-3599">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3599">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3600">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3600">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3601">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3601">16</span></span> |
| <span data-ttu-id="04ce8-3602">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3602">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3604">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3604">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3606">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3606">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3608">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3609">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3610">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3612">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3612">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3614">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3614">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3616">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3616">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3618">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3618">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3620">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3620">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3621">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3621">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3622">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3622">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3623">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3623">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3624">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3624">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3625">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3625">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3627">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3627">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3628">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3628">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3630">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3630">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3631">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3631">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3632">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3632">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3633">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3633">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3634">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3634">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3635">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3635">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3636">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3636">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3637">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3637">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3638">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3638">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3639">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3639">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3640">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3640">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3641">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3641">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3642">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3642">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3643">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3643">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3644">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3644">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3646">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3646">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3648">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3648">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3650">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3650">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3652">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3653">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3653">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3655">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3655">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3656">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3656">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3658">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3658">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3659">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3659">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3660">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3660">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3661">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3661">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-3662">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3662">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="04ce8-3663">\_<sup>PC</sup> DXGI_FORMAT_R16 type (53)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3663">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="04ce8-3664">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3664">Target</span></span> | <span data-ttu-id="04ce8-3665">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3665">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3666">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3666">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3667">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3667">16</span></span> |
| <span data-ttu-id="04ce8-3668">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3668">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3670">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3670">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3671">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3671">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3672">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3672">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3673">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3673">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3674">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3674">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3676">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3676">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3678">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3678">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3680">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3680">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3682">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3682">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-3683">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3683">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3684">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3685">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3686">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3686">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3687">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3688">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3688">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3690">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3691">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3692">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3693">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3694">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3695">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3696">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3697">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3697">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3698">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3699">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3700">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3701">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3703">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3704">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3705">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3706">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3706">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3708">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3709">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3710">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-3711">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3712">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3712">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-3713">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3714">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3714">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3716">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3716">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3717">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3717">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3718">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3718">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3719">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3719">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3721">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3721">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a><span data-ttu-id="04ce8-3722">DXGI_FORMAT_R16 \_ float<sup>FCS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3722">DXGI_FORMAT_R16\_FLOAT<sup>FCS</sup> (54)</span></span>
| <span data-ttu-id="04ce8-3723">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3723">Target</span></span> | <span data-ttu-id="04ce8-3724">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3724">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3725">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3725">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3726">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3726">16</span></span> |
| <span data-ttu-id="04ce8-3727">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3727">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3729">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3729">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3731">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3731">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3733">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3733">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3734">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3734">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3735">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3735">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3737">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3737">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3739">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3739">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3741">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3741">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3743">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3743">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3745">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3745">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3747">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3747">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3748">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3748">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3749">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3749">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3751">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3751">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3752">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3752">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3754">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3754">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3756">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3756">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3758">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3758">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3760">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3760">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3761">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3761">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3762">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3762">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3763">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3763">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3764">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3764">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3765">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3765">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3766">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3766">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3767">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3767">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3768">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3768">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3769">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3769">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3770">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3770">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3771">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3771">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3772">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3772">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3773">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3773">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3775">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3775">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3777">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3777">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3779">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3779">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3781">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3781">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3783">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3783">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3785">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3785">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3786">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3786">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3788">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3788">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3789">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3789">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3790">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3790">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3791">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3791">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3793">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3793">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a><span data-ttu-id="04ce8-3794">DXGI_FORMAT_D16 \_ UNORM<sup>FCS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3794">DXGI_FORMAT_D16\_UNORM<sup>FCS</sup> (55)</span></span>
| <span data-ttu-id="04ce8-3795">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3795">Target</span></span> | <span data-ttu-id="04ce8-3796">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3796">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3797">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3797">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3798">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3798">16</span></span> |
| <span data-ttu-id="04ce8-3799">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3799">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3801">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3801">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3802">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3802">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3803">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3803">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3804">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3804">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3805">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3805">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3807">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3807">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3809">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3809">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-3810">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3810">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3812">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3812">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-3813">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3813">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3814">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3814">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3815">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3815">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3816">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3816">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3817">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3817">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3818">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3818">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3820">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3820">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3821">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3821">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3822">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3822">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3823">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3823">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3824">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3824">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3826">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3826">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3827">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3827">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3828">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3828">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3829">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3829">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3830">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3830">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3831">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3831">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3832">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3832">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3833">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3833">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3834">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3834">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3835">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3835">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3836">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3836">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3837">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3837">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3839">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3839">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3841">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3841">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3843">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3843">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3845">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3845">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3846">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3846">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-3847">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3847">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3848">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3848">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3850">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3850">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3851">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3851">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3852">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3852">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3853">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3853">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3855">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3855">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a><span data-ttu-id="04ce8-3856">DXGI_FORMAT_R16 \_ UNORM<sup>FCS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3856">DXGI_FORMAT_R16\_UNORM<sup>FCS</sup> (56)</span></span>
| <span data-ttu-id="04ce8-3857">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3857">Target</span></span> | <span data-ttu-id="04ce8-3858">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3858">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3859">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3859">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3860">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3860">16</span></span> |
| <span data-ttu-id="04ce8-3861">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3861">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3863">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3863">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3865">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3865">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3867">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3868">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3869">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3871">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3871">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3873">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3873">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3875">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3875">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3877">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3877">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3879">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3879">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3881">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3881">Shader sample\_c (comparison filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3883">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3883">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3884">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3884">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3886">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3886">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3887">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3887">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3889">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3889">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3891">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3891">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3893">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3893">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3895">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3895">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-3896">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3896">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3897">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3897">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3898">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3898">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3899">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3899">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3900">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3900">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3901">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3901">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3902">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3902">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3903">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3903">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3904">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3904">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3905">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3905">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3906">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3906">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3907">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3907">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3908">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3908">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3910">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3910">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3912">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3912">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3914">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3914">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3916">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3916">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3918">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3918">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3920">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3920">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3921">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3921">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3923">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3923">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3924">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3924">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3925">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3925">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3926">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3926">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3928">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a><span data-ttu-id="04ce8-3929">DXGI_FORMAT_R16 \_ uint<sup>FCS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3929">DXGI_FORMAT_R16\_UINT<sup>FCS</sup> (57)</span></span>
| <span data-ttu-id="04ce8-3930">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3930">Target</span></span> | <span data-ttu-id="04ce8-3931">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-3931">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-3932">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-3933">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-3933">16</span></span> |
| <span data-ttu-id="04ce8-3934">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-3934">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3936">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-3936">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3938">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3938">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3940">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3940">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3942">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-3942">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-3943">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3943">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3945">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3945">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3947">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-3947">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3949">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-3949">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3951">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-3951">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3953">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3953">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3954">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3954">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3955">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3955">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-3956">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-3956">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-3957">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-3957">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-3958">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-3958">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3960">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-3960">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-3961">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3961">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3963">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-3964">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-3964">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3966">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-3966">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-3967">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-3967">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3968">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-3968">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-3969">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-3969">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-3970">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3970">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-3971">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3971">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-3972">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-3972">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-3973">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3973">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-3974">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-3974">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-3975">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3975">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-3976">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-3976">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3977">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-3977">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-3978">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-3978">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3980">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-3980">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3982">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-3982">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3984">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-3984">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-3986">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-3986">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-3987">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-3987">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3989">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-3989">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-3990">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-3990">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3992">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3992">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-3993">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3993">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-3994">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-3994">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-3995">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-3995">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-3997">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-3997">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a><span data-ttu-id="04ce8-3998">DXGI_FORMAT_R16 \_ ronfler<sup>FCS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="04ce8-3998">DXGI_FORMAT_R16\_SNORM<sup>FCS</sup> (58)</span></span>
| <span data-ttu-id="04ce8-3999">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-3999">Target</span></span> | <span data-ttu-id="04ce8-4000">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4000">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4001">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4001">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4002">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-4002">16</span></span> |
| <span data-ttu-id="04ce8-4003">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4003">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4005">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4005">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4007">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4007">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4009">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4009">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4010">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4010">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4011">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4011">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4013">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4013">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4015">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4015">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4017">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4017">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4019">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4019">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4021">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4021">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4023">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4023">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4024">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4024">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4025">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4025">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4027">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4027">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4028">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4028">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4030">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4030">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4032">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4032">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4034">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4034">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4036">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4036">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4037">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4037">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4038">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4038">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4039">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4039">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4040">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4040">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4041">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4041">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4042">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4042">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4043">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4043">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4044">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4044">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4045">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4045">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4046">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4046">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4047">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4047">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4048">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4048">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4049">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4049">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4051">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4051">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4053">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4053">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4055">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4055">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4057">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4057">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4059">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4059">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4061">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4062">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4062">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4064">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4064">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4065">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4065">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4066">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4066">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4067">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4067">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4069">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4069">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a><span data-ttu-id="04ce8-4070">DXGI_FORMAT_R16 \_ Saint-<sup>FCS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4070">DXGI_FORMAT_R16\_SINT<sup>FCS</sup> (59)</span></span>
| <span data-ttu-id="04ce8-4071">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4071">Target</span></span> | <span data-ttu-id="04ce8-4072">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4072">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4073">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4073">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4074">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-4074">16</span></span> |
| <span data-ttu-id="04ce8-4075">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4075">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4077">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4077">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4079">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4079">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4081">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4081">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4082">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4082">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4083">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4083">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4085">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4085">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4087">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4087">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4089">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4089">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4091">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4091">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4093">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4093">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4094">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4094">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4095">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4095">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4096">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4096">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4097">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4097">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4098">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4098">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4100">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4100">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4101">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4101">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4103">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4103">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4104">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4104">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4105">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4105">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4106">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4106">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4107">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4107">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4108">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4108">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4109">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4109">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4110">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4110">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4111">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4111">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4112">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4112">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4113">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4113">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4114">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4114">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4115">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4115">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4116">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4116">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4117">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4117">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4119">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4119">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4121">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4121">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4123">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4123">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4125">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4125">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4126">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4126">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4128">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4128">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4129">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4129">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4131">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4131">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4132">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4132">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4133">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4133">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4134">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4134">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4136">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4136">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="04ce8-4137">\_<sup>PC</sup> DXGI_FORMAT_R8 type (60)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4137">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="04ce8-4138">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4138">Target</span></span> | <span data-ttu-id="04ce8-4139">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4139">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4140">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4140">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4141">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4141">8</span></span> |
| <span data-ttu-id="04ce8-4142">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4142">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4144">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4144">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4145">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4145">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4146">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4146">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4147">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4147">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4148">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4148">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4150">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4150">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4152">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4152">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4154">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4156">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4156">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-4157">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4157">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4158">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4158">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4159">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4159">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4160">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4160">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4161">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4161">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4162">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4162">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4164">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4164">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4165">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4165">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4166">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4166">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4167">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4167">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4168">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4168">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4169">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4169">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4170">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4170">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4171">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4171">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4172">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4172">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4173">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4173">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4174">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4174">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4175">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4175">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4176">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4176">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4177">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4177">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4178">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4178">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4179">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4179">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4180">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4180">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4182">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4182">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4183">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4183">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4184">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4184">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4185">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4185">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4186">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4186">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4187">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4187">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4188">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4188">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4190">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4190">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4191">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4191">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4192">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4192">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4193">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4193">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4195">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4195">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a><span data-ttu-id="04ce8-4196">DXGI_FORMAT_R8 \_ UNORM<sup>FCS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4196">DXGI_FORMAT_R8\_UNORM<sup>FCS</sup> (61)</span></span>
| <span data-ttu-id="04ce8-4197">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4197">Target</span></span> | <span data-ttu-id="04ce8-4198">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4198">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4199">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4199">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4200">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4200">8</span></span> |
| <span data-ttu-id="04ce8-4201">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4201">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4203">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4203">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4205">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4205">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4207">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4207">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4208">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4208">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4209">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4209">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4211">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4213">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4215">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4215">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4217">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4217">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4219">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4219">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4221">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4221">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4222">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4222">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4223">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4223">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4225">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4225">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4226">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4226">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4228">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4228">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4230">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4230">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4232">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4232">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4234">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4234">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4235">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4235">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4236">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4236">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4237">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4237">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4238">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4238">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4239">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4239">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4240">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4240">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4241">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4241">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4242">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4242">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4243">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4243">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4244">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4244">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4245">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4245">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4246">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4246">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4247">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4247">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4249">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4249">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4251">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4251">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4253">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4253">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4255">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4255">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4257">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4257">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4259">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4259">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4260">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4260">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4262">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4262">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4263">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4263">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4264">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4264">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4265">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4265">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4267">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4267">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a><span data-ttu-id="04ce8-4268">DXGI_FORMAT_R8 \_ uint<sup>FCS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4268">DXGI_FORMAT_R8\_UINT<sup>FCS</sup> (62)</span></span>
| <span data-ttu-id="04ce8-4269">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4269">Target</span></span> | <span data-ttu-id="04ce8-4270">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4270">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4271">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4271">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4272">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4272">8</span></span> |
| <span data-ttu-id="04ce8-4273">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4273">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4275">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4275">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4277">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4277">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4279">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4279">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4280">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4280">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4281">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4281">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4283">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4283">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4285">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4285">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4287">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4289">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4289">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4291">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4291">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4292">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4293">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4294">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4294">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4295">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4295">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4296">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4296">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4298">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4298">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4299">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4299">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4301">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4302">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4302">Output Merger Logic Op</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4304">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4305">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4306">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4307">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4307">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4308">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4309">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4310">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4311">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4312">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4313">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4314">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4315">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4316">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4316">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4318">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4318">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4320">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4320">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4322">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4322">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4324">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4324">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4325">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4325">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4327">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4327">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4328">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4328">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4330">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4331">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4332">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4333">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4333">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4335">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4335">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a><span data-ttu-id="04ce8-4336">DXGI_FORMAT_R8 \_ ronfler<sup>FCS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4336">DXGI_FORMAT_R8\_SNORM<sup>FCS</sup> (63)</span></span>
| <span data-ttu-id="04ce8-4337">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4337">Target</span></span> | <span data-ttu-id="04ce8-4338">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4338">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4339">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4339">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4340">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4340">8</span></span> |
| <span data-ttu-id="04ce8-4341">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4341">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4343">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4343">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4345">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4345">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4347">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4347">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4348">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4348">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4349">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4349">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4351">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4351">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4353">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4355">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4355">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4357">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4357">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4359">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4359">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4361">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4361">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4362">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4362">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4363">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4363">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4365">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4365">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4366">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4366">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4368">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4368">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4370">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4370">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4372">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4372">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4374">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4375">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4376">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4377">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4378">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4379">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4380">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4381">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4382">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4383">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4384">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4385">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4386">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4387">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4387">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4389">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4389">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4391">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4391">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4393">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4393">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4395">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4395">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4397">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4397">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4399">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4399">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4400">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4400">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4402">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4402">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4403">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4403">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4404">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4404">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4405">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4405">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4407">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4407">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a><span data-ttu-id="04ce8-4408">DXGI_FORMAT_R8 \_ Saint-<sup>FCS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4408">DXGI_FORMAT_R8\_SINT<sup>FCS</sup> (64)</span></span>
| <span data-ttu-id="04ce8-4409">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4409">Target</span></span> | <span data-ttu-id="04ce8-4410">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4410">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4411">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4411">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4412">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4412">8</span></span> |
| <span data-ttu-id="04ce8-4413">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4413">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4415">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4415">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4417">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4417">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4419">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4419">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4420">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4420">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4421">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4421">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4423">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4423">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4425">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4425">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4427">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4427">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4429">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4429">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4431">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4431">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4432">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4432">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4433">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4433">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4434">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4434">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4435">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4435">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4436">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4436">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4438">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4438">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4439">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4439">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4441">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4441">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4442">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4442">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4443">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4443">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4444">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4444">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4445">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4445">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4446">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4446">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4447">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4447">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4448">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4448">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4449">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4449">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4450">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4450">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4451">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4451">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4452">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4452">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4453">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4453">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4454">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4454">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4455">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4455">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4457">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4457">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4459">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4459">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4461">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4461">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4463">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4463">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4464">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4464">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4466">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4466">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4467">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4467">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4469">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4469">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4470">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4470">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4471">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4471">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4472">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4472">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4474">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4474">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="04ce8-4475">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4475">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="04ce8-4476">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4476">Target</span></span> | <span data-ttu-id="04ce8-4477">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4477">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4478">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4478">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4479">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4479">8</span></span> |
| <span data-ttu-id="04ce8-4480">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4480">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4482">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4482">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4483">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4483">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4484">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4484">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4485">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4485">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4486">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4486">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4488">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4488">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4490">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4490">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4492">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4492">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4494">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4494">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4496">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4496">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4498">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4498">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4499">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4499">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4500">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4500">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4501">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4501">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4502">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4502">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4504">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4504">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4506">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4506">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4508">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4508">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4510">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4510">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4511">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4511">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4512">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4512">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4513">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4513">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4514">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4514">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4515">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4515">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4516">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4516">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4517">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4517">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4518">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4518">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4519">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4519">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4520">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4520">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4521">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4521">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4522">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4522">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4523">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4523">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4525">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4525">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4527">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4527">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4529">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4529">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-4531">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4531">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4533">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4533">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4535">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4536">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-4537">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4538">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4539">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4540">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4540">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4542">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4542">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="04ce8-4543">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4543">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="04ce8-4544">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4544">Target</span></span> | <span data-ttu-id="04ce8-4545">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4545">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4546">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4546">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4547">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-4547">32</span></span> |
| <span data-ttu-id="04ce8-4548">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4548">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4550">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4550">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4551">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4551">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4552">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4552">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4553">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4553">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4554">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4554">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4556">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4558">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4558">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4560">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4560">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4562">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4562">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4564">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4564">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4566">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4567">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4568">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4569">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4570">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4570">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4572">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4572">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4573">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4573">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4574">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4574">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4575">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4575">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4576">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4576">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4577">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4577">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4578">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4578">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4579">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4579">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4580">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4580">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4581">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4581">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4582">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4582">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4583">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4583">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4584">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4584">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4585">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4585">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4586">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4586">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4587">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4587">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4588">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4588">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4590">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4590">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4591">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4591">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4592">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4592">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4593">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4593">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4594">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4594">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4595">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4595">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4596">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4596">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-4597">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4597">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4598">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4598">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4599">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4599">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4600">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4600">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-4601">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4601">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="04ce8-4602">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4602">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="04ce8-4603">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4603">Target</span></span> | <span data-ttu-id="04ce8-4604">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4604">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4605">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4605">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4606">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-4606">16</span></span> |
| <span data-ttu-id="04ce8-4607">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4607">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4609">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4609">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4610">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4610">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4611">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4611">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4612">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4612">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4613">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4613">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4615">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4615">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4617">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4617">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4619">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4619">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4621">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4621">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4623">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4623">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4625">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4625">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4626">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4626">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4627">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4627">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4628">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4628">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4629">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4629">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4631">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4631">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4632">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4632">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4633">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4633">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4634">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4634">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4635">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4635">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4636">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4636">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4637">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4637">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4638">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4638">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4639">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4639">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4640">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4640">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4641">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4641">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4642">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4642">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4643">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4643">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4644">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4644">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4645">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4645">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4646">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4646">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4647">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4647">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4649">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4649">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4650">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4650">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4651">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4651">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4652">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4652">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4653">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4653">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4654">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4654">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4655">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4655">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-4656">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4656">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4657">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4657">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4658">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4658">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4659">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4659">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-4660">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4660">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="04ce8-4661">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4661">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="04ce8-4662">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4662">Target</span></span> | <span data-ttu-id="04ce8-4663">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4663">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4664">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4664">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4665">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-4665">16</span></span> |
| <span data-ttu-id="04ce8-4666">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4666">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4668">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4668">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4669">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4669">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4670">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4670">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4671">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4671">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4672">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4672">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4674">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4674">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4676">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4676">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4678">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4678">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4680">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4680">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4682">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4682">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4684">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4684">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4685">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4685">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4686">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4686">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4687">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4687">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4688">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4688">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4690">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4690">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4691">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4691">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4692">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4692">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4693">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4693">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4694">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4694">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4695">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4695">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4696">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4696">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4697">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4697">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4698">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4698">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4699">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4699">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4700">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4700">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4701">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4701">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4702">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4702">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4703">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4703">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4704">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4704">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4705">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4705">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4706">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4706">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4708">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4708">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4709">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4709">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4710">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4710">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4711">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4711">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4712">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4712">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4713">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4713">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4714">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4714">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-4715">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4715">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4716">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4716">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4717">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4717">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4718">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4718">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-4719">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4719">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="04ce8-4720">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non typé (70)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4720">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="04ce8-4721">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4721">Target</span></span> | <span data-ttu-id="04ce8-4722">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4722">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4723">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4723">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4724">4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4724">4</span></span> |
| <span data-ttu-id="04ce8-4725">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4725">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4727">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4727">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4728">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4728">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4729">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4729">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4730">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4730">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4731">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4731">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-4732">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4732">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4734">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4734">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4736">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4736">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4738">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4738">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-4739">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4739">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4740">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4740">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4741">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4741">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4742">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4742">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4743">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4743">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4744">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4744">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4746">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4746">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4747">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4747">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4748">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4748">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4749">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4749">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4750">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4750">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4751">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4751">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4752">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4752">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4753">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4753">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4754">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4754">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4755">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4755">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4756">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4756">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4757">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4757">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4758">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4758">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4759">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4759">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4760">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4760">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4761">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4761">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4762">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4762">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4764">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4764">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4765">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4765">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4766">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4766">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4767">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4767">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4768">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4768">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4769">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4769">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4770">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4770">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4772">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4772">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4773">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4773">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4774">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4774">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4775">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4775">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4777">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4777">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfccsup-71"></a><span data-ttu-id="04ce8-4778">DXGI_FORMAT_BC1 \_ UNORM<sup>FCC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4778">DXGI_FORMAT_BC1\_UNORM<sup>FCC</sup> (71)</span></span>
| <span data-ttu-id="04ce8-4779">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4779">Target</span></span> | <span data-ttu-id="04ce8-4780">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4780">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4781">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4781">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4782">4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4782">4</span></span> |
| <span data-ttu-id="04ce8-4783">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4783">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4785">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4785">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4786">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4786">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4787">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4787">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4788">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4788">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4789">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4789">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-4790">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4790">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4792">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4792">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4794">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4794">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4796">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4796">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4798">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4798">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4800">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4800">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4801">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4801">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4802">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4802">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4803">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4803">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4804">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4804">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4806">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4806">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4807">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4807">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4808">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4808">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4809">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4809">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4810">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4810">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4811">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4811">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4812">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4812">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4813">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4813">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4814">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4814">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4815">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4815">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4816">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4816">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4817">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4817">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4818">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4818">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4819">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4819">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4820">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4820">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4821">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4821">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4822">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4822">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4824">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4824">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4825">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4825">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4826">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4826">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4827">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4827">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4828">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4828">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4829">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4829">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4830">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4830">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4832">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4832">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4833">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4833">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4834">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4834">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4835">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4835">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4837">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4837">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfccsup-72"></a><span data-ttu-id="04ce8-4838">DXGI_FORMAT_BC1 \_ UNORM \_ sRGB<sup>FCC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4838">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FCC</sup> (72)</span></span>
| <span data-ttu-id="04ce8-4839">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4839">Target</span></span> | <span data-ttu-id="04ce8-4840">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4840">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4841">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4841">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4842">4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4842">4</span></span> |
| <span data-ttu-id="04ce8-4843">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4843">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4845">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4845">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4846">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4846">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4847">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4847">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4848">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4848">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4849">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4849">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-4850">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4850">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4852">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4852">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4854">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4854">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4856">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4856">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4858">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4858">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4860">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4860">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4861">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4861">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4862">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4862">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4863">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4863">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4864">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4864">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4866">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4866">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4867">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4867">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4868">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4868">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4869">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4869">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4870">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4870">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4871">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4871">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4872">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4872">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4873">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4873">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4874">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4874">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4875">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4875">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4876">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4876">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4877">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4877">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4878">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4878">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4879">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4879">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4880">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4880">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4881">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4881">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4882">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4882">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4884">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4884">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4885">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4885">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4886">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4886">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4887">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4887">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4888">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4888">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4889">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4889">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4890">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4890">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4892">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4892">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4893">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4893">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4894">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4894">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4895">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4895">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4897">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4897">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="04ce8-4898">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non typé (73)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4898">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="04ce8-4899">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4899">Target</span></span> | <span data-ttu-id="04ce8-4900">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4900">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4901">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4901">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4902">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4902">8</span></span> |
| <span data-ttu-id="04ce8-4903">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4903">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4905">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4905">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4906">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4906">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4907">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4907">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4908">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4908">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4909">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4909">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-4910">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4910">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4912">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4912">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4914">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4914">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4916">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4916">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-4917">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4917">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4918">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4918">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4919">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4919">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4920">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4920">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4921">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4921">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4922">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4922">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4924">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4924">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4925">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4925">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4926">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4926">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4927">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4927">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4928">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4928">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4929">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4929">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4930">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4930">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4931">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4931">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4932">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4932">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4933">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4933">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4934">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4934">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4935">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4935">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4936">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4936">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4937">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4937">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4938">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4938">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4939">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4939">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4940">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4940">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4942">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-4942">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4943">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4943">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4944">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-4944">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-4945">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-4945">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-4946">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-4946">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-4947">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-4947">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-4948">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-4948">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4950">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4950">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-4951">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4951">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-4952">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-4952">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-4953">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4953">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4955">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-4955">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfccsup-74"></a><span data-ttu-id="04ce8-4956">DXGI_FORMAT_BC2 \_ UNORM<sup>FCC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4956">DXGI_FORMAT_BC2\_UNORM<sup>FCC</sup> (74)</span></span>
| <span data-ttu-id="04ce8-4957">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-4957">Target</span></span> | <span data-ttu-id="04ce8-4958">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-4958">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-4959">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4959">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-4960">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-4960">8</span></span> |
| <span data-ttu-id="04ce8-4961">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-4961">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4963">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-4963">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4964">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4964">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4965">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-4965">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4966">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-4966">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-4967">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4967">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-4968">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4968">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4970">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-4970">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-4972">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4974">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-4974">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4976">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4976">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4978">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4978">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4979">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-4979">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-4980">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-4980">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-4981">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-4981">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-4982">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-4982">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-4984">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-4984">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-4985">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-4985">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4986">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-4986">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-4987">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-4987">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-4988">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-4988">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-4989">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-4989">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4990">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-4990">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-4991">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-4991">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-4992">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4992">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-4993">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4993">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-4994">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-4994">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-4995">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4995">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-4996">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-4996">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-4997">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4997">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-4998">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-4998">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-4999">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-4999">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5000">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5000">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5002">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5002">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5003">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5003">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5004">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5004">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5005">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5005">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5006">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5006">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5007">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5007">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5008">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5008">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5010">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5011">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5012">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5013">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5013">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5015">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5015">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfccsup-75"></a><span data-ttu-id="04ce8-5016">DXGI_FORMAT_BC2 \_ UNORM \_ sRGB<sup>FCC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5016">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FCC</sup> (75)</span></span>
| <span data-ttu-id="04ce8-5017">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5017">Target</span></span> | <span data-ttu-id="04ce8-5018">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5018">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5019">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5019">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5020">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5020">8</span></span> |
| <span data-ttu-id="04ce8-5021">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5021">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5023">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5023">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5024">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5024">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5025">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5025">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5026">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5026">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5027">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5027">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5028">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5028">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5030">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5032">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5032">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5034">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5034">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5036">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5036">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5038">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5038">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5039">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5039">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5040">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5040">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5041">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5041">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5042">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5042">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5044">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5044">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5045">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5045">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5046">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5046">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5047">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5047">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5048">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5048">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5049">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5049">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5050">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5050">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5051">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5051">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5052">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5052">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5053">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5053">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5054">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5054">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5055">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5055">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5056">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5056">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5057">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5057">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5058">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5058">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5059">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5059">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5060">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5060">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5062">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5062">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5063">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5063">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5064">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5064">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5065">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5065">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5066">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5067">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5068">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5068">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5070">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5070">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5071">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5071">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5072">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5072">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5073">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5073">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5075">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5075">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="04ce8-5076">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non typé (76)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5076">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="04ce8-5077">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5077">Target</span></span> | <span data-ttu-id="04ce8-5078">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5078">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5079">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5079">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5080">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5080">8</span></span> |
| <span data-ttu-id="04ce8-5081">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5081">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5083">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5083">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5084">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5084">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5085">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5085">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5086">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5086">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5087">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5087">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5088">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5088">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5090">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5090">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5092">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5092">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5094">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5094">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-5095">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5095">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5096">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5096">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5097">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5097">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5098">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5098">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5099">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5099">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5100">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5100">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5102">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5102">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5103">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5103">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5104">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5104">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5105">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5105">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5106">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5106">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5107">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5107">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5108">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5108">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5109">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5109">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5110">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5110">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5111">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5111">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5112">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5112">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5113">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5113">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5114">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5114">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5115">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5115">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5116">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5116">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5117">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5117">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5118">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5118">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5120">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5120">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5121">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5121">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5122">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5122">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5123">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5123">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5124">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5124">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5125">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5125">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5126">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5126">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5128">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5128">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5129">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5129">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5130">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5130">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5131">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5131">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5133">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5133">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfccsup-77"></a><span data-ttu-id="04ce8-5134">DXGI_FORMAT_BC3 \_ UNORM<sup>FCC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5134">DXGI_FORMAT_BC3\_UNORM<sup>FCC</sup> (77)</span></span>
| <span data-ttu-id="04ce8-5135">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5135">Target</span></span> | <span data-ttu-id="04ce8-5136">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5136">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5137">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5137">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5138">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5138">8</span></span> |
| <span data-ttu-id="04ce8-5139">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5139">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5141">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5141">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5142">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5142">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5143">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5143">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5144">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5144">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5145">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5145">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5146">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5146">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5148">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5148">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5150">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5150">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5152">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5152">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5154">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5154">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5156">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5156">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5157">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5157">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5158">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5158">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5159">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5159">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5160">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5160">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5162">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5163">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5164">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5165">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5166">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5167">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5168">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5169">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5169">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5170">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5171">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5173">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5174">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5175">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5176">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5177">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5178">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5178">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5180">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5180">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5181">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5181">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5182">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5182">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5183">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5183">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5184">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5184">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5185">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5185">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5186">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5186">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5188">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5188">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5189">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5189">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5190">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5190">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5191">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5191">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5193">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5193">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfccsup-78"></a><span data-ttu-id="04ce8-5194">DXGI_FORMAT_BC3 \_ UNORM \_ sRGB<sup>FCC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5194">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FCC</sup> (78)</span></span>
| <span data-ttu-id="04ce8-5195">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5195">Target</span></span> | <span data-ttu-id="04ce8-5196">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5196">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5197">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5197">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5198">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5198">8</span></span> |
| <span data-ttu-id="04ce8-5199">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5199">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5201">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5201">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5202">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5202">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5203">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5203">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5204">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5204">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5205">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5205">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5206">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5206">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5208">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5208">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5210">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5210">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5212">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5212">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5214">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5214">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5216">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5216">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5217">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5217">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5218">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5218">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5219">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5219">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5220">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5220">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5222">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5224">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5225">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5226">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5227">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5228">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5229">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5230">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5231">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5232">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5233">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5234">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5235">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5236">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5237">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5238">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5238">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5240">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5241">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5242">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5243">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5244">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5245">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5246">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5246">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5248">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5248">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5249">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5249">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5250">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5250">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5251">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5251">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5253">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5253">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="04ce8-5254">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non typé (79)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5254">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="04ce8-5255">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5255">Target</span></span> | <span data-ttu-id="04ce8-5256">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5256">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5257">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5257">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5258">4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5258">4</span></span> |
| <span data-ttu-id="04ce8-5259">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5259">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5261">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5261">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5262">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5262">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5263">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5263">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5264">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5264">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5265">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5265">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5266">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5266">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5268">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5268">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5270">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5272">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5272">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-5273">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5273">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5274">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5274">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5275">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5275">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5276">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5276">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5277">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5277">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5278">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5278">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5280">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5280">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5281">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5281">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5282">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5282">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5283">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5283">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5284">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5284">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5285">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5285">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5286">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5286">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5287">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5287">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5288">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5288">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5289">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5289">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5290">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5290">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5291">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5291">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5292">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5292">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5293">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5293">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5294">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5294">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5295">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5295">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5296">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5296">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5298">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5298">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5299">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5299">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5300">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5300">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5301">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5301">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5302">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5302">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5303">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5303">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5304">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5304">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5306">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5306">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5307">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5307">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5308">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5308">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5309">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5310">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfccsup-80"></a><span data-ttu-id="04ce8-5311">DXGI_FORMAT_BC4 \_ UNORM<sup>FCC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5311">DXGI_FORMAT_BC4\_UNORM<sup>FCC</sup> (80)</span></span>
| <span data-ttu-id="04ce8-5312">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5312">Target</span></span> | <span data-ttu-id="04ce8-5313">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5314">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5315">4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5315">4</span></span> |
| <span data-ttu-id="04ce8-5316">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5316">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5318">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5319">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5320">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5321">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5323">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5325">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5327">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5327">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5329">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5329">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5331">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5331">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5333">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5333">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5334">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5334">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5335">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5335">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5336">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5336">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5337">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5337">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5339">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5339">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5340">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5340">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5341">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5341">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5342">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5342">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5343">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5343">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5344">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5344">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5345">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5345">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5346">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5346">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5347">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5347">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5348">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5348">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5349">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5349">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5350">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5350">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5351">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5351">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5352">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5352">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5353">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5353">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5354">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5354">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5355">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5355">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5357">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5357">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5358">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5358">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5359">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5359">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5360">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5360">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5361">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5361">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5362">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5362">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5363">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5363">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5365">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5365">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5366">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5366">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5367">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5367">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5368">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5368">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5369">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5369">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfccsup-81"></a><span data-ttu-id="04ce8-5370">DXGI_FORMAT_BC4 \_ ronfler<sup>FCC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5370">DXGI_FORMAT_BC4\_SNORM<sup>FCC</sup> (81)</span></span>
| <span data-ttu-id="04ce8-5371">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5371">Target</span></span> | <span data-ttu-id="04ce8-5372">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5372">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5373">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5373">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5374">4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5374">4</span></span> |
| <span data-ttu-id="04ce8-5375">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5375">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5377">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5377">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5378">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5378">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5379">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5379">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5380">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5380">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5381">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5381">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5382">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5382">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5384">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5384">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5386">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5386">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5388">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5388">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5390">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5390">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5392">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5392">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5393">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5393">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5394">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5394">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5395">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5395">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5396">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5396">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5398">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5398">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5399">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5399">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5400">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5400">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5401">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5401">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5402">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5402">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5403">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5403">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5404">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5404">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5405">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5405">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5406">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5406">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5407">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5407">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5408">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5408">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5409">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5409">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5410">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5410">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5411">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5411">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5412">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5412">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5413">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5413">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5414">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5414">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5416">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5416">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5417">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5417">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5418">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5418">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5419">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5419">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5420">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5420">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5421">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5421">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5422">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5422">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5424">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5424">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5425">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5425">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5426">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5426">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5427">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5427">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5428">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5428">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="04ce8-5429">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non typé (82)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5429">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="04ce8-5430">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5430">Target</span></span> | <span data-ttu-id="04ce8-5431">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5431">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5432">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5432">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5433">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5433">8</span></span> |
| <span data-ttu-id="04ce8-5434">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5434">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5436">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5436">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5437">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5437">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5438">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5438">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5439">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5439">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5440">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5440">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5441">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5441">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5443">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5443">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5445">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5445">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5447">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5447">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-5448">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5448">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5449">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5449">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5450">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5450">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5451">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5451">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5452">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5452">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5453">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5453">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5455">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5455">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5456">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5456">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5457">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5457">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5458">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5458">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5459">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5459">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5460">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5460">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5461">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5461">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5462">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5462">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5463">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5463">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5464">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5464">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5465">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5465">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5466">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5466">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5467">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5467">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5468">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5468">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5469">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5469">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5470">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5470">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5471">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5471">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5473">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5473">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5474">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5474">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5475">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5475">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5476">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5476">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5477">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5477">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5478">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5478">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5479">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5479">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5481">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5481">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5482">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5482">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5483">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5483">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5484">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5484">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5485">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5485">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfccsup-83"></a><span data-ttu-id="04ce8-5486">DXGI_FORMAT_BC5 \_ UNORM<sup>FCC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5486">DXGI_FORMAT_BC5\_UNORM<sup>FCC</sup> (83)</span></span>
| <span data-ttu-id="04ce8-5487">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5487">Target</span></span> | <span data-ttu-id="04ce8-5488">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5488">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5489">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5489">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5490">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5490">8</span></span> |
| <span data-ttu-id="04ce8-5491">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5491">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5493">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5493">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5494">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5494">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5495">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5495">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5496">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5496">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5497">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5497">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5498">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5498">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5500">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5500">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5502">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5502">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5504">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5504">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5506">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5506">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5508">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5509">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5510">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5510">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5511">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5512">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5512">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5514">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5514">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5515">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5515">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5516">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5516">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5517">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5517">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5518">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5518">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5519">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5519">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5520">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5520">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5521">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5521">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5522">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5522">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5523">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5523">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5524">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5524">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5525">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5525">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5526">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5526">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5527">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5527">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5528">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5528">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5529">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5529">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5530">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5530">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5532">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5532">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5533">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5533">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5534">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5534">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5535">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5535">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5536">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5536">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5537">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5537">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5538">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5538">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5540">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5541">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5542">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5543">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5543">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5544">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfccsup-84"></a><span data-ttu-id="04ce8-5545">DXGI_FORMAT_BC5 \_ ronfler<sup>FCC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5545">DXGI_FORMAT_BC5\_SNORM<sup>FCC</sup> (84)</span></span>
| <span data-ttu-id="04ce8-5546">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5546">Target</span></span> | <span data-ttu-id="04ce8-5547">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5547">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5548">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5549">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-5549">8</span></span> |
| <span data-ttu-id="04ce8-5550">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5550">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5552">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5552">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5553">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5553">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5554">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5554">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5555">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5555">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5556">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5556">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-5557">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5557">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5559">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5559">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5561">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5561">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5563">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5563">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5565">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5565">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5567">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5567">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5568">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5568">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5569">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5569">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5570">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5570">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5571">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5571">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5573">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5573">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5574">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5574">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5575">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5575">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5576">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5576">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5577">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5577">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5578">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5578">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5579">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5579">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5580">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5580">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5581">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5581">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5582">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5582">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5583">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5583">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5584">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5584">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5585">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5585">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5586">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5586">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5587">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5587">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5588">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5588">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5589">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5589">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5591">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5591">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5592">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5592">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5593">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5593">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5594">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5594">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5595">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5595">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5596">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5596">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5597">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5597">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5599">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5599">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5600">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5600">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5601">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5601">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5602">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5602">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5603">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5603">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="04ce8-5604">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5604">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="04ce8-5605">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5605">Target</span></span> | <span data-ttu-id="04ce8-5606">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5606">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5607">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5607">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5608">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-5608">16</span></span> |
| <span data-ttu-id="04ce8-5609">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5609">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5611">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5611">Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5613">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5613">Input Assembler Vertex Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5615">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5615">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5616">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5616">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5617">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5617">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5619">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5619">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5621">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5621">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5623">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5623">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5625">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5625">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5627">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5627">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5629">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5629">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5630">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5630">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5631">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5631">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5632">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5632">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5633">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5633">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5635">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5635">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5637">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5637">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5639">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5639">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5641">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5641">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5642">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5642">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5643">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5643">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5644">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5644">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5645">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5645">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5646">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5646">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5647">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5647">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5648">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5648">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5649">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5649">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5650">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5650">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5651">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5651">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5652">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5652">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5653">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5653">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5654">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5654">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5656">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5656">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5658">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5658">8x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5660">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5660">Other Multisample Count RT</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5662">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5662">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5664">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5664">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5666">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5666">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5667">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5667">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-5668">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5668">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5669">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5669">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5670">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5670">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5671">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5671">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5672">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5672">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="04ce8-5673">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5673">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="04ce8-5674">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5674">Target</span></span> | <span data-ttu-id="04ce8-5675">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5675">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5676">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5676">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5677">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-5677">16</span></span> |
| <span data-ttu-id="04ce8-5678">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5678">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5680">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5680">Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5682">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5682">Input Assembler Vertex Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5684">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5684">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5685">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5685">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5686">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5686">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5688">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5688">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5690">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5690">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5692">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5692">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5694">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5694">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5696">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5696">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5698">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5698">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5699">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5699">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5700">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5700">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5701">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5701">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5702">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5702">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5704">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5704">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5706">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5706">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5708">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5708">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5710">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5710">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5711">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5711">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5712">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5712">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5713">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5713">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5714">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5714">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5715">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5715">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5716">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5716">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5717">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5717">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5718">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5718">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5719">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5719">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5720">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5720">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5721">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5721">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5722">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5722">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5723">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5723">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5725">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5725">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5727">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5727">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5729">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5729">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5731">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5731">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5733">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5733">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5735">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5735">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5736">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5736">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-5737">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5737">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5738">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5738">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5739">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5739">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5740">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5740">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-5741">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5741">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="04ce8-5742">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8A8 type (90)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5742">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="04ce8-5743">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5743">Target</span></span> | <span data-ttu-id="04ce8-5744">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5744">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5745">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5745">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5746">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-5746">32</span></span> |
| <span data-ttu-id="04ce8-5747">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5747">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5749">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5749">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5750">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5750">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5751">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5751">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5752">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5752">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5753">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5753">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5755">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5755">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5757">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5757">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5759">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5759">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5761">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5761">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-5762">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5762">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5763">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5763">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5764">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5764">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5765">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5765">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5766">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5766">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5767">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5767">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5769">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5769">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5770">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5770">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5771">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5771">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5772">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5772">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5773">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5773">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5774">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5774">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5775">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5775">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5776">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5776">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5777">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5777">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5778">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5778">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5779">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5779">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5780">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5780">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5781">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5781">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5782">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5782">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5783">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5783">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5784">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5784">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5785">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5785">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5787">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5787">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5788">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5788">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5789">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5789">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5790">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5790">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5791">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5791">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5792">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5792">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5793">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5793">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5795">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5795">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5796">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5796">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-5797">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5797">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-5798">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5798">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5800">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a><span data-ttu-id="04ce8-5801">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FCS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5801">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FCS</sup> (87)</span></span>
| <span data-ttu-id="04ce8-5802">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5802">Target</span></span> | <span data-ttu-id="04ce8-5803">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5803">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5804">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5805">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-5805">32</span></span> |
| <span data-ttu-id="04ce8-5806">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5806">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5808">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5808">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5810">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5810">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5812">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5812">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5813">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5813">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5814">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5814">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5816">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5816">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5818">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5818">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5820">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5820">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5822">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5822">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5824">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5824">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5826">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5826">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5827">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5827">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5828">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5828">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5829">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5829">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5830">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5830">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5832">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5832">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5834">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5834">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5836">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5836">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5838">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5839">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5840">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5841">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5842">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5843">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5844">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5845">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5846">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5847">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5848">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5849">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5850">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5851">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5851">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5853">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5853">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5855">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5855">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5857">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5857">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5859">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5859">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5861">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5861">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5863">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5863">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5865">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5865">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5867">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5867">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5868">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5868">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5870">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5870">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5872">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5872">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5874">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5874">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a><span data-ttu-id="04ce8-5875">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRVB<sup>FCS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5875">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FCS</sup> (91)</span></span>
| <span data-ttu-id="04ce8-5876">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5876">Target</span></span> | <span data-ttu-id="04ce8-5877">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5877">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5878">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5878">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5879">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-5879">32</span></span> |
| <span data-ttu-id="04ce8-5880">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5880">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5882">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5882">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5883">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5883">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5884">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5884">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5885">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5885">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5886">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5886">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5888">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5888">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5890">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5890">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5892">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5894">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5894">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5896">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5896">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5898">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5898">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5899">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5899">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5900">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5900">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5901">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5901">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5902">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5902">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5904">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5904">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5906">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5906">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5908">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5908">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5910">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5910">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5911">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5911">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5912">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5912">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5913">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5913">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5914">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5914">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5915">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5915">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5916">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5916">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5917">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5917">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5918">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5918">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5919">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5919">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5920">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5920">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5921">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5921">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5922">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5922">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5923">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5923">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5925">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5925">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5927">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5927">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5929">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5929">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5931">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5931">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5933">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5933">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5935">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5935">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5937">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5937">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5939">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5939">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-5940">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5940">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5942">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-5942">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-5944">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5944">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5946">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-5946">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="04ce8-5947">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8X8 type (92)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5947">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="04ce8-5948">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-5948">Target</span></span> | <span data-ttu-id="04ce8-5949">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-5949">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-5950">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5950">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-5951">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-5951">32</span></span> |
| <span data-ttu-id="04ce8-5952">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-5952">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5954">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-5954">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5955">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5955">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5956">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-5956">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5957">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-5957">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-5958">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5958">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5960">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5960">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5962">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-5962">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5964">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-5964">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5966">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-5966">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-5967">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5967">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5968">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5968">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5969">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-5969">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-5970">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-5970">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-5971">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-5971">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-5972">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-5972">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5974">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-5974">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-5975">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5975">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5976">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5976">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5977">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-5977">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-5978">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-5978">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-5979">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-5979">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5980">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-5980">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-5981">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-5981">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-5982">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5982">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-5983">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5983">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-5984">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-5984">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-5985">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5985">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-5986">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-5986">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-5987">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5987">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-5988">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-5988">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5989">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-5989">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-5990">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-5990">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-5992">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-5992">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5993">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-5993">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-5994">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-5994">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-5995">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-5995">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-5996">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-5996">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-5997">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-5997">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-5998">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-5998">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6000">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6000">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-6001">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6001">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-6002">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6002">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-6003">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6003">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6005">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6005">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a><span data-ttu-id="04ce8-6006">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FCS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6006">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FCS</sup> (88)</span></span>
| <span data-ttu-id="04ce8-6007">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6007">Target</span></span> | <span data-ttu-id="04ce8-6008">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6008">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6009">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6009">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6010">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-6010">32</span></span> |
| <span data-ttu-id="04ce8-6011">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6011">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6013">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6013">Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6015">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6015">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6017">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6017">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6018">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6018">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6019">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6019">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6021">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6023">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6025">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6027">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6027">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6029">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6029">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6031">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6032">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6033">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6033">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-6034">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6035">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6035">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6037">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6037">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6039">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6041">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6041">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6043">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6044">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6045">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6046">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6047">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6047">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6048">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6049">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6051">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6052">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6053">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6054">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6055">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6056">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6056">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6058">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6058">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6060">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6060">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6062">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6062">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6064">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6064">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6066">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6066">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6068">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6068">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6069">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6069">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6071">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6071">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-6072">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6072">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6074">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6074">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6076">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6076">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6078">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6078">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a><span data-ttu-id="04ce8-6079">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRVB<sup>FCS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6079">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FCS</sup> (93)</span></span>
| <span data-ttu-id="04ce8-6080">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6080">Target</span></span> | <span data-ttu-id="04ce8-6081">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6081">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6082">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6082">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6083">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-6083">32</span></span> |
| <span data-ttu-id="04ce8-6084">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6084">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6086">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6086">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6087">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6087">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6088">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6088">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6089">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6089">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6090">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6090">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6092">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6092">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6094">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6094">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6096">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6096">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6098">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6098">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6100">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6100">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6102">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6102">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6103">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6103">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6104">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6104">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-6105">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6105">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6106">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6106">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6108">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6108">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6110">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6110">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6112">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6112">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6114">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6114">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6115">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6115">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6116">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6116">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6117">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6117">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6118">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6118">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6119">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6119">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6120">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6120">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6121">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6121">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6122">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6122">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6123">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6123">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6124">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6124">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6125">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6125">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6126">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6126">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6127">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6127">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6129">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6129">4x Multisample RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6131">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6131">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6133">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6133">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6135">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6135">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6137">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6137">Multisample Load</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6139">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6139">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6140">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6140">Cast Within Bit Layout</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6142">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6142">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-6143">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6143">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-6144">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6144">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-6145">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6145">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6147">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6147">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="04ce8-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6148">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="04ce8-6149">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6149">Target</span></span> | <span data-ttu-id="04ce8-6150">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6150">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6151">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6151">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6152">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-6152">32</span></span> |
| <span data-ttu-id="04ce8-6153">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6153">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6155">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6155">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6156">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6156">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6157">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6157">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6158">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6158">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6159">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6159">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6160">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6162">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6162">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6163">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6163">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6164">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6164">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6166">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6166">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6168">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6168">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6169">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6169">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6170">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6170">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6172">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6172">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6173">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6173">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6175">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6175">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6177">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6177">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6179">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6179">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6181">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6181">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6182">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6182">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6183">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6183">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6184">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6184">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6185">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6185">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6186">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6186">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6187">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6187">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6188">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6188">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6189">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6189">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6190">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6190">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6191">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6191">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6192">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6192">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6193">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6193">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6194">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6194">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6196">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6196">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6197">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6197">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6198">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6198">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6199">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6199">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6200">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6200">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6201">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6201">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6202">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6202">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6203">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6203">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6205">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6205">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6207">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6207">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6209">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6209">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6211">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6211">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="04ce8-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6212">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="04ce8-6213">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6213">Target</span></span> | <span data-ttu-id="04ce8-6214">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6214">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6215">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6215">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6216">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-6216">32</span></span> |
| <span data-ttu-id="04ce8-6217">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6217">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6219">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6219">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6220">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6220">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6221">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6221">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6222">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6222">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6223">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6223">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6224">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6224">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6226">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6226">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6227">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6227">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6228">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6228">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6230">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6230">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6232">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6232">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6233">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6233">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6234">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6234">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6236">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6236">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6237">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6237">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6238">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6238">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6239">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6239">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6240">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6240">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6241">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6241">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6242">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6242">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6243">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6243">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6244">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6244">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6245">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6245">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6246">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6246">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6247">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6247">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6248">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6248">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6249">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6249">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6250">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6250">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6251">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6251">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6252">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6252">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6253">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6253">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6254">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6254">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6256">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6256">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6257">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6257">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6258">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6258">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6259">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6259">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6260">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6260">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6261">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6261">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6262">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6262">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6263">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6263">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6265">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6265">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6267">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6267">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6269">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6269">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6271">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6271">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="04ce8-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6272">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="04ce8-6273">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6273">Target</span></span> | <span data-ttu-id="04ce8-6274">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6274">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6275">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6275">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6276">64</span><span class="sxs-lookup"><span data-stu-id="04ce8-6276">64</span></span> |
| <span data-ttu-id="04ce8-6277">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6277">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6279">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6279">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6280">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6280">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6281">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6281">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6282">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6282">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6283">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6283">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6284">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6284">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6286">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6286">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6287">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6287">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6288">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6288">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6290">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6290">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6292">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6292">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6293">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6293">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6294">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6294">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6296">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6296">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6297">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6297">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6299">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6299">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6300">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6300">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6301">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6301">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6302">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6302">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6303">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6303">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6304">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6304">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6305">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6305">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6306">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6306">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6307">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6307">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6308">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6308">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6309">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6309">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6310">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6310">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6311">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6311">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6312">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6312">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6313">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6313">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6314">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6314">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6315">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6315">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6317">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6318">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6319">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6320">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6321">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6321">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6322">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6323">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6324">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6324">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6326">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6326">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6328">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6328">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6330">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6330">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6332">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6332">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="04ce8-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6333">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="04ce8-6334">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6334">Target</span></span> | <span data-ttu-id="04ce8-6335">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6335">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6336">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6336">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6337">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-6337">8</span></span> |
| <span data-ttu-id="04ce8-6338">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6338">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6340">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6340">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6341">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6341">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6342">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6342">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6343">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6343">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6344">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6344">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6345">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6345">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6347">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6348">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6349">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6349">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6351">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6351">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6353">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6353">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6354">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6354">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6355">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6355">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6357">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6357">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6358">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6358">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6359">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6359">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6360">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6360">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6362">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6362">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6364">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6364">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6365">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6365">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6366">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6366">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6367">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6367">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6368">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6368">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6369">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6369">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6370">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6370">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6371">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6371">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6372">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6372">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6373">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6373">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6374">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6374">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6375">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6375">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6376">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6376">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6377">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6377">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6379">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6380">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6381">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6382">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6383">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6383">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6384">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6385">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6386">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6386">Video Decoder Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6388">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6388">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6390">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6390">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6392">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6392">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6394">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6394">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="04ce8-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6395">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="04ce8-6396">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6396">Target</span></span> | <span data-ttu-id="04ce8-6397">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6397">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6398">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6398">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6399">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-6399">16</span></span> |
| <span data-ttu-id="04ce8-6400">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6400">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6402">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6402">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6403">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6403">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6404">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6404">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6405">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6405">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6406">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6406">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6407">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6407">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6409">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6409">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6410">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6410">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6411">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6411">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6413">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6413">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6415">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6415">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6416">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6416">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6417">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6417">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6419">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6420">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6420">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6421">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6422">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6424">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6424">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6426">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6426">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6427">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6427">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6428">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6428">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6429">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6429">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6430">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6430">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6431">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6431">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6432">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6432">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6433">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6433">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6434">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6434">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6435">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6435">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6436">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6436">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6437">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6437">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6438">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6438">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6439">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6439">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6441">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6441">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6442">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6442">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6443">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6443">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6444">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6444">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6445">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6445">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6446">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6446">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6447">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6447">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6448">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6448">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6450">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6450">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6452">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6452">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6454">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6454">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6456">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6456">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="04ce8-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6457">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="04ce8-6458">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6458">Target</span></span> | <span data-ttu-id="04ce8-6459">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6459">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6460">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6460">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6461">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-6461">16</span></span> |
| <span data-ttu-id="04ce8-6462">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6462">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6464">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6464">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6465">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6465">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6466">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6466">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6467">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6467">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6468">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6468">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6469">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6469">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6471">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6471">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6472">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6472">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6473">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6473">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6475">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6475">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6477">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6477">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6478">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6478">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6479">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6479">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6481">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6481">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6482">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6482">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6483">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6483">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6484">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6484">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6486">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6486">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6488">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6488">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6489">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6489">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6490">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6490">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6491">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6491">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6492">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6492">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6493">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6493">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6494">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6494">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6495">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6495">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6496">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6496">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6497">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6497">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6498">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6498">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6499">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6499">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6500">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6500">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6501">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6501">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6503">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6503">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6504">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6504">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6505">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6505">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6506">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6506">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6507">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6507">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6508">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6508">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6509">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6509">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6510">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6510">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6512">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6512">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6514">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6514">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6516">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6516">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6518">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6518">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="04ce8-6519">DXGI_FORMAT_420 \_ <sup>V</sup> opaque (106)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6519">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="04ce8-6520">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6520">Target</span></span> | <span data-ttu-id="04ce8-6521">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6521">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6522">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6522">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6523">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-6523">8</span></span> |
| <span data-ttu-id="04ce8-6524">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6524">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6526">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6526">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6527">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6527">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6528">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6528">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6529">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6529">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6530">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6530">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6531">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6531">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6533">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6533">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6534">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6534">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6535">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6535">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-6536">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6536">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6537">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6537">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6538">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6538">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6539">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6539">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-6540">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6540">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6541">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6541">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6542">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6542">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6543">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6543">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6544">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6544">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6545">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6545">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6546">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6546">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6547">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6547">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6548">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6548">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6549">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6549">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6550">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6550">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6551">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6551">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6552">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6552">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6553">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6553">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6554">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6554">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6555">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6555">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6556">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6556">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6557">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6557">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6558">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6558">CPU Lockable</span></span> | \- |
| <span data-ttu-id="04ce8-6559">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6559">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6560">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6560">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6561">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6561">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6562">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6562">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6563">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6563">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6564">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6564">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6565">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6565">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6566">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6566">Video Decoder Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6568">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6568">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6570">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6570">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6572">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6572">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6574">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6574">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="04ce8-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6575">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="04ce8-6576">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6576">Target</span></span> | <span data-ttu-id="04ce8-6577">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6577">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6578">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6578">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6579">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-6579">16</span></span> |
| <span data-ttu-id="04ce8-6580">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6580">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6582">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6582">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6583">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6583">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6584">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6584">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6585">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6585">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6586">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6586">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6587">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6587">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6589">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6589">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6590">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6590">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6591">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6591">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6593">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6593">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6595">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6595">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6596">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6596">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6597">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6597">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6599">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6599">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6600">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6600">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6601">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6601">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6602">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6602">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6603">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6603">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6604">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6604">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6605">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6605">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6606">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6606">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6607">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6607">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6608">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6608">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6609">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6609">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6610">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6610">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6611">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6611">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6612">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6612">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6613">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6613">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6614">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6614">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6615">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6615">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6616">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6616">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6617">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6617">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6619">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6619">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6620">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6620">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6621">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6621">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6622">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6622">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6623">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6623">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6624">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6624">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6625">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6625">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6626">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6626">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6628">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6628">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6630">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6630">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6632">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6632">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6634">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6634">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="04ce8-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6635">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="04ce8-6636">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6636">Target</span></span> | <span data-ttu-id="04ce8-6637">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6637">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6638">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6638">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6639">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-6639">32</span></span> |
| <span data-ttu-id="04ce8-6640">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6640">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6642">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6642">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6643">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6643">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6644">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6644">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6645">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6645">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6646">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6646">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6647">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6647">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6649">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6649">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6650">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6650">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6651">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6651">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6653">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6653">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6655">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6655">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6656">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6656">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6657">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6657">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6659">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6659">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6660">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6660">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6661">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6661">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6662">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6662">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6663">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6663">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6664">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6664">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6665">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6665">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6666">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6666">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6667">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6667">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6668">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6668">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6669">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6669">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6670">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6670">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6671">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6671">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6672">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6672">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6673">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6673">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6674">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6674">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6675">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6675">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6676">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6676">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6677">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6677">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6679">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6679">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6680">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6680">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6681">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6681">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6682">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6682">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6683">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6683">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6684">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6684">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6685">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6685">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6686">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6686">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6688">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6688">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6690">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6690">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6692">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6692">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6694">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6694">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="04ce8-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6695">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="04ce8-6696">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6696">Target</span></span> | <span data-ttu-id="04ce8-6697">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6697">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6698">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6698">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6699">32</span><span class="sxs-lookup"><span data-stu-id="04ce8-6699">32</span></span> |
| <span data-ttu-id="04ce8-6700">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6700">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6702">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6702">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6703">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6703">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6704">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6704">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6705">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6705">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6706">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6706">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6707">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6707">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6709">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6709">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6710">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6710">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6711">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6711">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6713">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6713">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6715">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6715">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6716">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6716">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6717">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6717">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6719">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6719">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6720">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6720">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6721">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6721">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6722">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6722">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6723">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6723">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6724">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6724">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6725">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6725">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6726">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6726">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6727">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6727">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6728">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6728">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6729">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6729">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6730">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6730">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6731">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6731">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6732">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6732">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6733">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6733">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6734">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6734">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6735">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6735">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6736">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6736">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6737">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6737">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6739">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6740">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6741">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6742">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6743">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6743">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6744">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6745">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6746">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6746">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6748">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6748">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6750">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6750">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6752">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6752">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6754">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6754">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="04ce8-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6755">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="04ce8-6756">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6756">Target</span></span> | <span data-ttu-id="04ce8-6757">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6757">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6758">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6758">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6759">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-6759">8</span></span> |
| <span data-ttu-id="04ce8-6760">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6760">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6762">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6762">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6763">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6763">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6764">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6764">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6765">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6765">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6766">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6766">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6767">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6767">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6769">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6769">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6770">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6770">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6771">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6771">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6773">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6773">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6775">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6775">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6776">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6776">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6777">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6777">Shader gather4</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6779">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6780">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6780">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6781">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6782">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6784">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6784">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6786">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6786">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6787">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6787">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6788">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6788">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6789">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6789">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6790">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6790">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6791">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6791">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6792">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6792">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6793">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6793">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6794">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6794">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6795">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6795">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6796">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6796">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6797">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6797">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6798">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6798">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6799">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6799">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6801">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6801">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6802">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6802">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6803">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6803">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6804">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6804">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6805">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6805">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6806">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6806">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6807">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6807">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6808">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6808">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6810">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6810">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6812">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6812">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6814">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6814">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6816">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6816">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="04ce8-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6817">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="04ce8-6818">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6818">Target</span></span> | <span data-ttu-id="04ce8-6819">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6819">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6820">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6820">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6821">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-6821">8</span></span> |
| <span data-ttu-id="04ce8-6822">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6822">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6824">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6824">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6825">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6825">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6826">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6826">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6827">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6827">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6828">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6828">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6829">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6829">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6831">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6831">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6832">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6832">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6833">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6833">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-6834">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6834">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6835">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6835">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6836">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6836">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6837">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6837">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-6838">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6838">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6839">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6839">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6840">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6840">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6841">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6841">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6842">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6842">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6843">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6843">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6844">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6844">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6845">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6845">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6846">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6846">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6847">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6847">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6848">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6848">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6849">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6849">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6850">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6850">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6851">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6851">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6852">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6852">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6853">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6853">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6854">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6854">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6855">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6855">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6856">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6856">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6858">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6858">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6859">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6859">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6860">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6860">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6861">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6861">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6862">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6862">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6863">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6863">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6864">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6864">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6865">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6865">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-6866">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6866">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6868">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6868">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-6869">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6869">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-6870">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6870">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="04ce8-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6871">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="04ce8-6872">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6872">Target</span></span> | <span data-ttu-id="04ce8-6873">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6873">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6874">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6874">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6875">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-6875">8</span></span> |
| <span data-ttu-id="04ce8-6876">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6876">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6878">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6878">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6879">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6879">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6880">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6880">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6881">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6881">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6882">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6882">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6883">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6883">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6885">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6885">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6886">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6886">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6887">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6887">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-6888">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6888">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6889">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6889">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6890">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6890">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6891">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6891">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-6892">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6892">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6893">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6893">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6894">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6894">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6895">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6895">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6896">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6896">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6897">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6897">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6898">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6898">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6899">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6899">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6900">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6900">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6901">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6901">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6902">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6902">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6903">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6903">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6904">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6904">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6905">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6905">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6906">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6906">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6907">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6907">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6908">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6908">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6909">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6909">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6910">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6910">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6912">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6912">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6913">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6913">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6914">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6914">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6915">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6915">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6916">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6916">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6917">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6917">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6918">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6918">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6919">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6919">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-6920">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6920">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6922">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6922">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-6923">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6923">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-6924">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6924">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="04ce8-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6925">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="04ce8-6926">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6926">Target</span></span> | <span data-ttu-id="04ce8-6927">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6927">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6928">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6928">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6929">8</span><span class="sxs-lookup"><span data-stu-id="04ce8-6929">8</span></span> |
| <span data-ttu-id="04ce8-6930">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6930">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6932">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6932">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6933">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6933">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6934">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6934">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6935">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6935">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6936">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6936">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6937">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6937">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6939">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6939">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6940">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6940">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6941">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6941">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-6942">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6942">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6943">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6943">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6944">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6944">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6945">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6945">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-6946">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-6946">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-6947">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-6947">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-6948">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-6948">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-6949">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6949">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6950">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6950">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6951">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-6951">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-6952">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-6952">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-6953">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-6953">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6954">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-6954">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-6955">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-6955">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-6956">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6956">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-6957">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6957">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-6958">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-6958">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-6959">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6959">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-6960">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-6960">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-6961">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6961">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-6962">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-6962">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6963">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-6963">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-6964">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-6964">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6966">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-6966">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6967">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-6967">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-6968">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-6968">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-6969">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-6969">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-6970">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-6970">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-6971">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-6971">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-6972">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-6972">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-6973">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6973">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-6974">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6974">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6976">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-6976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-6977">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6977">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-6978">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-6978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="04ce8-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6979">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="04ce8-6980">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-6980">Target</span></span> | <span data-ttu-id="04ce8-6981">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-6981">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-6982">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-6983">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-6983">16</span></span> |
| <span data-ttu-id="04ce8-6984">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-6984">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-6986">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-6986">Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6987">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6987">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6988">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-6988">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6989">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-6989">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-6990">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6990">Texture1D</span></span> | \- |
| <span data-ttu-id="04ce8-6991">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6991">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-6993">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-6993">Texture3D</span></span> | \- |
| <span data-ttu-id="04ce8-6994">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-6994">TextureCube</span></span> | \- |
| <span data-ttu-id="04ce8-6995">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-6995">Shader ld</span></span> | \- |
| <span data-ttu-id="04ce8-6996">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6996">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6997">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6997">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6998">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-6998">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-6999">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-6999">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-7000">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-7000">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-7001">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-7001">Mipmap</span></span> | \- |
| <span data-ttu-id="04ce8-7002">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-7002">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="04ce8-7003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-7003">RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-7004">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-7004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-7005">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-7005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-7006">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-7006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-7007">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-7007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-7008">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-7008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-7009">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-7009">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-7010">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-7011">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-7012">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-7012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-7013">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-7014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-7014">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-7015">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-7016">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-7017">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-7017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-7018">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-7018">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7020">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-7020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-7021">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-7021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="04ce8-7022">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-7022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="04ce8-7023">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-7023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="04ce8-7024">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-7024">Multisample Load</span></span> | \- |
| <span data-ttu-id="04ce8-7025">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-7025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-7026">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-7026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-7027">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-7028">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7028">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7030">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7030">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-7031">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-7031">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-7032">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-7032">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="04ce8-7033">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="04ce8-7033">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="04ce8-7034">Cible</span><span class="sxs-lookup"><span data-stu-id="04ce8-7034">Target</span></span> | <span data-ttu-id="04ce8-7035">Support</span><span class="sxs-lookup"><span data-stu-id="04ce8-7035">Support</span></span> |
| - | - |
| <span data-ttu-id="04ce8-7036">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="04ce8-7036">Bits Per Element (BPE)</span></span> | <span data-ttu-id="04ce8-7037">16</span><span class="sxs-lookup"><span data-stu-id="04ce8-7037">16</span></span> |
| <span data-ttu-id="04ce8-7038">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="04ce8-7038">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7040">Buffer</span><span class="sxs-lookup"><span data-stu-id="04ce8-7040">Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7042">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-7042">Input Assembler Vertex Buffer</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7044">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="04ce8-7044">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-7045">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="04ce8-7045">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="04ce8-7046">Texture1D</span><span class="sxs-lookup"><span data-stu-id="04ce8-7046">Texture1D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7048">Texture2D</span><span class="sxs-lookup"><span data-stu-id="04ce8-7048">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7050">Texture3D</span><span class="sxs-lookup"><span data-stu-id="04ce8-7050">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7052">TextureCube</span><span class="sxs-lookup"><span data-stu-id="04ce8-7052">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7054">Nuanceur LD</span><span class="sxs-lookup"><span data-stu-id="04ce8-7054">Shader ld</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7056">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="04ce8-7056">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7058">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="04ce8-7058">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="04ce8-7059">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="04ce8-7059">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="04ce8-7060">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="04ce8-7060">Shader gather4</span></span> | \- |
| <span data-ttu-id="04ce8-7061">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="04ce8-7061">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="04ce8-7062">MIP</span><span class="sxs-lookup"><span data-stu-id="04ce8-7062">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7064">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="04ce8-7064">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7066">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-7066">RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7068">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="04ce8-7068">Blendable RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7070">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="04ce8-7070">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="04ce8-7071">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="04ce8-7071">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="04ce8-7072">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="04ce8-7072">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-7073">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="04ce8-7073">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="04ce8-7074">UAV typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-7074">Typed UAV</span></span> | \- |
| <span data-ttu-id="04ce8-7075">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7075">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="04ce8-7076">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7076">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="04ce8-7077">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="04ce8-7077">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="04ce8-7078">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7078">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="04ce8-7079">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="04ce8-7079">UAV Atomic Cmp&Store / Cmp&Exch</span></span> | \- |
| <span data-ttu-id="04ce8-7080">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7080">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="04ce8-7081">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="04ce8-7081">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-7082">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="04ce8-7082">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="04ce8-7083">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="04ce8-7083">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7085">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="04ce8-7085">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7087">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="04ce8-7087">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7089">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="04ce8-7089">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7091">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="04ce8-7091">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="04ce8-7093">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="04ce8-7093">Multisample Load</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="04ce8-7095">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="04ce8-7095">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="04ce8-7096">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="04ce8-7096">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="04ce8-7097">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7097">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="04ce8-7098">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7098">Video Processor Input</span></span> | \- |
| <span data-ttu-id="04ce8-7099">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7099">Video Processor Output</span></span> | \- |
| <span data-ttu-id="04ce8-7100">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="04ce8-7100">Shared Resource</span></span> | \- |
| <span data-ttu-id="04ce8-7101">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="04ce8-7101">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="04ce8-7102">Mettre en forme les notes</span><span class="sxs-lookup"><span data-stu-id="04ce8-7102">Format notes</span></span>

<span data-ttu-id="04ce8-7103">L’objectif du format peut passer d’un niveau de fonctionnalité matériel à l’autre.</span><span class="sxs-lookup"><span data-stu-id="04ce8-7103">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="04ce8-7104"><sup>L</sup> : format non typé</span><span class="sxs-lookup"><span data-stu-id="04ce8-7104"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="04ce8-7105"><sup>PC</sup> : disposition partiellement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="04ce8-7105"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="04ce8-7106"><sup>FCS</sup> : mise en page entièrement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="04ce8-7106"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="04ce8-7107"><sup>FNS</sup> : mise en page entièrement typée, non stable et simple</span><span class="sxs-lookup"><span data-stu-id="04ce8-7107"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="04ce8-7108"><sup>PCC</sup> : disposition partiellement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="04ce8-7108"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="04ce8-7109"><sup>FCC</sup> : mise en page entièrement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="04ce8-7109"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="04ce8-7110"><sup>FNC</sup> : mise en page entièrement typée, non stable et complexe</span><span class="sxs-lookup"><span data-stu-id="04ce8-7110"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="04ce8-7111"><sup>V</sup> : format vidéo</span><span class="sxs-lookup"><span data-stu-id="04ce8-7111"><sup>V</sup> : video format</span></span>
</dt> </dl>

<span data-ttu-id="04ce8-7112">Les mémoires tampons d’arrière-plan et les analyses avec le format [**dxgi \_ \_ \_ float R16G16B16A16**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) contiennent des données de gamma linéaires.</span><span class="sxs-lookup"><span data-stu-id="04ce8-7112">Back buffers and scan outs with the [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) format contain linear-valued gamma data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04ce8-7113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04ce8-7113">Related topics</span></span>

[<span data-ttu-id="04ce8-7114">Niveaux de fonctionnalité matérielle D3D12</span><span class="sxs-lookup"><span data-stu-id="04ce8-7114">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

[<span data-ttu-id="04ce8-7115">**ID3D10Device::CheckFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="04ce8-7115">**ID3D10Device::CheckFormatSupport**</span></span>](/windows/win32/api/d3d10/nf-d3d10-id3d10device-checkformatsupport)

[<span data-ttu-id="04ce8-7116">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="04ce8-7116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
