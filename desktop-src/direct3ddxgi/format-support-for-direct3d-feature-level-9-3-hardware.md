---
description: Cette section spécifie les formats ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 le matériel 9,3.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 9.3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033416"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a><span data-ttu-id="622b3-103">Prise en charge des formats du matériel Direct3D de niveau de fonctionnalité 9.3</span><span class="sxs-lookup"><span data-stu-id="622b3-103">Format support for Direct3D Feature 10Level9 9.3 hardware</span></span>

<span data-ttu-id="622b3-104">Cette section spécifie les formats ([_\* DXGI_FORMAT_\* \* _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valeurs) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 9,3 Hardware.</span><span class="sxs-lookup"><span data-stu-id="622b3-104">This section specifies the formats ([_\*DXGI_FORMAT_\*\*_](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) values) that are supported in Direct3D Feature 10Level9 9.3 hardware.</span></span>

<span data-ttu-id="622b3-105">Le tableau récapitule la prise en charge des fonctionnalités à l’aide de la clé suivante.</span><span class="sxs-lookup"><span data-stu-id="622b3-105">The table summarizes the feature support, using the following key.</span></span>

| <span data-ttu-id="622b3-106">Symbole</span><span class="sxs-lookup"><span data-stu-id="622b3-106">Symbol</span></span>                            | <span data-ttu-id="622b3-107">Description</span><span class="sxs-lookup"><span data-stu-id="622b3-107">Description</span></span>                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="622b3-108">_ *-*\*</span><span class="sxs-lookup"><span data-stu-id="622b3-108">_ *-*\*</span></span>                             | <span data-ttu-id="622b3-109">Non autorisé ou non disponible.</span><span class="sxs-lookup"><span data-stu-id="622b3-109">Disallowed or not available.</span></span>                                                  |
| ![obligatoire](images/letter-r.jpg)  | <span data-ttu-id="622b3-111">Un support matériel est requis.</span><span class="sxs-lookup"><span data-stu-id="622b3-111">Hardware support is required.</span></span>                                                 |
| ![facultatif](images/letter-o.jpg)  | <span data-ttu-id="622b3-113">Prise en charge du matériel facultative, le format peut ou non être accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="622b3-113">Hardware support optional, the format may or may not be hardware accelerated.</span></span> |
| ![dépendants](images/letter-d.jpg) | <span data-ttu-id="622b3-115">Obligatoire si la fonctionnalité facultative associée est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="622b3-115">Required if related optional feature is supported.</span></span>                            |

<span data-ttu-id="622b3-116">Cette rubrique contient une section par format.</span><span class="sxs-lookup"><span data-stu-id="622b3-116">This topic contains a section per format.</span></span> <span data-ttu-id="622b3-117">Une *cible* de format (tables contenant une ligne par cible) peut être un type de ressource, une fonction intrinsèque HLSL ou une fonctionnalité particulière qui est dépendante d’un format particulier.</span><span class="sxs-lookup"><span data-stu-id="622b3-117">A format *target* (the tables contain one row per target) can be a resource type, an HLSL intrinsic function, or a particular functionality that is dependent on a particular format.</span></span>

<span data-ttu-id="622b3-118">Pour vérifier par programmation la prise en charge du format dans D3D11 et D3D12, consultez vérification de la [prise en charge des fonctionnalités matérielles](checking-hardware-feature-support.md).</span><span class="sxs-lookup"><span data-stu-id="622b3-118">To programmatically verify format support in D3D11 and D3D12, refer to [Checking hardware feature support](checking-hardware-feature-support.md).</span></span>

> [!NOTE] 
> <span data-ttu-id="622b3-119">Les nombres des formats sont principalement, mais pas tous, dans l’ordre numérique croissant, &mdash; certains ne sont pas triés par ordre numérique et sont répertoriés avec d’autres formats pertinents.</span><span class="sxs-lookup"><span data-stu-id="622b3-119">The numbers of the formats are mostly, but not all, in ascending numerical order&mdash;some are out of numerical order, and listed alongside other relevant formats.</span></span> <span data-ttu-id="622b3-120">Notez également que les *types* sans type dans un nom de format peuvent signifier un type *partiellement* typé, et non strictement typés (reportez-vous à la section Remarques sur le [format](#format-notes) à la fin de la rubrique).</span><span class="sxs-lookup"><span data-stu-id="622b3-120">Note also that *typeless* in a format name can mean *partially* typed, and not strictly typeless (refer to the [Format notes](#format-notes) section at the end of the topic).</span></span>

## <a name="dxgi_format_unknownsuplsup-0"></a><span data-ttu-id="622b3-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span><span class="sxs-lookup"><span data-stu-id="622b3-121">DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)</span></span>
| <span data-ttu-id="622b3-122">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-122">Target</span></span> | <span data-ttu-id="622b3-123">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-123">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-124">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-124">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-125">0</span><span class="sxs-lookup"><span data-stu-id="622b3-125">0</span></span> |
| <span data-ttu-id="622b3-126">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-126">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-127">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-127">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-128">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-128">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-129">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-129">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-130">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-130">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-131">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-131">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-132">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-132">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-133">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-133">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-134">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-135">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-135">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-136">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-136">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-137">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-137">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-138">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-138">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-139">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-139">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-140">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-140">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-141">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-141">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-142">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-142">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-143">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-143">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-144">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-144">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-145">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-145">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-146">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-146">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-147">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-147">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-148">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-148">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-149">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-149">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-150">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-150">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-151">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-151">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-152">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-152">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-153">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-153">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-154">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-154">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-155">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-155">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-156">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-156">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-157">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-157">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-158">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-158">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-159">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-159">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-160">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-160">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-161">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-161">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-162">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-163">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-163">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-164">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-165">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-166">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-167">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-168">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-169">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-169">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-170">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a><span data-ttu-id="622b3-171">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32A32 type (1)</span><span class="sxs-lookup"><span data-stu-id="622b3-171">DXGI_FORMAT_R32G32B32A32\_TYPELESS<sup>PCS</sup> (1)</span></span>
| <span data-ttu-id="622b3-172">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-172">Target</span></span> | <span data-ttu-id="622b3-173">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-173">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-174">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-175">128</span><span class="sxs-lookup"><span data-stu-id="622b3-175">128</span></span> |
| <span data-ttu-id="622b3-176">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-176">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-177">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-177">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-178">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-178">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-179">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-179">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-180">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-180">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-181">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-181">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-182">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-182">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-183">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-184">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-185">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-185">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-186">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-186">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-187">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-187">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-188">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-188">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-189">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-189">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-190">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-190">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-191">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-191">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-192">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-192">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-193">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-193">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-194">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-194">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-195">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-195">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-196">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-196">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-197">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-197">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-198">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-198">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-199">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-199">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-200">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-200">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-201">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-201">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-202">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-202">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-203">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-203">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-204">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-204">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-205">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-205">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-206">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-206">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-207">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-207">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-208">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-208">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-209">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-209">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-210">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-210">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-211">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-211">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-212">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-212">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-213">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-213">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-214">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-214">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-215">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-215">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-216">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-216">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-217">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-217">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-218">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-218">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-219">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-219">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-220">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-220">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a><span data-ttu-id="622b3-221">DXGI_FORMAT_R32G32B32A32 \_ float<sup>FNS</sup> (2)</span><span class="sxs-lookup"><span data-stu-id="622b3-221">DXGI_FORMAT_R32G32B32A32\_FLOAT<sup>FNS</sup> (2)</span></span>
| <span data-ttu-id="622b3-222">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-222">Target</span></span> | <span data-ttu-id="622b3-223">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-223">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-224">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-224">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-225">128</span><span class="sxs-lookup"><span data-stu-id="622b3-225">128</span></span> |
| <span data-ttu-id="622b3-226">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-226">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-228">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-228">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-229">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-229">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-231">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-231">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-232">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-232">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-233">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-233">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-234">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-234">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-236">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-236">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-238">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-238">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-240">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-240">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-242">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-242">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-243">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-243">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-244">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-244">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-245">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-245">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-246">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-246">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-247">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-247">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-249">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-249">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-251">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-253">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-253">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-254">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-254">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-255">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-255">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-256">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-256">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-257">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-257">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-258">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-258">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-259">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-259">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-260">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-260">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-261">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-261">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-262">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-262">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-263">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-263">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-264">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-264">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-265">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-265">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-266">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-266">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-267">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-267">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-269">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-269">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-271">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-271">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-273">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-273">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-275">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-275">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-277">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-277">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-278">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-278">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-279">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-279">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-280">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-280">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-281">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-281">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-282">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-282">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-283">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-283">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-284">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-284">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a><span data-ttu-id="622b3-285">DXGI_FORMAT_R32G32B32A32 \_ uint<sup>FNS</sup> (3)</span><span class="sxs-lookup"><span data-stu-id="622b3-285">DXGI_FORMAT_R32G32B32A32\_UINT<sup>FNS</sup> (3)</span></span>
| <span data-ttu-id="622b3-286">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-286">Target</span></span> | <span data-ttu-id="622b3-287">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-287">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-288">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-288">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-289">128</span><span class="sxs-lookup"><span data-stu-id="622b3-289">128</span></span> |
| <span data-ttu-id="622b3-290">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-290">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-291">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-291">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-292">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-292">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-293">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-293">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-294">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-294">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-295">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-295">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-296">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-296">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-297">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-297">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-298">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-298">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-299">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-299">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-300">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-300">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-301">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-301">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-302">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-302">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-303">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-303">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-304">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-304">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-305">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-305">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-306">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-306">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-307">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-307">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-308">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-308">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-309">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-309">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-310">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-310">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-311">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-311">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-312">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-312">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-313">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-313">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-314">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-314">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-315">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-315">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-316">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-316">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-317">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-317">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-318">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-318">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-319">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-319">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-320">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-320">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-321">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-321">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-322">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-322">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-323">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-323">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-324">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-324">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-325">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-325">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-326">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-326">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-327">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-327">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-328">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-328">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-329">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-329">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-330">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-330">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-331">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-331">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-332">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-332">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-333">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-333">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-334">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-334">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a><span data-ttu-id="622b3-335">DXGI_FORMAT_R32G32B32A32 \_ Saint<sup>FNS</sup> (4)</span><span class="sxs-lookup"><span data-stu-id="622b3-335">DXGI_FORMAT_R32G32B32A32\_SINT<sup>FNS</sup> (4)</span></span>
| <span data-ttu-id="622b3-336">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-336">Target</span></span> | <span data-ttu-id="622b3-337">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-337">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-338">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-338">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-339">128</span><span class="sxs-lookup"><span data-stu-id="622b3-339">128</span></span> |
| <span data-ttu-id="622b3-340">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-340">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-341">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-341">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-342">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-342">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-343">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-343">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-344">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-344">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-345">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-345">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-346">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-346">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-347">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-347">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-348">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-348">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-349">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-349">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-350">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-350">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-351">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-351">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-352">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-352">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-353">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-353">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-354">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-354">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-355">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-355">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-356">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-356">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-357">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-357">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-358">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-358">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-359">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-359">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-360">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-360">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-361">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-361">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-362">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-362">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-363">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-363">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-364">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-364">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-365">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-365">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-366">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-366">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-367">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-367">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-368">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-368">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-369">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-369">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-370">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-370">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-371">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-371">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-372">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-372">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-373">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-373">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-374">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-374">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-375">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-375">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-376">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-376">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-377">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-377">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-378">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-378">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-379">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-379">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-380">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-380">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-381">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-381">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-382">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-382">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-383">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-383">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-384">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-384">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a><span data-ttu-id="622b3-385">\_<sup>PC</sup> DXGI_FORMAT_R32G32B32 type (5)</span><span class="sxs-lookup"><span data-stu-id="622b3-385">DXGI_FORMAT_R32G32B32\_TYPELESS<sup>PCS</sup> (5)</span></span>
| <span data-ttu-id="622b3-386">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-386">Target</span></span> | <span data-ttu-id="622b3-387">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-387">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-388">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-388">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-389">96</span><span class="sxs-lookup"><span data-stu-id="622b3-389">96</span></span> |
| <span data-ttu-id="622b3-390">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-390">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-391">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-391">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-392">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-392">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-393">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-393">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-394">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-394">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-395">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-395">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-396">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-396">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-397">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-397">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-398">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-398">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-399">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-399">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-400">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-401">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-402">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-403">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-403">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-404">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-405">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-405">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-406">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-406">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-407">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-407">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-408">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-408">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-409">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-409">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-410">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-410">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-411">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-411">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-412">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-412">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-413">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-413">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-414">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-414">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-415">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-415">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-416">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-416">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-417">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-417">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-418">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-418">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-419">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-419">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-420">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-420">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-421">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-421">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-422">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-422">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-423">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-423">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-424">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-424">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-425">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-425">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-426">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-426">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-427">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-427">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-428">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-428">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-429">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-429">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-430">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-430">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-431">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-431">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-432">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-432">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-433">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-433">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-434">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-434">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a><span data-ttu-id="622b3-435">DXGI_FORMAT_R32G32B32 \_ float<sup>FNS</sup> (6)</span><span class="sxs-lookup"><span data-stu-id="622b3-435">DXGI_FORMAT_R32G32B32\_FLOAT<sup>FNS</sup> (6)</span></span>
| <span data-ttu-id="622b3-436">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-436">Target</span></span> | <span data-ttu-id="622b3-437">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-437">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-438">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-438">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-439">96</span><span class="sxs-lookup"><span data-stu-id="622b3-439">96</span></span> |
| <span data-ttu-id="622b3-440">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-440">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-442">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-442">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-443">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-443">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-445">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-445">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-446">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-446">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-447">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-447">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-448">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-448">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-449">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-449">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-450">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-450">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-451">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-451">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-452">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-452">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-453">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-454">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-455">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-455">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-456">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-457">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-457">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-458">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-458">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-459">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-459">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-460">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-460">Blendable RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-462">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-462">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-463">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-463">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-464">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-464">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-465">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-465">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-466">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-466">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-467">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-467">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-468">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-468">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-469">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-469">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-470">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-470">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-471">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-471">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-472">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-472">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-473">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-473">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-474">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-474">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-475">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-475">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-476">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-476">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-478">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-478">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-480">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-480">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-481">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-481">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-482">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-482">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-483">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-483">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-484">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-484">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-485">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-485">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-486">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-486">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-487">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-487">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-488">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-488">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-489">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-489">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a><span data-ttu-id="622b3-490">DXGI_FORMAT_R32G32B32 \_ uint<sup>FNS</sup> (7)</span><span class="sxs-lookup"><span data-stu-id="622b3-490">DXGI_FORMAT_R32G32B32\_UINT<sup>FNS</sup> (7)</span></span>
| <span data-ttu-id="622b3-491">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-491">Target</span></span> | <span data-ttu-id="622b3-492">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-492">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-493">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-493">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-494">96</span><span class="sxs-lookup"><span data-stu-id="622b3-494">96</span></span> |
| <span data-ttu-id="622b3-495">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-495">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-496">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-496">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-497">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-497">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-498">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-498">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-499">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-499">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-500">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-500">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-501">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-501">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-502">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-502">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-503">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-503">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-504">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-504">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-505">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-505">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-506">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-506">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-507">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-507">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-508">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-508">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-509">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-509">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-510">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-510">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-511">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-511">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-512">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-512">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-513">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-513">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-514">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-514">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-515">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-515">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-516">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-516">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-517">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-517">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-518">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-518">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-519">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-519">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-520">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-520">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-521">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-521">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-522">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-522">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-523">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-523">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-524">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-524">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-525">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-525">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-526">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-526">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-527">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-527">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-528">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-528">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-530">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-530">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-532">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-533">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-534">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-534">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-535">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-536">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-537">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-538">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-539">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-540">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-540">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-541">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a><span data-ttu-id="622b3-542">DXGI_FORMAT_R32G32B32 \_ Saint<sup>FNS</sup> (8)</span><span class="sxs-lookup"><span data-stu-id="622b3-542">DXGI_FORMAT_R32G32B32\_SINT<sup>FNS</sup> (8)</span></span>
| <span data-ttu-id="622b3-543">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-543">Target</span></span> | <span data-ttu-id="622b3-544">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-544">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-545">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-546">96</span><span class="sxs-lookup"><span data-stu-id="622b3-546">96</span></span> |
| <span data-ttu-id="622b3-547">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-547">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-548">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-548">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-549">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-550">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-551">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-552">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-553">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-554">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-555">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-556">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-557">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-558">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-559">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-560">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-560">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-561">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-562">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-562">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-563">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-564">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-565">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-566">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-567">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-568">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-569">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-570">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-570">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-571">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-572">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-574">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-576">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-577">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-578">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-579">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-580">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-580">4x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-582">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-582">8x Multisample RenderTarget</span></span> | ![dépendants](images/letter-d.jpg) |
| <span data-ttu-id="622b3-584">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-584">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-585">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-585">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-586">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-586">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-587">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-587">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-588">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-588">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-589">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-589">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-590">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-590">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-591">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-591">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-592">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-592">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-593">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-593">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a><span data-ttu-id="622b3-594">\_<sup>PC</sup> DXGI_FORMAT_R16G16B16A16 type (9)</span><span class="sxs-lookup"><span data-stu-id="622b3-594">DXGI_FORMAT_R16G16B16A16\_TYPELESS<sup>PCS</sup> (9)</span></span>
| <span data-ttu-id="622b3-595">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-595">Target</span></span> | <span data-ttu-id="622b3-596">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-596">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-597">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-597">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-598">64</span><span class="sxs-lookup"><span data-stu-id="622b3-598">64</span></span> |
| <span data-ttu-id="622b3-599">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-599">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-600">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-600">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-601">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-601">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-602">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-602">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-603">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-603">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-604">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-604">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-605">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-605">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-606">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-606">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-607">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-607">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-608">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-608">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-609">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-609">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-610">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-610">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-611">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-611">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-612">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-612">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-613">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-613">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-614">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-614">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-615">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-615">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-616">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-616">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-617">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-617">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-618">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-618">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-619">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-619">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-620">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-620">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-621">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-621">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-622">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-622">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-623">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-623">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-624">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-624">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-625">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-625">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-626">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-626">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-627">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-627">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-628">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-628">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-629">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-629">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-630">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-630">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-631">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-631">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-632">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-632">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-633">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-633">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-634">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-634">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-635">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-635">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-636">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-636">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-637">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-637">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-638">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-638">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-639">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-639">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-640">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-640">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-641">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-641">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-642">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-642">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-643">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-643">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a><span data-ttu-id="622b3-644">DXGI_FORMAT_R16G16B16A16 \_ float<sup>FNS</sup> (10)</span><span class="sxs-lookup"><span data-stu-id="622b3-644">DXGI_FORMAT_R16G16B16A16\_FLOAT<sup>FNS</sup> (10)</span></span>
| <span data-ttu-id="622b3-645">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-645">Target</span></span> | <span data-ttu-id="622b3-646">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-646">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-647">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-647">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-648">64</span><span class="sxs-lookup"><span data-stu-id="622b3-648">64</span></span> |
| <span data-ttu-id="622b3-649">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-649">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-651">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-651">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-652">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-652">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-654">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-654">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-655">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-655">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-656">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-656">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-657">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-657">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-659">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-659">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-661">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-663">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-663">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-665">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-665">Shader sample (any filter)</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-667">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-668">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-669">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-669">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-670">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-671">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-671">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-673">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-673">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-675">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-675">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-677">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-677">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-679">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-679">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-680">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-680">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-681">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-681">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-682">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-682">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-683">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-683">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-684">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-684">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-685">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-685">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-686">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-686">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-687">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-687">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-688">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-688">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-689">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-689">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-690">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-690">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-691">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-691">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-692">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-692">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-694">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-694">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-696">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-696">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-698">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-698">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-700">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-700">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-702">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-702">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-703">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-703">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-704">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-704">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-705">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-705">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-706">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-706">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-707">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-707">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-708">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-708">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-710">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-710">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a><span data-ttu-id="622b3-711">DXGI_FORMAT_R16G16B16A16 \_ UNORM<sup>FNS</sup> (11)</span><span class="sxs-lookup"><span data-stu-id="622b3-711">DXGI_FORMAT_R16G16B16A16\_UNORM<sup>FNS</sup> (11)</span></span>
| <span data-ttu-id="622b3-712">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-712">Target</span></span> | <span data-ttu-id="622b3-713">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-713">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-714">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-714">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-715">64</span><span class="sxs-lookup"><span data-stu-id="622b3-715">64</span></span> |
| <span data-ttu-id="622b3-716">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-716">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-718">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-718">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-719">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-719">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-720">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-720">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-721">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-721">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-722">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-722">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-723">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-723">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-725">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-725">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-727">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-727">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-729">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-729">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-731">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-731">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-733">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-733">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-734">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-734">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-735">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-735">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-736">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-736">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-737">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-737">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-739">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-739">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-741">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-741">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-743">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-744">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-745">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-746">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-747">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-748">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-748">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-749">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-750">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-751">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-752">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-754">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-755">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-756">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-757">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-757">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-759">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-759">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-761">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-761">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-763">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-763">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-765">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-765">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-767">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-767">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-768">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-768">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-769">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-769">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-770">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-770">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-771">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-771">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-772">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-772">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-773">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-773">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-774">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-774">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a><span data-ttu-id="622b3-775">DXGI_FORMAT_R16G16B16A16 \_ uint<sup>FNS</sup> (12)</span><span class="sxs-lookup"><span data-stu-id="622b3-775">DXGI_FORMAT_R16G16B16A16\_UINT<sup>FNS</sup> (12)</span></span>
| <span data-ttu-id="622b3-776">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-776">Target</span></span> | <span data-ttu-id="622b3-777">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-777">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-778">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-778">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-779">64</span><span class="sxs-lookup"><span data-stu-id="622b3-779">64</span></span> |
| <span data-ttu-id="622b3-780">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-780">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-781">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-781">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-782">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-782">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-783">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-783">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-784">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-784">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-785">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-785">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-786">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-786">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-787">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-787">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-788">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-788">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-789">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-789">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-790">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-790">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-791">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-791">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-792">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-792">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-793">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-793">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-794">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-794">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-795">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-795">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-796">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-796">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-797">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-797">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-798">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-798">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-799">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-799">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-800">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-800">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-801">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-801">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-802">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-802">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-803">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-803">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-804">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-804">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-805">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-805">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-806">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-806">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-807">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-807">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-808">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-808">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-809">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-809">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-810">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-810">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-811">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-811">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-812">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-812">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-813">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-813">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-814">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-814">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-815">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-815">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-816">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-816">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-817">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-817">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-818">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-818">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-819">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-819">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-820">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-820">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-821">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-821">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-822">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-822">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-823">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-823">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-824">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-824">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a><span data-ttu-id="622b3-825">DXGI_FORMAT_R16G16B16A16 \_ ronfler<sup>FNS</sup> (13)</span><span class="sxs-lookup"><span data-stu-id="622b3-825">DXGI_FORMAT_R16G16B16A16\_SNORM<sup>FNS</sup> (13)</span></span>
| <span data-ttu-id="622b3-826">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-826">Target</span></span> | <span data-ttu-id="622b3-827">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-827">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-828">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-828">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-829">64</span><span class="sxs-lookup"><span data-stu-id="622b3-829">64</span></span> |
| <span data-ttu-id="622b3-830">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-830">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-832">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-832">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-833">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-833">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-835">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-835">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-836">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-836">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-837">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-837">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-838">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-838">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-839">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-839">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-840">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-840">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-841">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-841">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-842">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-842">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-843">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-844">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-845">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-845">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-846">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-847">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-847">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-848">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-848">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-849">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-849">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-850">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-850">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-851">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-851">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-852">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-852">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-853">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-853">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-854">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-854">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-855">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-855">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-856">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-856">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-857">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-857">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-858">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-858">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-859">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-859">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-860">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-860">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-861">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-861">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-862">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-862">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-863">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-863">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-864">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-864">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-865">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-865">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-866">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-866">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-867">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-867">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-868">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-868">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-869">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-869">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-870">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-870">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-871">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-871">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-872">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-872">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-873">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-873">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-874">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-874">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-875">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-875">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-876">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-876">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a><span data-ttu-id="622b3-877">DXGI_FORMAT_R16G16B16A16 \_ Saint<sup>FNS</sup> (14)</span><span class="sxs-lookup"><span data-stu-id="622b3-877">DXGI_FORMAT_R16G16B16A16\_SINT<sup>FNS</sup> (14)</span></span>
| <span data-ttu-id="622b3-878">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-878">Target</span></span> | <span data-ttu-id="622b3-879">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-879">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-880">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-880">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-881">64</span><span class="sxs-lookup"><span data-stu-id="622b3-881">64</span></span> |
| <span data-ttu-id="622b3-882">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-882">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-884">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-884">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-885">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-885">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-887">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-887">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-888">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-888">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-889">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-889">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-890">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-890">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-891">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-891">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-892">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-892">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-893">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-893">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-894">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-894">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-895">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-895">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-896">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-896">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-897">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-897">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-898">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-898">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-899">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-899">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-900">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-900">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-901">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-901">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-902">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-902">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-903">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-903">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-904">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-904">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-905">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-905">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-906">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-906">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-907">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-907">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-908">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-908">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-909">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-909">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-910">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-910">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-911">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-911">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-912">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-912">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-913">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-913">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-914">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-914">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-915">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-915">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-916">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-916">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-917">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-917">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-918">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-918">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-919">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-919">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-920">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-920">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-921">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-921">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-922">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-922">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-923">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-923">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-924">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-924">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-925">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-925">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-926">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-926">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-927">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-927">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-928">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-928">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a><span data-ttu-id="622b3-929">\_<sup>PC</sup> DXGI_FORMAT_R32G32 type (15)</span><span class="sxs-lookup"><span data-stu-id="622b3-929">DXGI_FORMAT_R32G32\_TYPELESS<sup>PCS</sup> (15)</span></span>
| <span data-ttu-id="622b3-930">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-930">Target</span></span> | <span data-ttu-id="622b3-931">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-931">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-932">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-932">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-933">64</span><span class="sxs-lookup"><span data-stu-id="622b3-933">64</span></span> |
| <span data-ttu-id="622b3-934">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-934">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-935">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-935">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-936">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-936">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-937">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-937">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-938">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-938">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-939">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-939">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-940">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-940">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-941">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-941">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-942">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-942">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-943">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-943">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-944">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-944">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-945">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-945">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-946">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-946">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-947">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-947">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-948">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-948">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-949">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-949">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-950">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-950">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-951">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-951">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-952">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-952">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-953">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-953">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-954">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-954">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-955">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-955">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-956">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-956">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-957">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-957">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-958">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-958">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-959">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-959">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-960">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-960">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-961">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-961">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-962">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-962">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-963">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-963">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-964">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-964">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-965">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-965">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-966">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-966">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-967">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-967">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-968">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-968">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-969">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-969">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-970">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-970">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-971">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-971">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-972">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-972">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-973">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-973">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-974">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-974">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-975">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-975">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-976">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-976">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-977">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-977">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-978">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-978">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a><span data-ttu-id="622b3-979">DXGI_FORMAT_R32G32 \_ float<sup>FNS</sup> (16)</span><span class="sxs-lookup"><span data-stu-id="622b3-979">DXGI_FORMAT_R32G32\_FLOAT<sup>FNS</sup> (16)</span></span>
| <span data-ttu-id="622b3-980">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-980">Target</span></span> | <span data-ttu-id="622b3-981">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-981">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-982">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-982">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-983">64</span><span class="sxs-lookup"><span data-stu-id="622b3-983">64</span></span> |
| <span data-ttu-id="622b3-984">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-984">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-986">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-986">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-987">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-987">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-989">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-989">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-990">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-990">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-991">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-991">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-992">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-992">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-994">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-994">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-996">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-996">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-998">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-998">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1000">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1000">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1001">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1001">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1002">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1002">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1003">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1003">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1004">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1004">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1005">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1005">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1006">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1006">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1007">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1007">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1009">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1009">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1010">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1010">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1011">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1011">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1012">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1012">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1013">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1013">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1014">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1014">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1015">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1015">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1016">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1016">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1017">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1017">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1018">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1018">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1019">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1019">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1020">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1020">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1021">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1021">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1022">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1022">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1023">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1023">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1025">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1025">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1027">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1027">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1029">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1029">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1031">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1031">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1033">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1033">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1034">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1034">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1035">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1035">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1036">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1036">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1037">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1037">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1038">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1038">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1039">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1039">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1040">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1040">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a><span data-ttu-id="622b3-1041">DXGI_FORMAT_R32G32 \_ uint<sup>FNS</sup> (17)</span><span class="sxs-lookup"><span data-stu-id="622b3-1041">DXGI_FORMAT_R32G32\_UINT<sup>FNS</sup> (17)</span></span>
| <span data-ttu-id="622b3-1042">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1042">Target</span></span> | <span data-ttu-id="622b3-1043">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1043">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1044">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1044">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1045">64</span><span class="sxs-lookup"><span data-stu-id="622b3-1045">64</span></span> |
| <span data-ttu-id="622b3-1046">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1046">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1047">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1047">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1048">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1048">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1049">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1049">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1050">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1050">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1051">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1051">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1052">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1052">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1053">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1053">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1054">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1054">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1055">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1055">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1056">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1056">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1057">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1057">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1058">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1058">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1059">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1059">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1060">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1060">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1061">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1061">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1062">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1062">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1063">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1063">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1064">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1064">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1065">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1065">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1066">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1066">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1067">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1067">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1068">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1068">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1069">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1069">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1070">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1070">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1071">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1071">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1072">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1072">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1073">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1073">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1074">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1074">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1075">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1075">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1076">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1076">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1077">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1077">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1078">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1078">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1079">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1079">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1080">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1080">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1081">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1081">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1082">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1082">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1083">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1083">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1084">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1084">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1085">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1085">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1086">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1086">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1087">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1087">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1088">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1088">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1089">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1089">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1090">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1090">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a><span data-ttu-id="622b3-1091">DXGI_FORMAT_R32G32 \_ Saint<sup>FNS</sup> (18)</span><span class="sxs-lookup"><span data-stu-id="622b3-1091">DXGI_FORMAT_R32G32\_SINT<sup>FNS</sup> (18)</span></span>
| <span data-ttu-id="622b3-1092">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1092">Target</span></span> | <span data-ttu-id="622b3-1093">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1093">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1094">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1094">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1095">64</span><span class="sxs-lookup"><span data-stu-id="622b3-1095">64</span></span> |
| <span data-ttu-id="622b3-1096">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1096">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1097">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1097">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1098">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1098">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1099">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1099">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1100">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1100">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1101">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1101">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1102">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1102">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1103">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1103">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1104">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1104">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1105">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1105">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1106">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1106">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1107">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1107">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1108">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1108">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1109">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1109">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1110">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1110">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1111">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1111">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1112">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1112">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1113">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1113">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1114">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1114">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1115">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1115">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1116">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1116">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1117">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1117">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1118">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1118">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1119">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1119">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1120">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1120">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1121">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1121">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1122">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1122">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1123">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1123">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1124">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1124">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1125">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1125">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1126">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1126">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1127">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1127">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1128">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1128">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1129">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1129">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1130">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1130">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1131">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1131">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1132">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1132">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1133">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1133">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1134">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1134">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1135">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1135">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1136">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1136">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1137">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1137">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1138">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1138">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1139">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1139">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1140">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1140">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a><span data-ttu-id="622b3-1141">\_<sup>PC</sup> DXGI_FORMAT_R32G8X24 type (19)</span><span class="sxs-lookup"><span data-stu-id="622b3-1141">DXGI_FORMAT_R32G8X24\_TYPELESS<sup>PCS</sup> (19)</span></span>
| <span data-ttu-id="622b3-1142">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1142">Target</span></span> | <span data-ttu-id="622b3-1143">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1143">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1144">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1144">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1145">64</span><span class="sxs-lookup"><span data-stu-id="622b3-1145">64</span></span> |
| <span data-ttu-id="622b3-1146">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1146">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1147">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1147">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1148">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1148">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1149">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1149">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1150">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1150">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1151">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1151">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1152">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1152">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1153">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1153">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1154">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1154">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1155">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1155">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1156">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1156">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1157">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1157">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1158">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1158">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1159">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1159">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1160">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1160">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1161">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1161">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1162">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1162">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1163">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1163">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1164">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1164">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1165">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1165">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1166">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1166">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1167">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1167">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1168">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1168">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1169">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1169">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1170">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1170">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1171">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1171">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1172">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1172">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1173">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1173">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1174">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1174">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1175">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1175">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1176">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1176">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1177">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1177">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1178">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1178">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1179">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1179">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1180">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1180">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1181">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1181">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1182">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1182">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1183">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1183">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1184">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1184">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1185">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1185">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1186">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1186">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1187">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1187">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1188">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1188">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1189">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1189">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1190">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1190">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a><span data-ttu-id="622b3-1191">DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup>FNS</sup> (20)</span><span class="sxs-lookup"><span data-stu-id="622b3-1191">DXGI_FORMAT_D32\_FLOAT\_S8X24\_UINT<sup>FNS</sup> (20)</span></span>
| <span data-ttu-id="622b3-1192">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1192">Target</span></span> | <span data-ttu-id="622b3-1193">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1193">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1194">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1194">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1195">64</span><span class="sxs-lookup"><span data-stu-id="622b3-1195">64</span></span> |
| <span data-ttu-id="622b3-1196">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1196">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1197">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1197">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1198">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1198">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1199">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1199">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1200">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1200">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1201">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1201">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1202">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1202">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1203">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1203">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1204">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1204">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1205">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1205">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1206">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1206">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1207">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1207">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1208">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1208">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1209">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1209">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1210">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1210">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1211">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1211">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1212">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1212">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1213">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1213">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1214">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1214">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1215">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1215">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1216">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1216">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1217">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1217">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1218">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1218">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1219">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1219">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1220">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1220">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1221">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1221">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1222">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1222">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1223">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1223">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1224">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1224">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1225">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1225">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1226">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1226">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1227">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1227">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1228">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1228">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1229">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1229">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1230">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1230">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1231">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1231">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1232">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1232">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1233">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1233">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1234">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1234">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1235">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1235">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1236">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1236">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1237">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1237">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1238">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1238">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1239">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1239">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1240">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1240">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a><span data-ttu-id="622b3-1241">DXGI_FORMAT_R32 \_ float \_ X8X24 \_ de type<sup>FNS</sup> (21)</span><span class="sxs-lookup"><span data-stu-id="622b3-1241">DXGI_FORMAT_R32\_FLOAT\_X8X24\_TYPELESS<sup>FNS</sup> (21)</span></span>
| <span data-ttu-id="622b3-1242">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1242">Target</span></span> | <span data-ttu-id="622b3-1243">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1243">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1244">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1244">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1245">64</span><span class="sxs-lookup"><span data-stu-id="622b3-1245">64</span></span> |
| <span data-ttu-id="622b3-1246">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1246">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1247">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1247">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1248">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1248">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1249">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1249">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1250">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1250">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1251">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1251">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1252">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1252">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1253">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1253">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1254">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1254">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1255">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1255">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1256">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1256">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1257">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1257">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1258">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1258">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1259">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1259">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1260">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1260">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1261">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1261">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1262">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1262">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1263">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1263">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1264">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1264">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1265">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1265">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1266">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1266">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1267">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1267">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1268">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1268">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1269">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1269">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1270">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1270">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1271">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1271">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1272">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1272">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1273">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1273">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1274">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1274">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1275">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1275">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1276">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1276">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1277">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1277">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1278">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1278">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1279">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1280">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1281">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1282">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1283">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1283">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1284">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1285">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1286">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1287">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1288">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1289">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1289">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1290">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1290">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a><span data-ttu-id="622b3-1291">DXGI_FORMAT_X32 \_ \_ G8X24 \_ uint<sup>FNS</sup> (22)</span><span class="sxs-lookup"><span data-stu-id="622b3-1291">DXGI_FORMAT_X32\_TYPELESS\_G8X24\_UINT<sup>FNS</sup> (22)</span></span>
| <span data-ttu-id="622b3-1292">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1292">Target</span></span> | <span data-ttu-id="622b3-1293">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1293">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1294">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1294">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1295">64</span><span class="sxs-lookup"><span data-stu-id="622b3-1295">64</span></span> |
| <span data-ttu-id="622b3-1296">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1296">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1297">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1297">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1298">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1298">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1299">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1299">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1300">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1300">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1301">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1301">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1302">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1302">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1303">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1303">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1304">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1304">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1305">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1305">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1306">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1306">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1307">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1307">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1308">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1308">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1309">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1309">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1310">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1310">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1311">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1311">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1312">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1312">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1313">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1313">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1314">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1314">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1315">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1315">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1316">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1316">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1317">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1317">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1318">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1318">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1319">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1319">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1320">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1320">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1321">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1321">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1322">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1322">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1323">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1323">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1324">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1324">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1325">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1325">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1326">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1326">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1327">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1327">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1328">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1328">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1329">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1329">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1330">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1330">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1331">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1331">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1332">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1332">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1333">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1333">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1334">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1334">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1335">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1335">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1336">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1336">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1337">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1337">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1338">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1338">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1339">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1339">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1340">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1340">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a><span data-ttu-id="622b3-1341">\_<sup>PC</sup> DXGI_FORMAT_R10G10B10A2 type (23)</span><span class="sxs-lookup"><span data-stu-id="622b3-1341">DXGI_FORMAT_R10G10B10A2\_TYPELESS<sup>PCS</sup> (23)</span></span>
| <span data-ttu-id="622b3-1342">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1342">Target</span></span> | <span data-ttu-id="622b3-1343">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1343">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1344">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1344">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1345">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1345">32</span></span> |
| <span data-ttu-id="622b3-1346">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1346">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1347">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1347">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1348">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1348">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1349">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1349">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1350">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1350">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1351">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1351">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1352">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1352">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1353">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1353">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1354">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1354">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1355">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1355">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1356">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1356">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1357">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1357">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1358">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1358">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1359">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1359">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1360">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1360">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1361">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1361">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1362">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1362">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1363">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1363">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1364">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1364">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1365">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1365">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1366">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1366">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1367">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1367">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1368">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1368">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1369">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1369">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1370">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1370">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1371">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1371">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1372">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1372">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1373">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1373">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1374">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1374">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1375">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1375">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1376">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1376">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1377">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1377">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1378">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1378">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1379">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1379">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1380">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1380">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1381">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1381">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1382">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1382">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1383">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1383">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1384">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1384">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1385">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1385">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1386">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1386">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1387">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1387">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1388">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1388">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1389">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1389">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1390">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1390">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a><span data-ttu-id="622b3-1391">DXGI_FORMAT_R10G10B10A2 \_ UNORM<sup>FNS</sup> (24)</span><span class="sxs-lookup"><span data-stu-id="622b3-1391">DXGI_FORMAT_R10G10B10A2\_UNORM<sup>FNS</sup> (24)</span></span>
| <span data-ttu-id="622b3-1392">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1392">Target</span></span> | <span data-ttu-id="622b3-1393">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1393">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1394">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1394">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1395">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1395">32</span></span> |
| <span data-ttu-id="622b3-1396">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1396">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1397">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1397">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1398">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1398">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1399">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1399">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1400">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1400">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1401">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1401">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1402">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1402">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1403">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1403">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1404">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1404">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1405">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1405">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1406">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1406">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1407">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1407">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1408">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1408">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1409">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1409">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1410">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1410">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1411">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1411">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1412">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1412">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1413">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1413">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1414">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1414">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1415">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1415">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1416">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1416">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1417">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1417">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1418">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1418">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1419">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1419">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1420">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1420">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1421">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1421">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1422">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1422">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1423">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1423">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1424">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1424">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1425">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1425">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1426">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1426">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1427">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1427">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1428">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1428">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1429">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1429">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1430">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1430">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1431">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1431">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1432">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1432">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1433">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1433">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1434">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1434">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1435">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1435">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1436">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1436">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1437">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1437">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1438">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1438">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1439">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1439">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1441">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1441">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a><span data-ttu-id="622b3-1442">DXGI_FORMAT_R10G10B10A2 \_ uint<sup>FNS</sup> (25)</span><span class="sxs-lookup"><span data-stu-id="622b3-1442">DXGI_FORMAT_R10G10B10A2\_UINT<sup>FNS</sup> (25)</span></span>
| <span data-ttu-id="622b3-1443">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1443">Target</span></span> | <span data-ttu-id="622b3-1444">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1444">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1445">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1445">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1446">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1446">32</span></span> |
| <span data-ttu-id="622b3-1447">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1447">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1448">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1448">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1449">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1449">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1450">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1450">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1451">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1451">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1452">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1452">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1453">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1453">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1454">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1454">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1455">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1455">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1456">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1456">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1457">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1457">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1458">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1458">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1459">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1459">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1460">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1460">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1461">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1461">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1462">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1462">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1463">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1463">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1464">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1464">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1465">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1465">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1466">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1466">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1467">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1467">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1468">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1468">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1469">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1469">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1470">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1470">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1471">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1471">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1472">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1472">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1473">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1473">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1474">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1474">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1475">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1475">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1476">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1476">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1477">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1477">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1478">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1478">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1479">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1479">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1480">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1480">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1481">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1481">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1482">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1482">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1483">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1483">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1484">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1484">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1485">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1485">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1486">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1486">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1487">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1487">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1488">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1488">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1489">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1489">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1490">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1490">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1491">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a><span data-ttu-id="622b3-1492">DXGI_FORMAT_R10G10B10 \_ XR \_ \_ de décalage a2 \_ UNORM<sup>FNS</sup> (89)</span><span class="sxs-lookup"><span data-stu-id="622b3-1492">DXGI_FORMAT_R10G10B10\_XR\_BIAS\_A2\_UNORM<sup>FNS</sup> (89)</span></span>
| <span data-ttu-id="622b3-1493">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1493">Target</span></span> | <span data-ttu-id="622b3-1494">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1494">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1495">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1496">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1496">32</span></span> |
| <span data-ttu-id="622b3-1497">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1497">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1498">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1498">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1499">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1500">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1501">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1502">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1503">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1504">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1505">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1506">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1507">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1508">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1509">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1510">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1510">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1511">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1512">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1512">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1513">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1514">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1515">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1516">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1517">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1518">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1519">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1520">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1520">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1521">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1522">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1523">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1524">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1526">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1527">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1528">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1529">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1530">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1531">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1532">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1533">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1534">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1534">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1535">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1536">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1537">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1538">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1539">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1540">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1540">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1541">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a><span data-ttu-id="622b3-1542">DXGI_FORMAT_R11G11B10 \_ float<sup>FNS</sup> (26)</span><span class="sxs-lookup"><span data-stu-id="622b3-1542">DXGI_FORMAT_R11G11B10\_FLOAT<sup>FNS</sup> (26)</span></span>
| <span data-ttu-id="622b3-1543">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1543">Target</span></span> | <span data-ttu-id="622b3-1544">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1544">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1545">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1546">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1546">32</span></span> |
| <span data-ttu-id="622b3-1547">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1547">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1548">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1548">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1549">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1550">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1551">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1552">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1553">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1554">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1555">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1556">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1557">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1558">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1559">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1560">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1560">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1561">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1562">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1562">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1563">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1564">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1565">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1566">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1567">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1568">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1569">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1570">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1570">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1571">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1572">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1574">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1576">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1577">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1578">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1579">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1580">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1581">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1582">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1583">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1584">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1584">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1585">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1586">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1587">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1588">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1589">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1590">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1590">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1591">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a><span data-ttu-id="622b3-1592">\_<sup>PC</sup> DXGI_FORMAT_R8G8B8A8 type (27)</span><span class="sxs-lookup"><span data-stu-id="622b3-1592">DXGI_FORMAT_R8G8B8A8\_TYPELESS<sup>PCS</sup> (27)</span></span>
| <span data-ttu-id="622b3-1593">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1593">Target</span></span> | <span data-ttu-id="622b3-1594">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1594">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1595">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1596">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1596">32</span></span> |
| <span data-ttu-id="622b3-1597">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1597">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1598">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1598">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1599">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1600">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1601">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1602">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1603">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1604">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1605">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1606">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1607">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1608">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1609">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1610">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1610">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1611">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1612">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1612">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1613">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1614">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1615">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1616">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1617">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1618">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1619">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1620">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1620">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1621">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1622">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1624">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1626">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1627">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1628">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1629">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1630">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1631">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1632">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1633">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1634">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1634">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1635">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1636">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1637">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1638">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1639">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1640">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1640">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1641">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a><span data-ttu-id="622b3-1642">DXGI_FORMAT_R8G8B8A8 \_ UNORM<sup>FNS</sup> (28)</span><span class="sxs-lookup"><span data-stu-id="622b3-1642">DXGI_FORMAT_R8G8B8A8\_UNORM<sup>FNS</sup> (28)</span></span>
| <span data-ttu-id="622b3-1643">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1643">Target</span></span> | <span data-ttu-id="622b3-1644">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1644">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1645">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1646">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1646">32</span></span> |
| <span data-ttu-id="622b3-1647">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1647">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1649">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1649">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1650">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1650">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1652">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1652">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1653">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1653">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1654">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1654">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1655">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1655">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1657">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1657">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1659">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1659">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1661">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1661">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1663">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1663">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1665">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1665">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1666">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1666">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1667">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1667">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1668">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1668">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1669">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1669">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1671">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1671">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1673">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1675">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1675">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1677">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1677">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1678">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1678">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1679">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1679">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1680">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1680">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1681">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1681">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1682">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1682">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1683">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1683">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1684">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1684">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1685">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1685">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1686">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1686">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1687">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1687">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1688">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1688">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1689">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1689">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1690">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1690">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1692">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1692">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1694">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1694">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1696">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1696">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1698">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1698">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1700">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1700">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1701">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1701">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1703">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1703">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1704">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1704">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1705">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1705">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1707">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1707">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1709">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1709">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1711">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1711">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a><span data-ttu-id="622b3-1712">DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ sRVB<sup>FNS</sup> (29)</span><span class="sxs-lookup"><span data-stu-id="622b3-1712">DXGI_FORMAT_R8G8B8A8\_UNORM\_SRGB<sup>FNS</sup> (29)</span></span>
| <span data-ttu-id="622b3-1713">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1713">Target</span></span> | <span data-ttu-id="622b3-1714">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1714">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1715">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1715">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1716">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1716">32</span></span> |
| <span data-ttu-id="622b3-1717">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1717">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1719">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1719">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1720">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1720">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1721">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1721">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1722">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1722">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1723">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1723">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1724">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1724">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1726">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1726">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1728">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1728">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1730">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1730">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1732">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1732">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1734">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1734">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1735">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1735">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1736">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1736">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1737">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1737">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1738">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1738">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1740">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1740">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1742">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1744">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1744">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1746">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1746">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1747">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1747">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1748">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1748">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1749">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1749">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1750">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1750">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1751">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1751">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1752">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1752">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1753">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1753">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1754">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1754">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1755">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1755">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1756">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1756">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1757">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1757">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1758">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1758">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1759">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1759">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1761">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1761">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1763">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1763">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1765">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1765">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1767">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1767">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1769">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1769">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1770">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1770">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1772">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1772">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1773">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1773">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1774">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1774">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-1776">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1776">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1778">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1778">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1780">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1780">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a><span data-ttu-id="622b3-1781">DXGI_FORMAT_R8G8B8A8 \_ uint<sup>FNS</sup> (30)</span><span class="sxs-lookup"><span data-stu-id="622b3-1781">DXGI_FORMAT_R8G8B8A8\_UINT<sup>FNS</sup> (30)</span></span>
| <span data-ttu-id="622b3-1782">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1782">Target</span></span> | <span data-ttu-id="622b3-1783">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1783">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1784">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1784">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1785">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1785">32</span></span> |
| <span data-ttu-id="622b3-1786">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1786">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1788">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1788">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1789">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1789">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1791">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1791">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1792">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1792">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1793">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1793">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1794">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1794">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1795">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1795">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1796">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1796">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1797">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1797">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1798">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1798">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1799">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1799">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1800">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1800">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1801">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1801">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1802">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1802">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1803">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1803">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1804">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1804">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1805">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1805">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1806">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1806">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1807">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1807">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1808">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1808">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1809">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1809">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1810">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1810">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1811">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1811">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1812">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1812">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1813">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1813">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1814">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1814">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1815">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1815">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1816">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1816">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1817">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1817">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1818">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1818">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1819">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1819">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1820">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1820">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1821">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1821">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1822">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1822">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1823">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1823">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1824">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1824">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1825">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1825">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1826">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1826">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1827">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1827">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1828">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1828">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1829">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1829">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1830">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1830">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1831">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1831">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1832">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1832">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a><span data-ttu-id="622b3-1833">DXGI_FORMAT_R8G8B8A8 \_ ronfler<sup>FNS</sup> (31)</span><span class="sxs-lookup"><span data-stu-id="622b3-1833">DXGI_FORMAT_R8G8B8A8\_SNORM<sup>FNS</sup> (31)</span></span>
| <span data-ttu-id="622b3-1834">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1834">Target</span></span> | <span data-ttu-id="622b3-1835">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1835">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1836">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1836">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1837">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1837">32</span></span> |
| <span data-ttu-id="622b3-1838">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1838">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1840">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1840">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1841">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1841">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1842">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1842">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1843">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1843">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1844">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1844">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1845">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1845">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1847">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1847">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1848">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1848">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1850">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1850">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1852">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1852">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1854">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1854">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1855">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1855">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1856">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1856">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1857">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1857">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1858">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1858">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1860">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1860">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1861">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1861">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1862">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1862">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1863">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1863">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1864">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1864">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1865">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1865">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1866">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1866">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1867">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1867">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1868">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1868">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1869">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1869">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1870">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1870">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1871">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1871">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1872">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1872">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1873">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1873">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1874">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1874">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1875">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1875">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1876">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1876">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1878">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1878">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1879">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1879">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1880">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1880">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1881">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1881">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1882">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1882">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1883">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1883">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1884">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1884">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1885">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1885">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1886">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1886">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1887">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1887">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1888">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1888">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1889">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a><span data-ttu-id="622b3-1890">DXGI_FORMAT_R8G8B8A8 \_ Saint<sup>FNS</sup> (32)</span><span class="sxs-lookup"><span data-stu-id="622b3-1890">DXGI_FORMAT_R8G8B8A8\_SINT<sup>FNS</sup> (32)</span></span>
| <span data-ttu-id="622b3-1891">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1891">Target</span></span> | <span data-ttu-id="622b3-1892">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1892">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1893">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1894">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1894">32</span></span> |
| <span data-ttu-id="622b3-1895">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1895">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1896">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1896">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1897">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1897">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1898">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1898">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1899">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1899">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1900">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1900">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1901">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1901">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1902">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1902">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1903">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1903">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1904">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1904">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1905">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1905">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1906">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1906">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1907">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1907">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1908">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1908">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1909">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1909">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1910">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1910">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1911">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1911">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1912">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1912">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1913">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1913">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1914">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1914">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1915">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1915">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1916">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1916">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1917">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1917">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1918">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1918">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1919">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1919">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1920">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1920">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1921">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1921">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1922">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1922">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1923">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1923">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1924">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1924">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1925">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1925">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1926">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1926">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1927">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1927">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1928">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1928">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1929">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1929">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1930">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1930">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1931">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1931">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1932">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1932">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1933">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1933">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1934">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1934">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1935">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1935">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1936">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1936">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1937">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1937">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1938">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1938">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1939">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1939">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a><span data-ttu-id="622b3-1940">\_<sup>PC</sup> DXGI_FORMAT_R16G16 type (33)</span><span class="sxs-lookup"><span data-stu-id="622b3-1940">DXGI_FORMAT_R16G16\_TYPELESS<sup>PCS</sup> (33)</span></span>
| <span data-ttu-id="622b3-1941">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1941">Target</span></span> | <span data-ttu-id="622b3-1942">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1942">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1943">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1943">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1944">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1944">32</span></span> |
| <span data-ttu-id="622b3-1945">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1945">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-1946">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1946">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1947">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1947">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1948">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1948">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1949">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-1949">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1950">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-1950">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-1951">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-1951">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-1952">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-1952">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-1953">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-1953">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-1954">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-1954">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-1955">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-1955">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-1956">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-1956">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-1957">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-1957">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-1958">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-1958">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-1959">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-1959">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-1960">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-1960">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-1961">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-1961">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-1962">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1962">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1963">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-1963">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1964">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-1964">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-1965">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-1965">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-1966">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-1966">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1967">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-1967">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-1968">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-1968">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-1969">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1969">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-1970">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1970">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-1971">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-1971">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-1972">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1972">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-1973">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-1973">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-1974">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1974">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-1975">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-1975">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1976">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-1976">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-1977">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-1977">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-1978">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-1978">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1979">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-1979">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-1980">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-1980">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-1981">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-1981">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-1982">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-1982">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-1983">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-1983">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-1984">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-1984">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-1985">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1985">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-1986">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1986">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-1987">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-1987">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-1988">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-1988">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-1989">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-1989">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a><span data-ttu-id="622b3-1990">DXGI_FORMAT_R16G16 \_ float<sup>FNS</sup> (34)</span><span class="sxs-lookup"><span data-stu-id="622b3-1990">DXGI_FORMAT_R16G16\_FLOAT<sup>FNS</sup> (34)</span></span>
| <span data-ttu-id="622b3-1991">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-1991">Target</span></span> | <span data-ttu-id="622b3-1992">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-1992">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-1993">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-1993">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-1994">32</span><span class="sxs-lookup"><span data-stu-id="622b3-1994">32</span></span> |
| <span data-ttu-id="622b3-1995">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-1995">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-1997">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-1997">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-1998">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-1998">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2000">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2000">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2001">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2001">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2002">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2002">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2003">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2003">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2005">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2005">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2007">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2007">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2009">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2009">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2011">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2011">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2012">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2012">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2013">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2013">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2014">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2014">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2015">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2015">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2016">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2016">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2018">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2018">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2020">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2020">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2022">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2022">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2023">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2023">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2024">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2024">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2025">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2025">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2026">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2026">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2027">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2027">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2028">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2028">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2029">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2029">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2030">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2030">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2031">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2031">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2032">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2032">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2033">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2033">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2034">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2034">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2035">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2035">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2036">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2036">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2038">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2038">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2040">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2040">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2042">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2042">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2044">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2044">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2046">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2046">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2047">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2047">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2048">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2048">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2049">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2049">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2050">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2050">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2051">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2051">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2052">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2052">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2053">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2053">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a><span data-ttu-id="622b3-2054">DXGI_FORMAT_R16G16 \_ UNORM<sup>FNS</sup> (35)</span><span class="sxs-lookup"><span data-stu-id="622b3-2054">DXGI_FORMAT_R16G16\_UNORM<sup>FNS</sup> (35)</span></span>
| <span data-ttu-id="622b3-2055">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2055">Target</span></span> | <span data-ttu-id="622b3-2056">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2056">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2057">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2057">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2058">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2058">32</span></span> |
| <span data-ttu-id="622b3-2059">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2059">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2061">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2061">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2062">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2062">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2063">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2063">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2064">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2064">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2065">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2065">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2066">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2066">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2068">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2068">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2070">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2070">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2072">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2072">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2074">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2074">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2076">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2076">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2077">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2077">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2078">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2078">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2079">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2079">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2080">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2080">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2082">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2082">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2084">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2084">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2086">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2086">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2087">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2087">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2088">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2088">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2089">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2089">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2090">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2090">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2091">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2091">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2092">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2092">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2093">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2093">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2094">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2094">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2095">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2095">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2096">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2096">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2097">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2097">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2098">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2098">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2099">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2099">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2100">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2100">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2102">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2102">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2104">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2104">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2106">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2106">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2108">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2108">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2110">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2110">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2111">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2111">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2112">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2112">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2113">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2113">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2114">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2114">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2115">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2115">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2116">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2116">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2117">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2117">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a><span data-ttu-id="622b3-2118">DXGI_FORMAT_R16G16 \_ uint<sup>FNS</sup> (36)</span><span class="sxs-lookup"><span data-stu-id="622b3-2118">DXGI_FORMAT_R16G16\_UINT<sup>FNS</sup> (36)</span></span>
| <span data-ttu-id="622b3-2119">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2119">Target</span></span> | <span data-ttu-id="622b3-2120">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2120">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2121">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2121">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2122">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2122">32</span></span> |
| <span data-ttu-id="622b3-2123">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2123">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2124">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2124">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2125">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2125">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2126">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2126">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2127">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2127">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2128">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2128">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2129">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2129">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2130">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2130">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2131">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2132">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2132">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2133">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2133">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2134">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2134">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2135">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2135">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2136">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2136">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2137">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2137">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2138">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2138">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2139">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2139">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2140">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2140">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2141">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2141">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2142">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2142">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2143">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2143">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2144">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2145">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2146">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2146">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2147">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2148">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2149">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2150">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2152">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2153">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2154">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2155">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2156">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2156">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2157">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2157">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2158">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2158">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2159">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2159">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2160">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2160">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2161">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2161">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2162">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2162">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2163">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2163">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2164">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2164">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2165">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2165">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2166">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2166">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2167">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2167">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a><span data-ttu-id="622b3-2168">DXGI_FORMAT_R16G16 \_ ronfler<sup>FNS</sup> (37)</span><span class="sxs-lookup"><span data-stu-id="622b3-2168">DXGI_FORMAT_R16G16\_SNORM<sup>FNS</sup> (37)</span></span>
| <span data-ttu-id="622b3-2169">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2169">Target</span></span> | <span data-ttu-id="622b3-2170">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2170">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2171">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2171">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2172">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2172">32</span></span> |
| <span data-ttu-id="622b3-2173">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2173">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2175">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2175">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2176">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2176">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2178">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2178">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2179">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2179">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2180">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2180">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2181">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2181">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2183">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2183">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2185">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2185">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2187">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2187">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2189">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2189">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2191">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2191">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2192">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2192">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2193">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2193">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2194">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2194">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2195">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2195">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2197">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2197">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2198">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2198">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2199">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2199">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2200">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2200">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2201">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2201">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2202">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2202">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2203">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2203">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2204">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2204">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2205">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2205">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2206">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2206">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2207">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2207">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2208">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2208">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2209">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2209">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2210">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2210">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2211">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2211">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2212">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2212">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2213">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2213">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2215">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2215">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2216">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2216">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2217">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2217">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2218">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2218">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2219">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2219">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2220">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2220">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2221">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2221">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2222">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2222">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2223">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2223">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2224">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2224">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2225">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2225">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2226">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2226">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a><span data-ttu-id="622b3-2227">DXGI_FORMAT_R16G16 \_ Saint<sup>FNS</sup> (38)</span><span class="sxs-lookup"><span data-stu-id="622b3-2227">DXGI_FORMAT_R16G16\_SINT<sup>FNS</sup> (38)</span></span>
| <span data-ttu-id="622b3-2228">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2228">Target</span></span> | <span data-ttu-id="622b3-2229">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2229">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2230">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2230">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2231">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2231">32</span></span> |
| <span data-ttu-id="622b3-2232">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2232">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2234">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2234">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2235">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2235">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2237">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2237">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2238">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2238">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2239">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2239">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2240">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2240">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2241">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2241">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2242">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2242">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2243">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2243">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2244">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2244">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2245">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2245">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2246">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2246">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2247">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2247">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2248">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2248">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2249">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2249">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2250">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2250">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2251">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2251">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2252">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2252">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2253">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2253">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2254">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2254">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2255">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2255">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2256">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2256">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2257">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2257">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2258">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2258">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2259">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2259">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2260">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2260">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2261">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2261">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2262">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2262">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2263">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2263">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2264">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2264">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2265">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2265">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2266">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2266">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2267">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2267">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2268">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2268">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2269">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2269">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2270">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2270">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2271">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2271">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2272">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2272">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2273">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2273">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2274">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2274">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2275">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2275">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2276">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2276">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2277">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2277">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2278">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2278">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a><span data-ttu-id="622b3-2279">\_<sup>PC</sup> DXGI_FORMAT_R32 type (39)</span><span class="sxs-lookup"><span data-stu-id="622b3-2279">DXGI_FORMAT_R32\_TYPELESS<sup>PCS</sup> (39)</span></span>
| <span data-ttu-id="622b3-2280">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2280">Target</span></span> | <span data-ttu-id="622b3-2281">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2281">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2282">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2282">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2283">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2283">32</span></span> |
| <span data-ttu-id="622b3-2284">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2284">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2285">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2285">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2286">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2286">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2287">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2287">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2288">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2288">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2289">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2289">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2290">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2290">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2291">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2291">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2292">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2292">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2293">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2293">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2294">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2294">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2295">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2295">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2296">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2296">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2297">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2297">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2298">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2298">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2299">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2299">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2300">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2300">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2301">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2301">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2302">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2302">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2303">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2303">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2304">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2304">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2305">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2305">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2306">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2306">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2307">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2307">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2308">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2308">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2309">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2309">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2310">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2310">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2311">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2311">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2312">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2312">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2313">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2313">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2314">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2314">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2315">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2315">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2316">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2316">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2317">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2317">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2318">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2318">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2319">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2319">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2320">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2320">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2321">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2321">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2322">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2322">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2323">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2323">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2324">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2324">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2325">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2325">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2326">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2326">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2327">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2327">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2328">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2328">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a><span data-ttu-id="622b3-2329">DXGI_FORMAT_D32 \_ float<sup>FNS</sup> (40)</span><span class="sxs-lookup"><span data-stu-id="622b3-2329">DXGI_FORMAT_D32\_FLOAT<sup>FNS</sup> (40)</span></span>
| <span data-ttu-id="622b3-2330">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2330">Target</span></span> | <span data-ttu-id="622b3-2331">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2331">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2332">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2332">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2333">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2333">32</span></span> |
| <span data-ttu-id="622b3-2334">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2334">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2335">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2335">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2336">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2336">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2337">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2337">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2338">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2338">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2339">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2339">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2340">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2340">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2341">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2341">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2342">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2342">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2343">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2343">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2344">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2344">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2345">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2345">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2346">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2346">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2347">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2347">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2348">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2348">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2349">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2349">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2350">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2350">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2351">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2351">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2352">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2352">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2353">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2353">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2354">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2354">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2355">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2355">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2356">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2356">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2357">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2357">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2358">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2358">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2359">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2359">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2360">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2360">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2361">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2361">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2362">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2362">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2363">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2363">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2364">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2364">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2365">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2365">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2366">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2366">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2367">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2367">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2368">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2368">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2369">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2369">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2370">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2370">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2371">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2371">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2372">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2372">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2373">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2373">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2374">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2374">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2375">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2375">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2376">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2376">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2377">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2377">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2378">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2378">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a><span data-ttu-id="622b3-2379">DXGI_FORMAT_R32 \_ float<sup>FNS</sup> (41)</span><span class="sxs-lookup"><span data-stu-id="622b3-2379">DXGI_FORMAT_R32\_FLOAT<sup>FNS</sup> (41)</span></span>
| <span data-ttu-id="622b3-2380">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2380">Target</span></span> | <span data-ttu-id="622b3-2381">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2381">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2382">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2382">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2383">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2383">32</span></span> |
| <span data-ttu-id="622b3-2384">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2384">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2386">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2386">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2387">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2387">Input Assembler Vertex Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2389">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2390">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2391">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2392">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2394">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2394">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2396">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2396">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2398">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2398">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2400">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2400">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2401">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2401">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2402">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2402">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2403">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2403">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2404">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2404">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2405">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2405">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2407">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2407">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2409">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2409">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2411">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2411">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2412">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2412">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2413">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2413">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2414">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2414">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2415">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2415">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2416">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2416">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2417">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2417">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2418">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2418">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2419">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2419">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2420">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2420">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2421">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2421">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2422">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2422">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2423">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2423">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2424">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2424">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2425">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2425">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2427">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2427">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2429">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2429">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2431">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2431">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2433">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2433">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2435">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2435">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2436">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2436">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2437">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2437">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2438">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2438">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2439">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2439">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2440">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2440">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2441">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2441">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2442">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2442">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a><span data-ttu-id="622b3-2443">DXGI_FORMAT_R32 \_ uint<sup>FNS</sup> (42)</span><span class="sxs-lookup"><span data-stu-id="622b3-2443">DXGI_FORMAT_R32\_UINT<sup>FNS</sup> (42)</span></span>
| <span data-ttu-id="622b3-2444">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2444">Target</span></span> | <span data-ttu-id="622b3-2445">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2445">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2446">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2446">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2447">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2447">32</span></span> |
| <span data-ttu-id="622b3-2448">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2448">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2450">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2450">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2451">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2451">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2452">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2452">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2454">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2454">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2455">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2455">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2456">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2456">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2457">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2457">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2458">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2458">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2459">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2459">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2460">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2460">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2461">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2461">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2462">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2462">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2463">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2463">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2464">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2464">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2465">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2465">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2466">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2466">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2467">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2467">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2468">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2468">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2469">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2469">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2470">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2470">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2471">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2471">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2472">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2472">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2473">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2473">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2474">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2474">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2475">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2475">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2476">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2476">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2477">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2477">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2478">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2478">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2479">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2479">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2480">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2480">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2481">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2481">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2482">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2482">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2483">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2483">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2484">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2484">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2485">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2485">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2486">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2486">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2487">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2487">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2488">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2488">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2489">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2489">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2490">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2490">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2491">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2491">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2492">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2492">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2493">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2493">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2494">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2494">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a><span data-ttu-id="622b3-2495">DXGI_FORMAT_R32 \_ Saint<sup>FNS</sup> (43)</span><span class="sxs-lookup"><span data-stu-id="622b3-2495">DXGI_FORMAT_R32\_SINT<sup>FNS</sup> (43)</span></span>
| <span data-ttu-id="622b3-2496">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2496">Target</span></span> | <span data-ttu-id="622b3-2497">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2497">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2498">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2498">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2499">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2499">32</span></span> |
| <span data-ttu-id="622b3-2500">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2500">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2501">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2501">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2502">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2502">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2503">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2503">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2504">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2504">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2505">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2505">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2506">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2506">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2507">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2507">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2508">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2508">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2509">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2509">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2510">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2510">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2511">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2511">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2512">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2512">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2513">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2513">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2514">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2514">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2515">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2515">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2516">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2516">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2517">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2517">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2518">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2518">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2519">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2519">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2520">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2520">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2521">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2521">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2522">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2522">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2523">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2523">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2524">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2524">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2525">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2525">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2526">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2526">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2527">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2527">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2528">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2528">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2529">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2529">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2530">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2530">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2531">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2531">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2532">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2532">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2533">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2533">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2534">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2534">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2535">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2535">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2536">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2536">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2537">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2537">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2538">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2538">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2539">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2539">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2540">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2540">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2541">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2541">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2542">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2542">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2543">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2543">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2544">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2544">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a><span data-ttu-id="622b3-2545">\_<sup>PC</sup> DXGI_FORMAT_R24G8 type (44)</span><span class="sxs-lookup"><span data-stu-id="622b3-2545">DXGI_FORMAT_R24G8\_TYPELESS<sup>PCS</sup> (44)</span></span>
| <span data-ttu-id="622b3-2546">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2546">Target</span></span> | <span data-ttu-id="622b3-2547">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2547">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2548">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2548">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2549">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2549">32</span></span> |
| <span data-ttu-id="622b3-2550">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2550">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2551">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2551">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2552">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2552">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2553">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2553">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2554">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2554">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2555">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2555">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2556">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2556">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2557">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2557">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2558">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2558">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2559">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2559">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2560">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2560">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2561">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2561">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2562">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2562">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2563">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2563">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2564">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2564">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2565">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2565">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2566">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2566">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2567">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2567">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2568">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2568">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2569">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2569">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2570">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2570">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2571">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2571">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2572">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2572">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2573">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2573">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2574">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2574">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2575">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2575">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2576">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2576">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2577">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2577">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2578">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2578">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2579">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2579">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2580">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2580">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2581">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2581">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2582">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2582">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2583">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2583">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2584">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2584">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2585">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2585">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2586">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2586">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2587">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2587">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2588">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2588">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2589">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2589">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2590">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2590">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2591">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2591">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2592">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2592">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2593">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2593">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2594">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2594">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a><span data-ttu-id="622b3-2595">DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)</span><span class="sxs-lookup"><span data-stu-id="622b3-2595">DXGI_FORMAT_D24\_UNORM\_S8\_UINT<sup>FNS</sup> (45)</span></span>
| <span data-ttu-id="622b3-2596">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2596">Target</span></span> | <span data-ttu-id="622b3-2597">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2597">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2598">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2598">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2599">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2599">32</span></span> |
| <span data-ttu-id="622b3-2600">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2600">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2602">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2602">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2603">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2603">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2604">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2604">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2605">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2605">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2606">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2606">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2607">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2607">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2609">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2609">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2610">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2610">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2611">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2611">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2612">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2612">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2613">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2613">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2614">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2614">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2615">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2615">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2616">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2616">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2617">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2617">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2618">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2618">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2619">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2619">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2620">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2620">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2621">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2621">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2622">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2622">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2624">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2624">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2625">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2625">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2626">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2626">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2627">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2627">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2628">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2628">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2629">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2629">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2630">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2630">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2631">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2631">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2632">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2632">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2633">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2633">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2634">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2634">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2635">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2635">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2636">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2636">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2638">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2638">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2640">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2640">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-2642">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2642">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2643">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2643">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2644">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2644">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2645">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2645">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2646">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2646">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2647">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2647">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2648">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2648">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2649">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2649">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2650">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2650">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a><span data-ttu-id="622b3-2651">DXGI_FORMAT_R24 \_ UNORM \_ x8 \_ de type<sup>FNS</sup> (46)</span><span class="sxs-lookup"><span data-stu-id="622b3-2651">DXGI_FORMAT_R24\_UNORM\_X8\_TYPELESS<sup>FNS</sup> (46)</span></span>
| <span data-ttu-id="622b3-2652">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2652">Target</span></span> | <span data-ttu-id="622b3-2653">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2653">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2654">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2654">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2655">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2655">32</span></span> |
| <span data-ttu-id="622b3-2656">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2656">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2657">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2657">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2658">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2659">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2660">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2661">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2662">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2663">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2663">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2664">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2664">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2665">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2665">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2666">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2666">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2667">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2667">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2668">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2668">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2669">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2669">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2670">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2670">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2671">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2671">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2672">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2672">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2673">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2673">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2674">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2674">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2675">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2675">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2676">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2676">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2677">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2677">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2678">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2678">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2679">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2679">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2680">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2680">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2681">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2681">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2682">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2682">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2683">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2683">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2684">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2684">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2685">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2685">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2686">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2686">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2687">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2687">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2688">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2688">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2689">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2690">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2691">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2692">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2693">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2693">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2694">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2695">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2696">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2697">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2698">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2699">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2699">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2700">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2700">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a><span data-ttu-id="622b3-2701">DXGI_FORMAT_X24 \_ \_ G8 \_ UINT<sup>FNS</sup> (47)</span><span class="sxs-lookup"><span data-stu-id="622b3-2701">DXGI_FORMAT_X24\_TYPELESS\_G8\_UINT<sup>FNS</sup> (47)</span></span>
| <span data-ttu-id="622b3-2702">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2702">Target</span></span> | <span data-ttu-id="622b3-2703">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2703">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2704">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2704">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2705">32</span><span class="sxs-lookup"><span data-stu-id="622b3-2705">32</span></span> |
| <span data-ttu-id="622b3-2706">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2706">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2707">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2707">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2708">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2708">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2709">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2709">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2710">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2710">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2711">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2711">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2712">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2712">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2713">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2713">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2714">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2714">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2715">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2715">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2716">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2716">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2717">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2717">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2718">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2718">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2719">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2719">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2720">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2720">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2721">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2721">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2722">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2722">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2723">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2723">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2724">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2724">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2725">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2725">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2726">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2726">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2727">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2727">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2728">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2728">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2729">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2729">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2730">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2730">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2731">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2731">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2732">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2732">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2733">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2733">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2734">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2734">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2735">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2735">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2736">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2736">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2737">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2737">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2738">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2738">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2739">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2739">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2740">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2740">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2741">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2741">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2742">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2742">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2743">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2743">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2744">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2744">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2745">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2745">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2746">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2746">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2747">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2747">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2748">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2748">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2749">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2749">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2750">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2750">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a><span data-ttu-id="622b3-2751">\_<sup>PC</sup> DXGI_FORMAT_R8G8 type (48)</span><span class="sxs-lookup"><span data-stu-id="622b3-2751">DXGI_FORMAT_R8G8\_TYPELESS<sup>PCS</sup> (48)</span></span>
| <span data-ttu-id="622b3-2752">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2752">Target</span></span> | <span data-ttu-id="622b3-2753">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2753">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2754">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2754">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2755">16</span><span class="sxs-lookup"><span data-stu-id="622b3-2755">16</span></span> |
| <span data-ttu-id="622b3-2756">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2756">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2757">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2757">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2758">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2758">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2759">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2759">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2760">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2760">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2761">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2761">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2762">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2762">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2763">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2763">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2764">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2764">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2765">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2765">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2766">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2766">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2767">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2767">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2768">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2768">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2769">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2769">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2770">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2770">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2771">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2771">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2772">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2772">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2773">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2773">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2774">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2774">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2775">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2775">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2776">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2776">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2777">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2777">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2778">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2778">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2779">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2779">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2780">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2780">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2781">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2781">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2782">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2782">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2783">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2783">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2784">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2784">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2785">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2785">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2786">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2786">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2787">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2787">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2788">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2788">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2789">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2789">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2790">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2790">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2791">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2791">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2792">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2792">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2793">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2793">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2794">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2794">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2795">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2795">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2796">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2796">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2797">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2797">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2798">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2798">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2799">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2799">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2800">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2800">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a><span data-ttu-id="622b3-2801">DXGI_FORMAT_R8G8 \_ UNORM<sup>FNS</sup> (49)</span><span class="sxs-lookup"><span data-stu-id="622b3-2801">DXGI_FORMAT_R8G8\_UNORM<sup>FNS</sup> (49)</span></span>
| <span data-ttu-id="622b3-2802">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2802">Target</span></span> | <span data-ttu-id="622b3-2803">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2803">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2804">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2804">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2805">16</span><span class="sxs-lookup"><span data-stu-id="622b3-2805">16</span></span> |
| <span data-ttu-id="622b3-2806">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2806">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2808">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2808">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2809">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2810">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2811">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2812">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2813">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2815">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2815">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2816">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2816">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2817">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2817">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2819">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2819">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2821">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2821">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2822">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2822">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2823">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2823">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2824">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2824">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2825">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2825">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2826">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2826">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2827">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2827">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2829">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2829">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2831">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2831">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2832">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2832">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2833">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2833">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2834">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2834">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2835">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2835">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2836">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2836">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2837">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2837">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2838">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2838">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2839">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2839">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2840">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2840">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2841">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2841">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2842">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2842">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2843">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2843">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2844">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2844">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2846">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2846">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2847">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2847">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2848">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2848">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2849">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2849">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2850">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2850">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2851">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2851">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2852">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2852">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2853">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2853">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2854">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2854">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2855">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2855">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2856">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2856">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2858">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2858">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a><span data-ttu-id="622b3-2859">DXGI_FORMAT_R8G8 \_ uint<sup>FNS</sup> (50)</span><span class="sxs-lookup"><span data-stu-id="622b3-2859">DXGI_FORMAT_R8G8\_UINT<sup>FNS</sup> (50)</span></span>
| <span data-ttu-id="622b3-2860">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2860">Target</span></span> | <span data-ttu-id="622b3-2861">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2861">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2862">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2862">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2863">16</span><span class="sxs-lookup"><span data-stu-id="622b3-2863">16</span></span> |
| <span data-ttu-id="622b3-2864">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2864">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2865">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2865">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2866">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2866">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2867">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2867">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2868">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2868">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2869">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2869">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2870">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2870">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2871">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2871">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2872">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2872">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2873">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2873">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2874">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2874">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2875">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2875">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2876">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2876">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2877">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2877">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2878">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2878">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2879">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2879">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2880">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2880">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2881">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2881">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2882">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2882">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2883">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2883">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2884">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2884">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2885">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2885">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2886">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2886">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2887">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2887">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2888">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2888">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2889">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2889">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2890">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2890">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2891">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2891">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2892">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2892">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2893">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2893">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2894">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2894">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2895">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2895">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2896">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2896">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-2897">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2897">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2898">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2898">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2899">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2899">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2900">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2900">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2901">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2901">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2902">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2902">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2903">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2903">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2904">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2904">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2905">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2905">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2906">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2906">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2907">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2907">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2908">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2908">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a><span data-ttu-id="622b3-2909">DXGI_FORMAT_R8G8 \_ ronfler<sup>FNS</sup> (51)</span><span class="sxs-lookup"><span data-stu-id="622b3-2909">DXGI_FORMAT_R8G8\_SNORM<sup>FNS</sup> (51)</span></span>
| <span data-ttu-id="622b3-2910">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2910">Target</span></span> | <span data-ttu-id="622b3-2911">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2911">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2912">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2912">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2913">16</span><span class="sxs-lookup"><span data-stu-id="622b3-2913">16</span></span> |
| <span data-ttu-id="622b3-2914">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2914">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2916">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2916">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2917">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2917">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2918">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2918">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2919">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2919">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2920">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2920">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2921">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2921">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2923">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2923">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2924">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2924">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2925">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2925">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2927">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2927">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2929">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2929">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2930">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2930">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2931">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2931">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2932">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2932">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2933">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2933">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2935">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2935">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2936">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2936">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2937">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2937">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2938">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2938">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2939">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2939">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2940">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2940">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2941">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2941">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2942">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2942">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2943">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2943">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2944">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2944">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2945">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2945">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2946">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2946">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2947">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2947">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2948">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2948">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-2949">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2949">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2950">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-2950">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-2951">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-2951">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-2953">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-2953">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2954">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2954">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2955">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-2955">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-2956">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-2956">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-2957">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-2957">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-2958">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-2958">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-2959">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-2959">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-2960">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2960">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-2961">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2961">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-2962">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-2962">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-2963">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-2963">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-2964">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-2964">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a><span data-ttu-id="622b3-2965">DXGI_FORMAT_R8G8 \_ Saint<sup>FNS</sup> (52)</span><span class="sxs-lookup"><span data-stu-id="622b3-2965">DXGI_FORMAT_R8G8\_SINT<sup>FNS</sup> (52)</span></span>
| <span data-ttu-id="622b3-2966">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-2966">Target</span></span> | <span data-ttu-id="622b3-2967">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-2967">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-2968">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-2968">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-2969">16</span><span class="sxs-lookup"><span data-stu-id="622b3-2969">16</span></span> |
| <span data-ttu-id="622b3-2970">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-2970">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-2971">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-2971">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2972">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2972">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2973">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-2973">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2974">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-2974">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-2975">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-2975">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-2976">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-2976">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-2977">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-2977">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-2978">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-2978">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-2979">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-2979">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-2980">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-2980">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-2981">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-2981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-2982">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-2982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-2983">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-2983">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-2984">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-2984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-2985">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-2985">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-2986">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-2986">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-2987">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-2987">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2988">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-2988">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-2989">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-2989">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-2990">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-2990">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-2991">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-2991">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2992">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-2992">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-2993">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-2993">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-2994">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2994">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-2995">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2995">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-2996">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-2996">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-2997">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2997">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-2998">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-2998">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-2999">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-2999">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3000">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3000">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3001">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3001">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3002">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3002">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3003">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3003">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3004">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3004">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3005">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3005">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3006">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3006">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3007">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3007">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3008">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3008">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3009">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3009">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3010">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3010">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3011">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3011">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3012">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3012">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3013">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3013">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3014">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3014">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a><span data-ttu-id="622b3-3015">\_<sup>PC</sup> DXGI_FORMAT_R16 type (53)</span><span class="sxs-lookup"><span data-stu-id="622b3-3015">DXGI_FORMAT_R16\_TYPELESS<sup>PCS</sup> (53)</span></span>
| <span data-ttu-id="622b3-3016">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3016">Target</span></span> | <span data-ttu-id="622b3-3017">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3017">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3018">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3018">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3019">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3019">16</span></span> |
| <span data-ttu-id="622b3-3020">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3020">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3021">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3021">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3022">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3022">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3023">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3023">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3024">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3024">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3025">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3025">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3026">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3026">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3027">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3027">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3028">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3028">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3029">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3029">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3030">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3030">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3031">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3032">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3033">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3033">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3034">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3035">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3035">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3036">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3036">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3037">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3037">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3038">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3038">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3039">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3039">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3040">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3040">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3041">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3041">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3042">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3042">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3043">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3043">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3044">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3044">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3045">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3045">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3046">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3046">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3047">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3047">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3048">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3048">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3049">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3049">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3050">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3050">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3051">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3051">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3052">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3052">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3053">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3053">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3054">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3054">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3055">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3055">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3056">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3056">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3057">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3057">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3058">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3058">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3059">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3059">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3060">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3060">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3061">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3061">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3062">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3062">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3063">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3063">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3064">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3064">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a><span data-ttu-id="622b3-3065">DXGI_FORMAT_R16 \_ float<sup>FNS</sup> (54)</span><span class="sxs-lookup"><span data-stu-id="622b3-3065">DXGI_FORMAT_R16\_FLOAT<sup>FNS</sup> (54)</span></span>
| <span data-ttu-id="622b3-3066">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3066">Target</span></span> | <span data-ttu-id="622b3-3067">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3067">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3068">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3068">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3069">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3069">16</span></span> |
| <span data-ttu-id="622b3-3070">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3070">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3071">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3071">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3072">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3072">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3073">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3073">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3074">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3074">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3075">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3075">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3076">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3076">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3077">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3077">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3078">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3078">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3079">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3079">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3080">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3080">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3081">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3081">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3082">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3082">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3083">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3083">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3084">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3084">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3085">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3085">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3086">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3086">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3087">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3087">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3088">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3088">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3089">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3089">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3090">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3090">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3091">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3091">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3092">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3092">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3093">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3093">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3094">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3094">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3095">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3095">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3096">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3096">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3097">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3097">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3098">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3098">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3099">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3099">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3100">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3100">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3101">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3101">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3102">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3102">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3103">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3103">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3104">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3104">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3105">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3105">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3106">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3106">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3107">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3107">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3108">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3108">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3109">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3109">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3110">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3110">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3111">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3111">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3112">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3112">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3113">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3113">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3114">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3114">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a><span data-ttu-id="622b3-3115">DXGI_FORMAT_D16 \_ UNORM<sup>FNS</sup> (55)</span><span class="sxs-lookup"><span data-stu-id="622b3-3115">DXGI_FORMAT_D16\_UNORM<sup>FNS</sup> (55)</span></span>
| <span data-ttu-id="622b3-3116">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3116">Target</span></span> | <span data-ttu-id="622b3-3117">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3117">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3118">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3118">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3119">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3119">16</span></span> |
| <span data-ttu-id="622b3-3120">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3120">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3122">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3122">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3123">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3123">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3124">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3124">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3125">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3125">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3126">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3127">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3127">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3129">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3129">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3130">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3130">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3131">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3131">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3132">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3132">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3133">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3133">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3134">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3134">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3135">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3135">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3136">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3136">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3137">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3137">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3138">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3138">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3139">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3139">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3140">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3140">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3141">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3141">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3142">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3142">Depth/Stencil Target</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3144">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3144">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3145">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3145">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3146">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3146">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3147">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3147">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3148">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3148">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3149">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3149">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3150">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3150">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3151">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3151">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3152">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3152">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3153">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3153">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3154">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3154">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3155">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3155">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3156">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3156">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-3158">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3158">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-3160">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3160">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-3162">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3162">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3163">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3163">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3164">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3164">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3165">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3165">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3166">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3166">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3167">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3167">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3168">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3168">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3169">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3169">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3170">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3170">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a><span data-ttu-id="622b3-3171">DXGI_FORMAT_R16 \_ UNORM<sup>FNS</sup> (56)</span><span class="sxs-lookup"><span data-stu-id="622b3-3171">DXGI_FORMAT_R16\_UNORM<sup>FNS</sup> (56)</span></span>
| <span data-ttu-id="622b3-3172">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3172">Target</span></span> | <span data-ttu-id="622b3-3173">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3173">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3174">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3174">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3175">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3175">16</span></span> |
| <span data-ttu-id="622b3-3176">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3176">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3178">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3178">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3179">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3179">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3180">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3180">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3181">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3181">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3182">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3182">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3183">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3183">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3185">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3185">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3187">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3187">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3189">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3189">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3191">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3191">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3193">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3193">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3194">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3194">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3195">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3195">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3196">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3196">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3197">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3197">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3199">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3199">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3200">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3200">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3201">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3201">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3202">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3202">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3203">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3203">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3204">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3204">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3205">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3205">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3206">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3206">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3207">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3207">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3208">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3208">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3209">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3209">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3210">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3210">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3211">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3211">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3212">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3212">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3213">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3213">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3214">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3214">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3215">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3215">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3217">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3217">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3218">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3218">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3219">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3219">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3220">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3220">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3221">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3221">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3222">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3222">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3223">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3223">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3224">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3224">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3225">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3225">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3226">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3226">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3227">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3227">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3228">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3228">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a><span data-ttu-id="622b3-3229">DXGI_FORMAT_R16 \_ uint<sup>FNS</sup> (57)</span><span class="sxs-lookup"><span data-stu-id="622b3-3229">DXGI_FORMAT_R16\_UINT<sup>FNS</sup> (57)</span></span>
| <span data-ttu-id="622b3-3230">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3230">Target</span></span> | <span data-ttu-id="622b3-3231">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3231">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3232">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3232">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3233">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3233">16</span></span> |
| <span data-ttu-id="622b3-3234">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3234">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3236">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3236">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3237">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3237">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3238">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3238">Input Assembler Index Buffer</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3240">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3240">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3241">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3241">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3242">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3242">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3243">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3243">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3244">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3244">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3245">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3245">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3246">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3246">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3247">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3247">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3248">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3248">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3249">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3249">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3250">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3250">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3251">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3251">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3252">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3252">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3253">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3253">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3254">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3254">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3255">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3255">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3256">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3256">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3257">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3257">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3258">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3258">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3259">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3259">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3260">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3260">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3261">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3261">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3262">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3262">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3263">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3263">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3264">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3264">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3265">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3265">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3266">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3266">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3267">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3267">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3268">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3268">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3269">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3269">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3270">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3270">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3271">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3271">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3272">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3272">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3273">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3273">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3274">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3274">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3275">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3275">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3276">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3276">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3277">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3277">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3278">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3278">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3279">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3279">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3280">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3280">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a><span data-ttu-id="622b3-3281">DXGI_FORMAT_R16 \_ ronfler<sup>FNS</sup> (58)</span><span class="sxs-lookup"><span data-stu-id="622b3-3281">DXGI_FORMAT_R16\_SNORM<sup>FNS</sup> (58)</span></span>
| <span data-ttu-id="622b3-3282">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3282">Target</span></span> | <span data-ttu-id="622b3-3283">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3283">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3284">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3284">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3285">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3285">16</span></span> |
| <span data-ttu-id="622b3-3286">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3286">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3287">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3287">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3288">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3288">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3289">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3289">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3290">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3290">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3291">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3291">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3292">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3292">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3293">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3293">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3294">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3294">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3295">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3295">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3296">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3296">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3297">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3297">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3298">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3298">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3299">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3299">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3300">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3300">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3301">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3301">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3302">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3302">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3303">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3303">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3304">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3304">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3305">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3305">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3306">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3306">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3307">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3307">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3308">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3308">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3309">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3309">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3310">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3310">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3311">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3311">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3312">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3312">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3313">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3313">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3314">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3314">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3315">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3315">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3316">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3316">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3317">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3317">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3318">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3318">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3319">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3319">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3320">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3320">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3321">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3321">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3322">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3322">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3323">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3323">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3324">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3324">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3325">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3325">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3326">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3326">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3327">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3327">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3328">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3328">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3329">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3329">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3330">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3330">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a><span data-ttu-id="622b3-3331">DXGI_FORMAT_R16 \_ Saint<sup>FNS</sup> (59)</span><span class="sxs-lookup"><span data-stu-id="622b3-3331">DXGI_FORMAT_R16\_SINT<sup>FNS</sup> (59)</span></span>
| <span data-ttu-id="622b3-3332">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3332">Target</span></span> | <span data-ttu-id="622b3-3333">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3333">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3334">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3334">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3335">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3335">16</span></span> |
| <span data-ttu-id="622b3-3336">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3336">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3337">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3337">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3338">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3338">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3339">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3339">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3340">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3340">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3341">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3341">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3342">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3342">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3343">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3343">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3344">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3344">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3345">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3345">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3346">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3346">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3347">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3347">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3348">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3348">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3349">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3349">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3350">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3350">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3351">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3351">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3352">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3352">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3353">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3353">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3354">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3354">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3355">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3355">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3356">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3356">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3357">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3357">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3358">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3358">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3359">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3359">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3360">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3360">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3361">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3361">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3362">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3362">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3363">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3363">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3364">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3364">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3365">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3365">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3366">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3366">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3367">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3367">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3368">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3368">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3369">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3369">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3370">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3370">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3371">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3371">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3372">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3372">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3373">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3373">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3374">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3374">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3375">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3375">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3376">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3376">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3377">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3377">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3378">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3378">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3379">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3379">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3380">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3380">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a><span data-ttu-id="622b3-3381">\_<sup>PC</sup> DXGI_FORMAT_R8 type (60)</span><span class="sxs-lookup"><span data-stu-id="622b3-3381">DXGI_FORMAT_R8\_TYPELESS<sup>PCS</sup> (60)</span></span>
| <span data-ttu-id="622b3-3382">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3382">Target</span></span> | <span data-ttu-id="622b3-3383">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3383">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3384">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3384">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3385">8</span><span class="sxs-lookup"><span data-stu-id="622b3-3385">8</span></span> |
| <span data-ttu-id="622b3-3386">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3386">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3387">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3387">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3388">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3388">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3389">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3389">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3390">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3390">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3391">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3391">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3392">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3392">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3393">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3393">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3394">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3394">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3395">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3395">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3396">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3396">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3397">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3397">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3398">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3398">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3399">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3399">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3400">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3400">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3401">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3401">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3402">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3402">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3403">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3403">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3404">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3404">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3405">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3405">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3406">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3406">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3407">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3407">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3408">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3408">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3409">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3409">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3410">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3410">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3411">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3411">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3412">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3412">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3413">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3413">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3414">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3414">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3415">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3415">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3416">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3416">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3417">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3417">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3418">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3418">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3419">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3419">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3420">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3420">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3421">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3421">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3422">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3422">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3423">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3423">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3424">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3424">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3425">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3425">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3426">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3426">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3427">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3427">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3428">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3428">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3429">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3429">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3430">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3430">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a><span data-ttu-id="622b3-3431">DXGI_FORMAT_R8 \_ UNORM<sup>FNS</sup> (61)</span><span class="sxs-lookup"><span data-stu-id="622b3-3431">DXGI_FORMAT_R8\_UNORM<sup>FNS</sup> (61)</span></span>
| <span data-ttu-id="622b3-3432">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3432">Target</span></span> | <span data-ttu-id="622b3-3433">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3433">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3434">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3434">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3435">8</span><span class="sxs-lookup"><span data-stu-id="622b3-3435">8</span></span> |
| <span data-ttu-id="622b3-3436">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3436">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3438">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3438">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3439">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3439">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3440">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3440">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3441">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3441">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3442">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3442">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3443">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3443">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3445">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3445">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3447">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3447">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3449">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3449">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3451">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3451">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3453">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3453">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3454">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3454">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3455">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3455">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3456">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3456">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3457">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3457">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3459">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3459">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3460">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3460">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3462">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3462">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3464">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3464">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3465">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3465">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3466">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3466">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3467">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3467">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3468">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3468">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3469">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3469">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3470">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3470">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3471">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3471">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3472">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3472">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3473">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3473">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3474">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3474">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3475">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3475">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3476">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3476">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3477">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3477">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3479">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3479">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3480">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3480">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3481">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3481">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3482">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3482">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3483">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3483">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3484">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3484">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3485">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3485">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3486">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3486">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3487">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3487">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3488">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3488">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3489">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3489">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3491">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3491">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a><span data-ttu-id="622b3-3492">DXGI_FORMAT_R8 \_ uint<sup>FNS</sup> (62)</span><span class="sxs-lookup"><span data-stu-id="622b3-3492">DXGI_FORMAT_R8\_UINT<sup>FNS</sup> (62)</span></span>
| <span data-ttu-id="622b3-3493">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3493">Target</span></span> | <span data-ttu-id="622b3-3494">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3494">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3495">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3495">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3496">8</span><span class="sxs-lookup"><span data-stu-id="622b3-3496">8</span></span> |
| <span data-ttu-id="622b3-3497">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3497">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3498">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3498">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3499">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3499">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3500">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3500">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3501">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3501">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3502">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3502">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3503">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3503">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3504">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3504">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3505">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3505">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3506">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3506">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3507">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3507">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3508">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3508">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3509">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3509">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3510">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3510">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3511">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3511">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3512">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3512">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3513">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3513">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3514">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3514">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3515">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3515">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3516">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3516">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3517">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3517">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3518">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3518">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3519">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3519">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3520">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3520">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3521">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3521">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3522">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3522">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3523">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3523">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3524">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3524">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3525">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3525">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3526">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3526">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3527">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3527">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3528">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3528">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3529">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3529">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3530">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3530">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3531">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3531">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3532">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3532">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3533">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3533">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3534">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3534">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3535">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3535">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3536">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3536">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3537">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3537">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3538">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3538">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3539">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3539">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3540">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3540">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3541">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3541">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a><span data-ttu-id="622b3-3542">DXGI_FORMAT_R8 \_ ronfler<sup>FNS</sup> (63)</span><span class="sxs-lookup"><span data-stu-id="622b3-3542">DXGI_FORMAT_R8\_SNORM<sup>FNS</sup> (63)</span></span>
| <span data-ttu-id="622b3-3543">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3543">Target</span></span> | <span data-ttu-id="622b3-3544">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3544">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3545">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3545">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3546">8</span><span class="sxs-lookup"><span data-stu-id="622b3-3546">8</span></span> |
| <span data-ttu-id="622b3-3547">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3547">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3548">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3548">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3549">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3549">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3550">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3550">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3551">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3551">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3552">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3552">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3553">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3553">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3554">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3554">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3555">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3555">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3556">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3556">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3557">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3557">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3558">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3558">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3559">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3559">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3560">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3560">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3561">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3561">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3562">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3562">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3563">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3563">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3564">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3564">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3565">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3565">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3566">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3566">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3567">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3567">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3568">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3568">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3569">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3569">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3570">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3570">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3571">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3571">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3572">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3572">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3573">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3573">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3574">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3574">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3575">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3575">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3576">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3576">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3577">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3577">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3578">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3578">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3579">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3579">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3580">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3580">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3581">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3581">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3582">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3582">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3583">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3583">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3584">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3584">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3585">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3585">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3586">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3586">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3587">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3587">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3588">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3588">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3589">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3589">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3590">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3590">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3591">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3591">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a><span data-ttu-id="622b3-3592">DXGI_FORMAT_R8 \_ Saint<sup>FNS</sup> (64)</span><span class="sxs-lookup"><span data-stu-id="622b3-3592">DXGI_FORMAT_R8\_SINT<sup>FNS</sup> (64)</span></span>
| <span data-ttu-id="622b3-3593">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3593">Target</span></span> | <span data-ttu-id="622b3-3594">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3594">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3595">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3595">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3596">8</span><span class="sxs-lookup"><span data-stu-id="622b3-3596">8</span></span> |
| <span data-ttu-id="622b3-3597">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3597">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3598">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3598">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3599">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3599">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3600">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3600">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3601">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3601">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3602">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3602">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3603">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3603">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3604">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3605">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3606">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3607">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3608">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3609">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3610">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3610">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3611">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3612">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3612">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3613">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3614">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3615">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3616">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3617">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3618">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3619">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3620">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3620">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3621">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3622">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3624">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3626">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3627">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3628">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3629">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3629">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3630">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3630">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3631">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3631">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3632">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3632">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3633">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3633">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3634">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3634">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3635">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3635">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3636">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3636">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3637">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3637">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3638">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3638">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3639">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3639">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3640">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3640">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3641">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3641">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a><span data-ttu-id="622b3-3642">DXGI_FORMAT_A8 \_ UNORM<sup>FNS</sup> (65)</span><span class="sxs-lookup"><span data-stu-id="622b3-3642">DXGI_FORMAT_A8\_UNORM<sup>FNS</sup> (65)</span></span>
| <span data-ttu-id="622b3-3643">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3643">Target</span></span> | <span data-ttu-id="622b3-3644">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3644">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3645">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3645">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3646">8</span><span class="sxs-lookup"><span data-stu-id="622b3-3646">8</span></span> |
| <span data-ttu-id="622b3-3647">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3647">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3649">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3649">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3650">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3650">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3651">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3651">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3652">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3652">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3653">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3653">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3654">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3654">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3656">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3656">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3658">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3658">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3660">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3660">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3662">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3662">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3664">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3665">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3666">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3666">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3667">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3668">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3668">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3669">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3670">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3672">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3672">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3674">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3674">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3675">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3675">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3676">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3676">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3677">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3677">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3678">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3678">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3679">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3679">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3680">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3680">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3681">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3681">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3682">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3682">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3683">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3683">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3684">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3684">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3685">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3685">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3686">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3686">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3687">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3687">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3689">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3689">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3690">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3690">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3691">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3691">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3692">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3692">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3693">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3693">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3694">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3694">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3695">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3695">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3696">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3696">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3697">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3697">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3698">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3698">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3699">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3699">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3701">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a><span data-ttu-id="622b3-3702">DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)</span><span class="sxs-lookup"><span data-stu-id="622b3-3702">DXGI_FORMAT_R9G9B9E5\_SHAREDEXP<sup>FNC</sup> (67)</span></span>
| <span data-ttu-id="622b3-3703">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3703">Target</span></span> | <span data-ttu-id="622b3-3704">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3704">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3705">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3706">32</span><span class="sxs-lookup"><span data-stu-id="622b3-3706">32</span></span> |
| <span data-ttu-id="622b3-3707">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3707">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3708">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3708">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3709">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3709">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3710">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3710">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3711">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3711">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3712">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3712">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3713">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3713">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3714">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3714">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3715">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3715">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3716">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3716">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3717">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3717">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3718">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3718">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3719">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3719">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3720">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3720">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3721">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3721">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3722">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3722">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3723">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3723">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3724">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3724">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3725">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3725">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3726">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3726">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3727">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3727">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3728">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3728">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3729">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3729">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3730">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3730">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3731">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3731">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3732">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3732">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3733">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3733">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3734">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3734">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3735">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3735">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3736">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3736">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3737">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3737">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3738">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3738">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3739">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3739">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3740">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3740">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3741">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3741">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3742">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3742">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3743">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3743">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3744">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3744">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3745">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3745">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3746">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3746">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3747">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3747">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3748">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3748">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3749">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3749">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3750">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3750">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3751">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3751">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a><span data-ttu-id="622b3-3752">DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)</span><span class="sxs-lookup"><span data-stu-id="622b3-3752">DXGI_FORMAT_R8G8\_B8G8\_UNORM<sup>FNC</sup> (68)</span></span>
| <span data-ttu-id="622b3-3753">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3753">Target</span></span> | <span data-ttu-id="622b3-3754">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3754">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3755">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3755">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3756">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3756">16</span></span> |
| <span data-ttu-id="622b3-3757">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3757">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3758">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3758">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3759">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3759">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3760">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3760">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3761">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3761">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3762">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3762">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3763">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3763">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3764">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3764">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3765">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3765">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3766">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3766">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3767">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3767">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3768">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3768">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3769">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3769">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3770">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3770">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3771">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3771">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3772">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3772">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3773">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3773">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3774">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3774">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3775">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3775">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3776">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3776">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3777">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3777">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3778">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3778">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3779">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3779">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3780">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3780">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3781">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3781">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3782">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3782">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3783">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3783">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3784">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3784">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3785">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3785">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3786">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3786">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3787">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3787">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3788">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3788">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3789">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3789">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3790">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3790">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3791">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3791">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3792">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3792">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3793">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3793">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3794">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3794">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3795">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3795">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3796">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3796">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3797">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3797">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3798">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3798">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3799">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3799">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3800">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3800">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3801">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3801">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a><span data-ttu-id="622b3-3802">DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)</span><span class="sxs-lookup"><span data-stu-id="622b3-3802">DXGI_FORMAT_G8R8\_G8B8\_UNORM<sup>FNC</sup> (69)</span></span>
| <span data-ttu-id="622b3-3803">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3803">Target</span></span> | <span data-ttu-id="622b3-3804">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3804">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3805">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3805">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3806">16</span><span class="sxs-lookup"><span data-stu-id="622b3-3806">16</span></span> |
| <span data-ttu-id="622b3-3807">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3807">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3808">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3808">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3809">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3809">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3810">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3810">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3811">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3811">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3812">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3812">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3813">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3813">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3814">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3814">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3815">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3815">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3816">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3816">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3817">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3817">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3818">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3818">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3819">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3819">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3820">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3820">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3821">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3821">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3822">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3822">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3823">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3823">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3824">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3824">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3825">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3825">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3826">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3826">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3827">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3827">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3828">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3828">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3829">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3829">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3830">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3830">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3831">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3831">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3832">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3832">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3833">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3833">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3834">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3834">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3835">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3835">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3836">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3836">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3837">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3837">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3838">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3838">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3839">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3839">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3840">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3840">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3841">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3841">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3842">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3842">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3843">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3843">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3844">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3844">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3845">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3845">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3846">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3846">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3847">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3847">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3848">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3848">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3849">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3849">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3850">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3850">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3851">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3851">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a><span data-ttu-id="622b3-3852">DXGI_FORMAT_BC1 \_ <sup>PCC</sup> non typé (70)</span><span class="sxs-lookup"><span data-stu-id="622b3-3852">DXGI_FORMAT_BC1\_TYPELESS<sup>PCC</sup> (70)</span></span>
| <span data-ttu-id="622b3-3853">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3853">Target</span></span> | <span data-ttu-id="622b3-3854">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3854">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3855">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3855">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3856">4</span><span class="sxs-lookup"><span data-stu-id="622b3-3856">4</span></span> |
| <span data-ttu-id="622b3-3857">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3857">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-3858">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3858">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3859">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3859">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3860">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3860">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3861">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3861">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3862">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3862">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3863">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3863">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-3864">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3864">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3865">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3865">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-3866">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3866">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-3867">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3867">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-3868">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3868">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3869">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3869">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3870">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3870">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3871">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3871">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3872">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3872">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-3873">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3873">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3874">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3874">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3875">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3875">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3876">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3876">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3877">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3877">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3878">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3878">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3879">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3879">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3880">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3880">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3881">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3881">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3882">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3882">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3883">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3883">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3884">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3884">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3885">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3885">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3886">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3886">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3887">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3887">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3888">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3888">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3889">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3889">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-3890">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3890">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3891">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3891">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3892">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3892">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3893">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3893">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3894">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3894">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3895">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3895">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3896">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3896">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3897">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3897">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3898">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3898">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3899">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3899">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3900">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3900">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-3901">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3901">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a><span data-ttu-id="622b3-3902">DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)</span><span class="sxs-lookup"><span data-stu-id="622b3-3902">DXGI_FORMAT_BC1\_UNORM<sup>FNC</sup> (71)</span></span>
| <span data-ttu-id="622b3-3903">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3903">Target</span></span> | <span data-ttu-id="622b3-3904">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3904">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3905">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3905">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3906">4</span><span class="sxs-lookup"><span data-stu-id="622b3-3906">4</span></span> |
| <span data-ttu-id="622b3-3907">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3907">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3909">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3909">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3910">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3910">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3911">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3911">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3912">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3912">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3913">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3913">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3914">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3914">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3916">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3916">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3917">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3917">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3919">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3919">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3921">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3921">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3923">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3923">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3924">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3924">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3925">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3925">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3926">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3926">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3927">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3927">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3929">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3929">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3930">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3930">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3931">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3931">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3932">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3932">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3933">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3933">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3934">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3934">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3935">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3935">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3936">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3936">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3937">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3937">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3938">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3938">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3939">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3939">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3940">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3940">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3941">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3941">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-3942">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3942">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-3943">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3943">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3944">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-3944">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-3945">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-3945">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3947">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-3947">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3948">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3948">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3949">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-3949">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-3950">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-3950">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-3951">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-3951">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-3952">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-3952">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-3953">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-3953">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-3954">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3954">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-3955">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3955">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-3956">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-3956">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-3957">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-3957">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3959">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-3959">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a><span data-ttu-id="622b3-3960">DXGI_FORMAT_BC1 \_ UNORM \_ sRVB<sup>FNC</sup> (72)</span><span class="sxs-lookup"><span data-stu-id="622b3-3960">DXGI_FORMAT_BC1\_UNORM\_SRGB<sup>FNC</sup> (72)</span></span>
| <span data-ttu-id="622b3-3961">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-3961">Target</span></span> | <span data-ttu-id="622b3-3962">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-3962">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-3963">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-3963">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-3964">4</span><span class="sxs-lookup"><span data-stu-id="622b3-3964">4</span></span> |
| <span data-ttu-id="622b3-3965">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-3965">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3967">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-3967">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3968">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3968">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3969">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-3969">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3970">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-3970">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-3971">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-3971">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-3972">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-3972">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3974">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-3974">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-3975">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-3975">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3977">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-3977">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3979">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-3979">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3981">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-3981">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-3982">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-3982">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-3983">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-3983">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-3984">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-3984">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-3985">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-3985">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-3987">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-3987">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-3988">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-3988">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3989">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-3989">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-3990">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-3990">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-3991">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-3991">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-3992">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-3992">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3993">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-3993">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-3994">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-3994">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-3995">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3995">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-3996">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3996">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-3997">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-3997">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-3998">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-3998">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-3999">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-3999">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4000">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4000">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4001">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4001">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4002">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4002">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4003">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4003">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4005">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4005">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4006">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4006">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4007">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4007">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4008">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4008">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4009">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4009">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4010">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4010">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4011">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4011">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4012">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4012">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4013">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4013">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4014">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4014">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4015">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4015">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4017">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4017">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a><span data-ttu-id="622b3-4018">DXGI_FORMAT_BC2 \_ <sup>PCC</sup> non typé (73)</span><span class="sxs-lookup"><span data-stu-id="622b3-4018">DXGI_FORMAT_BC2\_TYPELESS<sup>PCC</sup> (73)</span></span>
| <span data-ttu-id="622b3-4019">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4019">Target</span></span> | <span data-ttu-id="622b3-4020">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4020">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4021">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4021">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4022">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4022">8</span></span> |
| <span data-ttu-id="622b3-4023">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4023">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4024">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4024">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4025">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4025">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4026">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4026">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4027">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4027">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4028">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4028">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4029">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4029">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4030">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4030">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4031">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4031">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4032">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4032">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4033">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4033">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4034">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4034">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4035">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4035">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4036">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4036">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4037">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4037">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4038">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4038">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4039">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4039">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4040">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4040">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4041">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4041">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4042">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4042">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4043">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4043">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4044">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4044">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4045">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4045">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4046">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4046">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4047">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4047">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4048">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4048">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4049">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4049">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4050">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4050">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4051">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4051">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4052">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4052">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4053">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4053">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4054">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4054">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4055">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4055">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4056">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4056">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4057">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4057">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4058">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4058">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4059">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4059">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4060">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4060">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4061">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4061">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4062">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4062">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4063">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4063">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4064">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4064">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4065">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4065">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4066">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4066">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4067">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4067">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a><span data-ttu-id="622b3-4068">DXGI_FORMAT_BC2 \_ UNORM<sup>FNC</sup> (74)</span><span class="sxs-lookup"><span data-stu-id="622b3-4068">DXGI_FORMAT_BC2\_UNORM<sup>FNC</sup> (74)</span></span>
| <span data-ttu-id="622b3-4069">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4069">Target</span></span> | <span data-ttu-id="622b3-4070">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4070">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4071">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4071">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4072">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4072">8</span></span> |
| <span data-ttu-id="622b3-4073">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4073">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4075">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4075">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4076">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4076">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4077">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4077">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4078">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4078">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4079">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4079">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4080">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4080">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4082">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4082">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4083">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4083">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4085">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4085">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4087">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4087">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4089">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4089">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4090">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4090">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4091">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4091">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4092">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4092">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4093">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4093">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4095">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4095">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4096">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4096">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4097">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4097">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4098">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4098">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4099">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4099">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4100">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4100">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4101">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4101">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4102">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4102">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4103">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4103">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4104">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4104">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4105">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4105">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4106">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4106">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4107">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4107">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4108">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4108">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4109">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4109">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4110">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4110">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4111">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4111">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4113">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4113">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4114">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4114">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4115">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4115">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4116">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4116">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4117">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4117">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4118">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4118">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4119">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4119">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4120">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4120">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4121">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4121">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4122">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4122">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4123">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4123">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4125">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4125">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a><span data-ttu-id="622b3-4126">DXGI_FORMAT_BC2 \_ UNORM \_ sRVB<sup>FNC</sup> (75)</span><span class="sxs-lookup"><span data-stu-id="622b3-4126">DXGI_FORMAT_BC2\_UNORM\_SRGB<sup>FNC</sup> (75)</span></span>
| <span data-ttu-id="622b3-4127">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4127">Target</span></span> | <span data-ttu-id="622b3-4128">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4128">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4129">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4129">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4130">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4130">8</span></span> |
| <span data-ttu-id="622b3-4131">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4131">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4133">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4133">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4134">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4134">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4135">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4135">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4136">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4136">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4137">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4137">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4138">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4138">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4140">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4141">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4141">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4143">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4143">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4145">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4145">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4147">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4147">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4148">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4148">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4149">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4149">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4150">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4150">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4151">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4151">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4153">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4153">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4154">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4154">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4155">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4155">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4156">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4156">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4157">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4157">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4158">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4158">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4159">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4159">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4160">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4160">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4161">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4161">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4162">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4162">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4163">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4163">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4164">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4164">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4165">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4165">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4166">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4166">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4167">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4167">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4168">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4168">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4169">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4169">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4171">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4171">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4172">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4172">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4173">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4173">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4174">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4174">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4175">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4175">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4176">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4176">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4177">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4177">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4178">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4178">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4179">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4179">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4180">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4180">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4181">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4181">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4183">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4183">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a><span data-ttu-id="622b3-4184">DXGI_FORMAT_BC3 \_ <sup>PCC</sup> non typé (76)</span><span class="sxs-lookup"><span data-stu-id="622b3-4184">DXGI_FORMAT_BC3\_TYPELESS<sup>PCC</sup> (76)</span></span>
| <span data-ttu-id="622b3-4185">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4185">Target</span></span> | <span data-ttu-id="622b3-4186">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4186">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4187">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4187">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4188">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4188">8</span></span> |
| <span data-ttu-id="622b3-4189">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4189">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4190">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4190">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4191">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4191">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4192">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4192">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4193">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4193">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4194">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4194">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4195">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4195">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4196">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4196">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4197">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4197">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4198">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4198">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4199">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4199">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4200">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4200">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4201">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4201">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4202">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4202">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4203">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4203">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4204">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4204">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4205">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4205">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4206">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4206">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4207">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4207">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4208">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4208">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4209">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4209">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4210">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4210">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4211">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4211">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4212">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4212">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4213">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4213">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4214">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4214">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4215">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4215">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4216">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4216">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4217">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4217">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4218">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4218">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4219">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4219">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4220">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4220">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4221">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4221">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4222">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4222">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4223">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4223">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4224">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4224">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4225">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4225">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4226">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4226">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4227">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4227">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4228">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4228">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4229">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4229">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4230">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4230">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4231">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4231">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4232">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4232">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4233">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4233">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a><span data-ttu-id="622b3-4234">DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)</span><span class="sxs-lookup"><span data-stu-id="622b3-4234">DXGI_FORMAT_BC3\_UNORM<sup>FNC</sup> (77)</span></span>
| <span data-ttu-id="622b3-4235">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4235">Target</span></span> | <span data-ttu-id="622b3-4236">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4236">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4237">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4237">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4238">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4238">8</span></span> |
| <span data-ttu-id="622b3-4239">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4239">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4241">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4241">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4242">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4242">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4243">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4243">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4244">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4244">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4245">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4245">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4246">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4246">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4248">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4248">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4249">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4249">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4251">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4251">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4253">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4253">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4255">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4255">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4256">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4256">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4257">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4257">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4258">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4258">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4259">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4259">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4261">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4261">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4262">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4262">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4263">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4263">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4264">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4264">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4265">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4265">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4266">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4266">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4267">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4267">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4268">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4268">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4269">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4269">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4270">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4270">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4271">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4271">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4272">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4272">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4273">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4273">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4274">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4274">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4275">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4275">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4276">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4276">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4277">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4277">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4279">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4279">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4280">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4280">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4281">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4281">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4282">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4282">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4283">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4283">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4284">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4284">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4285">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4285">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4286">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4286">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4287">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4287">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4288">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4288">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4289">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4289">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4291">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4291">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a><span data-ttu-id="622b3-4292">DXGI_FORMAT_BC3 \_ UNORM \_ sRVB<sup>FNC</sup> (78)</span><span class="sxs-lookup"><span data-stu-id="622b3-4292">DXGI_FORMAT_BC3\_UNORM\_SRGB<sup>FNC</sup> (78)</span></span>
| <span data-ttu-id="622b3-4293">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4293">Target</span></span> | <span data-ttu-id="622b3-4294">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4294">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4295">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4295">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4296">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4296">8</span></span> |
| <span data-ttu-id="622b3-4297">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4297">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4299">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4299">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4300">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4300">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4301">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4301">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4302">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4302">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4303">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4303">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4304">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4304">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4306">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4306">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4307">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4307">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4309">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4309">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4311">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4311">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4313">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4313">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4314">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4314">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4315">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4315">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4316">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4316">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4317">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4317">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4319">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4319">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4320">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4320">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4321">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4321">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4322">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4322">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4323">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4323">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4324">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4324">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4325">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4325">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4326">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4326">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4327">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4327">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4328">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4328">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4329">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4329">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4330">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4330">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4331">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4331">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4332">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4332">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4333">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4333">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4334">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4334">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4335">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4335">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4337">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4337">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4338">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4338">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4339">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4339">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4340">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4340">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4341">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4341">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4342">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4342">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4343">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4343">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4344">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4344">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4345">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4345">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4346">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4346">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4347">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4347">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4349">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4349">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a><span data-ttu-id="622b3-4350">DXGI_FORMAT_BC4 \_ <sup>PCC</sup> non typé (79)</span><span class="sxs-lookup"><span data-stu-id="622b3-4350">DXGI_FORMAT_BC4\_TYPELESS<sup>PCC</sup> (79)</span></span>
| <span data-ttu-id="622b3-4351">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4351">Target</span></span> | <span data-ttu-id="622b3-4352">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4352">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4353">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4353">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4354">4</span><span class="sxs-lookup"><span data-stu-id="622b3-4354">4</span></span> |
| <span data-ttu-id="622b3-4355">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4355">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4356">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4356">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4357">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4357">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4358">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4358">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4359">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4359">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4360">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4360">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4361">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4361">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4362">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4362">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4363">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4363">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4364">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4364">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4365">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4365">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4366">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4366">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4367">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4367">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4368">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4368">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4369">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4369">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4370">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4370">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4371">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4371">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4372">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4372">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4373">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4373">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4374">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4374">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4375">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4375">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4376">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4376">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4377">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4377">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4378">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4378">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4379">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4379">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4380">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4380">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4381">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4381">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4382">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4382">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4383">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4383">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4384">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4384">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4385">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4385">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4386">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4386">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4387">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4387">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4388">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4388">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4389">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4389">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4390">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4390">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4391">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4391">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4392">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4392">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4393">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4393">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4394">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4394">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4395">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4395">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4396">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4396">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4397">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4397">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4398">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4398">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4399">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4399">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a><span data-ttu-id="622b3-4400">DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)</span><span class="sxs-lookup"><span data-stu-id="622b3-4400">DXGI_FORMAT_BC4\_UNORM<sup>FNC</sup> (80)</span></span>
| <span data-ttu-id="622b3-4401">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4401">Target</span></span> | <span data-ttu-id="622b3-4402">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4402">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4403">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4403">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4404">4</span><span class="sxs-lookup"><span data-stu-id="622b3-4404">4</span></span> |
| <span data-ttu-id="622b3-4405">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4405">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4406">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4406">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4407">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4407">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4408">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4408">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4409">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4409">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4410">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4410">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4411">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4411">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4412">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4412">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4413">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4413">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4414">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4414">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4415">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4415">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4416">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4416">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4417">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4417">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4418">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4418">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4419">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4419">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4420">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4420">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4421">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4421">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4422">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4422">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4423">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4423">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4424">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4424">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4425">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4425">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4426">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4426">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4427">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4427">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4428">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4428">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4429">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4429">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4430">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4430">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4431">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4431">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4432">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4432">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4433">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4433">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4434">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4434">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4435">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4435">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4436">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4436">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4437">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4437">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4438">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4438">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4439">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4439">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4440">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4440">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4441">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4441">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4442">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4442">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4443">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4443">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4444">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4444">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4445">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4445">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4446">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4446">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4447">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4447">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4448">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4448">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4449">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4449">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a><span data-ttu-id="622b3-4450">DXGI_FORMAT_BC4 \_ ronfler<sup>FNC</sup> (81)</span><span class="sxs-lookup"><span data-stu-id="622b3-4450">DXGI_FORMAT_BC4\_SNORM<sup>FNC</sup> (81)</span></span>
| <span data-ttu-id="622b3-4451">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4451">Target</span></span> | <span data-ttu-id="622b3-4452">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4452">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4453">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4453">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4454">4</span><span class="sxs-lookup"><span data-stu-id="622b3-4454">4</span></span> |
| <span data-ttu-id="622b3-4455">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4455">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4456">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4456">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4457">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4457">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4458">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4458">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4459">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4459">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4460">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4460">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4461">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4461">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4462">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4462">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4463">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4463">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4464">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4464">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4465">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4465">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4466">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4466">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4467">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4467">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4468">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4468">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4469">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4469">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4470">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4470">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4471">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4471">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4472">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4472">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4473">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4473">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4474">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4474">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4475">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4475">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4476">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4476">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4477">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4477">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4478">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4478">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4479">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4479">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4480">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4480">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4481">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4481">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4482">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4482">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4483">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4483">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4484">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4484">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4485">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4485">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4486">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4486">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4487">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4487">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4488">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4488">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4489">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4489">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4490">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4490">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4491">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4491">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4492">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4492">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4493">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4493">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4494">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4494">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4495">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4495">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4496">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4496">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4497">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4497">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4498">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4498">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4499">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4499">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a><span data-ttu-id="622b3-4500">DXGI_FORMAT_BC5 \_ <sup>PCC</sup> non typé (82)</span><span class="sxs-lookup"><span data-stu-id="622b3-4500">DXGI_FORMAT_BC5\_TYPELESS<sup>PCC</sup> (82)</span></span>
| <span data-ttu-id="622b3-4501">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4501">Target</span></span> | <span data-ttu-id="622b3-4502">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4502">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4503">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4503">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4504">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4504">8</span></span> |
| <span data-ttu-id="622b3-4505">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4505">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4506">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4506">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4507">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4507">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4508">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4508">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4509">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4509">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4510">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4510">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4511">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4511">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4512">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4512">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4513">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4513">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4514">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4514">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4515">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4515">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4516">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4516">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4517">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4517">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4518">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4518">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4519">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4519">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4520">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4520">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4521">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4521">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4522">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4522">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4523">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4523">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4524">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4524">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4525">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4525">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4526">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4526">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4527">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4527">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4528">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4528">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4529">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4529">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4530">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4530">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4531">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4531">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4532">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4532">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4533">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4533">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4534">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4534">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4535">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4535">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4536">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4536">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4537">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4537">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4538">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4538">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4539">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4539">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4540">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4540">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4541">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4541">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4542">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4542">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4543">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4543">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4544">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4544">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4545">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4545">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4546">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4546">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4547">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4547">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4548">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4548">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4549">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4549">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a><span data-ttu-id="622b3-4550">DXGI_FORMAT_BC5 \_ UNORM<sup>FNC</sup> (83)</span><span class="sxs-lookup"><span data-stu-id="622b3-4550">DXGI_FORMAT_BC5\_UNORM<sup>FNC</sup> (83)</span></span>
| <span data-ttu-id="622b3-4551">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4551">Target</span></span> | <span data-ttu-id="622b3-4552">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4552">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4553">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4553">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4554">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4554">8</span></span> |
| <span data-ttu-id="622b3-4555">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4555">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4556">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4556">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4557">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4557">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4558">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4558">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4559">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4559">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4560">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4560">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4561">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4561">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4562">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4562">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4563">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4563">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4564">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4564">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4565">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4565">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4566">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4566">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4567">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4567">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4568">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4568">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4569">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4569">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4570">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4570">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4571">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4571">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4572">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4572">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4573">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4573">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4574">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4574">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4575">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4575">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4576">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4576">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4577">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4577">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4578">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4578">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4579">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4579">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4580">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4580">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4581">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4581">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4582">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4582">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4583">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4583">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4584">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4584">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4585">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4585">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4586">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4586">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4587">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4587">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4588">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4588">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4589">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4589">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4590">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4590">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4591">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4591">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4592">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4592">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4593">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4593">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4594">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4594">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4595">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4595">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4596">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4596">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4597">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4597">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4598">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4598">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4599">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4599">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a><span data-ttu-id="622b3-4600">DXGI_FORMAT_BC5 \_ ronfler<sup>FNC</sup> (84)</span><span class="sxs-lookup"><span data-stu-id="622b3-4600">DXGI_FORMAT_BC5\_SNORM<sup>FNC</sup> (84)</span></span>
| <span data-ttu-id="622b3-4601">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4601">Target</span></span> | <span data-ttu-id="622b3-4602">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4602">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4603">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4603">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4604">8</span><span class="sxs-lookup"><span data-stu-id="622b3-4604">8</span></span> |
| <span data-ttu-id="622b3-4605">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4605">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4606">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4606">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4607">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4607">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4608">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4608">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4609">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4609">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4610">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4610">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4611">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4611">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4612">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4612">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4613">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4613">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4614">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4614">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4615">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4615">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4616">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4616">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4617">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4617">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4618">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4618">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4619">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4619">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4620">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4620">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4621">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4621">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4622">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4622">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4623">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4623">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4624">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4624">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4625">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4625">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4626">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4626">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4627">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4627">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4628">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4628">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4629">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4629">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4630">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4630">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4631">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4631">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4632">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4632">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4633">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4633">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4634">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4634">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4635">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4635">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4636">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4636">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4637">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4637">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4638">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4638">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4639">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4639">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4640">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4640">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4641">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4641">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4642">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4642">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4643">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4643">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4644">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4644">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4645">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4645">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4646">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4646">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4647">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4647">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4648">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4648">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4649">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4649">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a><span data-ttu-id="622b3-4650">DXGI_FORMAT_B5G6R5 \_ UNORM<sup>FNS</sup> (85)</span><span class="sxs-lookup"><span data-stu-id="622b3-4650">DXGI_FORMAT_B5G6R5\_UNORM<sup>FNS</sup> (85)</span></span>
| <span data-ttu-id="622b3-4651">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4651">Target</span></span> | <span data-ttu-id="622b3-4652">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4652">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4653">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4653">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4654">16</span><span class="sxs-lookup"><span data-stu-id="622b3-4654">16</span></span> |
| <span data-ttu-id="622b3-4655">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4655">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4657">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4657">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4658">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4658">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4659">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4659">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4660">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4660">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4661">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4661">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4662">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4662">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4664">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4664">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4665">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4665">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4667">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4667">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4669">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4669">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4671">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4671">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4672">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4672">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4673">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4673">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4674">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4674">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4675">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4675">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4677">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4677">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4679">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4679">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4681">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4681">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4683">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4683">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4684">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4684">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4685">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4685">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4686">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4686">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4687">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4687">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4688">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4688">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4689">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4689">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4690">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4690">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4691">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4691">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4692">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4692">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4693">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4693">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4694">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4694">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4695">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4695">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4696">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4696">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4698">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4698">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4700">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4700">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4702">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4702">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4704">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4704">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4706">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4706">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4707">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4707">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4708">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4708">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4709">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4709">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4710">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4710">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4711">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4711">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4712">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4712">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4713">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4713">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a><span data-ttu-id="622b3-4714">DXGI_FORMAT_B5G5R5A1 \_ UNORM<sup>FNS</sup> (86)</span><span class="sxs-lookup"><span data-stu-id="622b3-4714">DXGI_FORMAT_B5G5R5A1\_UNORM<sup>FNS</sup> (86)</span></span>
| <span data-ttu-id="622b3-4715">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4715">Target</span></span> | <span data-ttu-id="622b3-4716">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4716">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4717">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4717">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4718">16</span><span class="sxs-lookup"><span data-stu-id="622b3-4718">16</span></span> |
| <span data-ttu-id="622b3-4719">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4719">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4721">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4721">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4722">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4722">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4723">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4723">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4724">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4724">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4725">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4725">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4726">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4726">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4728">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4728">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4729">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4729">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4731">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4731">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4733">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4733">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4735">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4735">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4736">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4736">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4737">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4737">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4738">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4738">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4739">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4739">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4741">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4741">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4742">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4742">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4743">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4743">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4744">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4744">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4745">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4745">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4746">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4746">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4747">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4747">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4748">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4748">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4749">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4749">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4750">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4750">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4751">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4751">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4752">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4752">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4753">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4753">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4754">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4754">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4755">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4755">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4756">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4756">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4757">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4757">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4759">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4759">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4760">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4760">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4761">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4761">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4762">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4762">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4763">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4763">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4764">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4764">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4765">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4765">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4766">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4766">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4767">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4767">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4768">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4768">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4769">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4769">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4770">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4770">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a><span data-ttu-id="622b3-4771">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8A8 type (90)</span><span class="sxs-lookup"><span data-stu-id="622b3-4771">DXGI_FORMAT_B8G8R8A8\_TYPELESS<sup>PCS</sup> (90)</span></span>
| <span data-ttu-id="622b3-4772">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4772">Target</span></span> | <span data-ttu-id="622b3-4773">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4773">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4774">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4774">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4775">32</span><span class="sxs-lookup"><span data-stu-id="622b3-4775">32</span></span> |
| <span data-ttu-id="622b3-4776">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4776">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4777">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4777">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4778">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4778">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4779">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4779">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4780">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4780">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4781">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4781">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4782">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4782">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4783">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4783">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4784">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4784">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4785">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4785">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4786">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4786">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4787">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4787">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4788">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4788">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4789">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4789">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4790">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4790">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4791">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4791">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4792">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4792">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4793">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4793">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4794">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4794">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4795">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4795">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4796">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4796">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4797">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4797">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4798">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4798">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4799">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4799">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4800">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4800">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4801">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4801">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4802">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4802">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4803">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4803">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4804">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4804">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4805">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4805">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4806">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4806">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4807">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4807">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4808">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4808">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4809">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4809">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4810">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4810">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4811">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4811">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-4812">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4812">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-4813">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4813">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4814">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4814">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-4815">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4815">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4816">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4816">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4817">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4817">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-4818">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4818">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-4819">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4819">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-4820">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4820">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a><span data-ttu-id="622b3-4821">DXGI_FORMAT_B8G8R8A8 \_ UNORM<sup>FNS</sup> (87)</span><span class="sxs-lookup"><span data-stu-id="622b3-4821">DXGI_FORMAT_B8G8R8A8\_UNORM<sup>FNS</sup> (87)</span></span>
| <span data-ttu-id="622b3-4822">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4822">Target</span></span> | <span data-ttu-id="622b3-4823">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4823">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4824">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4824">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4825">32</span><span class="sxs-lookup"><span data-stu-id="622b3-4825">32</span></span> |
| <span data-ttu-id="622b3-4826">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4826">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4828">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4828">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4829">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4829">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4830">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4830">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4831">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4831">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4832">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4832">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4833">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4833">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4835">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4835">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4837">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4837">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4839">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4839">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4841">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4841">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4843">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4843">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4844">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4844">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4845">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4845">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4846">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4846">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4847">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4847">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4849">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4849">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4851">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4851">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4853">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4853">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4855">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4855">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4856">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4856">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4857">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4857">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4858">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4858">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4859">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4859">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4860">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4860">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4861">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4861">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4862">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4862">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4863">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4863">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4864">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4864">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4865">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4865">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4866">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4866">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4867">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4867">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4868">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4868">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4870">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4870">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4872">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4872">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4874">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4874">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4876">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4876">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4878">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4878">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4879">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4879">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4881">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4881">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4882">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4882">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4883">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4883">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4885">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4885">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4887">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4887">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4889">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4889">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a><span data-ttu-id="622b3-4890">DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ sRVB<sup>FNS</sup> (91)</span><span class="sxs-lookup"><span data-stu-id="622b3-4890">DXGI_FORMAT_B8G8R8A8\_UNORM\_SRGB<sup>FNS</sup> (91)</span></span>
| <span data-ttu-id="622b3-4891">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4891">Target</span></span> | <span data-ttu-id="622b3-4892">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4892">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4893">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4893">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4894">32</span><span class="sxs-lookup"><span data-stu-id="622b3-4894">32</span></span> |
| <span data-ttu-id="622b3-4895">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4895">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4897">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4897">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4898">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4898">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4899">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4899">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4900">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4900">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4901">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4901">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4902">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4902">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4904">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4904">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4906">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4906">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4908">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4908">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4910">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4910">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4912">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4912">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4913">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4913">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4914">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4914">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4915">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4915">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4916">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4916">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4918">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4918">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4920">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4920">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4922">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4922">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4924">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4924">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4925">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4925">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4926">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4926">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4927">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4927">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4928">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4928">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4929">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4929">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4930">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4930">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4931">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4931">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4932">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4932">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4933">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4933">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4934">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4934">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4935">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4935">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4936">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4936">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4937">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4937">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4939">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4939">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4941">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4941">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4943">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4943">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4945">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-4945">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4947">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-4947">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-4948">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-4948">Display Scan-Out</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4950">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-4950">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-4951">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4951">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-4952">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4952">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-4954">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-4954">Video Processor Output</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4956">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-4956">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-4958">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-4958">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a><span data-ttu-id="622b3-4959">\_<sup>PC</sup> DXGI_FORMAT_B8G8R8X8 type (92)</span><span class="sxs-lookup"><span data-stu-id="622b3-4959">DXGI_FORMAT_B8G8R8X8\_TYPELESS<sup>PCS</sup> (92)</span></span>
| <span data-ttu-id="622b3-4960">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-4960">Target</span></span> | <span data-ttu-id="622b3-4961">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-4961">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-4962">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-4962">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-4963">32</span><span class="sxs-lookup"><span data-stu-id="622b3-4963">32</span></span> |
| <span data-ttu-id="622b3-4964">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-4964">Format Support</span></span> | \- |
| <span data-ttu-id="622b3-4965">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-4965">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4966">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4966">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4967">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-4967">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4968">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-4968">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-4969">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-4969">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-4970">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-4970">Texture2D</span></span> | \- |
| <span data-ttu-id="622b3-4971">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-4971">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-4972">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-4972">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-4973">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-4973">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-4974">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-4974">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-4975">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-4975">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-4976">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-4976">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-4977">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-4977">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-4978">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-4978">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-4979">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-4979">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-4980">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-4980">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-4981">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4981">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4982">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-4982">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4983">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-4983">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-4984">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-4984">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-4985">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-4985">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4986">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-4986">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-4987">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-4987">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-4988">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4988">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-4989">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4989">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-4990">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-4990">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-4991">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4991">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-4992">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-4992">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-4993">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4993">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-4994">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-4994">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4995">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-4995">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-4996">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-4996">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-4997">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-4997">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4998">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-4998">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-4999">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-4999">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5000">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5000">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5001">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5001">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5002">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5002">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5003">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5003">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5004">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5004">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5005">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5005">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-5006">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5006">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-5007">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5007">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5008">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5008">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a><span data-ttu-id="622b3-5009">DXGI_FORMAT_B8G8R8X8 \_ UNORM<sup>FNS</sup> (88)</span><span class="sxs-lookup"><span data-stu-id="622b3-5009">DXGI_FORMAT_B8G8R8X8\_UNORM<sup>FNS</sup> (88)</span></span>
| <span data-ttu-id="622b3-5010">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5010">Target</span></span> | <span data-ttu-id="622b3-5011">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5011">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5012">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5012">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5013">32</span><span class="sxs-lookup"><span data-stu-id="622b3-5013">32</span></span> |
| <span data-ttu-id="622b3-5014">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5014">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5016">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5016">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5017">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5017">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5018">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5018">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5019">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5019">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5020">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5020">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5021">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5021">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5023">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5023">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5025">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5025">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5027">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5027">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5029">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5029">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5031">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5031">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5032">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5032">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5033">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5033">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5034">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5034">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5035">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5035">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5037">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5037">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5039">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5039">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5041">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5041">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5043">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5043">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5044">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5044">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5045">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5045">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5046">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5046">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5047">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5047">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5048">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5048">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5049">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5049">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5050">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5050">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5051">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5051">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5052">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5052">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5053">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5053">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5054">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5054">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5055">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5055">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5056">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5056">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5058">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5058">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5060">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5060">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5062">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5062">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5064">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5064">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5066">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5066">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5067">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5067">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5068">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5068">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5069">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5069">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5070">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5070">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5072">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5072">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5074">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5074">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5076">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5076">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a><span data-ttu-id="622b3-5077">DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ sRVB<sup>FNS</sup> (93)</span><span class="sxs-lookup"><span data-stu-id="622b3-5077">DXGI_FORMAT_B8G8R8X8\_UNORM\_SRGB<sup>FNS</sup> (93)</span></span>
| <span data-ttu-id="622b3-5078">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5078">Target</span></span> | <span data-ttu-id="622b3-5079">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5079">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5080">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5080">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5081">32</span><span class="sxs-lookup"><span data-stu-id="622b3-5081">32</span></span> |
| <span data-ttu-id="622b3-5082">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5082">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5084">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5084">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5085">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5085">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5086">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5086">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5087">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5087">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5088">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5088">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5089">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5089">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5091">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5091">Texture3D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5093">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5093">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5095">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5095">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5097">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5097">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5099">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5099">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5100">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5100">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5101">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5101">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5102">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5102">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5103">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5103">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5105">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5105">Mipmap Auto-Generation</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5107">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5107">RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5109">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5109">Blendable RenderTarget</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5111">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5111">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5112">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5112">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5113">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5113">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5114">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5114">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5115">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5115">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5116">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5116">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5117">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5117">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5118">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5118">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5119">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5119">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5120">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5120">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5121">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5121">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5122">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5122">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5123">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5123">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5124">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5124">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5126">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5126">4x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5128">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5128">8x Multisample RenderTarget</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5130">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5130">Other Multisample Count RT</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5132">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5132">Multisample Resolve</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5134">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5134">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5135">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5135">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5136">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5136">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5137">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5137">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5138">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5138">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-5139">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5139">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-5140">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5140">Shared Resource</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5142">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5142">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a><span data-ttu-id="622b3-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span><span class="sxs-lookup"><span data-stu-id="622b3-5143">DXGI_FORMAT_AYUV<sup>V</sup> (100)</span></span>
| <span data-ttu-id="622b3-5144">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5144">Target</span></span> | <span data-ttu-id="622b3-5145">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5145">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5146">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5146">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5147">32</span><span class="sxs-lookup"><span data-stu-id="622b3-5147">32</span></span> |
| <span data-ttu-id="622b3-5148">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5148">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5150">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5150">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5151">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5151">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5152">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5152">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5153">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5153">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5154">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5154">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5155">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5155">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5157">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5157">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5158">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5158">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5159">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5159">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5160">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5160">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5161">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5161">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5162">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5162">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5163">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5163">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5164">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5164">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5165">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5165">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5166">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5166">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5167">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5167">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5168">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5168">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5169">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5169">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5170">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5170">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5171">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5171">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5172">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5172">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5173">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5173">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5174">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5174">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5175">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5175">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5176">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5176">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5177">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5177">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5178">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5178">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5179">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5179">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5180">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5180">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5181">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5181">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5182">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5182">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5184">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5184">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5185">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5185">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5186">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5186">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5187">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5187">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5188">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5188">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5189">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5189">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5190">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5190">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5191">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5191">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5193">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5193">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5195">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5195">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5197">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5197">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5198">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5198">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y410supvsup-101"></a><span data-ttu-id="622b3-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span><span class="sxs-lookup"><span data-stu-id="622b3-5199">DXGI_FORMAT_Y410<sup>V</sup> (101)</span></span>
| <span data-ttu-id="622b3-5200">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5200">Target</span></span> | <span data-ttu-id="622b3-5201">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5201">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5202">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5202">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5203">32</span><span class="sxs-lookup"><span data-stu-id="622b3-5203">32</span></span> |
| <span data-ttu-id="622b3-5204">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5204">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5206">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5206">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5207">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5207">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5208">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5208">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5209">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5209">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5210">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5210">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5211">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5211">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5213">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5213">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5214">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5214">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5215">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5215">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5216">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5216">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5217">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5217">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5218">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5218">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5219">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5219">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5220">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5220">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5221">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5221">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5222">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5222">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5223">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5223">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5224">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5224">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5225">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5225">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5226">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5226">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5227">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5227">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5228">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5228">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5229">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5229">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5230">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5230">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5231">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5231">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5232">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5232">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5233">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5233">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5234">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5234">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5235">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5235">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5236">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5236">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5237">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5237">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5238">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5238">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5240">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5240">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5241">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5241">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5242">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5242">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5243">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5243">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5244">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5244">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5245">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5245">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5246">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5246">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5247">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5247">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5249">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5249">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5251">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5251">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5253">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5253">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5254">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5254">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y416supvsup-102"></a><span data-ttu-id="622b3-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span><span class="sxs-lookup"><span data-stu-id="622b3-5255">DXGI_FORMAT_Y416<sup>V</sup> (102)</span></span>
| <span data-ttu-id="622b3-5256">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5256">Target</span></span> | <span data-ttu-id="622b3-5257">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5257">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5258">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5258">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5259">64</span><span class="sxs-lookup"><span data-stu-id="622b3-5259">64</span></span> |
| <span data-ttu-id="622b3-5260">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5260">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5262">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5262">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5263">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5263">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5264">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5264">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5265">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5265">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5266">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5266">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5267">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5267">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5269">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5269">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5270">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5270">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5271">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5271">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5272">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5272">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5273">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5273">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5274">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5274">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5275">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5275">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5276">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5276">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5277">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5277">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5278">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5278">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5279">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5279">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5280">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5280">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5281">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5281">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5282">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5282">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5283">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5283">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5284">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5284">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5285">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5285">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5286">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5286">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5287">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5287">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5288">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5288">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5289">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5289">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5290">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5290">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5291">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5291">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5292">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5292">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5293">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5293">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5294">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5294">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5296">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5296">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5297">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5297">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5298">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5298">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5299">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5299">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5300">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5300">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5301">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5301">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5302">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5302">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5303">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5303">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5305">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5305">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5307">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5307">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5309">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5309">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5310">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5310">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv12supvsup-103"></a><span data-ttu-id="622b3-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span><span class="sxs-lookup"><span data-stu-id="622b3-5311">DXGI_FORMAT_NV12<sup>V</sup> (103)</span></span>
| <span data-ttu-id="622b3-5312">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5312">Target</span></span> | <span data-ttu-id="622b3-5313">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5313">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5314">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5314">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5315">8</span><span class="sxs-lookup"><span data-stu-id="622b3-5315">8</span></span> |
| <span data-ttu-id="622b3-5316">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5316">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5318">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5318">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5319">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5319">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5320">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5320">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5321">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5321">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5322">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5322">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5323">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5323">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5325">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5325">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5326">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5326">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5327">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5327">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5328">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5328">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5329">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5329">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5330">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5330">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5331">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5331">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5332">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5332">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5333">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5333">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5334">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5334">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5335">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5335">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5336">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5336">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5337">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5337">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5338">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5338">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5339">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5339">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5340">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5340">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5341">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5341">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5342">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5342">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5343">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5343">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5344">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5344">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5345">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5345">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5346">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5346">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5347">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5347">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5348">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5348">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5349">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5349">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5350">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5350">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5352">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5352">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5353">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5353">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5354">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5354">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5355">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5355">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5356">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5356">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5357">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5357">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5358">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5358">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5359">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5359">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5361">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5361">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5363">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5363">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5365">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5365">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5366">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5366">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p010supvsup-104"></a><span data-ttu-id="622b3-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span><span class="sxs-lookup"><span data-stu-id="622b3-5367">DXGI_FORMAT_P010<sup>V</sup> (104)</span></span>
| <span data-ttu-id="622b3-5368">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5368">Target</span></span> | <span data-ttu-id="622b3-5369">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5369">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5370">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5370">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5371">16</span><span class="sxs-lookup"><span data-stu-id="622b3-5371">16</span></span> |
| <span data-ttu-id="622b3-5372">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5372">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5374">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5374">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5375">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5375">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5376">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5376">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5377">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5377">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5378">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5378">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5379">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5379">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5381">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5381">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5382">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5382">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5383">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5383">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5384">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5384">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5385">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5385">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5386">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5386">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5387">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5387">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5388">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5388">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5389">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5389">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5390">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5390">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5391">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5391">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5392">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5392">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5393">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5393">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5394">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5394">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5395">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5395">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5396">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5396">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5397">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5397">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5398">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5398">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5399">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5399">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5400">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5400">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5401">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5401">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5402">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5402">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5403">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5403">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5404">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5404">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5405">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5405">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5406">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5406">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5408">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5408">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5409">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5409">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5410">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5410">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5411">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5411">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5412">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5412">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5413">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5413">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5414">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5414">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5415">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5415">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5417">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5417">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5419">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5419">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5421">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5421">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5422">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5422">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p016supvsup-105"></a><span data-ttu-id="622b3-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span><span class="sxs-lookup"><span data-stu-id="622b3-5423">DXGI_FORMAT_P016<sup>V</sup> (105)</span></span>
| <span data-ttu-id="622b3-5424">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5424">Target</span></span> | <span data-ttu-id="622b3-5425">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5425">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5426">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5426">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5427">16</span><span class="sxs-lookup"><span data-stu-id="622b3-5427">16</span></span> |
| <span data-ttu-id="622b3-5428">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5428">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5430">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5430">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5431">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5431">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5432">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5432">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5433">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5433">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5434">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5434">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5435">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5435">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5437">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5437">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5438">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5438">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5439">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5439">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5440">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5440">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5441">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5441">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5442">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5442">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5443">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5443">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5444">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5444">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5445">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5445">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5446">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5446">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5447">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5447">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5448">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5448">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5449">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5449">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5450">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5450">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5451">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5451">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5452">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5452">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5453">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5453">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5454">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5454">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5455">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5455">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5456">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5456">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5457">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5457">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5458">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5458">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5459">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5459">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5460">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5460">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5461">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5461">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5462">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5462">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5464">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5464">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5465">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5465">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5466">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5466">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5467">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5467">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5468">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5468">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5469">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5469">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5470">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5470">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5471">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5471">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5473">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5473">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5475">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5475">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5477">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5477">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5478">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5478">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a><span data-ttu-id="622b3-5479">DXGI_FORMAT_420 \_ <sup>V</sup> opaque (106)</span><span class="sxs-lookup"><span data-stu-id="622b3-5479">DXGI_FORMAT_420\_OPAQUE<sup>V</sup> (106)</span></span>
| <span data-ttu-id="622b3-5480">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5480">Target</span></span> | <span data-ttu-id="622b3-5481">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5481">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5482">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5482">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5483">8</span><span class="sxs-lookup"><span data-stu-id="622b3-5483">8</span></span> |
| <span data-ttu-id="622b3-5484">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5484">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5486">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5486">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5487">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5487">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5488">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5488">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5489">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5489">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5490">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5490">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5491">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5491">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5493">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5493">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5494">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5494">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5495">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5495">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5496">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5496">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5497">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5497">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5498">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5498">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5499">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5499">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5500">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5500">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5501">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5501">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5502">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5502">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5503">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5503">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5504">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5504">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5505">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5505">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5506">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5506">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5507">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5507">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5508">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5508">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5509">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5509">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5510">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5510">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5511">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5511">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5512">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5512">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5513">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5513">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5514">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5514">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5515">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5515">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5516">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5516">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5517">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5517">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5518">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5518">CPU Lockable</span></span> | \- |
| <span data-ttu-id="622b3-5519">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5519">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5520">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5520">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5521">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5521">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5522">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5522">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5523">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5523">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5524">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5524">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5525">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5525">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5526">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5526">Video Decoder Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5528">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5528">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5530">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5530">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5532">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5532">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5533">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5533">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a><span data-ttu-id="622b3-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span><span class="sxs-lookup"><span data-stu-id="622b3-5534">DXGI_FORMAT_YUY2<sup>V</sup> (107)</span></span>
| <span data-ttu-id="622b3-5535">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5535">Target</span></span> | <span data-ttu-id="622b3-5536">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5536">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5537">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5537">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5538">16</span><span class="sxs-lookup"><span data-stu-id="622b3-5538">16</span></span> |
| <span data-ttu-id="622b3-5539">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5539">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5541">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5541">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5542">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5542">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5543">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5543">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5544">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5544">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5545">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5545">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5546">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5546">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5548">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5548">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5549">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5549">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5550">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5550">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5551">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5551">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5552">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5552">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5553">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5553">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5554">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5554">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5555">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5555">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5556">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5556">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5557">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5557">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5558">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5558">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5559">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5559">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5560">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5560">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5561">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5561">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5562">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5562">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5563">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5563">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5564">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5564">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5565">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5565">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5566">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5566">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5567">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5567">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5568">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5568">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5569">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5569">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5570">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5570">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5571">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5571">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5572">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5572">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5573">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5573">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5575">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5575">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5576">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5576">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5577">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5577">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5578">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5578">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5579">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5579">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5580">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5580">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5581">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5581">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5582">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5582">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5584">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5584">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5586">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5586">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5588">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5588">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5589">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5589">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y210supvsup-108"></a><span data-ttu-id="622b3-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span><span class="sxs-lookup"><span data-stu-id="622b3-5590">DXGI_FORMAT_Y210<sup>V</sup> (108)</span></span>
| <span data-ttu-id="622b3-5591">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5591">Target</span></span> | <span data-ttu-id="622b3-5592">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5592">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5593">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5593">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5594">32</span><span class="sxs-lookup"><span data-stu-id="622b3-5594">32</span></span> |
| <span data-ttu-id="622b3-5595">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5595">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5597">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5597">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5598">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5598">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5599">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5599">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5600">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5600">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5601">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5601">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5602">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5602">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5604">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5604">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5605">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5605">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5606">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5606">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5607">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5607">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5608">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5608">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5609">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5609">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5610">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5610">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5611">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5611">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5612">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5612">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5613">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5613">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5614">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5614">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5615">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5615">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5616">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5616">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5617">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5617">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5618">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5618">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5619">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5619">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5620">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5620">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5621">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5621">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5622">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5622">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5623">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5623">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5624">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5624">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5625">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5625">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5626">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5626">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5627">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5627">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5628">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5628">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5629">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5629">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5631">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5631">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5632">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5632">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5633">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5633">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5634">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5634">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5635">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5635">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5636">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5636">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5637">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5637">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5638">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5638">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5640">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5640">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5642">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5642">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5644">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5644">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5645">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5645">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_y216supvsup-109"></a><span data-ttu-id="622b3-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span><span class="sxs-lookup"><span data-stu-id="622b3-5646">DXGI_FORMAT_Y216<sup>V</sup> (109)</span></span>
| <span data-ttu-id="622b3-5647">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5647">Target</span></span> | <span data-ttu-id="622b3-5648">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5648">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5649">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5649">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5650">32</span><span class="sxs-lookup"><span data-stu-id="622b3-5650">32</span></span> |
| <span data-ttu-id="622b3-5651">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5651">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5653">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5653">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5654">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5654">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5655">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5655">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5656">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5656">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5657">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5657">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5658">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5658">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5660">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5660">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5661">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5661">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5662">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5662">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5663">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5663">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5664">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5664">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5665">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5665">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5666">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5666">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5667">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5667">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5668">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5668">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5669">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5669">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5670">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5670">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5671">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5671">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5672">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5672">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5673">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5673">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5674">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5674">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5675">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5675">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5676">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5676">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5677">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5677">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5678">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5678">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5679">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5679">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5680">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5680">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5681">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5681">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5682">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5682">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5683">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5683">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5684">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5684">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5685">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5685">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5687">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5687">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5688">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5688">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5689">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5689">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5690">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5690">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5691">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5691">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5692">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5692">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5693">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5693">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5694">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5694">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5696">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5696">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5698">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5698">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5700">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5700">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5701">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5701">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_nv11supvsup-110"></a><span data-ttu-id="622b3-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span><span class="sxs-lookup"><span data-stu-id="622b3-5702">DXGI_FORMAT_NV11<sup>V</sup> (110)</span></span>
| <span data-ttu-id="622b3-5703">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5703">Target</span></span> | <span data-ttu-id="622b3-5704">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5704">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5705">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5705">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5706">8</span><span class="sxs-lookup"><span data-stu-id="622b3-5706">8</span></span> |
| <span data-ttu-id="622b3-5707">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5707">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5709">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5709">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5710">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5710">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5711">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5711">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5712">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5712">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5713">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5713">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5714">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5714">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5716">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5716">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5717">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5717">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5718">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5718">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5719">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5719">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5720">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5720">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5721">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5721">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5722">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5722">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5723">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5723">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5724">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5724">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5725">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5725">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5726">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5726">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5727">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5727">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5728">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5728">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5729">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5729">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5730">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5730">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5731">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5731">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5732">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5732">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5733">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5733">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5734">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5734">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5735">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5735">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5736">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5736">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5737">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5737">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5738">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5738">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5739">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5739">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5740">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5740">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5741">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5741">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5743">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5743">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5744">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5744">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5745">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5745">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5746">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5746">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5747">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5747">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5748">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5748">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5749">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5749">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5750">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5750">Video Decoder Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5752">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5752">Video Processor Input</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5754">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5754">Video Processor Output</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5756">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5756">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5757">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5757">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ai44supvsup-111"></a><span data-ttu-id="622b3-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span><span class="sxs-lookup"><span data-stu-id="622b3-5758">DXGI_FORMAT_AI44<sup>V</sup> (111)</span></span>
| <span data-ttu-id="622b3-5759">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5759">Target</span></span> | <span data-ttu-id="622b3-5760">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5760">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5761">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5761">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5762">8</span><span class="sxs-lookup"><span data-stu-id="622b3-5762">8</span></span> |
| <span data-ttu-id="622b3-5763">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5763">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5765">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5765">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5766">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5766">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5767">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5767">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5768">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5768">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5769">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5769">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5770">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5770">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5772">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5772">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5773">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5773">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5774">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5774">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5775">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5775">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5776">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5776">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5777">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5777">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5778">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5778">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5779">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5779">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5780">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5780">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5781">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5781">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5782">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5782">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5783">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5783">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5784">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5784">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5785">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5785">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5786">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5786">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5787">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5787">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5788">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5788">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5789">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5789">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5790">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5790">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5791">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5791">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5792">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5792">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5793">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5793">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5794">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5794">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5795">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5795">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5796">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5796">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5797">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5797">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5799">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5799">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5800">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5800">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5801">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5801">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5802">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5802">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5803">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5803">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5804">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5804">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5805">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5805">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5806">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5806">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5807">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5807">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5809">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5809">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-5810">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5810">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5811">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5811">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_ia44supvsup-112"></a><span data-ttu-id="622b3-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span><span class="sxs-lookup"><span data-stu-id="622b3-5812">DXGI_FORMAT_IA44<sup>V</sup> (112)</span></span>
| <span data-ttu-id="622b3-5813">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5813">Target</span></span> | <span data-ttu-id="622b3-5814">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5814">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5815">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5815">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5816">8</span><span class="sxs-lookup"><span data-stu-id="622b3-5816">8</span></span> |
| <span data-ttu-id="622b3-5817">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5817">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5819">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5819">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5820">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5820">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5821">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5821">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5822">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5822">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5823">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5823">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5824">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5824">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5826">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5826">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5827">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5827">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5828">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5828">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5829">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5829">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5830">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5830">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5831">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5831">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5832">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5832">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5833">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5833">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5834">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5834">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5835">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5835">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5836">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5836">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5837">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5837">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5838">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5838">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5839">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5839">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5840">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5840">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5841">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5841">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5842">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5842">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5843">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5843">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5844">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5844">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5845">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5845">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5846">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5846">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5847">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5847">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5848">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5848">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5849">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5849">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5850">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5850">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5851">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5851">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5853">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5853">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5854">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5854">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5855">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5855">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5856">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5856">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5857">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5857">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5858">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5858">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5859">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5859">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5860">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5860">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5861">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5861">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5863">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5863">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-5864">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5864">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5865">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5865">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_p8supvsup-113"></a><span data-ttu-id="622b3-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span><span class="sxs-lookup"><span data-stu-id="622b3-5866">DXGI_FORMAT_P8<sup>V</sup> (113)</span></span>
| <span data-ttu-id="622b3-5867">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5867">Target</span></span> | <span data-ttu-id="622b3-5868">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5868">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5869">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5869">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5870">8</span><span class="sxs-lookup"><span data-stu-id="622b3-5870">8</span></span> |
| <span data-ttu-id="622b3-5871">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5871">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5873">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5873">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5874">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5874">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5875">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5875">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5876">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5876">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5877">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5877">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5878">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5878">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5880">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5880">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5881">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5881">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5882">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5882">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5883">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5883">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5884">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5884">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5885">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5885">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5886">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5886">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5887">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5887">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5888">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5888">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5889">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5889">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5890">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5890">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5891">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5891">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5892">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5892">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5893">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5893">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5894">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5894">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5895">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5895">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5896">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5896">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5897">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5897">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5898">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5898">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5899">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5899">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5900">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5900">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5901">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5901">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5902">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5902">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5903">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5903">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5904">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5904">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5905">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5905">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5907">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5907">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5908">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5908">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5909">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5909">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5910">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5910">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5911">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5911">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5912">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5912">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5913">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5913">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5914">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5914">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5915">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5915">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5917">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5917">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-5918">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5918">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5919">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5919">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a><span data-ttu-id="622b3-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span><span class="sxs-lookup"><span data-stu-id="622b3-5920">DXGI_FORMAT_A8P8<sup>V</sup> (114)</span></span>
| <span data-ttu-id="622b3-5921">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5921">Target</span></span> | <span data-ttu-id="622b3-5922">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5922">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5923">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5923">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5924">16</span><span class="sxs-lookup"><span data-stu-id="622b3-5924">16</span></span> |
| <span data-ttu-id="622b3-5925">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5925">Format Support</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-5927">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5927">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5928">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5928">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5929">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5929">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5930">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5930">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5931">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5931">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5932">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5932">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5934">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5934">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5935">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5935">TextureCube</span></span> | \- |
| <span data-ttu-id="622b3-5936">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5936">Shader sample (point sample only)</span></span> | \- |
| <span data-ttu-id="622b3-5937">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5937">Shader sample (any filter)</span></span> | \- |
| <span data-ttu-id="622b3-5938">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5938">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5939">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5939">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5940">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5940">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5941">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5941">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5942">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5942">Mipmap</span></span> | \- |
| <span data-ttu-id="622b3-5943">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-5943">Mipmap Auto-Generation</span></span> | \- |
| <span data-ttu-id="622b3-5944">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5944">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5945">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-5945">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5946">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-5946">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-5947">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-5947">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-5948">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-5948">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5949">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-5949">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-5950">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-5950">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-5951">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5951">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-5952">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5952">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-5953">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-5953">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-5954">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5954">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-5955">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-5955">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-5956">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5956">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-5957">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-5957">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5958">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-5958">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-5959">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-5959">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5961">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-5961">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5962">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-5962">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-5963">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-5963">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-5964">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-5964">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-5965">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-5965">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-5966">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-5966">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-5967">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-5967">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-5968">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5968">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-5969">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5969">Video Processor Input</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5971">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-5971">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-5972">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-5972">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-5973">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-5973">Tiled Resource</span></span> | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a><span data-ttu-id="622b3-5974">DXGI_FORMAT_B4G4R4A4 \_ UNORM<sup>FNS</sup> (115)</span><span class="sxs-lookup"><span data-stu-id="622b3-5974">DXGI_FORMAT_B4G4R4A4\_UNORM<sup>FNS</sup> (115)</span></span>
| <span data-ttu-id="622b3-5975">Cible</span><span class="sxs-lookup"><span data-stu-id="622b3-5975">Target</span></span> | <span data-ttu-id="622b3-5976">Support</span><span class="sxs-lookup"><span data-stu-id="622b3-5976">Support</span></span> |
| - | - |
| <span data-ttu-id="622b3-5977">Bits par élément (BPE)</span><span class="sxs-lookup"><span data-stu-id="622b3-5977">Bits Per Element (BPE)</span></span> | <span data-ttu-id="622b3-5978">16</span><span class="sxs-lookup"><span data-stu-id="622b3-5978">16</span></span> |
| <span data-ttu-id="622b3-5979">Prise en charge du format</span><span class="sxs-lookup"><span data-stu-id="622b3-5979">Format Support</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5981">Buffer</span><span class="sxs-lookup"><span data-stu-id="622b3-5981">Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5982">Mémoire tampon du vertex assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5982">Input Assembler Vertex Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5983">Tampon d’index assembleur d’entrée</span><span class="sxs-lookup"><span data-stu-id="622b3-5983">Input Assembler Index Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5984">Mémoire tampon de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="622b3-5984">Stream Output Buffer</span></span> | \- |
| <span data-ttu-id="622b3-5985">Texture1D</span><span class="sxs-lookup"><span data-stu-id="622b3-5985">Texture1D</span></span> | \- |
| <span data-ttu-id="622b3-5986">Texture2D</span><span class="sxs-lookup"><span data-stu-id="622b3-5986">Texture2D</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5988">Texture3D</span><span class="sxs-lookup"><span data-stu-id="622b3-5988">Texture3D</span></span> | \- |
| <span data-ttu-id="622b3-5989">TextureCube</span><span class="sxs-lookup"><span data-stu-id="622b3-5989">TextureCube</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5991">Exemple de nuanceur (échantillon de point uniquement)</span><span class="sxs-lookup"><span data-stu-id="622b3-5991">Shader sample (point sample only)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5993">Exemple de nuanceur (n’importe quel filtre)</span><span class="sxs-lookup"><span data-stu-id="622b3-5993">Shader sample (any filter)</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-5995">Exemple de nuanceur \_ c (filtre de comparaison)</span><span class="sxs-lookup"><span data-stu-id="622b3-5995">Shader sample\_c (comparison filter)</span></span> | \- |
| <span data-ttu-id="622b3-5996">Exemple de nuanceur (filtre mono 1 bit)</span><span class="sxs-lookup"><span data-stu-id="622b3-5996">Shader sample (mono 1-bit filter)</span></span> | \- |
| <span data-ttu-id="622b3-5997">Nuanceur gather4</span><span class="sxs-lookup"><span data-stu-id="622b3-5997">Shader gather4</span></span> | \- |
| <span data-ttu-id="622b3-5998">Nuanceur gather4 \_ c</span><span class="sxs-lookup"><span data-stu-id="622b3-5998">Shader gather4\_c</span></span> | \- |
| <span data-ttu-id="622b3-5999">MIP</span><span class="sxs-lookup"><span data-stu-id="622b3-5999">Mipmap</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-6001">Génération automatique de mipmap</span><span class="sxs-lookup"><span data-stu-id="622b3-6001">Mipmap Auto-Generation</span></span> | ![facultatif](images/letter-o.jpg) |
| <span data-ttu-id="622b3-6003">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-6003">RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-6004">RenderTarget Blendable</span><span class="sxs-lookup"><span data-stu-id="622b3-6004">Blendable RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-6005">Sortie fusion Logic op</span><span class="sxs-lookup"><span data-stu-id="622b3-6005">Output Merger Logic Op</span></span> | \- |
| <span data-ttu-id="622b3-6006">Cible de la profondeur/du stencil</span><span class="sxs-lookup"><span data-stu-id="622b3-6006">Depth/Stencil Target</span></span> | \- |
| <span data-ttu-id="622b3-6007">UAV et SRV bruts</span><span class="sxs-lookup"><span data-stu-id="622b3-6007">Raw UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-6008">UAV et SRV structurés</span><span class="sxs-lookup"><span data-stu-id="622b3-6008">Structured UAV and SRV</span></span> | \- |
| <span data-ttu-id="622b3-6009">UAV typé</span><span class="sxs-lookup"><span data-stu-id="622b3-6009">Typed UAV</span></span> | \- |
| <span data-ttu-id="622b3-6010">Magasin typé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-6010">UAV Typed Store</span></span> | \- |
| <span data-ttu-id="622b3-6011">Charge typée UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-6011">UAV Typed Load</span></span> | \- |
| <span data-ttu-id="622b3-6012">UAV Atomic Add</span><span class="sxs-lookup"><span data-stu-id="622b3-6012">UAV Atomic Add</span></span> | \- |
| <span data-ttu-id="622b3-6013">Opérations de bits atomiques UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-6013">UAV Atomic Bitwise Ops</span></span> | \- |
| <span data-ttu-id="622b3-6014">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="622b3-6014">UAV Atomic Cmp&Store/ Cmp&Exch</span></span> | \- |
| <span data-ttu-id="622b3-6015">Échange atomique UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-6015">UAV Atomic Exchange</span></span> | \- |
| <span data-ttu-id="622b3-6016">Min ou Max signé UAV</span><span class="sxs-lookup"><span data-stu-id="622b3-6016">UAV Atomic Signed Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-6017">UAV Atomic non signé min ou Max</span><span class="sxs-lookup"><span data-stu-id="622b3-6017">UAV Atomic Unsigned Min or Max</span></span> | \- |
| <span data-ttu-id="622b3-6018">UC verrouillable</span><span class="sxs-lookup"><span data-stu-id="622b3-6018">CPU Lockable</span></span> | ![obligatoire](images/letter-r.jpg) |
| <span data-ttu-id="622b3-6020">RenderTarget multiéchantillon 4x</span><span class="sxs-lookup"><span data-stu-id="622b3-6020">4x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-6021">8x-échantillonnage RenderTarget</span><span class="sxs-lookup"><span data-stu-id="622b3-6021">8x Multisample RenderTarget</span></span> | \- |
| <span data-ttu-id="622b3-6022">Autre nombre d’échantillons en RT</span><span class="sxs-lookup"><span data-stu-id="622b3-6022">Other Multisample Count RT</span></span> | \- |
| <span data-ttu-id="622b3-6023">Résolution d’échantillonnages</span><span class="sxs-lookup"><span data-stu-id="622b3-6023">Multisample Resolve</span></span> | \- |
| <span data-ttu-id="622b3-6024">Charge d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="622b3-6024">Multisample Load</span></span> | \- |
| <span data-ttu-id="622b3-6025">Afficher Scan-Out</span><span class="sxs-lookup"><span data-stu-id="622b3-6025">Display Scan-Out</span></span> | \- |
| <span data-ttu-id="622b3-6026">Cast dans la disposition binaire</span><span class="sxs-lookup"><span data-stu-id="622b3-6026">Cast Within Bit Layout</span></span> | \- |
| <span data-ttu-id="622b3-6027">Prise en charge du décodeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-6027">Video Decoder Support</span></span> | \- |
| <span data-ttu-id="622b3-6028">Entrée du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-6028">Video Processor Input</span></span> | \- |
| <span data-ttu-id="622b3-6029">Sortie du processeur vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-6029">Video Processor Output</span></span> | \- |
| <span data-ttu-id="622b3-6030">Ressource partagée</span><span class="sxs-lookup"><span data-stu-id="622b3-6030">Shared Resource</span></span> | \- |
| <span data-ttu-id="622b3-6031">Ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="622b3-6031">Tiled Resource</span></span> | \- |

## <a name="format-notes"></a><span data-ttu-id="622b3-6032">Mettre en forme les notes</span><span class="sxs-lookup"><span data-stu-id="622b3-6032">Format notes</span></span>

<span data-ttu-id="622b3-6033">L’objectif du format peut passer d’un niveau de fonctionnalité matériel à l’autre.</span><span class="sxs-lookup"><span data-stu-id="622b3-6033">The purpose of the format can change from one hardware feature level to the next.</span></span>

<dl> <dt>

<span data-ttu-id="622b3-6034"><sup>L</sup> : format non typé</span><span class="sxs-lookup"><span data-stu-id="622b3-6034"><sup>L</sup> : typeless format</span></span>
</dt> <dt>

<span data-ttu-id="622b3-6035"><sup>PC</sup> : disposition partiellement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="622b3-6035"><sup>PCS</sup> : partially typed, castable and simple layout</span></span>
</dt> <dt>

 <span data-ttu-id="622b3-6036"><sup>FCS</sup> : mise en page entièrement typée, castable et simple</span><span class="sxs-lookup"><span data-stu-id="622b3-6036"><sup>FCS</sup> : fully typed, castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="622b3-6037"><sup>FNS</sup> : mise en page entièrement typée, non stable et simple</span><span class="sxs-lookup"><span data-stu-id="622b3-6037"><sup>FNS</sup> : fully typed, non-castable and simple layout</span></span>
</dt> <dt>

<span data-ttu-id="622b3-6038"><sup>PCC</sup> : disposition partiellement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="622b3-6038"><sup>PCC</sup> : partially typed, castable and complex layout</span></span>
</dt> <dt>

 <span data-ttu-id="622b3-6039"><sup>FCC</sup> : mise en page entièrement typée, castable et complexe</span><span class="sxs-lookup"><span data-stu-id="622b3-6039"><sup>FCC</sup> : fully typed, castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="622b3-6040"><sup>FNC</sup> : mise en page entièrement typée, non stable et complexe</span><span class="sxs-lookup"><span data-stu-id="622b3-6040"><sup>FNC</sup> : fully typed, non-castable and complex layout</span></span>
</dt> <dt>

<span data-ttu-id="622b3-6041"><sup>V</sup> : format vidéo</span><span class="sxs-lookup"><span data-stu-id="622b3-6041"><sup>V</sup> : video format</span></span>
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="622b3-6042">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="622b3-6042">Related topics</span></span>

[<span data-ttu-id="622b3-6043">Niveaux de fonctionnalité matérielle D3D12</span><span class="sxs-lookup"><span data-stu-id="622b3-6043">D3D12 Hardware Feature Levels</span></span>](../direct3d12/hardware-feature-levels.md)

<span data-ttu-id="622b3-6044">[Implémentation de mémoires tampons secondaires pour le niveau de fonctionnalité Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="622b3-6044">[Implementing shadow buffers for Direct3D feature level 9](/previous-versions/windows/apps/jj262110(v=win.10))</span></span>

[<span data-ttu-id="622b3-6045">Mappage des formats hérités</span><span class="sxs-lookup"><span data-stu-id="622b3-6045">Mapping Legacy Formats</span></span>](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[<span data-ttu-id="622b3-6046">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="622b3-6046">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
